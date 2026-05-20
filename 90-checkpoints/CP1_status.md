# CP1 — Контрольная точка 1: артефакты и статус

| Версия | Статус | Дата        |
|--------|--------|-------------|
| v1.0   | Done   | 2026-05-13  |

---

## Выполненные артефакты

| Артефакт                        | Файл                                            | Статус |
|---------------------------------|-------------------------------------------------|--------|
| Карточка проекта                | `docs/00-governance/project_card.md`            | ✅     |
| RACI-матрица                    | `docs/00-governance/raci_matrix.md`             | ✅     |
| Правила командной работы        | `docs/00-governance/team_and_communication.md`  | ✅     |
| Исследование предметной области | `docs/01-discovery/problem_statement.md`        | ✅     |
| Персоны пользователей           | `docs/01-discovery/personas.md`                 | ✅     |
| User Stories (US-01 – US-15)    | `docs/02-requirements/user_stories.md`          | ✅     |
| User Story Map                  | `docs/02-requirements/user_story_map.md`        | ✅     |
| MoSCoW-матрица                  | `docs/02-requirements/moscow_matrix.md`         | ✅     |
| Feature List                    | `docs/02-requirements/feature_list.md`          | ✅     |
| Оценка реализуемости            | `docs/03-planning/technical_feasibility.md`     | ✅     |
| WBS и план работ                | `docs/03-planning/wbs.md`                       | ✅     |
| Матрица рисков                  | `docs/03-planning/risk_matrix.md`               | ✅     |

## Отставания и риски

Отставаний нет. Риски R1 (перегрузка ПВЗ в данных) и R7 (нагрузка команды) зафиксированы и находятся под контролем.

## План на КТ2

- Завершить проектирование архитектуры (ER, BPMN, API-контракт).
- Реализовать Backend API: операции, отчёты, авторизация.
- Настроить интеграцию с SQLite.
- Сгенерировать синтетические данные (≥200 операций).
