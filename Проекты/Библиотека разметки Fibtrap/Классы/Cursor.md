---
Key: cursor
---

## Основное

| Ключ   | Значение     | Описание                               |
| ------ | ------------ | -------------------------------------- |
| def    | default      | Обычный курсор (стрелка)               |
| point  | pointer      | Рука, как при наведении на ссылку      |
| text   | text         | Текстовый курсор (I-палочка)           |
| text-v | vertical-tet |                                        |
| move   | move         | Крест с четырьмя стрелками             |
| help   | help         | Знак вопроса (не везде работает)       |
| forb   | not-allowed  | Запрещено                              |
| wait   | wait         | Часы/ожидание                          |
| prog   | progress     | Курсор + индикатор ожидания            |
| alias  | alias        | Ссылка/псевдоним                       |
| auto   | auto         | Автоматический выбор курсора браузером |
| copy   | copy         | Копирование (обычно с плюсом)          |
## Перетаскивание

| Ключ    | Значение   | Описание                  |
| ------- | ---------- | ------------------------- |
| grab    | grab       | Рука (готов к захвату)    |
| grabg   | grabbing   | Зажатая рука (в процессе) |
| n-drop  | no-drop    | Запрещённое место сброса  |
| a-scr   | all-scroll | Стрелки во все стороны    |
| col-res | col-resize | Изменение ширины столбца  |
| row-res | row-resize | Изменение высоты строки   |
| t-res   | n-resize   | Стрелка вверх             |
| b-res   | s-resize   | Вниз                      |
| r-res   | e-resize   | Вправо                    |
| l-res   | w-resize   | Влево                     |
| tr-res  | ne-resize  | Диагональ вправо-вверх    |
| tl-res  | nw-resize  | Диагональ влево-вверх     |
| br-res  | se-resize  | Вправо-вниз               |
| bl-res  | sw-resize  | Влево-вниз                |
## Прочее

| Ключ   | Значение     | Описание                         |
| ------ | ------------ | -------------------------------- |
| none   | none         | Скрывает курсор                  |
| cross  | crosshair    | Крестик (прицел)                 |
| cell   | cell         | Сетка, как в таблицах            |
| z-in   | zoom-in      | Увеличение                       |
| z-out  | zoom-out     | Уменьшение                       |
| c-menu | context-menu | Меню по правой кнопке (не везде) |
## Кастомный

```css
/* Основное */
.curs-alias    { cursor: alias; }
.curs-auto     { cursor: auto; }
.curs-copy     { cursor: copy; }
.curs-def      { cursor: default; }
.curs-point    { cursor: pointer; }
.curs-text     { cursor: text; }
.curs-text-v   { cursor: vertical-text; }
.curs-move     { cursor: move; }
.curs-help     { cursor: help; }
.curs-forb     { cursor: not-allowed; }
.curs-wait     { cursor: wait; }
.curs-prog     { cursor: progress; }

/* Перетаскивание */
.curs-grab     { cursor: grab; }
.curs-grabg    { cursor: grabbing; }
.curs-n-drop   { cursor: no-drop; }
.curs-a-scr    { cursor: all-scroll; }
.curs-col-res  { cursor: col-resize; }
.curs-row-res  { cursor: row-resize; }
.curs-n-res    { cursor: n-resize; }
.curs-s-res    { cursor: s-resize; }
.curs-e-res    { cursor: e-resize; }
.curs-w-res    { cursor: w-resize; }
.curs-ne-res   { cursor: ne-resize; }
.curs-nw-res   { cursor: nw-resize; }
.curs-se-res   { cursor: se-resize; }
.curs-sw-res   { cursor: sw-resize; }

/* Прочее */
.curs-none     { cursor: none; }
.curs-cross    { cursor: crosshair; }
.curs-cell     { cursor: cell; }
.curs-z-in     { cursor: zoom-in; }
.curs-z-out    { cursor: zoom-out; }
.curs-c-menu   { cursor: context-menu; }
```