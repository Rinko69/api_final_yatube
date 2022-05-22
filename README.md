# Yatube

Социальная сеть для общения, развлечения и творчества!
Помогает объединять людей по всему миру, находить новые знакомства и круги по интересам.

## Технологии:

Python 3.7 Django 2.2.19

## Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/Rinko69/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python -m venv env
```

```
source venv/Scripts/activate
```

Установить зависимости из файла requirements.txt:

```
python -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Перейти в главную папку проекта:

```
cd yatube_api
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```

## Примеры запросов:

Получение публикаций:

```
http://127.0.0.1:8000/api/v1/posts/
```
{
"count": 123,
"next": "http://api.example.org/accounts/?offset=400&limit=100",
"previous": "http://api.example.org/accounts/?offset=200&limit=100",
"results": [
{}
]
}
```
Получение комментариев:

```
http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/
```
[
  {
    "id": 0,
    "author": "string",
    "text": "string",
    "created": "2019-08-24T14:15:22Z",
    "post": 0
  }
]
```
Список сообществ:

```
http://127.0.0.1:8000/api/v1/groups/
```
[
  {
    "id": 0,
    "title": "string",
    "slug": "string",
    "description": "string"
  }
]
```
Подписки:

```
http://127.0.0.1:8000/api/v1/follow/
```
[
  {
    "user": "string",
    "following": "string"
  }
]
```
Получение JWT-токена:
```
http://127.0.0.1:8000/api/v1/jwt/create/
```
{
  "username": "string",
  "password": "string"
}
```