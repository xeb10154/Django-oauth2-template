FROM python:3.10-slim-bullseye
LABEL raymond xeb

ENV PYTHONUNBUFFERED 1

COPY ./requirements.txt /requirements.txt
RUN pip install -r /requirements.txt

RUN mkdir /auth
WORKDIR /auth
# This dot (.) is used to copy the current files to the /auth folder. This dot represents the context path set in the docker-compose.yml file.
COPY . /auth

RUN useradd -s /bin/bash dev
USER dev