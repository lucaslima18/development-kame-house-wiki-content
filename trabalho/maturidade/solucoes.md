---
title: Notas
description: 
published: true
date: 2024-01-22T09:23:45.650Z
tags: 
editor: markdown
dateCreated: 2024-01-20T09:14:48.346Z
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