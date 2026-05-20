# DOC-OPS-002 — Deployment Plan & Runbook

| Версия | Статус | Дата создания | Дата обновления |
|--------|--------|---------------|-----------------|
| v1.0   | Draft  | 2026-05-15    | 2026-05-19      |

О документе: инструкция по установке, запуску и эксплуатации системы PVZ Monitor.

Для кого: разработчик, DevOps, преподаватель.

Основано на: [карточке проекта](../00-governance/project_card.md).

---

## Системные требования

| Компонент       | Минимум                     |
|-----------------|-----------------------------|
| ОС              | Ubuntu 22.04+ / Windows 10+ |
| Python          | 3.10+                       |
| Свободное место | 500 MB                      |
| RAM             | 512 MB                      |

## Переменные окружения

```bash
SECRET_KEY=your_secret_key_here   # секрет Flask-сессии
DB_URL=sqlite:///pvz.db           # путь к базе данных
```

---

## Локальный запуск (разработка)

```bash
# 1. Клонировать репозиторий
git clone https://github.com/your-org/pvz-monitor.git
cd pvz-monitor

# 2. Создать виртуальное окружение
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# 3. Установить зависимости
pip install -r requirements.txt

# 4. Сгенерировать данные (если БД пуста)
python generate_realistic_data.py

# 5. Запустить приложение
python app.py

# Приложение доступно по адресу: http://127.0.0.1:5000
```

---

## Продакшн-запуск (nginx + pm2)

### Nginx конфигурация

```nginx
server {
    listen 80;
    server_name pvz-monitor.example.com;

    location / {
        proxy_pass http://localhost:5000;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }
}
```

### PM2 запуск

```bash
npm install -g pm2
pm2 start app.py --name "pvz-monitor" --interpreter python3
pm2 save
pm2 startup
```

---

## Бэкап и восстановление

```bash
# Создать резервную копию БД
cp pvz.db pvz_backup_$(date +%Y%m%d).db

# Восстановить из резервной копии
cp pvz_backup_20260519.db pvz.db
```

Рекомендуется настроить ежедневный cron-бэкап:

```bash
0 3 * * * cp /path/to/pvz.db /backups/pvz_$(date +\%Y\%m\%d).db
```

---

## Запуск тестов

```bash
pip install pytest pytest-flask
pytest -v
```

---

## Типичные проблемы

| Проблема                          | Решение                                          |
|-----------------------------------|--------------------------------------------------|
| `ImportError: No module named flask` | `pip install -r requirements.txt`             |
| БД пуста, нет данных              | `python generate_realistic_data.py`              |
| Порт 5000 занят                   | Изменить порт в `app.py`: `app.run(port=5001)`  |
| Ошибка прав на файл `pvz.db`     | `chmod 664 pvz.db`                              |
