FROM ubuntu:20.04

RUN apt-get update && \
    apt-get install -y python3-pip 

RUN pip3 install Django

WORKDIR /home/app

RUN django-admin startproject miapp

WORKDIR /home/app/miapp

COPY settings.py miapp/settings.py

CMD ["python3", "manage.py", "runserver", "0.0.0.0:8000"]
