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

<span style="color:blue">2. Autônomos</span>

Um microserviço deve ser autônomo, ou seja, não deve depender de outros serviços que interajam com ele. Isto implica na mudança de um microserviço dentro de uma aplicação. Ele não deve forçar que outros microserviços necessitem mudar. O ponto importante desse princípio reflete que cada microserviço deve ter seu próprio banco de dados ou outro serviço de armazenamento.

<span style="color:blue">3. Resiliência</span>

Não importa a velocidade e os custos das soluções, é importante construir sistemas que reajam a falhas inesperadas. Em uma arquitetura de microserviço este é um ponto muito importante. Precisamos ter certeza que nossos microserviços são resilientes. Ou seja, são capazes de validar os dados recebidos (mesmo que estes estejam corrompidos) e tratar a perda ou falha na comunicação com outro serviço da cadeia, sem quebrar o fluxo da aplicação.

<span style="color:blue">4. Observável</span>

Outro ponto importante quando pensamos em microserviços é poder acompanhar o status do sistema. Ou seja, conseguir observar o que está acontecendo atualmente no nosso sistema, como erros. Esse tipo de monitoramento precisa ser centralizado para facilitar a busca de informações sobre o status atual do sistema. Como microserviços é uma arquitetura distribuída, a ideia de centralizar o monitoramento, principalmente os logs, facilita verificação do ciclo completo de toda mensageria trocada. Desde a primeira iteração do usuário até a solução entregue pela aplicação.

<span style="color:blue">5. Automatização</span>

Com a divisão de uma aplicação entre diversos mini blocos há uma necessidade maior de automatizar algumas tarefas para manter este tipo de arquitetura. Como integração contínua e entrega contínua. Esse é um dos aspectos que fazem esse modelo ser abraçado por defensores da cultura DevOps. Pois esta é a ideia principal que move essa cultura.

<span style="color:blue">6. Centrado no domínio do negócio</span>

Um microserviço deve estar focado no domínio do negócio. Assim sendo, deve ser uma função do negócio. Quem conhece o padrão de desenvolvimento DDD sabe que o domínio é o coração de uma aplicação. Utilizando um padrão distribuído como microserviços não é diferente. O conceito base que alicerça este pensamento é o que no DDD chamamos de Bounded Context (ou contextos delimitados).  Os contextos delimitados servem para refatorar um grande domínio em pequenos conjuntos de domínios que unidos representam o modelo de negócio de uma aplicação ou empresa. E é exatamente essa característica um dos pontos fundamentais no modelo de microserviços.

<span style="color:gray">Abaixo segue uma imagem demonstrando como funciona uma arquitetura focada em microserviços. </span>

![](/assets/images/\microoservice/micro-servicos.png)

Observe que como descrito acima, cada serviço é responsável por seu próprio sistema de armazenamento.

Outro ponto importante é que geralmente há uma camada designada a orquestrar esses serviços. Essa orquestração pode ser realizada através uma API de orquestração ou de um Service BUS.