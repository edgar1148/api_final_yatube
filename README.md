### Проект api_final_yatube


## Описание
Настроена API для социальной сети Yatube.
Позволяет публикацию записей, комментарии, подписки на авторов.

## Запуск проекта

- Клонировать репозиторий
- Установить и активировать виртуальное окружение

```
python -m venv venv
```

```
source venv/Scripts/activate
```

- Установить зависимости requirements.txt

```
pip install -r requirements.txt
```

- Выполнить миграции:

```
python manage.py migrate
```

- Создать суперпользователя:

```
python manage.py createsuperuser
```

- Запустить проект:

```
python manage.py runserver
```

## Примеры работы с API для всех пользователей

- Cписок всех публикаций
```
GET api/v1/posts/
```
- Получить публикацию по id
```
GET api/v1/posts/{id}/ 
```
- Получить список групп
```
GET api/v1/groups/
```
- Получить информацию о группе
```
GET api/v1/groups/{id}/
```
- Получить все комментарии к публикациям
```
GET api/v1/{post_id}/comments/
```
Получить комментарий по id
```
GET api/v1/{post_id}/comments/{id}/
```

## Примеры работы с API для авторизованных пользователей

- Для создания публикации

```
POST /api/v1/posts/
```

- Ответ:

```json
{
"text": "string",
"image": "string",
"group": 0
}
```

- Обновление публикации:

```
PUT /api/v1/posts/{id}/
```

- Ответ:

```json
{
"text": "string",
"image": "string",
"group": 0
}
```

- Частичное обновление публикации:

```
PATCH /api/v1/posts/{id}/
```

Ответ:

```json
{
"text": "string",
"image": "string",
"group": 0
}
```

- Удаление публикации:

```
DEL /api/v1/posts/{id}/
```
