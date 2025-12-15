---
softDelete: true
timestamps: true
---
# Таблица всех дорог
Связывают локации между собой обеспечивая переходы

| name               | type         | default | unique | desctiption   |
| ------------------ | ------------ | ------- | ------ | ------------- |
| from_location_code | [[Location]] |         |        | Откуда        |
| to_location_code   | [[Location]] |         |        | Куда          |
| is_one_way         | boolean      | false   |        | Односторонняя |
- from_location_code - локация с которой был произведен переход
- to_location_code - локация на которую был произведен переход
- is_one_way - можно двигаться только в одну сторону