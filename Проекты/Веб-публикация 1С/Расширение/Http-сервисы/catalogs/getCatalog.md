---
Method: GET
Endpoint: /catalogs/{catalogGuid}
Authorization: none
Content-Type: application/json
Responce-Type: object
---
#1С/API
# Формирование карточки каталога
## Параметры запроса

| key            | type    | default | enum | note             |
| -------------- | ------- | ------- | ---- | ---------------- |
| catalogGuid    | string  |         |      | Гуид каталога    |
| contractorGuid | ?string | null    |      | Гуид контрагента |
## Структура ответа

| key      | type   | value                        | note |
| -------- | ------ | ---------------------------- | ---- |
| catalog  | object | [[Информация о каталоге]]    |      |
| catalogs | array  | [[Каталоги по каталогу]]     |      |
| offers   | array  | [[Номенклатура по каталогу]] |      |
