<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>

<h1>Ansible</h1>

    <h2>Описание</h2>
    <p>Этот проект включает два плейбука Ansible для настройки сервера Debian и установки PostgreSQL 16.</p>
    
    <h2>Плейбук 1: Basic Server Setup for Debian</h2>
    <p>Этот плейбук выполняет следующие задачи:</p>
    <ul>
        <li>Устанавливает ntpdate и синхронизирует системное время.</li>
        <li>Обновляет и улучшает систему.</li>
        <li>Устанавливает необходимые пакеты: vim, gnupg2, curl, ufw, unattended-upgrades, whois.</li>
        <li>Добавляет пользователей и создает их домашние директории.</li>
        <li>Настраивает и включает UFW (файрвол).</li>
        <li>Включает автоматические обновления и настройки безопасности.</li>
        <li>Перезагружает сервер при необходимости.</li>
    </ul>
    
    <h2>Плейбук 2: Install and Configure PostgreSQL 16</h2>
    <p>Этот плейбук выполняет следующие задачи:</p>
    <ul>
        <li>Устанавливает ntpdate и синхронизирует системное время.</li>
        <li>Обновляет и улучшает систему.</li>
        <li>Устанавливает необходимые пакеты: vim, gnupg2, curl.</li>
        <li>Скачивает и добавляет GPG-ключ PostgreSQL.</li>
        <li>Добавляет репозиторий PostgreSQL.</li>
        <li>Обновляет список пакетов.</li>
        <li>Устанавливает PostgreSQL 16.</li>
        <li>Запускает и включает сервис PostgreSQL.</li>
    </ul>
    
    <h2>Как использовать</h2>
    <ol>
        <li>Клонируйте репозиторий на свою машину.</li>
        <li>Запустите плейбук 1 для базовой настройки сервера:
            <pre><code>ansible-playbook -i inventory_file basic_server_setup.yml</code></pre>
        </li>
        <li>Запустите плейбук 2 для установки и настройки PostgreSQL 16:
            <pre><code>ansible-playbook -i inventory_file postgresql_setup.yml</code></pre>
        </li>
    </ol>

<h1>CI/CD</h1>

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
