# Проект Yatube API

### Описание
Доступ к дневникам пользователей посредством API сайта

## Как запустить проект:
### Клонировать репозиторий и перейти в него в командной строке:
- cd api_final_yatube

### Cоздать и активировать виртуальное окружение:
- python -m venv env
- source env/bin/activate
- python -m pip install --upgrade pip

### Установить зависимости из файла requirements.txt:
- pip install -r requirements.txt

### Выполнить миграции:
- python manage.py migrate

### Запустить проект:
- python manage.py runserver

## Примеры запросов к API:
# Получение публикаций:
- GET /api/v1/posts/

# Создание публикации:
- POST /api/v1/posts/
{
"text": "string",
"image": "string",
"group": 0
}

# Получение публикаций:
- GET /api/v1/posts/{id}/

# Обновление публикации:
- PUT /api/v1/posts/{id}/
{
"text": "string",
"image": "string",
"group": 0
}

# Частичное обновление публикации:
- PATCH /api/v1/posts/{id}/
{
"text": "string",
"image": "string",
"group": 0
}

# Удаление публикации:
- DELETE /api/v1/posts/{id}/

# Получение комментариев:
- GET /api/v1/posts/{post_id}/comments/

# Добавление комментария:
- POST /api/v1/posts/{post_id}/comments/
{
"text": "string"
}

# Получение комментария:
- GET /api/v1/posts/{post_id}/comments/{id}

# Обновление комментария:
- PUT /api/v1/posts/{post_id}/comments/{id}
{
"text": "string"
}

# Частичное обновление комментария:
- PATCH /api/v1/posts/{post_id}/comments/{id}
{
"text": "string"
}

# Удаление комментария:
- DELETE /api/v1/posts/{post_id}/comments/{id}

# С о группе:
- GET /api/v1/groups/{id}

# Список групп:
- GET /api/v1/groups/

# Подписки пользователя:
- GET /api/v1/follow/

# Подписка на автора:
- POST /api/v1/follow/
{
"following": "string"
}

# Получить JWT-токен:
- POST /api/v1/jwt/create/
{
"username": "string",
"password": "string"
}

# Обновить JWT-токен:
- POST /api/v1/jwt/refresh/
{
"refresh": "string"
}