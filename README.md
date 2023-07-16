# Социальная сеть Kittygram (как Onlyfans, только с котиками)
## Описание проекта:
В данной социальной сети пользователи могут регистрироваться, загружать картинки котиков с описанием, а также(!!) смотреть фотографии котиков других пользователей!
Главная цель данной задачи - обучение управлению на удаленном сервере.

## Технологии:
Python
Django
djangorestframework
Nginx
Gunicorn

## Установка проекта на локальный компьютер:
Клонировать репозиторий
В директории с клонированным репозиторием установить виртальное окружение python -m venv venv
Установить зависимости pip install -r requirements.txt

# Размещение проекта на удаленном сервере

## Подключение сервера к акку на GitHub

Проверить установлен ли GIT на сервере:
sudo apt update
git --version

Если ли не установлен:
sudo apt install git

Сгенерировать пару SSH-ключей:
ssh-keygen

Вывести ключ в терминал командой cat .ssh/id_rsa.pub. 
Сохранить открытый ключ в Вашем аккаунте на GitHub
Клонировать проект с GitHub на сервер:
git clone

# Запуск бэкенда на сервере:
sudo apt install python3-pip python3-venv -y
Установить виртаульное окружение
python3 -m venv venv
Активировать виртуальное окружение:
source venv/bin/activate
Установить зависимости:
pip install -r requirements.txt
Выполнить миграции:
python manage.py migrate
Создать суперпользователя:
python manage.py createsupersuser

В settings.py, в ALLOWED_HOSTS добавить:
внешний IP Вашего сервера;
127.0.0.1;
localhost;
