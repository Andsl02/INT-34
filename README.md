FastAPI Server
Этот проект представляет собой простой HTTP-сервер на основе FastAPI, который возвращает "200 OK" на запрос /healthz.
Постройте Docker образ:
docker build -t my-fastapi-server .
Запустите Docker контейнер:
docker run -p 8080:8080 my-fastapi-server
