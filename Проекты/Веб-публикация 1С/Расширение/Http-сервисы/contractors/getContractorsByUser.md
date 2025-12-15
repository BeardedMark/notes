---
Method: GET
Endpoint: /user/{userGuid}/contractors
Authorization:
  - token
Content-Type: application/json
Responce-Type: "[[Контрагенты по пользователю]]"
---
#1С/API
# Список контрагентов по пользователю
## Параметры запроса

| key      | type   | default | enum | note                            |
| -------- | ------ | ------- | ---- | ------------------------------- |
| userGuid | string |         |      |                                 |
| limit    | ?int   | null    |      | количество возвращаемых записей |
