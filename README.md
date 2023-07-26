# Описание
Проект является финальным заданием спринта 11. Он служит для закрепления навыков работы с Django Rest Framework.

# Как запустить проект
Клонировать репозиторий и перейти в него в командной строке:
```
git clone git@github.com:altdinov/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python3 -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python3 manage.py migrate
```

Запустить проект:

```
python3 manage.py runserver
```


# Примеры
Ниже показаны некоторые примеры запросов к API.

## Получение публикаций
**GET**  http://127.0.0.1:8000/api/v1/posts/

_Response samples_
```
{
    "count": 123,
    "next": "http://api.example.org/accounts/?offset=400&limit=100",
    "previous": "http://api.example.org/accounts/?offset=200&limit=100",
    "results": 
[
        {
            "id": 0,
            "author": "string",
            "text": "string",
            "pub_date": "2021-10-14T20:41:29.648Z",
            "image": "string",
            "group": 0
        }
    ]
}
```
## Создание публикации
**POST**  http://127.0.0.1:8000/api/v1/posts/

_Request samples_
```
{
    "text": "string",
    "image": "string",
    "group": 0
}
```

_Response samples_
```
{
    "id": 0,
    "author": "string",
    "text": "string",
    "pub_date": "2019-08-24T14:15:22Z",
    "image": "string",
    "group": 0
}
```
