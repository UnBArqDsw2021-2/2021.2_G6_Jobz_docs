# <center> Documento de Arquitetura de Software - DAS

<div align="justify">

## 1. Introdução

O *Documento de Arquitetura de Software* (DAS) pode ser descrito como "uma visão arquitetural abrangente do sistema, usando diversas visões de arquitetura para representar diferentes aspectos do sistema" (IBM Corp, 2006). Possui o objetivo de descrever toda a arquitetura da aplicação web [**Jobz**](https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/) e deve ser usado para a documentação e comunicação entre os participantes do projeto sobre questões arquiteturais. O Jobz é um sistema criado para conectar empresas e profissionais autônomos que realizam serviços em geral a clientes que buscam por esses serviços, afim de ser útil para os dois perfis, tanto divulgando o trabalho desses prestadores quanto auxiliando os clientes a encontrarem a melhor solução.

### 1.1. Finalidade
O presente documento apresenta a arquitetura geral do sistema do projeto [**Jobz**](https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/), com a finalidade de especificar e documentar as diversas decisões arquiteturais que foram tomadas no decorrer do desenvolvimento do projeto, as quais foram documentadas por meio da utilização de tabelas, diagramas, entre outros artefatos.

### 1.2. Escopo
Esse documento refere-se a aplicação [**Jobz**](https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/), que consiste em uma aplicação web com o objetivo de intermediar prestadores de serviços em geral e clientes interessados, criando um espaço para que os profissionais divulguem suas habilidades, alcançando um maior público, e facilitando a busca dos clientes.

No documento são contemplados padrões de software, componentes de software, plataformas e frameworks de desenvolvimento, casos de uso e serviços de persistência de dados. Desta forma, o documento é utilizado como um guia para o entendimento do desenvolvimento do projeto ao abordar os principais pontos desenvolvidos na construção de sua arquitetura.

### 1.3. Definições, Acrônimos e Abreviações
| Abreviação | Acrônimo | Definição |
|:-:|:-:|:-|
| API | Application Program Interface (Interface de Programação de Aplicações) | É uma interface de programação de aplicações, um conjunto de definições e protocolos para criar e integrar softwares de aplicações. |
| HTTP | HyperText Transfer Protocol (Protocolo de Transferência de Hipertexto) | É um protocolo de comunicação utilizado para sistemas de informação de hipermídia, distribuídos e colaborativos. |
| MTV | Model Template View | É um padrão de projeto de software baseado em 3 componentes importantes: model, template e view. |
| REST | Representational State Transfer | É um estilo de arquitetura de software que define um conjunto de restrições a serem usadas para a criação de web services (serviços Web). |
| DRY | Don’t Repeat Yourself | DRY é um conceito de programação de computadores o qual propõe que cada porção de conhecimento em um sistema deve possuir uma representação única, de autoridade e livre de ambiguidades em todo o sistema. |
| WEB | World Wide Web | A World Wide Web designa um sistema de documentos em hipermídia que são interligados e executados na Internet. |
| DAS | Documento de Arquitetura de Software | Documento que descreve toda a arquitetura da aplicação. |
| DE-R | Diagrama Entidade Relacionamento | É um modelo de dados para descrever os dados ou aspectos de informação de um domínio de negócio ou seus requisitos de processo, de uma maneira abstrata que em última análise se presta a ser implementada em um banco de dados, como um banco de dados relacional. |
| DLD | Diagrama Lógico de Dados | Representa as estruturas que irão armazenar os dados dentro de um Banco de Dados.  |
| UML | Unified Modeling Language(Linguagem de modelagem unificada) | É uma linguagem-padrão para a elaboração da estrutura de projetos de software. Ela poderá ser empregada para a visualização, a especificação, a construção e a documentação de artefatos que façam uso de sistemas complexos de software. |

### 1.4. Visão Geral
Com o objetivo de facilitar o entendimento do documento, o texto está organizado em 10 tópicos, nos quais foram documentadas a construção da arquitetura do projeto [**Jobz**](https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/) e as decisões tomadas durante seu desenvolvimento. Cada um dos tópicos possuem sua devida importância e estão divididos da seguinte forma:

