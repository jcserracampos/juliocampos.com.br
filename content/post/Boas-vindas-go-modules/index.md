---
title: Boas-vindas, Go Modules
date: "2018-11-08T16:51:00.000Z"
layout: post
draft: true
path: "/posts/boas-vindas-go-modules/"
category: "Blog"
tags:
  - "Golang"
  - "Web Development"
description: "É possível ser mais simples ainda programar em Go? Sim, com go modules!"
---

O maior problema que enfrentei quando comecei a aprender Golang foi entender que todos os meus projetos, seja eles de teste ou até para produção, deveriam ficar em uma pasta específica.

Vindo do Ruby, eu já estava bem acostumado a ter minhas pasta Projetos e deixar meus códigos por ali mesmo, mas nada que me prendesse a essa pasta.

Muitas vezes fiz o download de um código-fonte compactado e trabalhei nele diretamente da pasta de download e funcionava.

---

![Talvez o melhor gopher de todos](./01.png)

A linguagem criada pelo Google possui o conceito de $GOPATH que facilita muito a executar códigos go, já que basta adicionar `${GOPATH//://bin:}/bin` a seu PATH e você terá acesso em qualquer pasta dentro do seu terminal a qualquer binário instalado na sua máquina. Parece prático, né?

Só que do mesmo jeito que todos os binários do Go estão dentro do seu $GOPATH, os códigos também estão. A estrutura começa a ficar mais confusa quando o gopher resolve nos recomendar usar um conceito de namespace um pouco confuso. Seus códigos ficarão salvos no github, né? Então que tal você colocar seu código dentro da pasta `$GOPATH/src/github.com/seuusuarioaqui`? Melhor ainda! Que tal colocar todos seus códigos dentro dessa mesma pasta?

É lógico que existem as vantagens de centralizar todos os códigos, inclusive das dependências, em uma pasta só. É muito prático instalar uma dependência para seu código em go, até parece que você está dando um apt-get e só.

Mesmo assim o meu TOC não lidou bem com isso, além de ter sofrido um pouco com o gerenciamento de versão dos meus códigos — quem nunca deu um git init na pasta github.com?

Pensando em modularidade a equipe da Golang lançou na versão 1.11 da linguagem a possibilidade de criar pequenos pacotes de código que foram chamados — você nem vai acreditar !— go modules.

---

Go mods — já somos íntimos — é o primeiro passo para a criação de uma ferramenta oficial de gerenciamento de pacotes. E como está funcionando?
Você escreve sua aplicação declarando suas dependências.
Um arquivo lock é gerado ajudando a versionar o projeto.
Opcionalmente você pode colocar seus assets também.

Parece familiar, né?

E a melhor parte:

É simples.

Talvez gere uma pequena barreira porque criar módulos em Go exige a utilização de versionamento semântico e algumas pessoas desenvolvedoras não chegaram a estudar ou utilizar no trabalho. Mas nada que uma lida rápida não resolva.

---

Eu sei o que você, pessoa que trabalha em empresa e precisa lidar com mil versões de projetos e dependências, está pensando.

A resposta é sim!

Os módulos não serão atualizados para versões majoritárias automaticamente, então será possível ter maior controle sobre a sua base de código sem ter preocupação com correções de bugs lançadas em versões minoritárias.

---

E aí? O que está esperando para tentar?

A [documentação oficial](https://golang.org/cmd/go/#hdr-Module_maintenance) traz mais informações.

Qualquer dúvida, pode me procurar no Twitter que trocamos uma ideia.