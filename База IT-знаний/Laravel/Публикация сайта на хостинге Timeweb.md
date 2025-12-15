[Laravel - Виртуальный хостинг - Справочный центр Timeweb](https://timeweb.com/ru/docs/virtualnyj-hosting/prilozheniya-i-frejmvorki/laravel/)

1. В разделе «Сайты» — «[Мои сайты](https://hosting.timeweb.ru/sites)» панели управления аккаунта создайте новый сайт.
2. В директории нового сайта удалите автоматически созданный каталог `public_html`.
3. Перенесите файлы вашего сайта в созданную директорию.
4. Подключитесь к серверу по [SSH](https://timeweb.com/ru/docs/virtualnyj-hosting/podklyuchenie-k-serveru-hostinga/podklyuchenie-po-ssh/).
5. Выполните следующую команду на сервере через SSH-подключение, указав имя директории сайта:

```bash
ln -s ~/___/public ~/___/public_html
```

```bash
ln -s ~/___/storage/app/public ~/___/public/storage
```

# .env (database)

```php
DB_CONNECTION=mysql

DB_HOST=127.0.0.1
DB_HOST=vh396.timeweb.ru

DB_PORT=3306
DB_DATABASE=login_table
DB_USERNAME=login_table
DB_PASSWORD=password
```