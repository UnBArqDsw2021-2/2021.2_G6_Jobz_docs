# <center> DAS - DOCUMENTO DE ARQUITETURA DE SOFTWARE

<div align="justify">

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

## 3. Visão de Processos

Essa visão corresponde a diferentes processos, suas responsabilidades, colaborações e como elas interagem entre si. É uma visão de modelo de projeto que pode ser representada utilizando objetos e mensagens trocadas, representados em classes e diagramas de interação usando a notação de processo.

Para o nosso projeto temos os diagramas de [sequência](./pages/modelagem/diagramaSequencia.md), [atividades](./pages/modelagem/diagramaAtividades.md) e [comunicação](./pages/modelagem/diagrama-comunicacao.md) que trazem um detalhamento sobre essa visão e podem ser visualizados nas imagens a seguir:

### 3.1 Diagrama de Sequência

O diagrama de sequência da contratação de serviços, que é o principal processo da nossa aplicação.

<p align='center'>
    <img src='assets/images/diagramaSequencia/sequenceDiagramHiring.png' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 5: Diagrama de Sequência da Contratação de Serviços</b>
        <br>
    </figcaption>
</p>

### 3.2 Diagramas de Atividades

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

### 3.3 Diagramas de Comunicação

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

## 4. Visão de implementação

Para melhorar a compreensão física do processamento do sistema utilizamos a visão de implementação, no qual nos permite ilustrar e captar as decisões de arquitetura tomadas para a implementação. No qual, se aproveita do [diagrama de componentes](./pages/modelagem/componentes) que apresenta os subsistemas e suas organizações em camadas de hierarquia.
Além de que, a visão de implementação nos permite entender a quantidade de código que será produzida, discutir reutilizações no sistema, considerar estratégias para a release e até mesmo atribuir o trabalho de implementação ao indivíduos ou equipes.

### 4.1 Diagrama de Componentes

Um diagrama de componentes é considerado quase que indispensável para a criação de um sistema de software, existe até mesmo o chamado desenvolvimento baseado em componentes([CBD](https://www.techopedia.com/definition/31002/component-based-development-cbd)). Pois essa representação mostra com detalhes o relacionamento de diferentes módulos do sistema.

<p>Mesmo que esse diagrama pareça complexo, ele é capaz de representar a estrutura física do sistema, dá atenção aos seus componentes e relacionamentos, além de destacar o comportamento do serviço em relação a interface.</p>
<p align='center'>
    <img src='assets/images/Diagrama_Compomentes/Diagrama compomente.jpeg' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 11: Diagrama de Componentes</b>
        <br>
    </figcaption>
</p>

## 5. Visão de Casos de Uso

A visão de casos de uso é uma representação visual mais aproximada do usuário, descrevendo as relações das funcionalidades do sistema esperadas pelo cliente. Essas relações podem ser observadas no documento de [diagrama de casos de uso](./pages/modelagem/casosUso.md) que apresenta uma visão mais completa sobre a utilização desse diagrama em nosso projeto.

### 5.1 Casos de uso

<p align='center'>
    <img src='assets/images/CasosUso/CasosUsoJOBZ2.png' width=80% height=auto>
    <figcaption align='center'>
        <b>Figura 12: Diagrama de Casos de Uso. </b>
        <br>
    </figcaption>
</p>




## 6. Qualidade

Para avaliar a qualidade de nosso projeto, decidimos utilizar a [ISO/IEC 9126](https://jkolb.com.br/wp-content/uploads/2014/02/NBR-ISO_IEC-9126-1.pdf). Essa ISO possui por objetivo padronizar a avaliação da qualidade de um software, possibilitando assim, que sejamos capazes de apresentar um produto final com qualidade, nos baseando em suas características e atributos.

### 6.1 ISO/IEC 9126 in Software Engineering

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

## 7. Referências

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

### Histórico de versão

|    Data    |  Versão  |              Autor               |                          Descrição                           |
| :--------: | :------: | :------------------------------: | :----------------------------------------------------------: |
| 28/03/2022 |   0.1    |      Guilherme Braz e Rodrigo Balbino          |                     Criação do documento                     |
| 28/03/2022 |   0.2    | Guilherme Braz e Rodrigo Balbino |                   adição das visão logica                    |
| 28/03/2022 |   0.3    | Guilherme Braz e Rodrigo Balbino |              adição das visão de implementação               |
| 28/03/2022 |   0.4    | Guilherme Braz e Rodrigo Balbino |               adição do tópico sobre qualidade               |
| 30/03/2022 |   0.5    |  Guilherme Braz e Rodrigo Balbino          |      Adicionando referências e conteúdo da visão lógica      |
| 30/03/2022 |   0.6    |   Guilherme Braz e Rodrigo Balbino          | Adicionando referências e conteúdo da visão de implementação |
| 30/03/2022 |  0.7   | João Victor e Álvaro Gouvea | Adição do tópico visão de Processos |
| 30/03/2022 |  0.8   | João Victor e Álvaro | Adição do tópico visão de Casos de Uso |
| 31/03/2022 |  0.8.1   | João Victor e Álvaro Gouvea | Adição de mais uma referência |
| 31/03/2022 |  0.8.2   |        Fernando e Antonio   |      Revião parcial do documento        |
| 31/03/2022 |  0.8.3   | João Victor e Álvaro Gouvea | Adição das imagens dos diagramas no tópico Visão de Processos              |
| 31/03/2022 |  0.9   | Fernando e Antonio |  Revisão da Visão de processos |
| 31/03/2022 |  0.9.1   | João Victor e Álvaro Gouvea | Alteração na formatação de frase |
| 31/03/2022 |  0.9.2  | Fernando e Antonio |  Revisão da Visão de Casos de Uso |

