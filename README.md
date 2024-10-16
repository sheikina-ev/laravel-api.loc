## Установка проекта из репозитория
1. Склонируйте репозиторий 
```sh
cd domains
git clone https://github.com/sheikina-ev/laravel-api.loc.git
```
2. Перейдите в папку с проектом и установите composer-зависимости
```sh
cd laravel-api.loc
composer install
```
3. Скопируйте файл .env.example в .env
```sh
cp .env.
```
4. Сгенерируйте ключ шифрования
```shell
php artisan key:generate
```
5. Измените файл конфигурации .env (пример для БД MySql)
```php
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=Имя_БД
DB_USERNAME=Логин_пользователя_БД
DB_PASSWORD=Пароль_пользователя_БД

SESSION_DRIVER=file
```


## Пустой проект 
Создан в OpenServer следующими командами:
```sh
cd domains
mkdir laravel-api.loc
cd laravel-api.loc
composer self-update
composer create-project laravel/laravel .
php artisan install:api
php artisan config:publish cors
php artisan storage:link
```

В корне проекта создан файл .htaccess
```php
RewriteEngine on
RewriteRule ^(.*)$ public/$1 [L]
```
