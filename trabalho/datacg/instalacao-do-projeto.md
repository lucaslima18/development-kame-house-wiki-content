---
title: API + Front Documentation
description: 
published: true
date: 2023-12-06T08:45:02.068Z
tags: 
editor: markdown
dateCreated: 2023-12-05T14:45:04.076Z
---

## Test This API
[![Run in Insomnia}](https://insomnia.rest/images/run.svg)]()

## Installation

```bash
# install dependencies
$ npm install or npm i
```

```bash
# generate .env
$ cp .env.example .env
```

```bash
# generate tables in database
$ npm run migrate
```

```bash
# populate database
$ npm run seed
```

```bash
# generate migration
$ npx sequelize-cli migration:create --name=create-table
```

```bash
# rollback all migrations
$ npm run migrate:rollback
```

```bash
# rollback specific migration
$ npx sequelize-cli db:migrate:undo:all --to XXXXXXXXXXXXXX-create-table.js
```

```bash
# rollback all seeds
$ npm run seed:rollback
```

```bash
# rollback specific seed
$ npx sequelize-cli db:seed:undo --seed name-of-seed-as-in-data
```

## Running Apps

#### With Ng/Nx CLI

- First download and up the local SMTP server with Mailhog: https://github.com/mailhog/MailHog/releases
- Change MAILHOG_HOST .env variable to `localhost`

```bash
# running default app (biview)
ng serve
```

```bash
# running api
ng serve api
```

#### With docker-compose

- Change MAILHOG_HOST .env variable to `mailhog`(same service name in develop docker-compose file)

```bash
# running all apps with docker compose(admin, admin-api, mailhog, mysql, etc...)
docker-compose -f ./develop/docker-compose.yml --env-file .env up -d
```
```bash
# running specific apps with docker compose
docker-compose -f ./develop/docker-compose.yml --env-file .env start mailhog biview-database admin-api admin
```
## Homolog

* First clone this project
* Just keep this files:
  - .env-example
  - docker-compose.yml
  - docker.production.template.yml  
* Remove .git too
* Run this commands
```Bash 
cp .env.example .env
```
* Change .env with your configs
> Caddy server port: 85 and 449

## Prod

```Bash
# Run in prod
# Copy .env.example .env
# Copy docker-compose.yml and docker.production.template.yml
# Run commands above

EXPORT API_TAG=2.0.0
EXPORT CADDY_TAG=2.0.0
EXPORT PLATFORM_TAG=2.0.0

envsubst < "docker.production.template.yml" > "docker.production.yml"
docker-compose -f docker-compose.yml -f docker.production.yml up -d
```

## Create Modules NestJS

```bash
# generate module
$ nest g mo modules/test
```

```bash
# generate service
$ nest g service modules/test
```

```bash
# generate controller
$ nest g co modules/test
```

```bash
# generate resolver
$ nest g r modules/test
```

## API Documentation

## Quick Start

1. After git clone and install dependencies, execute command below in root directory:

```bash
$ ng serve api
```

2. Explore:

swagger.json: `http://localhost:3000/api/document-json`

swagger.ui: `http://localhost:3000/api/document`

## Grahpql Documentation

1. After git clone and install dependencies, execute command below in root directory:

```bash
$ ng serve student-api
```

```bash
$ npm run graphql:document
```

2. Explore:

`http://localhost:4400`
