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

## 3. Referências

> Ludidchart, O que é um diagrama de implementação?. Disponível em: https://www.lucidchart.com/pages/pt/o-que-e-diagrama-de-implementacao-uml. Acesso em 28 de Março de 2022.

> Silva O. Flávio. Visões da Arquitetura Diagramas UML. Disponível em: http://www.facom.ufu.br/~flavio/swmod-files/files/2015-02/12-Visoes-Arquitetura.pdf. Acesso em 28 de Março de 2022.

</div>

### Histórico de versão

|    Data    | Versão |              Autor               |             Descrição             |
| :--------: | :----: | :------------------------------: | :-------------------------------: |
| 29/01/2022 |  0.1   |           João Victor            |       Criação do documento        |
| 28/03/2022 |  0.2   | Guilherme Braz e Rodrigo Balbino |      adição das visão logica      |
| 28/03/2022 |  0.3   | Guilherme Braz e Rodrigo Balbino | adição das visão de implementação |