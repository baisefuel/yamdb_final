# Проект «API YamDB»
#### API и документация для приложения YamDB.
Проект YaMDb собирает отзывы (Review) пользователей на произведения (Titles). Произведения делятся на категории: «Книги», «Фильмы», «Музыка». Список категорий (Category) может быть расширен администратором.
___
## Стек технологий:
- Python,
- Djando,
- DRF
- JWT - библиотека Simple JWT
- Gunicorn
- nginx
___
## Как запустить проект:

Клонировать репозиторий, перейти в него в командной строке и создать контейнер:

```bash
git clone https://github.com/baisefuel/infra_sp2.git
```

```bash
cd api_yamdb
```

```bash
docker build -t infra .
```

```bash
cd ..
cd infra
```

```bash
docker compose up -d --build
```

Выполнить миграции:

```bash
docker-compose exec web python manage.py migrate
docker-compose exec web python manage.py createsuperuser
```

На примере .env.example нужно создать файл .env

```.env.example

DB_ENGINE=django.db.backends.postgresql # указываем, что работаем с postgresql
DB_NAME=postgres # имя базы данных
POSTGRES_USER=postgres # логин для подключения к базе данных
POSTGRES_PASSWORD=postgres # пароль для подключения к БД (установите свой)
DB_HOST=db # название сервиса (контейнера)
DB_PORT=5432 # порт для подключения к БД

```

Запустить проект:

```bash
http://localhost/
```

https://github.com/baisefuel/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg