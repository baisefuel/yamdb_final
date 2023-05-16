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

Файл .env.example лежит в директории infra. На его основе нужно создать файл .env в той же директории

Запустить проект:

```bash
http://localhost/
```

![example workflow](https://github.com/baisefuel/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)