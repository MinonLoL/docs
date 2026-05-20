# CP2 — Контрольная точка 2: артефакты и статус

| Версия | Статус | Дата        |
|--------|--------|-------------|
| v1.0   | Done   | 2026-05-20  |

---

## Выполненные артефакты

| Артефакт                           | Файл                                                       | Статус |
|------------------------------------|------------------------------------------------------------|--------|
| Логическая модель данных и ERD     | `docs/05-data-and-integration/logical_data_model.md`       | ✅     |
| Словарь данных и правила валидации | `docs/05-data-and-integration/data_dictionary_and_validations.md` | ✅ |
| API-спецификация                   | `docs/05-data-and-integration/api_specification.md`        | ✅     |
| OpenAPI YAML                       | `api/openapi.yaml`                                         | ✅     |
| BPMN-описание                      | `docs/04-design/bpmn_description.md`                       | ✅     |
| Event Storming                     | `docs/04-design/event_storming.md`                         | ✅     |
| Диаграмма состояний                | `docs/04-design/state_diagram.md`                          | ✅     |
| Backend API (Flask)                | `routes/`, `db.py`, `auth.py`                              | ✅     |
| Синтетические данные (≥200 ops)    | `generate_realistic_data.py`, `pvz.db`                     | ✅     |
| Frontend (дашборд, тепловая карта) | `templates/index.html`                                     | ✅     |

## Отставания и риски

Отставаний нет. Риск R4 (тепловая карта) успешно закрыт — Chart.js интегрирован.

## План на КТ3

- Финальное тестирование (unit + интеграционное).
- Подготовить полную техническую документацию.
- Написать демо-сценарий и приёмочные тесты.
- Финальный README.
