# O que é serverless?

Publicado em: 31 de outubro de 2017•11 minutos (tempo de leitura)



Copiar URL

IR PARA SEÇÃO

- [Visão geral](https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-serverless#visão-geral)
- [Visão geral da arquitetura serverless](https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-serverless#visão-geral-da-arquitetura-serverless)
- [Função do provedor de nuvem](https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-serverless#função-do-provedor-de-nuvem)
- [O que é FaaS?](https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-serverless#o-que-é-faas)
- [Casos de uso](https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-serverless#casos-de-uso)
- [O que é Knative e Kubernetes serverless?](https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-serverless#o-que-é-knative-e-kubernetes-serverless)
- [Prós e contras](https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-serverless#prós-e-contras)
- [A evolução do serverless](https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-serverless#a-evolução-do-serverless)

## Visão geral

Serverless é um modelo de desenvolvimento [nativo em nuvem](https://www.redhat.com/pt-br/topics/cloud-native-apps) para criação e execução de aplicações sem o gerenciamento de servidores.

Os servidores ainda são usados nesse modelo, mas eles são abstraídos do desenvolvimento de aplicações. O [provedor de nuvem](https://www.redhat.com/pt-br/topics/cloud-computing/what-are-cloud-providers) fica responsável pelas tarefas rotineiras de [provisionamento](https://www.redhat.com/pt-br/topics/automation/what-is-provisioning), manutenção e escala da [infraestrutura](https://www.redhat.com/pt-br/topics/cloud-computing/what-is-it-infrastructure) do servidor. Os desenvolvedores só precisam empacotar o código em [containers](https://www.redhat.com/pt-br/topics/containers) para fazer a implantação.

Depois da implantação, as aplicações serverless atendem à demanda e aumentam ou diminuem a escala [automaticamente](https://www.redhat.com/pt-br/topics/automation) de acordo com as necessidades. As soluções serverless dos provedores de [nuvem pública](https://www.redhat.com/pt-br/topics/cloud-computing/what-is-public-cloud) costumam ser oferecidas sob demanda por meio de um modelo de execução [orientado a eventos](https://www.redhat.com/pt-br/topics/integration/what-is-event-driven-architecture). Por isso, não há cobrança pelas funções serverless não utilizadas.

[Ouça o podcast "At Your Serverless" do Command Line Heroes](https://www.redhat.com/pt-br/command-line-heroes/season-2/at-your-serverless)

## Visão geral da arquitetura serverless

O serverless é diferente de outros modelos de [cloud computing](https://www.redhat.com/pt-br/topics/cloud) em que o provedor de nuvem é responsável por gerenciar a [infraestrutura da nuvem](https://www.redhat.com/pt-br/topics/cloud-computing/what-is-cloud-infrastructure) e por escalar as aplicações. As aplicações serverless são implantadas em containers que são iniciados sob demanda e automaticamente quando chamados.

Em um modelo padrão de cloud computing baseado em [infraestrutura como serviço (IaaS)](https://www.redhat.com/pt-br/topics/cloud-computing/what-is-iaas), os usuários compram unidades de capacidade. Ou seja, o provedor de nuvem pública fornece componentes de servidor "sempre ativos" para a execução das aplicações. Os usuários precisam aumentar a capacidade do servidor nos momentos de alta demanda e diminuí-la quando a capacidade alta não é mais necessária. Mesmo quando as aplicações não são usadas, a infraestrutura de nuvem necessária para executá-las continua ativa.

Em comparação, com a arquitetura serverless, as aplicações são iniciadas apenas quando necessárias. Quando um evento aciona a execução do código da aplicação, o provedor de nuvem pública aloca os recursos relacionados dinamicamente. Os usuários deixam de ser cobrados quando essa execução termina. Além do aumento da eficiência e da economia, o modelo serverless livra os desenvolvedores das tarefas rotineiras e manuais associadas ao provisionamento do servidor e à escala da aplicação.

Com o modelo serverless, todas as tarefas rotineiras são realizadas pelo provedor de serviços de nuvem. Elas incluem, por exemplo, o [gerenciamento](https://www.redhat.com/pt-br/topics/management) do sistema operacional e de arquivos, a [aplicação de patches de segurança](https://www.redhat.com/pt-br/topics/management/what-patch-management-and-automation), o balanceamento de carga, a administração da capacidade, a escala, a geração de registros e o monitoramento.

É possível criar uma aplicação totalmente serverless ou uma formada por elementos de [microsserviços](https://www.redhat.com/pt-br/topics/microservices/what-are-microservices) parcialmente serverless e tradicionais.

### Tecnologia nativa em nuvem e a nuvem híbrida

Serverless é um novo modelo nativo em nuvem que gera benefícios significativos na produtividade e eficiência, mas exige planejamento. Leia o guia de estratégia nativa em nuvem para líderes de TI e arquitetos, que inclui insights para preparar os profissionais para uma abordagem serverless.

[Faça o download do ebook](https://www.redhat.com/pt-br/engage/cloud-native-meets-hybrid-cloud-strategy-guide?intcmp=701f2000001OMH6AAO)

## Qual é a função do provedor de nuvem na computação serverless?

Com o modelo serverless, o provedor de nuvem executa servidores físicos e aloca dinamicamente os recursos deles em nome dos usuários, que podem implantar código diretamente na produção.

As soluções de computação serverless costumam ser divididas em duas categorias: back-end como serviço (BaaS) e [função como serviço (FaaS)](https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-faas). 

Com o BaaS, os desenvolvedores têm acesso a vários serviços e aplicações de terceiros. Por exemplo, talvez um provedor de nuvem ofereça serviços de autenticação, criptografia extra, bancos de dados acessíveis pela nuvem e dados de uso de alta fidelidade. Normalmente, você chama as funções serverless por meio de [interfaces de programação de aplicações (APIs)](https://www.redhat.com/pt-br/topics/api/what-are-application-programming-interfaces).

Na verdade, quando os desenvolvedores se referem ao serverless, é mais provável que eles estejam falando do modelo FaaS. Com esse modelo, os desenvolvedores ainda gravam uma lógica personalizada no lado do servidor, mas ela é executada em containers totalmente gerenciados por um provedor de serviços de nuvem. 

Todos os principais provedores de nuvem pública oferecem pelo menos uma solução de FaaS. Eles incluem a [Amazon Web Services](https://www.redhat.com/pt-br/partners/amazon-web-services) com o AWS Lambda, o [Microsoft Azure](https://www.redhat.com/pt-br/partners/microsoft) com o Azure Functions, o [Google Cloud](https://www.redhat.com/pt-br/partners/google) com várias opções, o [IBM Cloud](https://www.redhat.com/pt-br/partners/red-hat-and-ibm) com o IBM Cloud Functions e muitos outros. 

Algumas organizações preferem executar os próprios ambientes de FaaS por meio de plataformas serverless open source, como o [Red Hat® OpenShift® Serverless](https://www.redhat.com/pt-br/topics/microservices/why-choose-openshift-serverless). Essa solução é baseada no projeto [Knative](https://www.redhat.com/pt-br/topics/microservices/what-is-knative) do [Kubernetes](https://www.redhat.com/pt-br/topics/containers/what-is-kubernetes).

[Saiba mais sobre o Red Hat OpenShift Serverless](https://www.redhat.com/pt-br/topics/microservices/why-choose-openshift-serverless)

## O que é função como serviço (FaaS)?

Função como serviço (FaaS) é um modelo de execução de computação orientado a eventos. Com ele, os desenvolvedores gravam a lógica, que é implantada em containers totalmente gerenciados por uma plataforma e executada sob demanda.

Em comparação com BaaS, o modelo FaaS proporciona maior controle aos desenvolvedores. Isso possibilita a criação de aplicações personalizadas, evitando a dependência de uma biblioteca de serviços pré-gravados. 

O código é implantado em containers gerenciados por um provedor de nuvem. Especificamente, esses containers são:

- [Sem estado](https://www.redhat.com/pt-br/topics/cloud-native-apps/stateful-vs-stateless), o que simplifica a [integração dos dados](https://www.redhat.com/pt-br/topics/integration).
- Efêmeros, para que eles sejam executados por muito pouco tempo.
- Acionados por eventos, para que eles sejam executados automaticamente quando necessário.
- Totalmente gerenciados por um provedor de nuvem. Assim, você paga somente o necessário, e não os servidores e aplicações "sempre ativos".

Com esse modelo, os desenvolvedores chamam aplicações serverless usando APIs, que são gerenciadas pelo provedor de FaaS por meio de um [gateway](https://www.redhat.com/pt-br/topics/api/what-does-an-api-gateway-do).

[Leia mais sobre o modelo FaaS](https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-faas)

## Casos de uso do modelo serverless

A arquitetura serverless é ideal para aplicações assíncronas e stateless que podem ser iniciadas instantaneamente. Da mesma forma, esse modelo também é uma ótima opção para os casos de uso em que a demanda aumenta de maneira aleatória e imprevisível.

Por exemplo, pense em uma tarefa como o processamento em lote de arquivos de imagem de entrada: ele não ocorre com muita frequência, mas precisa estar pronto para quando uma grande quantidade de arquivos chegar de uma só vez. Outro caso são as modificações feitas em um banco de dados: você pode aplicar uma série de funções (por exemplo, comparar as mudanças com os padrões de qualidade) ou traduzir as modificações automaticamente.

As aplicações serverless também são ideais para os casos de uso que incluem fluxos de dados de entrada, chat bots, tarefas agendadas e lógica empresarial.

Outros casos de uso comuns do modelo serverless são aplicações web e APIs de back-end, [automação de processos de negócios](https://www.redhat.com/pt-br/topics/automation/whats-business-automation), sites serverless e integração de diversos sistemas.

## O que é Knative e Kubernetes serverless?

A plataforma de orquestração de containers do Kubernetes é uma solução bem popular na execução de ambientes serverless. Essa é uma maneira de executar aplicações em containers em [infraestruturas automatizadas](https://www.redhat.com/pt-br/topics/automation/whats-it-automation). No entanto, o Kubernetes sozinho não é capaz de executar aplicações serverless de maneira nativa.

O [Knative](https://www.redhat.com/pt-br/topics/microservices/what-is-knative) é um projeto da comunidade [open source](https://www.redhat.com/pt-br/topics/open-source/what-is-open-source) que fornece componentes para implantar, executar e gerenciar aplicações serverless no Kubernetes.

Com o ambiente serverless do Knative, é possível implantar o código em plataformas de Kubernetes, como o [Red Hat OpenShift](https://www.redhat.com/pt-br/technologies/cloud-computing/openshift). Para criar um serviço com o Knative, basta empacotar o código como uma imagem de container e enviá-la ao sistema. Seu código será executado apenas quando necessário, pois o Knative inicia e encerra as instâncias automaticamente.

O Knative é formado por três componentes principais:

- **Build**: uma abordagem flexível para compilar código-fonte em containers.
- **Serving**: possibilita a implantação rápida e a escala automática de containers por meio de um modelo orientado a solicitações para o fornecimento de cargas de trabalho com base na demanda.
- **Eventing**: uma infraestrutura de consumo e produção de eventos para acionar aplicações. Isso é feito por várias fontes, como eventos gerados por suas próprias aplicações, [serviços de nuvem](https://www.redhat.com/pt-br/topics/cloud-computing/what-are-cloud-services) de vários provedores, sistemas de [software como serviço (SaaS)](https://www.redhat.com/pt-br/topics/cloud-computing/what-is-saas) e fluxos do [Red Hat AMQ](https://www.redhat.com/pt-br/technologies/jboss-middleware/amq-2).

Ao contrário dos frameworks serverless mais antigos, o Knative foi projetado para implantar qualquer carga de trabalho de aplicação moderna, incluindo monólitos, microsserviços e funções pequenas.

O Knative é uma alternativa às soluções de FaaS controladas por um único provedor de serviços e pode ser executado em qualquer plataforma de nuvem compatível com o Kubernetes. Isso inclui a execução em um datacenter on-premise. Assim, as organizações têm mais agilidade e flexibilidade para executar cargas de trabalho serverless.

[Saiba mais sobre o Knative](https://www.redhat.com/pt-br/topics/microservices/what-is-knative)

## Quais são os prós e contras da computação serverless?

**Prós**

- A computação serverless aumenta a produtividade dos desenvolvedores e reduz os custos operacionais. Ela livra os desenvolvedores das tarefas rotineiras de provisionamento e gerenciamento de servidores. Assim, eles têm mais tempo para se concentrar nas aplicações. 
- Com a computação serverless, é mais fácil adotar práticas de [DevOps](https://www.redhat.com/pt-br/topics/devops), porque os desenvolvedores não precisam mais descrever explicitamente a infraestrutura que eles querem que a equipe de operações provisione. 
- É possível incorporar componentes completos de soluções de BaaS de terceiros para otimizar ainda mais o desenvolvimento de aplicações.
- Os custos operacionais são reduzidos no modelo serverless porque você paga o tempo de computação baseado em nuvem conforme necessário. Isso não acontece quando você executa e gerencia os próprios servidores o tempo todo.

**Contras**

- Deixar de executar o seu próprio servidor ou controlar a sua própria lógica no lado dele tem algumas desvantagens.
- É possível que os provedores de nuvem tenham restrições sobre como as pessoas podem interagir com os componentes. Por sua vez, isso afeta a flexibilidade e a personalização dos sistemas. No caso de ambientes de BaaS, os desenvolvedores podem depender de serviços com código que não pode ser controlado por eles.
- Abrir mão de controlar esses aspectos do stack de TI também aumenta as chances de dependência de fornecedor. Além disso, quando você decide trocar de provedor, isso pode gerar custos. Você precisará fazer upgrade dos sistemas para que eles atendam às especificações do novo provedor.

## A evolução do serverless

O conceito de FaaS e de arquitetura serverless tem evoluído no mesmo ritmo que o aumento da popularidade das soluções de nuvem sob demanda e de containers. Um [estudo da 451 Research](https://www.redhat.com/pt-br/resources/451-research-red-hat-openshift-serverless) realizado em parceria com a Red Hat investigou a evolução do serverless, dividindo esse modelo em três fases diferentes:

A fase "1.0" incluía limitações que dificultavam o uso do serverless na computação geral. O serverless 1.0 tem as seguintes características:

- HTTP e algumas outras fontes
- Somente funções
- Tempo de execução limitado (5 a 10 minutos)
- Sem orquestração
- Desenvolvimento local limitado

Com o surgimento do Kubernetes, o modelo entrou na fase "1.5", em que muitos frameworks serverless começaram a escalar containers automaticamente. O serverless 1.5 tem as seguintes características:

- Knative
- Escalonamento automático baseado no Kubernetes
- Microsserviços e funções
- Fácil de fazer o debug e testar no local
- Portátil e com suporte a múltiplas linguagens

Hoje, a fase "2.0" está surgindo com a inclusão do estado e da integração. Os provedores começaram a adicionar os componentes que faltavam para que o modelo serverless fosse compatível com cargas de trabalho empresarial de uso geral. O serverless 2.0 tem as seguintes características:

- Gerenciamento de estado básico
- Uso de padrões de integração empresarial
- Recursos de mensageria avançados
- PaaS empresarial incorporado
- Fontes de evento prontas para empresas
- Estado e integração

[Faça o download do estudo da 451 Research sobre o Kubernetes serverless](https://www.redhat.com/pt-br/resources/451-research-red-hat-openshift-serverless)[Conheça a computação serverless](https://developers.redhat.com/topics/serverless-architecture?extIdCarryOver=true&intcmp=701f2000001OEGhAAO&sc_cid=7013a000002DgCjAAK)

#### Leia mais

- Tópico: [Introdução às aplicações nativas em nuvem](https://www.redhat.com/pt-br/topics/cloud-native-apps)
- Estudo: [451 Research: Red Hat OpenShift Serverless simplifica o Kubernetes](https://www.redhat.com/pt-br/resources/451-research-red-hat-openshift-serverless)
- Ebook: [O caminho para aplicações nativas em nuvem](https://www.redhat.com/pt-br/resources/path-to-cloud-native-applications-ebook)
- Blog: [O modelo serverless é a próxima fase do desenvolvimento de aplicações nativas em nuvem?](https://www.redhat.com/pt-br/blog/serverless-next-phase-cloud-native-application-development)
- Blog: [Evolução do modelo serverless e FaaS: Knative gera mudanças](https://developers.redhat.com/blog/2019/03/26/serverless-faas-knative/)
- Blog: [Primeiro ano do Knative: seu progresso e o futuro do serverless](https://www.redhat.com/pt-br/blog/knatives-first-year-where-its-and-whats-next-serverless)
- Artigo: [O que é Knative?](https://www.redhat.com/pt-br/topics/microservices/what-is-knative)
- Artigo: [O que é FaaS?](https://www.redhat.com/pt-br/topics/cloud-native-apps/what-is-faas)
- Artigo: [Qual é a função de um gateway de API?](https://www.redhat.com/pt-br/topics/api/what-does-an-api-gateway-do)
- Artigo: [Por que escolher o Red Hat OpenShift Serverless?](https://www.redhat.com/pt-br/topics/microservices/why-choose-openshift-serverless)