| Número | Tópico | Descrição |
|:-:|:-:|:-|
| 1 | Introdução | Fornece uma visão geral de todo o Documento de Arquitetura de Software, incluindo sua finalidade, seu escopo, definições, acrônimos e abreviações, e sua visão geral.  |
| 2 | Representação Arquitetural | Descreve a arquitetura do sistema e como ela é representada, assim como as tecnologias utilizadas em seu desenvolvimento. |
| 3 | Metas e Restrições Arquiteturais | Descreve as metas arquiteturais e os requisitos do software que têm algum impacto significativo em sua arquitetura. |
| 4 | Visão Lógica | Descreve as partes significativas do ponto de vista da arquitetura do modelo de design, como sua decomposição em classes e pacotes. |
| 5 | Visão de Dados | Descreve a perspectiva de armazenamento e modelagem de dados persistentes do sistema. |
| 6 | Visão de Processos | Descreve o sistema em tempo de execução através de interações e comportamentos dos elementos |
| 7 | Visão de Implementação | Descreve a estrutura geral do modelo de implementação, a decomposição do software em camadas e subsistemas no modelo de implementação e quaisquer componentes arquitetonicamente significativos. |
| 8 | Visão de Casos de Uso | Descreve casos de uso ou cenários do modelo de caso de uso se eles representam alguma funcionalidade central significativa do sistema final. |
| 9 | Visão de Implantação | Descreve a estrutura geral do modelo de implementação, a divisão do software em camadas e os subsistemas no modelo de implementação e todos os componentes significativos do ponto de vista da arquitetura. |
| 10 | Qualidade | Descreve o impacto da arquitetura nos atributos de qualidade do software. |

## 2. Representação Arquitetural

### 2.1. Diagrama de Arquitetura

