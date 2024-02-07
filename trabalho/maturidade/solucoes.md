---
title: Notas
description: 
published: true
date: 2024-02-07T17:24:06.999Z
tags: 
editor: markdown
dateCreated: 2024-02-06T19:57:32.000Z
---

# Notas

> caso ocorra no uma falha ao tentar logar falando sobre o ultimo reset de senha ser a mais de 2 meses, vc pode dar update no banco atualizando a coluna `last_password_reset`:
> 
> ```sql
> USE maturidade_digital;
> SELECT * FROM users WHERE id=1001;
> UPDATE users SET last_password_reset =NOW() where id=1001;
> ```
{.is-info}



> Para mandar uma task para uma coluna específica no board do DevOps, basta inserir o seguinte texto na descrição do pr:
>`{nome da coluna}:#{n° da task}`
{.is_info}

> Caso ocorra algum problema de regra de lgpd tente rodar as migrations
{.is_info}

> Caso suba algum package.lock.json indesejado, basta utilizar esse comando:
> ```shell
> $ git checkout preview -- package-lock.json
> ```

> Caso eu queria inserir um dump da cni no meu projeto, é necessário antes de fazer o cat renomear o define dos usuários:
> ```
> sed -i 's/DEFINER=usr_maturidadedigital@/DEFINER=root@root/g' {nome_do_dump}.sql
> ```