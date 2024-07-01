<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FastAPI Server</title>
</head>
<body>

<h1>FastAPI Server</h1>

<p>Этот проект представляет собой простой HTTP-сервер на основе FastAPI, который возвращает "200 OK" на запрос <code>/healthz</code>.</p>

<h2>Требования</h2>
<ul>
    <li>Python 3.9+</li>
    <li>Docker</li>
</ul>

<h2>Установка и запуск</h2>

<h3>Локальный запуск</h3>
<ol>
    <li><strong>Клонируйте репозиторий:</strong>
        <pre><code>git clone &lt;URL вашего репозитория&gt;
cd &lt;название репозитория&gt;</code></pre>
    </li>
    <li><strong>Создайте и активируйте виртуальное окружение:</strong>
        <pre><code>python3 -m venv env
source env/bin/activate</code></pre>
    </li>
    <li><strong>Установите зависимости:</strong>
        <pre><code>pip install fastapi uvicorn</code></pre>
    </li>
    <li><strong>Запустите сервер:</strong>
        <pre><code>uvicorn main:app --host 0.0.0.0 --port 8080</code></pre>
    </li>
</ol>
<p>Сервер будет доступен по адресу <a href="http://localhost:8080/healthz">http://localhost:8080/healthz</a>.</p>

<h3>Сборка и запуск с использованием Docker</h3>
<ol>
    <li><strong>Постройте Docker образ:</strong>
        <pre><code>docker build -t my-fastapi-server .</code></pre>
    </li>
    <li><strong>Запустите Docker контейнер:</strong>
        <pre><code>docker run -p 8080:8080 my-fastapi-server</code></pre>
    </li>
</ol>
<p>Сервер будет доступен по адресу <a href="http://localhost:8080/healthz">http://localhost:8080/healthz</a>.</p>

<h2>Проверка работоспособности</h2>
<p>Для проверки работоспособности сервера выполните команду:</p>
<pre><code>curl http://localhost:8080/healthz</code></pre>
<p>Вы должны получить ответ "OK".</p>

<h2>Автор</h2>
<p>Ваше имя</p>

<h2>Лицензия</h2>
<p>Этот проект лицензирован под лицензией MIT. Подробности см. в файле LICENSE.</p>

</body>
</html>
