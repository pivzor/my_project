Проект на **Symfony 7** с реализацией REST API через **API Platform** и административной панели через **EasyAdminBundle**.

## Описание
Этот проект представляет собой пример веб-приложения с:
- CRUD для основных сущностей через API Platform.
- Админ-панель для управления сущностями через EasyAdmin.
- Настроенной базой данных PostgreSQL/MySQL.

Проект можно использовать как шаблон для старта любого Symfony-приложения с REST API и админкой.

## Технологии
- PHP 8+
- Symfony 7
- Composer
- Doctrine ORM
- API Platform
- EasyAdminBundle
- PostgreSQL / MySQL
- Git

## Установка

1. Клонируем репозиторий:
```
git clone https://github.com/pivzor/my_project.git
cd my_project
```
2. Устанавливаем зависимости:
```
composer install
```
3. Создаём файл .env и настраиваем подключение к базе данных:
```
APP_ENV=dev
APP_SECRET=your_secret_key
DEFAULT_URI="pgsql://username:password@127.0.0.1:5432/db_name"
CORS_ALLOW_ORIGIN="*"
```
4. Создаём базу данных и применяем миграции:
```
php bin/console doctrine:database:create
php bin/console doctrine:migrations:migrate
```
5. Запускаем локальный сервер:
```
symfony serve
```

Команды Symfony
Очистка кеша:
```
php bin/console cache:clear
```
Генерация миграций:
```
php bin/console make:migration
```
Применение миграций:
```
php bin/console doctrine:migrations:migrate
```
Использование
Админ-панель доступна по адресу: http://127.0.0.1:8000/admin
API доступно по адресу: http://127.0.0.1:8000/api
