# <center> DAS - Documento de Arquitetura

<div align="justify">

## 1. Introdução

## 2. Visão de Implantação

O Jobz é uma aplicação web que segue o modelo de camadas, onde temos as camadas do frontend, backend e a base da dados. A figura 1 abaixo é o diagrama de implantação com representações dessas camadas juntamente com a camada do usuário que tem acesso apenas a interface do frontend. O usuário acessa nossa aplicação por meio de um web browser, e o frontend realiza requisições ao backend, que por sua vez realiza os serviços solicitados, armazenado e buscando os dados necessários na base de dados.

<p align='center'>
    <img src='assets/images/diagrama_implantacao/diagrama_implantacao.png' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 1: Diagrama de Implantação</b>
    </figcaption>
</p>

## 3. Referências

> Modelo de Implantação - Wiki - DTIC. Disponível em: https://dtic.tjpr.jus.br/wiki/-/wiki/Governan%C3%A7a-TIC/Modelo+de+Implanta%C3%A7%C3%A3o/pop_up?_36_version=1.0. Acesso em: 28/03/2022.

</div>

### Histórico de versão

|    Data    | Versão |    Autor    |      Descrição       |
| :--------: | :----: | :---------: | :------------------: |
| 28/03/2022 |  0.1   | João Victor e Álvaro | Adição do tópico visão de Implantação |
