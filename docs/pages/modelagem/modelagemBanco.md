# <center> Modelagem banco de dados

<div align="justify">

## 1. Introdução

O processo de modelagem de banco de dados é um processo de desenvolvimento de software que visa a construção de um modelo de dados que represente a estrutura de dados de uma base de dados, nesse processo se usa de coletas, analises, categorização e a explorarão dos dados e seus tipos.

"O objetivo da Modelagem de Dados é transmitir e apresentar uma representação única"(Machado, 2004, p.25), tarefa que não é simples levando em conta a complexidade de tarefas realizadas por softwares atuais. Para que a modelagem das entidades que compõe um sistema seja feita de forma adequada, por profissionais que não são especialistas, "que se propõe a situar uma sequência de atividades em uma ordem que possa resultar em ganhos de produtividade e confiabilidade" (Machado, 2004, p.26), de forma mais específica, trataremos da técnica de Modelagem Conceitual de Dados neste documento.

A Modelagem Conceitual de Dados preve a estruturação em três níveis:

- Projeto Conceitual
- Projeto Lógico
- Projeto Físico


Para essa modelagem, optaremos por abordar as dois primeiros níveis **Projeto Conceitual** e **Projeto Lógico** em um banco de dados relacional.

Traremos:

1. ME-R (Modelo entidade e relacionamento)<br>
   Objetivo: Descrever os objetos do mundo real através de entidades, com suas propriedades que são os atributos e os seus relacionamentos.

2. DE-R (Diagrama Entidade-Relacionamento)<br>
   Objetivo: Representar em forma gráfica o que foi descrito no MER (Modelo Entidade Relacionamento).

3. DLD (Diagrama Lógico de Dados)<br>
   Objetivo: Representar a configuração lógica da totalidade ou de parte da base de dados relacional.

## 2. Modelo entidade e relacionamento (ME-R)

### 2.1 Entidades

**PERSON** (name, email, <u>cpf</u>, phone, password)<br>
-   **USER** (<u>idUser</u>)<br>
-   **PROVIDER** (<u>idProvider</u>, {occupation})<br>
**COMPANY** (<u>idCompany</u>, name, email, {phone})<br>
**SCHEDULE** (<u>idSchedule</u>, dayOfWeek, entryTime, endOfWork)<br>
**SERVICE** (<u>idService</u>, datePurchase, dateService, serviceDescription)<br>
**ADDRESS** (<u>idAddress</u>, state, city, cep, number, district, complement)<br>
**EVALUATION** (<u>idEvalutation</u>, comment, grade)<br>
**SERVICE_CATEGORY** (<u>idCategory</u>, nameService)<br>

### 2.2 Relacionamentos

**PROVIDER** -> works -> **COMPANY**

Um **PROVIDER** pode trabalhar para apenas uma **COMPANY**, porém uma **COMPANY** pode ter vários **PROVIDER**

Cardinalidade -> **n:1**

<hr>

**USER** -> has -> **ADDRESS**

Um **USER** pode ter mais de um **ADDRESS**, da mesma forma que um **ADDRESS** pode ser de mais de um **USER**

Cardinalidade -> **n:m**

<hr>

**USER** -> hires -> **SERVICE**

Um **USER** pode contratar vários **SERVICE**, porém um **SERVICE** pode ser contratado por apenas um **USER**

Cardinalidade -> **1:n**

<hr>

**COMPANY** -> has -> **ADDRESS**

Uma **COMPANY** pode ter mais de um **ADDRESS**, da mesma forma que um **ADDRESS** pode ser de mais de uma **COMPANY**

Cardinalidade -> **n:m**

<hr>

**COMPANY** -> offers -> **SERVICE**

Uma **COMPANY** pode oferecer vários **SERVICE**, assim como um **SERVICE** pode ser oferecido por muitas **COMPANY**

Cardinalidade -> **n:m**

<hr>

