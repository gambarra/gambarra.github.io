---
layout: post
title:  "Alta escalabilidade com microserviços"
description: "Atualmente, termos como escalabilidade, computação na nuvem e DevOps estão em alta. Mas como deixar suas aplicações altamente escaláveis e mutáveis? Este artigo tem o intuito de demonstrar como os microserviços podem ajudar a alcançar esses objetivos. No passado,..."
date:   2018-03-10 12:25:00
categories: ['Gambarra']
---

Atualmente, termos como escalabilidade, computação na nuvem e DevOps estão em alta. Mas como deixar suas aplicações altamente escaláveis e mutáveis? Este artigo tem o intuito de demonstrar como os microserviços podem ajudar a alcançar esses objetivos.
No passado, muitas aplicações eram construídas de forma Monolítica. Todo o negócio estava embutido em um único programa e, às vezes, até distribuídos em camadas. Porém, sempre com um alto acoplamento entre esses componentes. Um exemplo clássico disso são as aplicações construídas no modelo MVC (Model View Controller).

![](/assets/images/\microoservice/escalabilidade.gif)

Na tentativa de aumentar a escalabilidade destas aplicações, surgiu o padrão de arquitetura denominada SOA (arquitetura orientada para serviço).  SOA permitiu a criação de serviços de negócio interoperáveis que podem facilmente ser reutilizados e compartilhado entre aplicações em empresas.

O padrão SOA trouxe alguns benefícios:

* Facilidade de manutenção
* Reuso
* Flexibilidade
* Qualidade

Durante muito tempo, e ainda hoje, muitas empresas adotam esse padrão arquitetônico para suas aplicações. Contudo, alguns problemas ainda estão presentes nesta abordagem. Apesar de facilitar a escalabilidade, as aplicações continuam um grande monólito. Quando há uma distribuição da regra de negócio entre diversos serviços, há um grande acoplamento entre eles. Seja através do compartilhamento do mesmo banco de dados ou da interdependência entre os serviços.


<span style="color:blue">Como evoluir a arquitetura SOA?</span>

Há alguns anos, as pessoas começaram a falar sobre empresas que estavam conseguindo construir soluções mais rápidas, seguras, altamente escaláveis e que não enfrentavam os problemas descritos acima. Tentando entender esse novo cenário um grupo de arquitetos conseguiu mapear esse padrão e deu-lhe o nome de microserviços.

<span style="color:blue">Mas afinal o que são microserviços (microservices)?</span>

Embora não haja uma definição formal de microserviços, existem certas características que norteiam esse padrão arquitetônico. A principal ideia é construir serviços que sejam pequenos, independentes e focados na resolução de um único problema dentro de um ecossistema de uma aplicação.

<span style="color:blue">Principais características do modelo de microserviços</span>

Como mencionado anteriormente não há uma regra para definir o comportamento e os padrões de uma arquitetura microservice. Porém gosto bastante de seguir os seis princípios abaixo, também defendidos por [Rag Dhiman](https://www.linkedin.com/in/ragdhiman/).

<span style="color:blue">1. Alta Coesão</span>

Um dos princípios da arquitetura de microserviços é a alta coesão, o serviço deve ter um único foco. Ou seja, ter uma única responsabilidade  do domínio da aplicação. Este princípio é útil para controlar o tamanho e impedir que o microserviço se torne um serviço monolítico. Como ocorria com os serviços na arquitetura SOA.