---
title: Primeiros Passos
description: 
published: true
date: 2024-02-06T19:57:26.880Z
tags: 
editor: markdown
dateCreated: 2024-02-06T19:57:07.488Z
---

# Primeiros Passos

O objetivo deste curso é capacitar pessoas para desenvolverem sua primeira aplicação nest… mas que aplicação? pois bem, aqui iremos criar uma API REST utilizando NestJS.

> 💡 Para esta aplicação precisaremos apenas do NodeJs instalado na máquina para darmos início a instalação do NestJs.
> 

> 💡 Sou usuário de linux como programador, então, caso algum dos comandos que eu citar durante o curso não funcione e você esteja utilizando um sistema operacional diferente, não se preocupe, existem duas maneiras de resolver seu problema… “google it” ou venha para o lado linux da força.
> 

Brincadeiras a parte, vamos iniciar nosso curso.

## Instalando o NestJs e criando o projeto

Para fazer a instalação do NestJs na sua máquina basta utilizar o seguinte comando (recomendo a utilização do nodeJs na versão 20 ou superior para este curso):

```bash
 $ npm i -g @nestjs/cli
```

Em seguida iremos criar nosso projeto:

```bash
$ nest new nest-marketplace
```

Aqui o nest irá nos perguntar qual gerenciador de pacotes utilizaremos (no caso do nosso curso utilizarei o npm)

 

Após criado o projeto entre no mesmo e rode o start:

```bash
$ cd nest-marketplace
$ npm start
```

No seu navegador, basta entrar em http://localhost:3000 que sua aplicação estará rodando.

> 💡 é possível modificar a porta do arquivo editando o arquivo **main.ts**
> 

> 💡 para rodar a aplicação em modo de desenvolvedor (onde a aplicação restarta automaticamente e nos exibe mais conteúdo) utilize o comando `npm start:dev`
> 

## Limpando o excesso

Neste projeto iremos criar tudo quase do zero, então sinta-se a vontade para entrar em src/ e apagar o que for desnecessário no momento, como (fique a vontade para manter o `app.module.ts`):

- app.controller.ts
- app.controller.spec.ts
- app.service.ts