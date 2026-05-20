# Документация проекта «PVZ Monitor»

| Версия | Дата обновления |
|--------|-----------------|
| v1.0   | 2026-05-19      |

Система мониторинга загрузки пунктов выдачи заказов (ПВЗ) для сбалансирования нагрузки и сокращения очередей/простоя.

---

## Структура документации

### 00. Governance — Управление проектом

| Документ | Описание |
|----------|----------|
| [Карточка проекта](00-governance/project_card.md) | Паспорт проекта: цели, стек, команда, KPI |
| [RACI-матрица](00-governance/raci_matrix.md) | Матрица ответственности участников |
| [Правила командной работы](00-governance/team_and_communication.md) | Роли, правила, инструменты |

### 01. Discovery — Исследование

| Документ | Описание |
|----------|----------|
| [Исследование предметной области](01-discovery/problem_statement.md) | AS-IS, проблемы, термины, TO-BE |
| [Персоны пользователей](01-discovery/personas.md) | Описание 3 ролей: цели и боли |

### 02. Requirements — Требования

| Документ | Описание |
|----------|----------|
| [User Stories](02-requirements/user_stories.md) | US-01 – US-15 с критериями приёмки |
| [User Story Map](02-requirements/user_story_map.md) | Карта историй по активностям и релизам |
| [UX-сценарии](02-requirements/ux_scenarios.md) | Пошаговые сценарии для каждой роли |
| [MoSCoW-матрица](02-requirements/moscow_matrix.md) | Приоритизация требований |
| [Feature List](02-requirements/feature_list.md) | Полный перечень функций со статусом |

### 03. Planning — Планирование

| Документ | Описание |
|----------|----------|
| [Оценка реализуемости](03-planning/technical_feasibility.md) | Техническая и организационная оценка |
| [WBS и план работ](03-planning/wbs.md) | Иерархическая структура работ + roadmap |
| [Матрица рисков](03-planning/risk_matrix.md) | Риски, оценки, планы реагирования |
| [Roadmap](03-planning/roadmap.md) | Календарный план по этапам |

### 04. Design — Проектирование

| Документ | Описание |
|----------|----------|
| [BPMN-описание](04-design/bpmn_description.md) | Бизнес-процесс регистрации операции |
| [Event Storming](04-design/event_storming.md) | События, команды, агрегаты |
| [ER-диаграмма](04-design/er_diagram.md) | Логическая модель данных (Mermaid) |
| [Схема БД](04-design/db_schema.md) | Физическая структура таблиц SQLite |
| [Диаграмма состояний](04-design/state_diagram.md) | Состояния ПВЗ по уровню загрузки |
| [Тепловая карта и дашборд](04-design/heatmap_dashboard.md) | Описание визуализаций |

### 05. Data & Integration — Данные и интеграция

| Документ | Описание |
|----------|----------|
| [Логическая модель и ERD](05-data-and-integration/logical_data_model.md) | Сущности, атрибуты, связи |
| [Словарь данных и валидации](05-data-and-integration/data_dictionary_and_validations.md) | Типы полей, ограничения, правила V1–V8 |
| [API-спецификация](05-data-and-integration/api_specification.md) | Все эндпоинты, форматы запросов/ответов |

### 06. Final Specification — Финальная спецификация

| Документ | Описание |
|----------|----------|
| [Финальная тех. спецификация](06-final-specification/final_technical_specification.md) | Итоговое описание MVP |

### 07. Validation & Delivery — Валидация и сдача

| Документ | Описание |
|----------|----------|
| [Демо-сценарий](07-validation-and-delivery/demo_scenario.md) | TC-001–TC-011, маршрут демонстрации |
| [Приёмочные тесты](07-validation-and-delivery/acceptance_tests.md) | 12 приёмочных сценариев |
| [Deployment Runbook](07-validation-and-delivery/deployment_runbook.md) | Локальный запуск, продакшн, бэкап |

### 05. Technical — Техническая документация (legacy)

| Документ | Описание |
|----------|----------|
| [API-контракт](05-technical/api_contract.md) | Краткое описание эндпоинтов |
| [Развёртывание](05-technical/deployment.md) | Инструкция по запуску |

### 90. Checkpoints — Контрольные точки

| Документ | Описание |
|----------|----------|
| [CP1 — статус](90-checkpoints/CP1_status.md) | Артефакты первой КТ |
| [CP2 — статус](90-checkpoints/CP2_status.md) | Артефакты второй КТ |
| [CP3 — статус](90-checkpoints/CP3_status.md) | Финальный статус проекта |
