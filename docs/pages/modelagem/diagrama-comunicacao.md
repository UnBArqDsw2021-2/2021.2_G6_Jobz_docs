# <center> Diagrama de Comunicação

<div align="justify">

## 1. Introdução

Diagrama de comunicação, também chamado de diagrama de colaboração no UML 1.x, é um diagrama dinâmico que mostra as interações entre objetos ou partes do software atraves de uma sequência de mensagens. Este diagrama corresponde a um diagrama de sequências simples, sem mecanismos estruturais como usos de interações e fragmentos combinados.

Os principais elementos do diagrama de comunicação podem ser vistos na imagem a seguir:

<p align='center'>
    <img src='assets/images/diagrama-comunicacao/communication-diagram-overview.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 1: Os principais elementos do Diagrama de Comunicação</b>
        <br>
        <small>Fonte: https://www.uml-diagrams.org/communication-diagrams.html</small>
    </figcaption>
</p>

O diagrama de comunicação são inseridos dentro de um Frame, que é uma borda retangular com o nome do canto superior esquerdo.

<p align='center'>
    <img src='assets/images/diagrama-comunicacao/communication-frame-long.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 2: Representação de um Frame</b>
        <br>
        <small>Fonte: https://www.uml-diagrams.org/communication-diagrams.html</small>
    </figcaption>
</p>

Esse diagrama possui também um elemento chamado de Lifeline, que é uma especialização de um participante da interação, representando apenas uma entidade.

<p align='center'>
    <img src='assets/images/diagrama-comunicacao/communication-lifeline.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 3: Representação de uma Lifeline</b>
        <br>
        <small>Fonte: https://www.uml-diagrams.org/communication-diagrams.html</small>
    </figcaption>
</p>

A mensagem no diagrama de comunicação é mostrada como uma linha com expressão de sequência e seta acima da linha. A seta indica a direção da comunicação.

<p align='center'>
    <img src='assets/images/diagrama-comunicacao/message.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 4: Representação de uma Mensagem</b>
        <br>
        <small>Fonte: https://www.uml-diagrams.org/communication-diagrams.html</small>
    </figcaption>
</p>

## 2. Diagramas de Comunicação

### 2.1 Criação do serviço

<p align='center'>
    <img src='assets/images/diagrama-comunicacao/collaborator.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 5: Diagrama de comunicação da criação do serviço</b>
        <br>
        <small>Fonte: AUTOR</small>
    </figcaption>
</p>

### 2.2 Contratação do serviço

<p align='center'>
    <img src='assets/images/diagrama-comunicacao/comunicacao-criacao-cliente.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 6: Diagrama de comunicação da contratação do serviço</b>
        <br>
        <small>Fonte: AUTOR</small>
    </figcaption>
</p>

## 3. Referências

> -   UML Communication Diagrams Overview, Disponível em: https://www.uml-diagrams.org/communication-diagrams.html
> -   Diagrama de comunicação. Animalesco. Disponível em: https://unbarqdsw2021-1.github.io/2021.1_G01_Animalesco_docs/#/pages/communication-diagram

</div>

### Histórico de versão

|    Data    | Versão |    Autor    |              Descrição              |
| :--------: | :----: | :---------: | :---------------------------------: |
| 08/02/2022 |  0.1   | João Victor |        Criação do documento         |
| 14/02/2022 |  1.0   | João Victor | Adição dos diagramas de comunicação |
