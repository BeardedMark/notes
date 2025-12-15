---
softDelete: true
timestamps: true
---
# Таблица всех переходов
Запись о текущем положении персонажа

| name          | type                             | default | unique | desctiption  |
| ------------- | -------------------------------- | ------- | ------ | ------------ |
| character_id  | [[Character]]                    |         |        | Персонаж     |
| location_code | [[Location]]                     |         |        | Локация      |
| hideout_id    | ?[[Hideout]]                     |         |        | Убежище      |
| modifiers     | ?array [[Modifier Instance]]     |         |        | Модификаторы |
| inventory     | ?array [[Item Instance]]         |         |        | Предметы     |
| enemies       | ?array [[Enemy Instance]]        |         |        | Враги        |
| containers    | ?array [[Container Instance]]    |         |        | Контейнеры   |
| constructions | ?array [[Construction Instance]] |         |        | Конструкции  |
- Создаются при входе на локацию
- Можно обновить содержимое переобходом локации
- Можно загрузить содержимое используя "карту"