Usamos [**Django**](https://docs.djangoproject.com/en/4.0/) com o [**REST Framework**](https://www.django-rest-framework.org/), [**PostgreSQL**](https://www.postgresql.org/) e [**ReactJS**](https://pt-br.reactjs.org/) para a cosntrução da aplicação.
O Django faz uso da arquitetura MVT (Model, View Template) em que o Model lida com requisições (querys) de dados com objetos python, as Views recebem requisições Http e enviam respostas http, e o Template específica o formato de apresentação dos dados, que aqui é representado pelo módulo de ReactJS.
Segue o diagrama de arquitetura do projeto.
<p align='center'>
    <img src='assets/images/arquitetura/Arquitetura.drawio.png' width=80% height=auto>
    <figcaption align='center'>
        <b>Figura 1: Diagrama de Arquitetura do produto </b>
        <br>
    </figcaption>
</p>

### 2.2. Tecnologias
Para o desenvolvimento da aplicação Jobz foi utilizado um conjunto de ferramentas, sendo elas o framework de desenvolvimento de API's web `Django Rest Framework` e a biblioteca `ReactJS` para a camada de visualização, além do sistema gerenciador de banco de dados relacional `PostgreSQL` e a virtualização do ambiente com  `Docker`.

#### 2.2.1. FrontEnd

O [**ReactJS**](https://pt-br.reactjs.org/) é uma biblioteca da linguagem JavaScript que utiliza certos padrões de design baseados em Components. A aplicação React começa com um único componente raiz, que é construído usando um ou mais componentes, e cada um desses componentes pode ser aninhado com outro componente em qualquer nível. O framework foi escolhido porque alguns integrantes já possuíam experiência e a equipe julgou como uma boa opção para o projeto.

#### 2.2.2. BackEnd
Tanto o [**Django**](https://docs.djangoproject.com/en/4.0/) quanto o [**Django REST Framework**](https://www.django-rest-framework.org/) são escritos em [Python](https://www.python.org/), porém possuem finalidades diferentes.

O **Django** tem o propósito focado no desenvolvimento de aplicações web e sites, fazendo uso do *Don't Repeat Yourself* (DRY), que em tradução livre significa *Não Seja Repetitivo*, aproveitando ao máximo o código criado facilitando a reutilização. Além disso, utiliza o padrão *model-template-view* (MTV), onde a aplicação é dividida em camadas, tornando o código mais organizado.

O **Django Rest Framework** tem como objetivo o desenvolvimento de API's de forma simples e ágil, gerando uma API navegável que facilita na usabilidade para os desenvolvedores, além de possuir sistema de autenticação e serialização de dados.

O framework foi escolhido porque alguns integrantes já possuíam experiência, se disponibilizando para fornecer ajuda aos demais, além de que a ferramenta oferece um rápido desenvolvimento.

#### 2.2.3. Banco de Dados
O [**PostgreSQL**](https://www.postgresql.org/) é um Sistema Gerenciador de Banco de Dados (SGBD) Relacional, utilizado para armazenar informações de soluções de informática em todas as áreas de negócios existentes (Milani, André. PostgreSQL: Guia do Programador. Novatec. 2008). É um dos cinco SGDB's relacionais mais utilizados do mercado, e foi escolhido por ser um sistema open-source de fácil instalação que possui interfaces simples e intuitivas que facilitam o aprendizado, além de ser muito fácil de manter devido a sua estabilidade.

#### 2.2.4. Docker
O [**Docker**](https://www.docker.com/) foi utilizado porque facilita o desenvolvimento em equipe possibilitando a containerização do ambiente de execução, permitindo o compartilhamento de tecnologias e dependências em qualquer host que contenha o Docker instalado.

## 3. Metas e Restrições Arquiteturais

### 3.1. Metas

#### 3.1.2 Portabilidade
A aplicação deve ser compatível e ser possível a execução com desempenho satisfatório nos navegadores mais utilizados e que possuem atualizações recentes.

#### 3.1.1 Escalabilidade
A aplicação deve ser estruturada com o objetivo de ser escalável o suficiente para ser possível futuras evoluções com o crescimento do projeto.

#### 3.1.2 Segurança
O aplicativo deve ser seguro e lidar com os dados dos usuários com segurança, de forma que a informação só pode ser acessada e atualizada por pessoas autorizadas e devidamente credenciadas (autenticação de usuários).

#### 3.1.3 Usabilidade
O sistema deverá ter a capacidade em fazer com que o usuário tenha sucesso na execução de suas tarefas de maneira simples.


### 3.2. Restrições

|Restrições||
|:-----|:------|
|Plataforma|A aplicação terá suporte para browsers para computador.|
|Público|A aplicação será desenvolvida para toda a população brasileira e será voltada para prestadores de diversos serviços e seus respectivos clientes.|
|Linguagem|A aplicação Jobz será desenvolvida em idioma português do Brasil.|
|Prazo|A aplicação terá o prazo estimado de termino até o fim da disciplina.|
|Equipe|A equipe possui 10 integrantes do curso de Eng. de Software da UnB.|
|Conectividade|É necessária a conectividade com a internet para o acesso e utilização da aplicação.|


## 4. Visão Lógica

A visão lógica tem o objetivo de representar a visão conceitual do projeto por meio de camadas, para que possamos compreender a estrutura e a organização do design do sistema, descrevendo melhor os elementos comportamentais e funcionalidades da arquitetura. Essa é a visão arquitetural que contém as classes de design mais importantes, além de sua essencial organização em pacotes e subsistemas de camadas.

Tendo isso em vista, elaboramos o diagrama de classe e o diagrama de pacotes, que foram desenvolvidos com uso do Framework [Django](https://www.djangoproject.com/) voltado para o Backend e a biblioteca [React.js](https://pt-br.reactjs.org/) para o Frontend de nossa aplicação.

### 4.1 Diagrama de Classes

O [diagrama de classe](./pages/modelagem/diagramaDeClasses) é um dos principais [diagramas UML](https://www.lucidchart.com/pages/pt/o-que-e-uml), pois consegue mapear claramente a estrutura de nosso sistema apresentando suas classes, atributos, operações e relações entre os objetos.

Com o seu uso, somos capazes de entender melhor a visão geral do esquema de nossa aplicação e conseguimos expressar visualmente as necessidades específicas de nosso sistema. Além de sermos capazes de criar modelos de dados de nossos sistema e até mesmo gráficos detalhados para destacar alguma informação específica que seja necessária.

<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramaClasses/classDiagramV2.svg' width=80% height=auto>
    <figcaption align='center'>
        <b>Figura 2: Diagrama de classes do produto v.2.0 </b>
        <br>
    </figcaption>
</p>

### 4.2 Diagrama de Pacotes

Um [diagrama de pacotes](./pages/modelagem/diagramaPacotes) apresenta no formato de pastas ou pacotes, a organização e disposição de diferentes elementos de um modelo. Esses elementos que podem ser documentos, classes e até mesmo outros pacotes, são dispostos dentro dessas pastas de arquivos que são apresentados em nosso diagrama, que por fim é organizado e apresentado de forma hierárquica.

O diagrama de pacotes é capaz de fornecer uma visibilidade geral melhor sobre projetos e sistemas de grande escala. Pois oferece uma versão simplificada de diagramas de classe complexos, além de permitir que atualizações sejam feitas com facilidade com o decorrer do desenvolvimento do produto

#### 4.2.1 Backend

Dessa forma, temos o diagrama de pacotes criado para apresentar a estrutura de nosso projeto do ponto de vista do backend da aplicação. No qual utiliza o banco de dados [PostgreSQL](https://www.postgresql.org/) para o seu armazenamento de dados.

<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramadepacotes.png' height=auto>
    <figcaption align='center'>
        <b>Figura 3: Diagrama de pacotes do backend do produto. </b>
        <br>
    </figcaption>
</p>

#### 4.2.2 Frontend

Por conseguinte, temos então o diagrama de pacotes voltado para o frontend de nossa aplicação, no qual realiza o reaproveitamento dos componentes para a criação da telas, além de definir o padrão de desenvolvimento e simplificar o código.

<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramapacotesfrontend.png' height=auto>
    <figcaption align='center'>
        <b>Figura 4: Diagrama de pacotes do frontend produto. </b>
        <br>
    </figcaption>
</p>

#### 4.2.3 Sistema

Por fim, temos a representação de nosso sistema completo, no qual é caracterizado pela conexão do frontend com o backend, nos quais utilizam o [protocolo HTTP](https://developer.mozilla.org/pt-BR/docs/Web/HTTP) para realizar trocas de dados por meio de suas requisições.

<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramapacotesgeral.png' height=auto>
    <figcaption align='center'>
        <b>Figura 5: Diagrama de pacotes do produto. </b>
        <br>
    </figcaption>
</p>

## 5. Visão de Dados

### 5.1. Diagrama Entidade-Relacionamento (DE-R)
<p align='center'>
    <img src='assets/images/modelagemBanco/DERR-PosG_Final.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 6: Diagrama de entidade relacionamento</b>
        <br>
    </figcaption>
</p>

### 5.2. Diagrama Logico de Dados (DLD)

<p align='center'>
    <img src='assets/images/modelagemBanco/DLDR-PosG_Final.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 7: Diagrama lógico</b>
        <br>
    </figcaption>
</p>

### 5.3. Dicionário de dados

#### 5.3.1. PERSON

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    name    |     Obrigatório     |               VARCHAR(500)                  |             Nome completo de cada pessoa.                 |
|    phone   |      Obrigatório       |               BIGINT                |             Telefone para contato de cada pessoa.             |
| email |      Obrigatório        |             VARCHAR(150)                     | Email de cada pessoa que será utilizado na aplicação. |
| cpf |      chave-Primária        |             VARCHAR(11)                     |  Chave-Primária Identificadora de cada pessoa.                            |
|  password  |      Obrigatório       |               VARCHAR(50)                |          Senha para autenticação do funcionário.           |

#### 5.3.2. USER

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    idUser    |     Chave-Primária    |               INT                  |             Chave-Primária identificadora de cada usuário.               |
|    cpf   |      Chave-Primaria, Estrangeira |               VARCHAR(11)                |             Chave-Primária Identificadora de cada pessoa.             |
| idAddress |      Chave-Estrangeira        |             INT                     | Chave estrangeira correspondente ao endereço do usuário. |


#### 5.3.3. ADDRESS

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    idAddress    |     Chave-Primária     |               INT                  |            Chave-Primária identificadora de cada endereço.                 |
|    city   |      Obrigatório       |               VARCHAR(100)                | Cidade correspondente ao endereço de cada usuário.             |
| state |      Obrigatório        |             VARCHAR(2)                     | Estado correspondente ao endereço de cada usuário. |
| cep |      Obrigatório        |             INT                       |  CEP correspondente ao endereço de cada usuário.                         |
|  number  |      Obrigatório       |               INT               |          Número correspondente ao endereço de cada usuário.           |
|  district  |      Obrigatório       |               VARCHAR(100)               |   Bairro correspondente ao endereço de cada usuário.           |
|  complement  |      Obrigatório       |               VARCHAR(100)               |   Complemento correspondente ao endereço de cada usuário.           |


#### 5.3.4. SERVICE

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    datePurchase    |     Obrigatório     |               DATETIME                  |             Data correspondente da aquisição do serviço.                 |
|    dateService   |      Obrigatório       |               DATETIME                |            Data correspondente da publicação do serviço.             |
| serviceDescription |      Obrigatório        |             VARCHAR(5000)                     | Descrição relativa a cada serviço disponibilizado. |
| idService |      Chave-Primária        |             INT                     |  Chave-Primária Identificadora de cada serviço.                            |
|  idUser  |      Chave-Estrangeira       |               INT                |          Chave estrangeira relativa ao id do usuário que contratou o serviço.           |
|  cpf  |      Chave-Estrangeira       |               VARCHAR(11)                |          Chave estrangeira relativa ao cpf do usuário que contratou o serviço.           |
|  idCategory  |      Chave-Estrangeira       |               INT                |          Chave estrangeira relativa ao id da categoria ao qual pertence o serviço.           |
|  idEvaluation  |      Chave-Estrangeira       |               INT                |          Chave estrangeira relativa ao id da avaliação do serviço.           |

#### 5.3.5. SERVICE_CATEGORY

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    idCategory    |     Chave-Primária     |               INT                  |             Chave Primária identificadora a cada categoria.                 |
|    nameService   |      Obrigatório       |               VARCHAR(100)                |      Nome de cada serviço que foi cadastrado.       |

#### 5.3.6. EVALUATION

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    idEvaluation    |     Chave-Primária     |               INT                  |            Chave primária identificadora de cada avaliação.                 |
|    comment   |      Obrigatório       |               VARCHAR(1000)                |            Comentário relativo a cada avaliação dos serviços disponibilizados.            |
| grade |      Obrigatório        |             INT                     | Grau relativo à avaliação relativa ao serviço.  |

#### 5.3.7. COMPANY

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    idCompany    |     Chave-Primária     |               INT                  |            Chave-Primária identificadora de cada empresa/companhia.                 |
| email |      Obrigatório        |             VARCHAR(150)                     | Email de cada empresa que será utilizado na aplicação. |
|    name   |      Obrigatório       |               VARCHAR(150)                |            Nome completo da empresa que será cadastrado na aplicação.            |


#### 5.3.8. PROVIDER

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    idProvider    |     Chave-Primária     |               INT                  |             Chave-Primária identificadora de cada prestador de serviços.                 |
| cpf |      chave-primária, Estrangeira       |             VARCHAR(11)                     |  Chave-Primária, Estrangeira Identificadora de cada pessoa.                            |
|    idOccupation   |      Obrigatório       |               INT                |             Chave-Estrangeira relativa ao id da ocupação de cada prestador de serviços.                |


#### 5.3.9. SCHEDULE

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    dayOfWeek    |     Obrigatório     |               ENUM('seg','ter', 'quar','quin','sex','sab')                  |             Dia da semana respectivo a disponibilidade de serviço da agenda do prestador.                 |
|    entryTime   |      Obrigatório       |               DATETIME                |             Horário de entrada respectivo a agenda de cada prestador de serviços.             |
| endOfWork |      Obrigatório        |             DATETIME                     | Horário de saída respectivo a agenda de cada prestador de serviços. |
| idSchedule |      Chave-Primária        |             INT                     |  Chave-Primária identificadora de cada agenda.                            |
|  idProvider  |      Chave-Estrangeira       |               INT                |          Chave-Estrangeira relativa ao id do prestador de serviços ao qual é dono da agenda.           |
|  cpf  |      Chave-Estrangeira       |               VARCHAR(11)                |          Chave-Estrangeira relativa ao cpf do prestador de serviços ao qual é dono da agenda.           |

#### 5.3.10. PROVIDER_PRESENTATION
|  Atributo       | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :-------------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
| idPresentation  | Chave-Primária         | INT                                 | Chave-Primária identificadora de cada perfil de apresentação.    |
| presetationPhoto| Obrigatório            | IMAGE                               | Foto do prestador de serviço.                             |
| description     | Obrigatório            | VARCHAR(5000)                       | Descrição dos serviços prestados.                            |
| cpf             | Chave-Estrangeira      | VARCHAR(11)                         | Chave-Estrangeira relativa ao cpf do prestador de serviços.|

## 6. Visão de Processos

Essa visão corresponde a diferentes processos, suas responsabilidades, colaborações e como elas interagem entre si. É uma visão de modelo de projeto que pode ser representada utilizando objetos e mensagens trocadas, representados em classes e diagramas de interação usando a notação de processo.

Para o nosso projeto temos os diagramas de [sequência](./pages/modelagem/diagramaSequencia.md), [atividades](./pages/modelagem/diagramaAtividades.md) e [comunicação](./pages/modelagem/diagrama-comunicacao.md) que trazem um detalhamento sobre essa visão e podem ser visualizados nas imagens a seguir:

### 6.1 Diagrama de Sequência

O diagrama de sequência da contratação de serviços, que é o principal processo da nossa aplicação.

<p align='center'>
    <img src='assets/images/diagramaSequencia/sequenceDiagramHiring.png' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 8: Diagrama de Sequência da Contratação de Serviços</b>
        <br>
    </figcaption>
</p>

### 6.2 Diagramas de Atividades

O diagrama de atividades descreve as etapas que ocorrem quando um determinado cenário é iniciado, até que este cenário seja encerrado, ajudando a compreensão do processo que será executado. Temos então o detalhamento dos fluxos de login, perfil do cliente e perfil do prestador de serviço.

<p align='center'>
    <img src='assets/images/diagramaAtividades/diagramaLogin.png' width=40% height=auto>
    <figcaption align='center'>
        <b>Figura 9: Diagrama de Atividades representando o login. </b>
        <br>
    </figcaption>
</p>

<p align='center'>
    <img src='assets/images/diagramaAtividades/diagramaCliente.png' width=40% height=auto>
    <figcaption align='center'>
        <b>Figura 10: Diagrama de Atividades representando o perfil de cliente.</b>
        <br>
    </figcaption>
</p>

<p align='center'>
    <img src='assets/images/diagramaAtividades/diagramaPrestador.png' width=40% height=auto>
    <figcaption align='center'>
        <b>Figura 11: Diagrama de Atividades representando o perfil de prestador de serviço.</b>
        <br>
    </figcaption>
</p>

### 6.3 Diagramas de Comunicação

O diagrama de comunicação demonstra o comportamento dinâmico de um sistema ou software, entendendo a interligação e a comunicação entre as partes de um sistema completo.

<p align='center'>
    <img src='assets/images/diagrama-comunicacao/collaborator.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 12: Diagrama de comunicação da criação do serviço</b>
        <br>
    </figcaption>
</p>

<p align='center'>
    <img src='assets/images/diagrama-comunicacao/comunicacao-criacao-cliente.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 13: Diagrama de comunicação da contratação do serviço</b>
        <br>
    </figcaption>
</p>

## 7. Visão de Implementação

Para melhorar a compreensão física do processamento do sistema utilizamos a visão de implementação, no qual nos permite ilustrar e captar as decisões de arquitetura tomadas para a implementação. No qual, se aproveita do [diagrama de componentes](./pages/modelagem/componentes) que apresenta os subsistemas e suas organizações em camadas de hierarquia.
Além de que, a visão de implementação nos permite entender a quantidade de código que será produzida, discutir reutilizações no sistema, considerar estratégias para a release e até mesmo atribuir o trabalho de implementação ao indivíduos ou equipes.

### 7.1 Diagrama de Componentes

Um diagrama de componentes é considerado quase que indispensável para a criação de um sistema de software, existe até mesmo o chamado desenvolvimento baseado em componentes([CBD](https://www.techopedia.com/definition/31002/component-based-development-cbd)). Pois essa representação mostra com detalhes o relacionamento de diferentes módulos do sistema.

<p>Mesmo que esse diagrama pareça complexo, ele é capaz de representar a estrutura física do sistema, dá atenção aos seus componentes e relacionamentos, além de destacar o comportamento do serviço em relação a interface.</p>
<p align='center'>
    <img src='assets/images/Diagrama_Compomentes/Diagrama compomente.jpeg' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 14: Diagrama de Componentes</b>
        <br>
    </figcaption>
</p>

## 8. Visão de Casos de Uso

A visão de casos de uso é uma representação visual mais aproximada do usuário, descrevendo as relações das funcionalidades do sistema esperadas pelo cliente. Essas relações podem ser observadas no documento de [diagrama de casos de uso](./pages/modelagem/casosUso.md) que apresenta uma visão mais completa sobre a utilização desse diagrama em nosso projeto.

### 8.1 Casos de uso

<p align='center'>
    <img src='assets/images/CasosUso/CasosUsoJOBZ2.png' width=80% height=auto>
    <figcaption align='center'>
        <b>Figura 15: Diagrama de Casos de Uso. </b>
        <br>
    </figcaption>
</p>

## 9. Visão de Implantação

O Jobz é uma aplicação web que segue o modelo de camadas, onde temos as camadas do frontend, backend e a base da dados. O [diagrama de implementação](./pages/modelagem/diagramaImplementacao.md) possui representações dessas camadas juntamente com a camada do usuário que tem acesso apenas a interface do frontend. O usuário acessa por meio de um web browser nossa aplicação e o frontend realiza requisições ao backend, que por sua vez realiza os serviços solicitados, armazenando e buscando os dados necessários na base de dados.

### 9.1 Diagrama de Implementação

<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramaImplementação.svg' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 16: Diagrama de implementação do produto. </b>
    </figcaption>
</p>


## 10. Qualidade

Para avaliar a qualidade de nosso projeto, decidimos utilizar a [ISO/IEC 9126](https://jkolb.com.br/wp-content/uploads/2014/02/NBR-ISO_IEC-9126-1.pdf). Essa ISO possui por objetivo padronizar a avaliação da qualidade de um software, possibilitando assim, que sejamos capazes de apresentar um produto final com qualidade, nos baseando em suas características e atributos.

### 10.1 ISO/IEC 9126 in Software Engineering

A [ISO/IEC 9126](https://jkolb.com.br/wp-content/uploads/2014/02/NBR-ISO_IEC-9126-1.pdf) é um padrão internacional de um modelo para medir de maneira mais sistemática e exata a qualidade de um software. Com isso usaremos ela como modelo para orientar nosso projeto de software com questão a qualidade do mesmo.

O padrão de qualidade pode ser dividido em 4 partes: 'Quality model', 'External Metrices', 'Internal Metrices' e 'Quality in use metrices'.
As três primeiras partes estão preocupadas em descrever e medir a qualidade do produto de software enquanto que a quarta está preocupada com a qualidade do produto do ponto de vista do usuário.

As qualidades externas e internas determinam a qualidade do produto por meio de seis diferentes características(Functionability, Reliability, Usability, Efficiency e Maintainability), nas quais são subdivididas em diferentes atributos. Sendo eles apresentados a seguir:

- **Functionality**: é considerado um fator crucial na qualidade do software, sendo as funções aquelas que resolverão os requisitos. É subdividida: suitability, accuracy, security, functionality compliance e interoperability.

- **Reliability**: é a capacidade do sistema performar conforme pretendido sem nenhuma falha. É subdividida: maturity, fault tolerance,recoverability e reliability compliance.

- **Usability** : esta relacionado a facilidade de uso do sistema e de sua velocidade de aprendizado. É subdividido em: training, learnability, communicativeness e usability compliance.

- **Efficiency**: é um grupo de atributos que lida com o nível de performance do software de acordo com determinadas condições: Time Behaviorm Resource Utilization e Efficiency Compliance.

- **Maintainability**: é um grupo de a atributos que possuem a capacidade de fazer modificações específicas, eles são: Analyzability, Changeability, Stability, Testability e Maintainability Compliance.

- **Portability**: um grupo de atributos que possui a habilidade de ser transferido de um ambiente de software para outro. É subdivido em adaptability, Installability, Co-existence, Replace ability e Portability Compliance.

| Fator de Qualidade |                                                                                                                                                                                        Jobz                                                                                                                                                                                        |
| :----------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|   Functionality    |                                                                                                                 O projeto esta seguindo os requisitos funcionais e não funcionais coerentemente de acordo com nosso [backlog](./pages/modelagem/backlogPriorizado)                                                                                                                 |
|    Reliability     |                                      Projetado utilizando conteiners e técnicas de deploy para garantir a fácil recuperção do mesmo, além de ser seguida variás práticas e [padrões de design](./pages/Padroes_projeto/gof/criacionais) ao longo do desenvolvimento o que ajuda a garantir maior maturidade de código e tolerância a falhas.                                       |
|     Usability      | O projeto visa elaborar uma [UI/UX minimalista](./pages/modelagem/prototipoAlta), sem a intenção de muitas funcionalidades avançadas, alem de usar de técnicas de design para facilitar a navegação e deixar o sistema mais direto e intuitivo. Também terá no webbapp uma página somente para ajuda com perguntas frequentes e formas de contato para tirar dúvidas caso existam. |
|     Efficiency     |                                                                                            A plataforma possui como objetivo ser minimalista utilizando códigos eficientes para manter a aplicação o mais simples possível, onde os computares mais simples são capazes de executá-la.                                                                                             |
|  Maintainability   |                                                                                                              Jobz foi elaborada visando possuir uma [alta coesão e baixo acoplamento](./pages/Padroes_projeto/GRASP/GRASPs) para manter viável sua manutenibilidade.                                                                                                               |
|    Portability     |                                                                                                                                                       A aplicação será responsiva de acordo com o tamnho de tela do usuário.                                                                                                                                                       |


## 11. Referências

> Ludidchart, O que é um diagrama de implementação?. Disponível em: https://www.lucidchart.com/pages/pt/o-que-e-diagrama-de-implementacao-uml. Acesso em 28 de Março de 2022.

> Silva O. Flávio. Visões da Arquitetura Diagramas UML. Disponível em: http://www.facom.ufu.br/~flavio/swmod-files/files/2015-02/12-Visoes-Arquitetura.pdf. Acesso em 28 de Março de 2022.

> GeeksforGeeks. ISO/IEC 9126 in Software Engineering. 29 Out, 2021. Disponível em: https://www.geeksforgeeks.org/iso-iec-9126-in-software-engineering/. Acesso em 28 de Março de 2022.

> R. Ruggero, Análise sobre a ISO 9126 – NBR 13596. Disponível em: https://www.tiespecialistas.com.br/analise-sobre-iso-9126-nbr-13596/. Acesso em 30 de Março de 2022.

> A. Washington, ISO 9126. 12 Jun 2020. Disponível em: https://blog.grancursosonline.com.br/iso-9126/. Acesso em 30 de Março de 2022.

> ABNT - Associação Brasileira de Normas Técnicas. Engenharia de software - Qualidade de produto. Jun 2003. Disponível em: https://jkolb.com.br/wp-content/uploads/2014/02/NBR-ISO_IEC-9126-1.pdf. Acesso em 30 de Março de 2022.

> Lucidchart. O que é um diagrama UML?. Disponível em: https://www.lucidchart.com/pages/pt/o-que-e-uml. Acesso em 30 de Março de 2022.

> Lucidchart. Tudo sobre diagramas de pacotes UML. Disponível em: https://bit.ly/3wSaRTE. Acesso em 30 de Março de 2022.

> Lucidchart. O que é um diagrama de classe UML?. Disponível em: https://www.lucidchart.com/pages/pt/o-que-e-diagrama-de-classe-uml. Acesso em 30 de Março de 2022.

> Conceito: Visão da Implementação. Disponível em: https://www.cin.ufpe.br/~gta/rup-vc/core.base_rup/guidances/concepts/implementation_view_E373E3B6.html. Acesso em 30 de Março de 2022.

> Lucidchart. Diagrama de componentes. Disponível em: https://www.lucidchart.com/pages/pt/diagrama-de-componentes-uml. Acesso em 30 de Março de 2022.

> Conceito: Visão Lógica. Disponível em: https://bit.ly/3uMHEa6. Acesso em 30 de Março de 2022.

> Modelo de Implantação - Wiki - DTIC. Disponível em: https://bit.ly/3j37ukC. Acesso em: 28/03/2022.

> 4+1 Architectural view model in Software - Javarevisited. Dísponivel em: https://medium.com/javarevisited/4-1-architectural-view-model-in-software-ec407bf27258. Acesso em: 30/03/2022.

> ReactJS - Architecture. Disponível em: <https://bit.ly/3x4CMA7>. Acesso em: 27 Mar. 2022.

>  Milani, André. PostgreSQL: guia do programador. São Paulo. Novatec, 2008. Disponível em: https://bit.ly/3x4CMA7. Acesso em: 27/03/2022.‌

> Metas usabilidade. Disponível em: https://medium.com/difournier-uxr/as-6-metas-de-usabilidade-9491442fd56a. Acesso em 30 Mar. 2022.

> Requisitos não funcionais. Disponível em: https://bit.ly/3J335ZP. Acesso em 30 Mar.

> ALURA. Django e Django Rest: Diferenças e aplicações. Alura. Disponível em: https://www.alura.com.br/artigos/django-django-rest-diferencas. Acesso em: 31 mar. 2022.



### Histórico de versão

|    Data    |  Versão  |              Autor(es)               |                          Descrição                           |
| :--------: | :------: | :------------------------------: | :----------------------------------------------------------: |
| 28/03/2022 |   0.1    |      Guilherme Braz e Rodrigo Balbino          |                     Criação do documento                     |
| 28/03/2022 |  0.2    | Pedro Campos e Luis Araujo       | Criação do tópico Metas e Restrições Arquiteturais.|
| 28/03/2022 |  0.3    | Pedro Campos e Luis Araujo       | Criação do tópico Visão de dados. |
| 28/03/2022 |  0.4    | Luis Araujo e Pedro Campos      | Criação dos subtópicos de Metas arquiteturais |
| 28/03/2022 |  0.5    | Luis Araujo e Pedro Campos      | Criação das descrições dos subtópicos de Metas arquiteturais |
| 28/03/2022 |   0.6    | Guilherme Braz e Rodrigo Balbino |                   adição das visão logica                    |
| 28/03/2022 |   0.7    | Guilherme Braz e Rodrigo Balbino |              adição das visão de implementação               |
| 28/03/2022 |   0.8    | Guilherme Braz e Rodrigo Balbino |               adição do tópico sobre qualidade               |
| 28/03/2022 |  0.9   | João Victor e Álvaro | Adição do tópico visão de Implantação |
| 30/03/2022 |   0.9.1    |  Guilherme Braz e Rodrigo Balbino          |      Adicionando referências e conteúdo da visão lógica      |
| 30/03/2022 |   0.9.2    |   Guilherme Braz e Rodrigo Balbino          | Adicionando referências e conteúdo da visão de implementação |
| 30/03/2022 |  0.9.3 | João Victor e Álvaro Gouvea | Adição do tópico visão de Processos |
| 30/03/2022 |  0.9.4   | João Victor e Álvaro | Adição do tópico visão de Casos de Uso |
| 31/03/2022 |  0.9.5   | João Victor e Álvaro Gouvea | Adição de mais uma referência |
| 31/03/2022 |  0.9.6   |        Fernando e Antonio   |      Revião parcial do documento        |
| 31/03/2022 |  0.9.7   | João Victor e Álvaro Gouvea | Adição das imagens dos diagramas no tópico Visão de Processos              |
| 31/03/2022 |  0.10   | Fernando e Antonio |  Revisão da Visão de processos |
| 31/03/2022 |  0.10.1   | João Victor e Álvaro Gouvea | Alteração na formatação de frase |
| 31/03/2022 |  0.10.2  | Fernando e Antonio |  Revisão da Visão de Casos de Uso |
| 03/04/2022 |  0.10.3  | Lorrayne Cardozo e Ariel Serafim |  Revisão da Visão de Implantação |
| 04/04/2022 |  0.10.4  | Luis Araujo e Pedro Campos |  União dos arquivos de documentos de arquitetura |
| 04/04/2022 |  0.10.5  | Lorrayne Cardozo e Ariel Serafim |  Adição do tópico de representação arquitetural |
| 04/04/2022 |  0.10.6  | Lorrayne Cardozo e Ariel Serafim |  Correção de ordem da página |
| 05/04/2022 |  0.10.7  | Lorrayne Cardozo e Ariel Serafim |  Adição da introdução |
| 15/04/2022 |  0.10.9  | Lorrayne Cardozo e Ariel Serafim |  Nova versão dos diagramas do banco |