---
layout: post
title:  "Alta escalabilidade com Microsserviços"
description: "Atualmente, termos como escalabilidade, computação na nuvem e DevOps estão em alta. Mas como deixar suas aplicações altamente escaláveis e mutáveis? Este artigo tem o intuito de demonstrar como os microsserviços podem ajudar a alcançar esses objetivos. No passado,..."
date:   2018-03-10 12:25:00
categories: ['Gambarra']
---

Atualmente, termos como escalabilidade, computação na nuvem e DevOps estão em alta. Mas como deixar suas aplicações altamente escaláveis e mutáveis? Este artigo tem o intuito de demonstrar como os microsserviços podem ajudar a alcançar esses objetivos.
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

Há alguns anos, as pessoas começaram a falar sobre empresas que estavam conseguindo construir soluções mais rápidas, seguras, altamente escaláveis e que não enfrentavam os problemas descritos acima. Tentando entender esse novo cenário um grupo de arquitetos conseguiu mapear esse padrão e deu-lhe o nome de microsserviços.

<span style="color:blue">Mas afinal o que são Microsserviços (microservices)?</span>

Embora não haja uma definição formal de microsserviços, existem certas características que norteiam esse padrão arquitetônico. A principal ideia é construir serviços que sejam pequenos, independentes e focados na resolução de um único problema dentro de um ecossistema de uma aplicação.

<span style="color:blue">Principais características do modelo de microsserviços</span>

