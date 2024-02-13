---
title: Integrando Elasticsearch APM em aplicações Python
description: 
published: true
date: 2024-02-06T19:57:25.172Z
tags: 
editor: markdown
dateCreated: 2024-02-06T19:57:24.022Z
---

# Introdução

> Em nosso exemplo utilizaremos a lib FastAPI em um exemplo fictício de aplicação web com python
{.is-info}

## Instalando o elasticsearch com docker

Neste caso irei criar um executável `elastic.sh` no linux para executar o elasticsearch:

```sh
docker run -d -p 9200:9200 -p 9300:9300 --name elasticsearch \
  -e "discovery.type=single-node" \
  docker.elastic.co/elasticsearch/elasticsearch:7.10.0
```

Logo em seguida rodo:

```bash
$ sh elastic.sh
```

Após subir a imagem, poderemos acessar o ambiente 