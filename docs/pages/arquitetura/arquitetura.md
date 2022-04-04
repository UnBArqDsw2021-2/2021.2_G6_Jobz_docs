# <center> DAS - DOCUMENTO DE ARQUITETURA DE SOFTWARE

<div align="justify">

## 1. Arquitetura

Usamos **Django** com o **REST Framework**, **PostgreSQL** e **ReactJS** para a cosntrução da aplicação.
O Django faz uso da arquitetura MVT, Model, View Template; Em que o Model lida com requisições (querys) de dados com objetos python, as Views recebem requisições Http e enviam respostas http, e o Template específica o formato de apresentação dos dados, que aqui é representado pelo módulo de ReactJS.
Segue o diagrama de arquitetura do projeto.
<p align='center'>
    <img src='assets/images/arquitetura/Arquitetura.drawio.png' width=80% height=auto>
    <figcaption align='center'>
        <b>Figura 1: Diagrama de Arquitetura do produto </b>
        <br>
    </figcaption>
</p>

## 2. Visão Lógica

A visão lógica tem o objetivo de representar a visão conceitual do projeto por meio de camadas, para que possamos compreender a estrutura e a organização do design do sistema, descrevendo melhor os elementos comportamentais e funcionalidades da arquitetura. Essa é a visão arquitetural que contém as classes de design mais importantes, além de sua essencial organização em pacotes e subsistemas de camadas.

