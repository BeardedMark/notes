# Инструкция размещения проекта на хостинге
[Laravel - Виртуальный хостинг - Справочный центр Timeweb](https://timeweb.com/ru/docs/virtualnyj-hosting/prilozheniya-i-frejmvorki/laravel/)

1. Открыть директорию сайта на хостинге в [файловом менеджере](https://hosting.timeweb.ru/fileman)
2. Удалить автоматически созданный каталог `public_html`
3. Перенести файлы сайта в директорию сайта на хостинге
4. Подключиться к серверу по [SSH Терминалу](https://timeweb.com/ru/docs/virtualnyj-hosting/podklyuchenie-k-serveru-hostinga/podklyuchenie-po-ssh/) для выполнения команд

```bash
# Создание ссылки на основе папки
ln -s ~/___/public ~/___/public_html
```

```bash
# Создание ссылки на хранилище
ln -s ~/___/storage/app/public ~/___/public/storage
```

## Подключение базы данных в .env

```php
DB_CONNECTION=mysql

DB_HOST=127.0.0.1 # vh396.timeweb.ru

DB_PORT=3306
DB_DATABASE=login_tablename
DB_USERNAME=login_tablename
DB_PASSWORD=password
```