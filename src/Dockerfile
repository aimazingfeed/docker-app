FROM alpine:latest

RUN apk update

CMD echo "Hello world"
RUN apk add --no-cache python3 py3-pip
RUN pip3 install fastapi uvicorn

COPY . ./
WORKDIR /app

ENV APP_PORT=8014
CMD uvicorn main:app --host 0.0.0.0 --port ${APP_PORT}