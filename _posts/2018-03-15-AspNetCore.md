---
layout: post
title:  "Entendendo o Entity Framework Core"
description: "Este é o primeiro artigo de uma série que demonstrará o que é o Entity Framework Core 2.0, suas principais mudanças em relação as versões anteriores e um overview completo de suas funcionalidades até o momento. Estes artigos destinam-se tanto para aqueles que conhecem o Entity Framework e agora estão migrando para o .Net Core quanto os iniciantes em desenvolvimento."
date:   2018-03-11 12:25:00
categories: ['Gambarra']
---

Este é o primeiro artigo de uma série que demonstrará o que é o Entity Framework Core 2.0, suas principais mudanças em relação as versões anteriores e um overview completo de suas funcionalidades até o momento. Estes artigos destinam-se tanto para aqueles que conhecem o Entity Framework e agora estão migrando para o .Net Core quanto os iniciantes em desenvolvimento.

A primeira coisa que precisamos saber é que o Entity Framework foi reescrito do zero e assim como todo o .Net Core Framework é multiplataforma. 

O EF Core é um ORM(Relational Object Mapping) que permite aos desenvolvedores trabalharem com um banco de dados usando objetos .NET. Eliminando assim a necessidade de utilizar códigos SQL para inserir, recuperar e alterar dados junto ao Database.  

O diagrama abaixo demonstra como o EF Core funciona. 

![](/assets/images/entityframework/entity.jpg)

### Agora veremos na prática o EF Core

Ao longo dessa série iremos construir um projeto onde será demonstrado como utilizar o EF Core. Estou utilizando o [Visual Studio 2017](https://www.visualstudio.com/pt-br/downloads/). 

Criando a estrutura do projeto

1. Abra o `Visual Studio` e crie um novo `Project...`
2. Selecione a opção `Other Project Types..` `Visual Studio Solutions..` `Blank Solution`
3. Renomei o projeto para LojaVirtualDemo (Ou outro nome da sua escolha)
4. Clique com o botão direito do mouse sobre a Solution e adicione dois projetos do typo `Class Library..` LojaVirtualDemo.Domain e LojaVirtualDemo.Repository

Adicionando o EF Core ao Projeto

Existem duas formas de adicionar o EF Core ao projeto

1. Através de linha de comando no `Package Manager Console`

![](/assets/images/installpackageefcore.jpg)

2. Instalando o pacote através do `Package Manager`

![](/assets/images/installmanagerpackageefcore.jpg)


Agora iremos criar a estrutura do domínio da nossa aplicação. Adicione as seguintes classes ao domínio.

**Produto**	
![](/assets/images/entityframework/produto.jpg)

**ItemCarrinho**
![](/assets/images/entityframework/itemcarrinho.jpg)

**Carrinho**	
![](/assets/images/entityframework/carrinho.jpg)

**Comprador**
![](/assets/images/entityframework/comprador.jpg)

**Pedido**
![](/assets/images/entityframework/pedido.jpg)


Por hoje é só. Continuamos no próximo artigo...