Como mencionado anteriormente não há uma regra para definir o comportamento e os padrões de uma arquitetura microservice. Porém gosto bastante de seguir os seis princípios abaixo, também defendidos por [Rag Dhiman](https://www.linkedin.com/in/ragdhiman/).

<span style="color:blue">1. Alta Coesão</span>

Um dos princípios da arquitetura de microsserviços é a alta coesão, o serviço deve ter um único foco. Ou seja, ter uma única responsabilidade  do domínio da aplicação. Este princípio é útil para controlar o tamanho e impedir que o microserviço se torne um serviço monolítico. Como ocorria com os serviços na arquitetura SOA.

<span style="color:blue">2. Autônomos</span>

Um microserviço deve ser autônomo, ou seja, não deve depender de outros serviços que interajam com ele. Isto implica na mudança de um microserviço dentro de uma aplicação. Ele não deve forçar que outros microsserviços necessitem mudar. O ponto importante desse princípio reflete que cada microserviço deve ter seu próprio banco de dados ou outro serviço de armazenamento.

<span style="color:blue">3. Resiliência</span>

Não importa a velocidade e os custos das soluções, é importante construir sistemas que reajam a falhas inesperadas. Em uma arquitetura de microserviço este é um ponto muito importante. Precisamos ter certeza que nossos microsserviços são resilientes. Ou seja, são capazes de validar os dados recebidos (mesmo que estes estejam corrompidos) e tratar a perda ou falha na comunicação com outro serviço da cadeia, sem quebrar o fluxo da aplicação.

<span style="color:blue">4. Observável</span>

Outro ponto importante quando pensamos em microsserviços é poder acompanhar o status do sistema. Ou seja, conseguir observar o que está acontecendo atualmente no nosso sistema, como erros. Esse tipo de monitoramento precisa ser centralizado para facilitar a busca de informações sobre o status atual do sistema. Como microsserviços é uma arquitetura distribuída, a ideia de centralizar o monitoramento, principalmente os logs, facilita verificação do ciclo completo de toda mensageria trocada. Desde a primeira iteração do usuário até a solução entregue pela aplicação.

<span style="color:blue">5. Automatização</span>

Com a divisão de uma aplicação entre diversos mini blocos há uma necessidade maior de automatizar algumas tarefas para manter este tipo de arquitetura. Como integração contínua e entrega contínua. Esse é um dos aspectos que fazem esse modelo ser abraçado por defensores da cultura DevOps. Pois esta é a ideia principal que move essa cultura.

<span style="color:blue">6. Centrado no domínio do negócio</span>

Um microserviço deve estar focado no domínio do negócio. Assim sendo, deve ser uma função do negócio. Quem conhece o padrão de desenvolvimento DDD sabe que o domínio é o coração de uma aplicação. Utilizando um padrão distribuído como microsserviços não é diferente. O conceito base que alicerça este pensamento é o que no DDD chamamos de Bounded Context (ou contextos delimitados).  Os contextos delimitados servem para refatorar um grande domínio em pequenos conjuntos de domínios que unidos representam o modelo de negócio de uma aplicação ou empresa. E é exatamente essa característica um dos pontos fundamentais no modelo de microsserviços.

<span style="color:gray">Abaixo segue uma imagem demonstrando como funciona uma arquitetura focada em microsserviços. </span>

![](/assets/images/\microoservice/micro-servicos.png)

Observe que como descrito acima, cada serviço é responsável por seu próprio sistema de armazenamento.

Outro ponto importante é que geralmente há uma camada designada a orquestrar esses serviços. Essa orquestração pode ser realizada através uma API de orquestração ou de um Service BUS.

<span style="color:blue">Quais as vantagens de utilizar microsserviços?</span>

Além de ser uma arquitetura utilizada em grandes cases de sucesso, ela traz algumas vantagens:

* Diminui as dependências entre equipes, resultando em um código entregue mais rápido para produção;
* Permite que muitas iniciativas sejam executadas em paralelo;
* Suporta múltiplas tecnologias, linguagens de programação e frameworks;
* Permite que a degradação do serviço seja mais branda;
* Promove a facilidade de inovação através de código descartável – é fácil falhar e seguir em frente.

Como cada serviço que compõe o software final é pequeno e independente, os ajustes são tarefas mais simples e menos impactantes. Mesmo que ocorra a substituição dele por uma versão mais nova, que altera inclusive a linguagem de programação. No entanto, a equipe de desenvolvimento deve respeitar a regra de negócio contida no serviço e o seu contrato. Isso cria oportunidades para mais equipes estarem construindo de forma paralela a mesma solução.

<span style="color:blue">Quais as desvantagens de utilizar microsserviços?</span>

Como no mundo computacional não existe uma solução perfeita e nem ideal para todos os cenários, os microsserviços também podem ter suas desvantagens:

* Desenvolvedores devem lidar com uma complexidade adicional de criar e manter um sistema distribuído;
* A maioria das IDE são orientadas para construção de aplicativos monolíticos e não fornecem de maneira simples suporte a aplicativos distribuídos;
* Na produção, há também a complexidade de implantar e gerenciar um sistema de muitos serviços;
* Dificuldade de um programador iniciante conseguir entender a estrutura do aplicativo, pois sistemas monolíticos são muito mais fáceis de serem entendidos.

<span style="color:blue">Quando devo utilizar microsserviços?</span>

Essa é uma dúvida recorrente no começo do planejamento de uma nova aplicação ou se deseja a migração de um sistema monolítico para microsserviços. Não há uma resposta precisa. É necessário analisar os recursos que a equipe dispõe e a previsão do crescimento e amplitude do aplicativo. Geralmente, aplicações monolíticas tendem a ser mais vantajosas quando o escopo da aplicação é menor. Entretanto, com o crescimento deste escopo, a arquitetura baseada em microserviço tem se mostrado mais produtiva.

Alguns cases de sucesso como Netflix e Amazon estão aí para nos mostrar que microsserviços não são o futuro. Eles são uma realidade cada vez mais presente.  Cabe ao arquiteto de cada empresa decidir qual o melhor padrão adotado para o cenário que deseja atacar.  Para saber mais, Martin Fowler explica de forma detalhada como fazer essa análise em seu artigo intitulado [Microservices](https://martinfowler.com/articles/microservices.html).

Por hoje é só... 