**SERVICE** -> has -> **SERVICE_CATEGORY**

Um **SERVICE** possui uma **SERVICE_CATEGORY** e uma **SERVICE_CATEGORY** pode pertencer a vários **SERVICE**

Cardinalidade -> **n:1**

<hr>

**SERVICE** -> has -> **EVALUTATION**

Um **SERVICE** possui uma **EVALUTATION** e uma **EVALUTATION** pertence a um **SERVICE**

Cardinalidade -> **1:1**

<hr>

**PROVIDER** -> has -> **SCHEDULE**

Um **PROVIDER** pode possuir várias **SCHEDULE** e uma **SCHEDULE** pertence a um **PROVIDER**

Cardinalidade -> **1:n**
<hr>

### 2.3. Especializações
#### 2.3.1. Exclusiva

**USER** -> is -> **PERSON**

Um **USER** é uma **PERSON**.

<hr>

**PROVIDER** -> is -> **PERSON**

Um **PROVIDER** é uma **PERSON**.

<hr>

## 3. Diagrama entidade e relacionamento (DE-R)

### Versão 1
<p align='center'>
    <img src='assets/images/modelagemBanco/V1-MER.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 1: Diagrama de entidade relacionamento</b>
        <br>
    </figcaption>
</p>

### Versão 2
<p align='center'>
    <img src='assets/images/modelagemBanco/v2-DERR.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 1: Diagrama de entidade relacionamento</b>
        <br>
    </figcaption>
</p>

## 4. Diagrama lógico

### Versão 1
<p align='center'>
    <img src='assets/images/modelagemBanco/V1-DE-LOGICO.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 2: Diagrama lógico</b>
        <br>
    </figcaption>
</p>


### Versão 2
<p align='center'>
    <img src='assets/images/modelagemBanco/v2-DLDR.png' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 2: Diagrama lógico</b>
        <br>
    </figcaption>
</p>

## 3. Referências

> DEVMEDIA. Modelagem de Dados Tutorial. Disponível em: https://www.devmedia.com.br/modelagem-de-dados-tutorial/20398. Acesso em: 14 jan. de 2022.

> CURUMIN. Modelo entidade relacionamento. Disponível em: https://unbarqdsw2021-1.github.io/2021.1_G6_Curumim/modelagem/modelagem-estatica/MER/. Acesso em: 14 jan. de 2022

> MACHADO, F. N. R; BANCO DE DADOS: PROJETO E IMPLEMENTAÇÃO. 11. ed. 2004. p. 25-26

</div>

### Histórico de versão

| Versão | Data       | Modificação                        | Autor(es)                       |
| :----: | ---------- | ---------------------------------- | ------------------------------- |
|  0.1   | 14/01/2022 | Criação do documento               | Luís Fernando Furtado de Araújo |
|  0.2   | 14/01/2022 | Criação da introdução e subtópicos | Luís Fernando Furtado de Araújo |
|  0.3   | 14/01/2022 | Criação do ME-R                    | Luís Fernando Furtado de Araújo |
|  0.4   | 14/01/2022 | Adição do Diagrama Lógico          | Luís Fernando Furtado de Araújo |
|  1.0   | 14/01/2022 | Adição do DE-R e revisões          | Luís Fernando Furtado de Araújo |
|  1.1   | 14/01/2022 | Revisão do documento               | João Victor                     |
|  1.2   | 21/02/2022 | Correções do documento             | Guilherme Braz                  |
|  2.0   | 15/03/2022 | Adição da nova versão do documento | Fernando, Lorrayne e Ariel      |
|  2.1   | 17/03/2022 | Melhorias pós revisão 	     	   | Fernando e Lorrayne             |
|  2.2   | 17/03/2022 | Revisão versão 2 documento 	       | Pedro Campos, Guilherme Braz    |
|  2.3   | 20/03/2022 | Corrigindo especialização     	   | Fernando e Lorrayne             |