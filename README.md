# api_yatube
API для сервиса yatube. Позволяет запрашивать данные о постах, группах и комментариях в социальной сети Yatube, а также управлять ими.
## Технологии
Python 3.8, Django 3.2, DRF, JWT + Djoser
## Как запустить
1. Клонируем репозиторий и переходим в него в командной строке

```
git clone https://github.com/QuiShimo/api_yatube.git
```

```
cd api_yatube
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
