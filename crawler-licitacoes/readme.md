---
title: README
description: 
published: true
date: 2024-03-06T13:12:45.996Z
tags: 
editor: markdown
dateCreated: 2024-02-06T19:57:05.729Z
---

# LicitaS

Este Crawler é um produto desenvolvido para atender as necessidades da Mesha Tecnologia relacionadas a obtenção de novas ropostas de contrato através do monitoramento de licitações vindas do sistema S.

O LiciaS Atualmente é capaz de fazer consultas periódicas e agendadas a uma lista de sites de licitações do sistema S.

# Requisitos do sistema
Instalação via docker:

- Sistema ou servidor Linux (qualquer distro) / macOS
- Docker >= 24.0

Instalação manual (ideal para testes locais)
- python >= 3.11.4
- Google Chrome >= 120.0.6099.109
- mysql >= 5

# Instalação

## Instalação via docker

## Instalação manual

Para fazer a instalação manual siga o seguinte passo a passo:

1 - Clone este repositório;
2 - Garanta que está seguindo todos os requisitos mínimos de instalação;
x-  Copie o conteúdo de `config.example.json` para um arquivo chamado `config.json` no mesmo diretório;
x - Altere as informações do banco de dados de acordo com o banco que será utilizado, seguindo o exemplo:
```json
  "db_host": "HOSTUTILIZADO",
  "db_port": "PORTADOBANCO",
  "db_database": "NOMEDOBANCO",
  "db_user": "SEUUSUARIO",
  "db_password": "SUASENHA",
```

x - (Opcional) Você também pode modificar outras opções como:

```json
  "log_level": "INFO", //log level: INFO, DEBUG, ERROR, WARN
  "scheduler_time": 24, // tempo em horas
```
3 - Para instalar o poetry vamos rodar no terminal `$ pip install poetry==1.2.0`;
4 - Rode `$ poetry shell` para entrar no ambiente virtual;
5 - Rode `$ poetry install` para instalar todas as dependencias do projeto;
6 - Vamos agora habilitar o nosso script .sh de inicialização para 
7 - Para iniciarmos o projeto vamos rodar ` 

# Sites Cobertos pelo crawler
z
Atualmente o crawler da cobertura aos seguintes links:

- https://licitacao.fiea.com.br/,
- http://transparencia.sesiac.org.br/sistema/editais_transparencia/index.php?Casa=2,
- https://licitacao.sesisenaiap.org.br/,
- https://licitacoes.fieam.com.br/,
- https://licitacoes.sistemafibra.org.br/,
- https://www.portaldaindustria.com.br/licitacoes/,
- https://transparencia.fiema.org.br/,
- https://transparencia.sesipa.org.br/licitacoes-e-editais,
- https://www.google.com/url?q=https://licitacoes.fiepb.org.br/&sa=D&source=docs&ust=1699038497030262&usg=AOvVaw35-4xyYl2IM2MEtdb23QeC,
- https://portaldecompras.sistemafiep.org.br/,
- http://licitacoes.pe.sesi.org.br:8081/,
- https://licitacao.fiero.org.br/,
- https://lsa.fies.org.br/,
- http://licitacao.sesi-to.com.br/
- http://licitacao.sesi-to.com.br/


# Sites consultados 

