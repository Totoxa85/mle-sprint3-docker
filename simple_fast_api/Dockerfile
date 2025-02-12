FROM python:3.11-slim

LABEL author=${AUTHOR}
COPY . ./simple_fast_api
WORKDIR simple_fast_api 

# директория simple_fast_api скопирована в Docker
# укажем инструкцию по запуску микросервиса
RUN pip3 install -r requirements.txt

VOLUME /speeches

EXPOSE ${APP_PORT}

CMD uvicorn app.main:app --host 0.0.0.0 --port ${APP_PORT}