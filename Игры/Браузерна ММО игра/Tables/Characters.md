---
softDelete: true
timestamps: true
---
# Таблица всех персонажей
Игровые персонажи пользователей

| name           | type                     | default | unique | desctiption  |
| -------------- | ------------------------ | ------- | ------ | ------------ |
| user_id        | [[User]]                 |         |        | Пользователь |
| experience     | int                      | 0       |        | Опыт         |
| is_current     | boolean                  | false   |        | Активный     |
| regenerated_at | timestamp                |         |        |              |
| next_action_at | timestamp                |         |        |              |
| activity_at    | timestamp                |         |        |              |
| inventory      | ?array [[Item Instance]] |         |        | Инвентарь    |
| equipment      | ?array [[Item Instance]] |         |        | Экипировка   |
| skills         | ?array [[Skill]]         |         |        | Навыки       |
