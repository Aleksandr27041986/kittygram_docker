# Kittygram

***
### Описание:
Kittygram — социальная сеть для обмена фотографиями любимых питомцев. 
У вас есть любимый питомец и есть весёлые фотографий с ним? Тогда Вам [сюда](https://kittygramshestakov.hopto.org)
Вы можете разместить фотографию своего питомца, подписать имя, указать год его рождения, достижения(выбрать из списка или добавить своё).
Все пользователи увидят вашего чудесного Снежка и умилятся. Ведь котиков любят все. 
Минута умиления над котиками продлевает вашу жить на целый час. 
***
### Технологии:
Проект включает в себя фронтенд(SPA-приложение на React) и бэкенд(Django-приложение). 
Бэкенд представляет собой API написанное с использованием Django Rest Framework, обмен данными идёт с использованием JSON формата. Примеры смотри ниже.
Проект настроен для работы с PostgreSQL, созданы настройки по упаковке приложений в Docker контейнеры и установке и использованием Docker Compose
#### Стек:
Python, JavaScript, Django, Django Rest Framework, PostgreSQL, Docker
***

### Как запустить проект:

#### 1. Клонировать репозиторий и перейти в него в командной строке:

```bash
git clone git@github.com:Aleksandr27041986/kittygram_final.git
```

```bash
cd kittygram/backend/
```

#### 2. Запуск проекта локально:
 ##### - запустить локально бэкенд:

Перейти в бэкенд командной строкой:
```bash
cd backend
```
Cоздать и активировать виртуальное окружение:
```bash
python3 -m venv env
```
* Если у вас Linux/macOS
    ```bash
    source env/bin/activate
    ```
* Если у вас windows
   ```bash
    source env/scripts/activate
    ```
```bash
python3 -m pip install --upgrade pip
```
Установить зависимости из файла requirements.txt:
```bash
pip install -r requirements.txt
```
Выполнить миграции:
```bash
python3 manage.py migrate
```
Запустить проект:
```bash
python3 manage.py runserver
```

##### - запустить локально фронтэнд:
Перейти во фронтенд в командной строке:
```bash
cd ../frontend
```
Установить зависимости:
```bash
npm i
```
Запустить проект:

```bash
npm run start
```

#### 3. Запуск проекта с использованием [Docker compose](https://hub.docker.com/):
 - установить Docker Compose:
```bash
sudo apt update
sudo apt install curl
curl -fSL https://get.docker.com -o get-docker.sh
sudo sh ./get-docker.sh
sudo apt-get install docker-compose-plugin 
```
 - запустить проект:
```bash
sudo docker compose up -d
```

### Примеры запросов:

Адрес для работы с API https://kittygramshestakov.hopto.org/api/
Пример Post-запроса по адресу [cats](https://kittygramshestakov.hopto.org/api/cats/)
```json
{
    "name": "string",
    "color": "string",
    "birth_year": 0,
    "achievement": [
      "string"
    ],
    "image": "string"
}
```
Полученный ответ:
```json
{
    "id": 0,
    "name": "string",
    "color": "string",
    "birth_year": 0,
    "achievements": [
      "string"
    ],
    "owner": 0,
    "age": 0,
    "image": "string",
    "image_url": "string"
}
```

#### Авторы проекта:
Автором является начинающий программист, обучающийся на курсе [Yandex Practicum](https://practicum.yandex.ru/)
Шестаков Александр - [github](https://github.com/Aleksandr27041986), [telegram](https://t.me/Sanila270486)

