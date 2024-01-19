---
title: Configuração do projeto
description: 
published: true
date: 2024-01-19T13:57:57.377Z
tags: 
editor: markdown
dateCreated: 2024-01-16T11:48:38.005Z
---

# API
- Acesso ao grafana:
```txt
User: adm
Pass: dQLY8otQ0hx87I^MPWoK
```

- Versão do node: `16.18.1`

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

rode com:

```sh
$ sh run {nome_do_arquivo}.{sh ou txt}
```

Caso não queira usar as seeds, utilize o [dump](https://drive.google.com/file/d/1hp2Nh6vdQEJQH0dzg6c8wgpzq-o1oQCe/view?pli=1)

Após baixar, utilize o comando:

```sh
$ cat {nome_do_dump}.sql | docker exec -i {nome_da_imagem} /usr/bin/mysql -u {user} --password={password} maturidade_digital
```

Acesso:

```txt
User: mateus.bezerra@somosmesha.com
Pass: Br!@3456
```

Para rodar a api:
```sh
$ npm run i
$ npm run build
$ npm run migration:run

// lembre fazer o processo do dump caso necessário aqui, ou rode seeds
$ npm run start
```

caso dê algum problema no processo, tente:

```sh
$ rm -rf dist
$ rm -rf build

// Repita o processo...
```



