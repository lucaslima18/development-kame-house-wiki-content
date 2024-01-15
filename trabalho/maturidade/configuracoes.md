---
title: Configuração do projeto
description: 
published: true
date: 2024-01-15T18:11:53.164Z
tags: 
editor: markdown
dateCreated: 2024-01-15T18:11:53.164Z
---

# API

- Salve em um arquivo `run.sh`, `run.txt`... whatever:
```sh
docker run -d \
--name mysql \
--hostname mysql \
-e MYSQL_USER=database \
-e MYSQL_PASSWORD=database \
-e MYSQL_DATABASE=database \
-e MYSQL_ROOT_PASSWORD=root \
-p 3306:3306 \
-v "${PWD}/data":/var/lib/mysql \
mysql:5.7

docker run -d \
--hostname rabbitmq \
--name rabbitmq \
-p 5672:5672 \
-p 15672:15672 \
-e RABBITMQ_DEFAULT_USER=rabbitmq \
-e RABBITMQ_DEFAULT_PASS=rabbitmq \
-v ./data:/var/lib/rabbitmq/mnesia/ \
rabbitmq:3-management

docker run -d \
--name redis \
-p 6379:6379 \
redis
```

