<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>

<h1>FastAPI Server</h1>

<p>Этот проект представляет собой простой HTTP-сервер на основе FastAPI, который возвращает "200 OK" на запрос <code>/healthz</code>.</p>


<h3>Сборка и запуск с использованием Docker</h3>
<ol>
    <li><strong>Постройте Docker образ:</strong>
        <pre><code>docker build -t my-fastapi-server .</code></pre>
    </li>
    <li><strong>Запустите Docker контейнер:</strong>
        <pre><code>docker run -p 8080:8080 my-fastapi-server</code></pre>
    </li>
</ol>

<h2>Проверка работоспособности</h2>
<p>Для проверки работоспособности сервера выполните команду:</p>
<pre><code>curl http://localhost:8080/healthz</code></pre>
<p>Вы должны получить ответ "OK".</p>

</body>
</html>
