FROM python:3.7-slim

LABEL author="Rostyslav"
LABEL version=1.0

# оновлюємо систему
RUN apt-get update && apt-get upgrade -y

# Встановлюємо потрібні пакети
RUN apt-get install git -y && pip install pipenv

# Створюємо робочу папку
WORKDIR /lab

# Завантажуємо файли з Git+
RUN git clone https://github.com/KoretskiyRostyslav/DevOpsNULP.git

# Створюємо остаточну робочу папку з Веб-сайтом та копіюємо туди файли
WORKDIR /app

RUN cp -r /lab/DevOpsNULP/lab3/* .
# Інсталюємо всі залежності
RUN pipenv --python 3.7
RUN pipenv install django 
# Відкриваємо порт 8000 на зовні
EXPOSE 8000

# Це команда яка виконається при створенні контейнера
ENTRYPOINT ["pipenv", "run", "python", "manage.py", "runserver", "0.0.0.0:8000"]
