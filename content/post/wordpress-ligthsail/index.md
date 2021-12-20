---
title: Configurando um site WordPress na AWS LightSail
date: "2021-08-03T10:36:00.000Z"
layout: post
draft: true
path: "/posts/wordpress-ligthsail/"
category: "Tutorial"
tags:
  - "WordPress"
  - "AWS"
description: "Mais uma opção para hospedar um site WordPress"
---

Existe uma grande gama de possibilidades de hospedagem de um site em WordPress,
seja hospedagem específicas, compartilhadas, o serviço da própria WordPress ou
em servidores VPS, em que você precisa configurar tudo do zero.

A Amazon possui um serviço na AWS chamado LightSail. Esse serviço simplifica
várias configurações para criar um servidor web, bem como disponibiliza alguns
templates de aplicações pré-configuradas.

Um desses templates é do WordPress fornecido pela Bitnami. Nele, já começamos
um servidor com WordPress instalado, banco de dados e Apache configurados.
Desta forma, basta fazer mais algumas configurações e teremos um site com SSL
e domínio configurados.

## Criando o servidor no LigthSail

cat bitnami_application_password

Step 3: Attach a static IP address to your WordPress instance

Registro.br A record

sudo /opt/bitnami/bncert-tool