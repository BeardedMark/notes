---
softDelete: true
timestamps: true
---
# Таблица всех пользователей
Персональные аккаунты пользователей

| name              | type       | default | unique | desctiption     |
| ----------------- | ---------- | ------- | ------ | --------------- |
| login             | string     |         |        | Логин           |
| password          | string     |         |        | Пароль          |
| email             | string     |         | true   | Почта           |
| is_admin          | boolean    | false   |        | Администратор   |
| activity_at       | timestamp  | now     |        | Дата активности |
| settings          | json       |         |        | Настройки       |
