# api_yatube
API для сервиса yatube. Позволяет запрашивать данные о постах, группах и комментариях в социальной сети Yatube, а также управлять ими.
## Технологии
Python 3.8, Django 3.2, DRF, JWT + Djoser
## Как запустить
1. Клонируем репозиторий и переходим в него в командной строке

```
git clone https://github.com/QuiShimo/api_final_yatube.git
```

```
cd api_final_yatube
```

2. Создаем и активируем виртуальное окружение

```
python -m venv env
```

```
source env/Scripts/activate
```

3. Устанавливаем необходимые зависимости из requirements

```
pip install -r requirements.txt
```

4. Делаем миграции

```
python yatube_api/manage.py migrate
```

5. Запускаем проект

```
python yatube_api/manage.py runserver
```
## Примеры работы с API для всех пользователей
Для неавторизованных пользователей работа с API доступна только в режиме чтения.
- Получить список всех публикаций:
```
GET api/v1/posts/
```
При указании параметров limit и offset выдача будет работать с пагинацией.
- Получение публикации по id:
``` 
GET api/v1/posts/{id}/
```
- Получение списка доступных сообществ:
```
GET api/v1/groups/
```
- Получение информации о сообществе по id:
```
GET api/v1/groups/{id}/
```
- Получение всех комментариев к публикации
```
GET api/v1/{post_id}/comments/
``` 
- Получение комментария к публикации по id:
```
GET api/v1/{post_id}/comments/{id}/
```
## Примеры работы с API для авторизованных пользователей
- Создание публикации:
``` 
POST /api/v1/posts/
```
тело запроса:
```
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
тело запроса:
```
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
тело запроса
```
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