Tendo isso em vista, elaboramos o diagrama de classe e o diagrama de pacotes, que foram desenvolvidos com uso do Framework [Django](https://www.djangoproject.com/) voltado para o Backend e a biblioteca [React.js](https://pt-br.reactjs.org/) para o Frontend de nossa aplicação.

### 2.1 Diagrama de Classes

O [diagrama de classe](./pages/modelagem/diagramaDeClasses) é um dos principais [diagramas UML](https://www.lucidchart.com/pages/pt/o-que-e-uml), pois consegue mapear claramente a estrutura de nosso sistema apresentando suas classes, atributos, operações e relações entre os objetos.

Com o seu uso, somos capazes de entender melhor a visão geral do esquema de nossa aplicação e conseguimos expressar visualmente as necessidades específicas de nosso sistema. Além de sermos capazes de criar modelos de dados de nossos sistema e até mesmo gráficos detalhados para destacar alguma informação específica que seja necessária.

<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramaClasses/classDiagramV2.svg' width=80% height=auto>
    <figcaption align='center'>
        <b>Figura 1: Diagrama de classes do produto v.2.0 </b>
        <br>
    </figcaption>
</p>

### 2.2 Diagrama de Pacotes

Um [diagrama de pacotes](./pages/modelagem/diagramaPacotes) apresenta no formato de pastas ou pacotes, a organização e disposição de diferentes elementos de um modelo. Esses elementos que podem ser documentos, classes e até mesmo outros pacotes, são dispostos dentro dessas pastas de arquivos que são apresentados em nosso diagrama, que por fim é organizado e apresentado de forma hierárquica.

O diagrama de pacotes é capaz de fornecer uma visibilidade geral melhor sobre projetos e sistemas de grande escala. Pois oferece uma versão simplificada de diagramas de classe complexos, além de permitir que atualizações sejam feitas com facilidade com o decorrer do desenvolvimento do produto

#### 2.2.1 Backend

Dessa forma, temos o diagrama de pacotes criado para apresentar a estrutura de nosso projeto do ponto de vista do backend da aplicação. No qual utiliza o banco de dados [PostgreSQL](https://www.postgresql.org/) para o seu armazenamento de dados.

<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramadepacotes.png' height=auto>
    <figcaption align='center'>
        <b>Figura 2: Diagrama de pacotes do backend do produto. </b>
        <br>
    </figcaption>
</p>

#### 2.2.2 Frontend

Por conseguinte, temos então o diagrama de pacotes voltado para o frontend de nossa aplicação, no qual realiza o reaproveitamento dos componentes para a criação da telas, além de definir o padrão de desenvolvimento e simplificar o código.

<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramapacotesfrontend.png' height=auto>
    <figcaption align='center'>
        <b>Figura 3: Diagrama de pacotes do frontend produto. </b>
        <br>
    </figcaption>
</p>

#### 2.2.3 Sistema

Por fim, temos a representação de nosso sistema completo, no qual é caracterizado pela conexão do frontend com o backend, nos quais utilizam o [protocolo HTTP](https://developer.mozilla.org/pt-BR/docs/Web/HTTP) para realizar trocas de dados por meio de suas requisições.

<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramapacotesgeral.png' height=auto>
    <figcaption align='center'>
        <b>Figura 4: Diagrama de pacotes do produto. </b>
        <br>
    </figcaption>
</p>

#### 2.2.4. Padrões de Projeto
Como explorado em módulos anteriores, padrões de projeto são uma continuação natural do     processo de desenvolvimento, que busca organizar não só estruturas e algoritmos, como também soluções a problemas comuns.
Foram usados de forma direta e indireta, padrões de projeto que facilitam a reutilização de código, ao definir uma maneira validada e bem documentada de se resolver determinada questão.

## 3. Representação Arquitetural

### 3.1. FrontEnd

O **ReactJS** é uma biblioteca da linguagem JavaScript que utiliza certos padrões de design baseados em Components. A aplicação React começa com um único componente raiz, que é construído usando um ou mais componentes, e cada um desses componentes pode ser aninhado com outro componente em qualquer nível.

### 3.2. BackEnd


### 3.3. Banco de Dados
O **PostgreSQL** é um Sistema Gerenciador de Banco de Dados (SGBD) Relacional, utilizado para armazenar informações de soluções de informática em todas as áreas de negócios existentes (Milani, André. PostgreSQL: Guia do Programador. Novatec. 2008).



## 4. Metas e Restrições Arquiteturais

### 4.1. Metas

#### 4.1.2 Portabilidade
A aplicação deve ser compatível e ser possível a execução com desempenho satisfatório nos navegadores mais utilizados e que possuem atualizações recentes.

#### 4.1.1 Escalabilidade
A aplicação deve ser estruturada com o objetivo de ser escalável o suficiente para ser possível futuras evoluções com o crescimento do projeto.

#### 4.1.2 Segurança
O aplicativo deve ser seguro e lidar com os dados dos usuários com segurança, de forma que a informação só pode ser acessada e atualizada por pessoas autorizadas e devidamente credenciadas (autenticação de usuários).

#### 4.1.3 Usabilidade
O sistema deverá ter a capacidade em fazer com que o usuário tenha sucesso na execução de suas tarefas de maneira simples.


### 4.2. Restrições

|Restrições||
|:-----|:------|
|Plataforma|A aplicação terá suporte para browsers para computador.|
|Público|A aplicação será desenvolvida para toda a população brasileira e será voltada para prestadores de diversos serviços e seus respectivos clientes.|
|Linguagem|A aplicação Jobz será desenvolvida em idioma português do Brasil.|
|Prazo|A aplicação terá o prazo estimado de termino até o fim da disciplina.|
|Equipe|A equipe possui 10 integrantes do curso de Eng. de Software da UnB.|
|Conectividade|É necessária a conectividade com a internet para o acesso e utilização da aplicação.|

## 5. Visão de dados

### 5.1. Diagrama Entidade-Relacionamento (DE-R)
<p align='center'>
    <img src='assets/images/modelagemBanco/v2-DERR.jpg' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 1: Diagrama de entidade relacionamento</b>
        <br>
    </figcaption>
</p>

### 5.2. Diagrama Logico de Dados (DLD)

<p align='center'>
    <img src='assets/images/modelagemBanco/v2-DLDR.jpg' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 2: Diagrama lógico</b>
        <br>
    </figcaption>
</p>

### 5.3. Dicionário de dados

Entidade: **PERSON**

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    name    |     Obrigatório     |               VARCHAR                  |             Nome completo de cada pessoa.                 |
|    phone   |      Obrigatório       |               BIGINT                |             Telefone para contato de cada. pessoa.             |
| email |      Obrigatório        |             VARCHAR                     | Email de cada pessoa que será utilizado na aplicação. |
| cpf |      chave-Primária        |             BIGINT                     |  Chave-Primária Identificadora de cada pessoa.                            |
|  password  |      Obrigatório       |               VARCHAR                |          Senha para autenticação do funcionário.           |

Entidade: **USER**

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    idUser    |     Chave-Primária    |               INT                  |             Chave-Primária identificadora de cada usuário.               |
|    cpf   |      Chave-Primaria, Estrangeira |               BIGINT                |             Chave-Primária Identificadora de cada pessoa.             |
| idAddress |      Chave-Estrangeira        |             INT                     | Chave estrangeira correspondente ao endereço do usuário. |


Entidade: **ADDRESS**

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    idAddress    |     Chave-Primária     |               INT                  |            Chave-Primária identificadora de cada endereço.                 |
|    city   |      Obrigatório       |               VARCHAR                | Cidade correspondente ao endereço de cada usuário.             |
| state |      Obrigatório        |             VARCHAR                     | Estado correspondente ao endereço de cada usuário. |
| cep |      Obrigatório        |             VARCHAR                       |  CEP correspondente ao endereço de cada usuário.                         |
|  number  |      Obrigatório       |               INT               |          Número correspondente ao endereço de cada usuário.           |
|  district  |      Obrigatório       |               VARCHAR               |   Bairro correspondente ao endereço de cada usuário.           |
|  complement  |      Obrigatório       |               VARCHAR               |   Complemento correspondente ao endereço de cada usuário.           |


Entidade: **SERVICE**

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    datePurchase    |     Obrigatório     |               DATETIME                  |             Data correspondente da aquisição do serviço.                 |
|    dateService   |      Obrigatório       |               DATETIME                |            Data correspondente da publicação do serviço.             |
| serviceDescription |      Obrigatório        |             VARCHAR                     | Descrição relativa a cada serviço disponibilizado. |
| idService |      Chave-Primária        |             INT                     |  Chave-Primária Identificadora de cada serviço.                            |
|  idUser  |      Chave-Estrangeira       |               INT                |          Chave estrangeira relativa ao id do usuário que contratou o serviço.           |
|  cpf  |      Chave-Estrangeira       |               BIGINT                |          Chave estrangeira relativa ao cpf do usuário que contratou o serviço.           |
|  idCategory  |      Chave-Estrangeira       |               INT                |          Chave estrangeira relativa ao id da categoria ao qual pertence o serviço.           |
|  idEvaluation  |      Chave-Estrangeira       |               INT                |          Chave estrangeira relativa ao id da avaliação do serviço.           |

Entidade: **SERVICE_CATEGORY**

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    idCategory    |     Chave-Primária     |               INT                  |             Chave Primária identificadora a cada categoria.                 |
|    nameService   |      Obrigatório       |               VARCHAR                |      Nome de cada serviço que foi cadastrado.       |

Entidade: **EVALUATION**

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    idEvaluation    |     Chave-Primária     |               INT                  |            Chave primária identificadora de cada avaliação.                 |
|    comment   |      Obrigatório       |               VARCHAR                |            Comentário relativo a cada avaliação dos serviços disponibilizados.            |
| grade |      Obrigatório        |             INT                     | Grau relativo à avaliação relativa ao serviço.  |

Entidade: **COMPANY**

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    idCompany    |     Chave-Primária     |               INT                  |            Chave-Primária identificadora de cada empresa/companhia.                 |
| email |      Obrigatório        |             VARCHAR                     | Email de cada empresa que será utilizado na aplicação. |
|    name   |      Obrigatório       |               VARCHAR                |            Nome completo da empresa que será cadastrado na aplicação.            |


Entidade: **PROVIDER**

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    idProvider    |     Chave-Primária     |               INT                  |             Chave-Primária identificadora de cada prestador de serviços.                 |
| cpf |      chave-primária, Estrangeira       |             BIGINT                     |  Chave-Primária, Estrangeira Identificadora de cada pessoa.                            |
|    idOccupation   |      Obrigatório       |               INT                |             Chave-Estrangeira relativa ao id da ocupação de cada prestador de serviços.                |


Entidade: **SCHEDULE**

|  Atributo  | Propriedade do aributo |            Tipo de Dado             |                         Descrição                         |
| :--------: | :--------------------: | :---------------------------------: | :-------------------------------------------------------: |
|    dayOfWeek    |     Obrigatório     |               ENUM('seg','ter', 'quar','quin','sex','sab')                  |             Dia da semana respectivo a disponibilidade de serviço da agenda do prestador.                 |
|    entryTime   |      Obrigatório       |               DATETIME                |             Horário de entrada respectivo a agenda de cada prestador de serviços.             |
| endOfWork |      Obrigatório        |             DATETIME                     | Horário de saída respectivo a agenda de cada prestador de serviços. |
| idSchedule |      Chave-Primária        |             INT                     |  Chave-Primária identificadora de cada agenda.                            |
|  idProvider  |      Chave-Estrangeira       |               INT                |          Chave-Estrangeira relativa ao id do prestador de serviços ao qual é dono da agenda.           |
|  cpf  |      Chave-Estrangeira       |               BIGINT                |          Chave-Estrangeira relativa ao cpf do prestador de serviços ao qual é dono da agenda.           |


## 6. Visão de Processos

Essa visão corresponde a diferentes processos, suas responsabilidades, colaborações e como elas interagem entre si. É uma visão de modelo de projeto que pode ser representada utilizando objetos e mensagens trocadas, representados em classes e diagramas de interação usando a notação de processo.

Para o nosso projeto temos os diagramas de [sequência](./pages/modelagem/diagramaSequencia.md), [atividades](./pages/modelagem/diagramaAtividades.md) e [comunicação](./pages/modelagem/diagrama-comunicacao.md) que trazem um detalhamento sobre essa visão e podem ser visualizados nas imagens a seguir:

### 6.1 Diagrama de Sequência

O diagrama de sequência da contratação de serviços, que é o principal processo da nossa aplicação.

<p align='center'>
    <img src='assets/images/diagramaSequencia/sequenceDiagramHiring.png' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 5: Diagrama de Sequência da Contratação de Serviços</b>
        <br>
    </figcaption>
</p>

### 6.2 Diagramas de Atividades

O diagrama de atividades descreve as etapas que ocorrem quando um determinado cenário é iniciado, até que este cenário seja encerrado, ajudando a compreensão do processo que será executado. Temos então o detalhamento dos fluxos de login, perfil do cliente e perfil do prestador de serviço.

<p align='center'>
    <img src='assets/images/diagramaAtividades/diagramaLogin.png' width=40% height=auto>
    <figcaption align='center'>
        <b>Figura 6 - Diagrama de Atividades representando o login. </b>
        <br>
    </figcaption>
</p>

<p align='center'>
    <img src='assets/images/diagramaAtividades/diagramaCliente.png' width=40% height=auto>
    <figcaption align='center'>
        <b>Figura 7 - Diagrama de Atividades representando o perfil de cliente.</b>
        <br>
    </figcaption>
</p>

<p align='center'>
    <img src='assets/images/diagramaAtividades/diagramaPrestador.png' width=40% height=auto>
    <figcaption align='center'>
        <b>Figura 8 - Diagrama de Atividades representando o perfil de prestador de serviço.</b>
        <br>
    </figcaption>
</p>

### 6.3 Diagramas de Comunicação

O diagrama de comunicação demonstra o comportamento dinâmico de um sistema ou software, entendendo a interligação e a comunicação entre as partes de um sistema completo.

<p align='center'>
    <img src='assets/images/diagrama-comunicacao/collaborator.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 9: Diagrama de comunicação da criação do serviço</b>
        <br>
    </figcaption>
</p>

<p align='center'>
    <img src='assets/images/diagrama-comunicacao/comunicacao-criacao-cliente.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 10: Diagrama de comunicação da contratação do serviço</b>
        <br>
    </figcaption>
</p>

## 7. Visão de implementação

Para melhorar a compreensão física do processamento do sistema utilizamos a visão de implementação, no qual nos permite ilustrar e captar as decisões de arquitetura tomadas para a implementação. No qual, se aproveita do [diagrama de componentes](./pages/modelagem/componentes) que apresenta os subsistemas e suas organizações em camadas de hierarquia.
Além de que, a visão de implementação nos permite entender a quantidade de código que será produzida, discutir reutilizações no sistema, considerar estratégias para a release e até mesmo atribuir o trabalho de implementação ao indivíduos ou equipes.

### 7.1 Diagrama de Componentes

Um diagrama de componentes é considerado quase que indispensável para a criação de um sistema de software, existe até mesmo o chamado desenvolvimento baseado em componentes([CBD](https://www.techopedia.com/definition/31002/component-based-development-cbd)). Pois essa representação mostra com detalhes o relacionamento de diferentes módulos do sistema.

<p>Mesmo que esse diagrama pareça complexo, ele é capaz de representar a estrutura física do sistema, dá atenção aos seus componentes e relacionamentos, além de destacar o comportamento do serviço em relação a interface.</p>
<p align='center'>
    <img src='assets/images/Diagrama_Compomentes/Diagrama compomente.jpeg' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 11: Diagrama de Componentes</b>
        <br>
    </figcaption>
</p>

## 8. Visão de Casos de Uso

A visão de casos de uso é uma representação visual mais aproximada do usuário, descrevendo as relações das funcionalidades do sistema esperadas pelo cliente. Essas relações podem ser observadas no documento de [diagrama de casos de uso](./pages/modelagem/casosUso.md) que apresenta uma visão mais completa sobre a utilização desse diagrama em nosso projeto.

### 8.1 Casos de uso

<p align='center'>
    <img src='assets/images/CasosUso/CasosUsoJOBZ2.png' width=80% height=auto>
    <figcaption align='center'>
        <b>Figura 12: Diagrama de Casos de Uso. </b>
        <br>
    </figcaption>
</p>

## 9. Visão de Implantação

O Jobz é uma aplicação web que segue o modelo de camadas, onde temos as camadas do frontend, backend e a base da dados. O [diagrama de implementação](./pages/modelagem/diagramaImplementacao.md) possui representações dessas camadas juntamente com a camada do usuário que tem acesso apenas a interface do frontend. O usuário acessa por meio de um web browser nossa aplicação e o frontend realiza requisições ao backend, que por sua vez realiza os serviços solicitados, armazenando e buscando os dados necessários na base de dados.

### 9.1 Diagrama de Implementação

<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramaImplementação.svg' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 13: Diagrama de implementação do produto. </b>
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

> Modelo de Implantação - Wiki - DTIC. Disponível em: https://dtic.tjpr.jus.br/wiki/-/wiki/Governan%C3%A7a-TIC/Modelo+de+Implanta%C3%A7%C3%A3o/pop_up?_36_version=1.0. Acesso em: 28/03/2022.

> 4+1 Architectural view model in Software - Javarevisited. Dísponivel em: https://medium.com/javarevisited/4-1-architectural-view-model-in-software-ec407bf27258. Acesso em: 30/03/2022.

> ReactJS - Architecture. Disponível em: <https://www.tutorialspoint.com/reactjs/reactjs_architecture.htm#:~:text=Architecture%20of%20the%20React%20Application&text=Developers%20are%20free%20to%20choose,.%2C%20to%20write%20better%20code.>. Acesso em: 27 Mar. 2022.

>  Milani, André. PostgreSQL: guia do programador. São Paulo. Novatec, 2008. Disponível em: https://books.google.com.br/books?hl=pt-BR&lr=&id=eb7fXbM70F4C&oi=fnd&pg=PA19&dq=postgresql&ots=FWcgYx_Oo1&sig=8Qv1Kfrdfj9Bzqz7ywREjIgBYZM#v=onepage&q=postgresql&f=false Acesso em: 27/03/2022.‌

> Metas usabilidade. Disponível em: https://medium.com/difournier-uxr/as-6-metas-de-usabilidade-9491442fd56a. Acesso em 30 Mar. 2022.

> Requisitos não funcionais. Disponível em: https://www.devmedia.com.br/artigo-engenharia-de-software-3-requisitos-nao-funcionais/9525#:~:text=Portabilidade%20pode%20ser%20definida%20como,ser%20executado%20em%20ambientes%20distintos. Acesso em 30 Mar.



### Histórico de versão

|    Data    |  Versão  |              Autor               |                          Descrição                           |
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
| 03/04/2022 |  0.10.3  | Lorrayne e Ariel |  Revisão da Visão de Implantação |
| 04/04/2022 |  0.10.4  | Luis Araujo e Pedro Campos |  União dos arquivos de documentos de arquitetura |