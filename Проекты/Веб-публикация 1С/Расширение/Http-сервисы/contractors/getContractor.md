---
Method: GET
Endpoint: /contractor/{contractorGuid}
Authorization: none
Content-Type: application/json
Responce-Type: object
---
#1С/API
# Формирование карточки контрагента
## Параметры запроса

| key            | type   | default | enum | note |
| -------------- | ------ | ------- | ---- | ---- |
| contractorGuid | string |         |      |      |

## Структура ответа

| key        | type   | value                     | note |
| ---------- | ------ | ------------------------- | ---- |
| contractor | object | [[Информация о контрагенте]]         |      |
| contacts   | array  | [[Контактная информация]] |      |
| offers     | array  | [[Заказы по контрагенту]]      |      |
