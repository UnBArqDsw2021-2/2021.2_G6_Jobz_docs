# <center> Modelagem banco de dados

<div align="justify">

## 1. Introdução

O processo de modelagem de banco de dados é um processo de desenvolvimento de software que visa a construção de um modelo de dados que represente a estrutura de dados de uma base de dados, nesse processo se usa de coletas, analises, categorização e a explorarão dos dados e seus tipos.

O documento em questão tem como objetivo documentar e apresentar a modelagem do banco de dados previamente definida e ir evoluindo de acordo com a evolução do software.

Para essa modelagem, optaremos por utilizar um banco de dados relacional.

Traremos:

1. ME-R (Modelo entidade e relacionamento)<br>
   Objetivo: Descrever os objetos do mundo real através de entidades, com suas propriedades que são os atributos e os seus relacionamentos.

2. DE-R (Diagrama Entidade-Relacionamento)<br>
   Objetivo: Representar em forma gráfica o que foi descrito no MER (Modelo Entidade Relacionamento).

3. DE (Diagrama de esquemas)<br>
   Objetivo: Representar a configuração lógica da totalidade ou de parte da base de dados relacional.

## 2. Modelo entidade e relacionamento (ME-R)

### 2.1 Entidades

**PERSON** (name, email, <u>cpf</u>, phone)<br>
-   **USER** (<u>idUser</u>)<br>
-   **PROVIDER** (<u>idProvider</u>, {occupation})<br>
**COMPANY** (<u>idCompany</u>, name, email, {phone})<br>
**SCHEDULE** (<u>idSchedule</u>, dayOfWeek, entryTime, endOfWork)<br>
**SERVICE** (<u>idService</u>, datePurchase, dateService, serviceDescription)<br>
**ADDRESS** (<u>idAddress</u>, state, city, cep, number, district, complement)<br>
**EVALUATION** (<u>idEvalutation</u>, comment, grade)<br>
**SERVICE_CATEGORY** (<u>idCategory</u>, nameService)<br>

### 2.2 Relacionamentos

**USER** -> is -> **PERSON**

Um **USER** é uma **PERSON**.

Cardinalidade -> **1:1**

<hr>

**PROVIDER** -> is -> **PERSON**

Um **PROVIDER** é uma **PERSON**.

Cardinalidade -> **1:1**

<hr>

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
