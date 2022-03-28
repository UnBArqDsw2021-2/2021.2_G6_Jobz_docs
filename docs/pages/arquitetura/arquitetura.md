# <center> DAS - DOCUMENTO DE ARQUITETURA DE SOFTWARE

<div align="justify">

## 1. Introdução

## 2. Visão Lógica

A visão lógica tem o objetivo de representar a visão conceitual do projeto por meio de camadas, descrevendo melhor os elementos comportamentais e funcionalidades da arquitetura. Tendo isso em vista, fizemos os diagramas de classe e o diagrama de pacotes, tendo sido desenvolvidos com os Frameworks Django voltado para o Backend e o React.js para o Frontend de nossa aplicação.

### 2.1 Diagrama de Classes

<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramaClasses/classDiagramV2.svg' width=80% height=auto>
    <figcaption align='center'>
        <b>Figura 1: Diagrama de classes do produto v.2.0 </b>
        <br>
    </figcaption>
</p>

### 2.2 Diagrana de Pacotes

#### 2.2.1 Backend

<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramadepacotes.png' height=auto>
    <figcaption align='center'>
        <b>Figura 2: Diagrama de pacotes do backend do produto. </b>
        <br>
    </figcaption>
</p>

#### 2.2.2 Frontend

<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramapacotesfrontend.png' height=auto>
    <figcaption align='center'>
        <b>Figura 3: Diagrama de pacotes do frontend produto. </b>
        <br>
    </figcaption>
</p>

#### 2.2.3 Sistema

<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramapacotesgeral.png' height=auto>
    <figcaption align='center'>
        <b>Figura 4: Diagrama de pacotes do produto. </b>
        <br>
    </figcaption>
</p>

## 3. Visão de implementação

A visão de implementacao tem o objetivo de representar de forma estática como o sistema será implementado. Tendo isso em vista, fizemos o diagrama de componentes para melhor detalhar as conexões entre os componentes e interfaces da arquitetura e a modelagem do banco de dados do sistema de em nossa aplicação.

<p align='center'>
    <img src='assets/images/Diagrama_Compomentes/Diagrama compomente.jpeg' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 5: Diagrama de Componentes</b>
        <br>
    </figcaption>
</p>

## 4. Qualidade

### ISO/IEC 9126 in Software Engineering

A ISO/IEC é um padrão internacional de um modelo para medir de maneira mais sistemática e exata a qualidade de um software. Com isso
usaremos ela como modelo para orientar nosso projeto de software com questão a qualidade do mesmo.

O padrão de qualidade pode ser dividido em 4 partes: 'Quality model', 'External Metrices', 'Internal Metrices' e 'Quality in use metrices'.
As três primeiras partes estão preocupadas em descrever e medir a qualidade do produto de software enquanto que a quarta está preocupada com a qualidade do produto do ponto de vista do usuário.

As qualidades externas e internas determinam a qualidade do produto por meio de seis diferentes características(Functionability, Reliability, Usability, Efficiency e Maintainability), nas quais são subdivididas em diferentes atributos. Sendo eles apresentados a seguir:

- Functionality: é considerado um fator crucial na qualidade do software, sendo as funções aquelas que resolverão os requisitos. É subdividida: suitability, accuracy, security, functionality compliance e interoperability.

- Reliability: é a capacidade do sistema performar conforme pretendido sem nenhuma falha. É subdividida: maturity, fault tolerance,recoverability e reliability compliance.

- Usability : esta relacionado a facilidade de uso do sistema e de sua velocidade de aprendizado. É subdividido em: training, learnability, communicativeness e usability compliance.

- Efficiency: é um grupo de atributos que lida com o nível de performance do software de acordo com determinadas condições: Time Behaviorm Resource Utilization e Efficiency Compliance.

- Maintainability: é um grupo de a atributos que possuem a capacidade de fazer modificações específicas, eles são: Analyzability, Changeability, Stability, Testability e Maintainability Compliance.

- Portability: um grupo de atributos que possui a habilidade de ser transferido de um ambiente de software para outro. É subdivido em adaptability, Installability, Co-existence, Replace ability e Portability Compliance
| Fator de Qualidade   |  Jobz   |
|:--------------------:|:-----:|
| Functionality        |  O projeto esta seguindo os requisitos funcionais e não funcionais coerentemente de acordo com nosso [backlog](./pages/modelagem/backlogPriorizado)    |
| Reliability          |   Projetado utilizando conteiners e técnicas de deploy para garantir a fácil recuperção do mesmo, além de ser seguida variás práticas e [padrões de design](./pages/Padroes_projeto/gof/criacionais) ao longo do desenvolvimento o que ajuda a garantir maior maturidade de código e tolerância a falhas.    |
| Usability            |  O projeto visa elaborar uma [UI/UX minimalista](./pages/modelagem/prototipoAlta), sem a intenção de muitas funcionalidades avançadas, alem de usar de técnicas de design para facilitar a navegação e deixar o sistema mais direto e intuitivo. Também terá no webbapp uma página somente para ajuda com perguntas frequentes e formas de contato para tirar dúvidas caso existam.   |
| Efficiency           |  A plataforma possui como objetivo ser minimalista utilizando códigos eficientes para manter a aplicação o mais simples possível, onde os computares mais simples são capazes de executá-la.     |
| Maintainability      |  Jobz foi elaborada visando possuir uma [alta coesão e baixo acoplamento](./pages/Padroes_projeto/GRASP/GRASPs) visando manter viável sua manutenibilidade.     |
| Portability          |  A aplicação será responsiva de acordo com o tamnho de tela do usuário.   |

## 3. Referências

> Ludidchart, O que é um diagrama de implementação?. Disponível em: https://www.lucidchart.com/pages/pt/o-que-e-diagrama-de-implementacao-uml. Acesso em 28 de Março de 2022.

> Silva O. Flávio. Visões da Arquitetura Diagramas UML. Disponível em: http://www.facom.ufu.br/~flavio/swmod-files/files/2015-02/12-Visoes-Arquitetura.pdf. Acesso em 28 de Março de 2022.

> GeeksforGeeks. ISO/IEC 9126 in Software Engineering. Disponível em 29 Out, 2021. Disponível em: https://www.geeksforgeeks.org/iso-iec-9126-in-software-engineering/. Acesso em 28 de Março de 2022.

</div>

### Histórico de versão

|    Data    | Versão |              Autor               |             Descrição             |
| :--------: | :----: | :------------------------------: | :-------------------------------: |
| 29/01/2022 |  0.1   |           João Victor            |       Criação do documento        |
| 28/03/2022 |  0.2   | Guilherme Braz e Rodrigo Balbino |      adição das visão logica      |
| 28/03/2022 |  0.3   | Guilherme Braz e Rodrigo Balbino | adição das visão de implementação |
| 28/03/2022 |  0.4   | Guilherme Braz e Rodrigo Balbino | adição do tópico sobre qualidade |
