# O que é Arquitetura Serverless?

![O que é Arquitetura Serverless?](https://blog.tecnospeed.com.br/wp-content/uploads/2018/09/lambda.png)

Tempo de Leitura: 4 minutos

*Descubra a Arquitetura Serverless em seus diversos aspectos: origem, vantagens, frameworks, e veja como começar a utilizar na sua empresa.*



------

Arquitetura Serverless, ou “computação sem servidores”, é uma arquitetura de computação **orientada a eventos**. Sua principal proposta é permitir que as empresas de software criem e mantenham seus aplicativos web sem se preocupar com a infraestrutura em que esses aplicativos estão rodando.

Trata-se de um conceito relativamente novo, que ganhou popularidade devido aos serviços como *AWS Lambda*, *Microsoft Azure*, *Google Cloud*, entre outros.

Neste artigo, analisaremos a Arquitetura Serverless em diversos aspectos: origem, definição, vantagens, e apresentaremos a palestra sobre Serverless do Fábio Rogério no [TecnoUpdate 2018](https://tecnospeed.com.br/tecnoupdate)!

 

## Antes da Arquitetura Serverless

Para compreender o conceito da Arquitetura Serverless, é necessário compreender como surgiu a demanda por ela. Para isso, vamos analisar os paradigmas que precederam a Arquitetura Serverless.

 

### Infraestrutura In-house

No início das aplicações web, era comum utilizar um hardware contendo um sistema operacional e a aplicação. Alguns chamam essa abordagem de “**infraestrutura in-house**“. Em muitos casos, esse hardware era hospedado em um data center, e a software house pagava pelo espaço e infra que utilizava.

 

### Computação Cloud Tradicional

Com o ganho de performance em virtualização de máquinas, começamos a trabalhar com a **computação cloud**. Na computação cloud tradicional, nossas aplicações ficam em máquinas virtuais onde era possível aumentar (upgrade) ou diminuir (downgrade) o poder de processamento.

Atualmente, a maiorias das aplicações online estão em máquinas virtuais.

 

### Backend as a Service (BaaS)

Com a evolução das provedoras de **cloud**, surgiu a oferta de serviços de **backend** já construído e distribuído, conhecido como “BaaS”. Desta forma, a software house pode concentrar seus recursos em regras de negócio de implementação, abstraindo as necessidades de infraestrutura.

![Serverless Esquema](https://tecnospeed.com.br/blog/wp-content/uploads/2018/09/pasted-image-0.png)

## **Não tão server*****less\*** **assim…**

Antes de mergulharmos de cabeça no magnífico conceito da arquitetura Serverless, precisamos desmistificar seu nome tendencioso.

*Serverless*, traduzido literalmente do inglês, significa “sem servidor”. Isso **não é verdade**. A arquitetura Serverless ainda é baseada em servidores. Nela, porém, o desenvolvedor não precisa configurar ou se preocupar com a maioria dos aspectos da infraestrutura em que sua aplicação será rodada. Essas decisões dinâmicas de infraestrutura ficam ocultas para o desenvolvedor ou operador.

Com essa possível confusão já desfeita, vamos ao que interessa.

 

## Arquitetura Serverless: Function as a Service (FaaS)

Utilizando uma plataforma Serverless, o time de desenvolvimento da software house não precisa gerenciar a infraestrutura de servidores, como provisionamento, capacidade de processamento, sistemas de armazenamento, atualização dos servidores, entre muitas outras configurações recorrentes: todas essas funções ficam a cargo do provedor cloud.

Com esse trabalho periférico mitigado, os desenvolvedores passam a ter mais mais tempo para se dedicar a suas funções primárias, entregando muito mais software em um mesmo período.

Apesar de ser a vantagem mais óbvia da arquitetura Serverless, o tempo ganho pelo dev é apenas um dos destaques da arquitetura Serverless.

 

## Quais as vantagens da Arquitetura Serverless?

As principais vantagens da Arquitetura Serverless são o escalamento automático (auto scaling) e a redução de custo.

 

### ***Auto scaling***

A escalabilidade é realizada de forma automática: quanto mais consumo você tem nas suas funções, mais disponibilidade ela terá. Deste modo, podemos dizer que a escalabilidade é quase infinita. No entanto, de acordo com seu provedor, podem existem limitações e bloqueios de segurança. Lembre-se: você paga cada vez que a função é executada.

 

### **Redução de custo**

Cada vez que sua função é executada, você é cobrado apenas pelo processamento consumido. Sendo assim, você não paga por tempo ocioso, que é um problema que ocorre em máquinas virtuais.

 

## **Como começar a utilizar Serverless?**

A forma mais prática de começar a desenvolver com serverless é utilizando um Framework específico para essa finalidade. Vamos falar sobre dois destes frameworks, cujas especificidades que merecem destaque:

 

### Serverless Framework

Sim, o framework tem exatamente o mesmo nome da arquitetura. **Não se confunda: são conceitos diferentes!**

![Serverless Framework](https://tecnospeed.com.br/blog/wp-content/uploads/2018/09/serverless-square-icon-text-150x150.png)

Sem mais delongas: o Serverless é um framework web e open-source, escrito em Node.js. Quando foi desenvolvido, o Serverless Framework era destinado exclusivamente para a criação de aplicações para o AWS Lambda, a plataforma da Amazon Web Services de serverless cloud computing. Posteriormente, foi compatibilizado com outros fornecedores de cloud, como a Microsoft Azure, IBM BlueMix, Google Cloud, Oracle Cloud, entre outros.

Utilizando o Serverless Framework, **seu código deve respeitar a interface da fornecedora cloud** que você optou por utilizar. Sendo assim, é 

muito mais difícil adaptar um software criado para rodar em cloud tradicional utilizando o Serverless Framework em relação ao próximo framework que será apresentado. 

No entanto, o Serverless Framework é muito vantajoso. Com ele, o desenvolvedor tem acesso a todos os recursos da arquitetura serverless – e são muitos! – para o seu software, que afetam desde a performance até a experiência do usuário.

**No geral, se você tem a opção de construir seu software com o Serverless Framework, faça-o!**

 

### Up

O Up também é um framework open-source para rodar aplicações em arquitetura serverless. No entanto, sua proposta é quase contrária à do Serverless Framework: o Up é “direto e reto”: não oferece as funcionalidades fantásticas propostas pelo concorrente, mas seu grande atrativo é, em muitos casos, suficiente para atrair os desenvolvedores.

Utilizando Up, não é necessário realizar nenhuma alteração no código de sua aplicação já existente. Ao utilizar o comando ‘Up’ que dá nome ao framework, seu software será adaptado para rodar com a arquitetura serverless, e em seguida já estará em produção.

Assim, se você desenvolveu seu software para rodar em arquitetura tradicional, migrá-lo para serverless com Up é **muito** mais fácil! Por outro lado, o seu software será **adaptado**, e portanto, não poderá utilizar as funcionalidades especiais dos provedores serverless.

 

## Aprenda mais sobre Arquitetura Serverless no TecnoUpdate 2018!

No [TecnoUpdate 2018](https://tecnospeed.com.br/tecnoupdate), **Fábio Rogério** do PlugMobile apresentará uma palestra completa sobre a Arquitetura Serverless:

- O que exatamente é Arquitetura Serverless?
- Como está sendo a experiência da TecnoSpeed e do [PlugMobile](https://www.plugmobile.com.br/) com Serverless?
- Como começar a utilizar Serverless em sua empresa?
- Quais são os frameworks para desenvolvimento em Serverless?
- e muito mais!