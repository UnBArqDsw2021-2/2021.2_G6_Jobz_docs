# <center> Modelagem banco de dados

## 1. Introdução

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

### Entidades

**USER** (<u>id</u>, name, email, cpf, password, profileType, {phone})<br>
**ADDRESS** (<u>id</u>, addressType, number, street, neighborhood, complement, city, state, zipcode)<br>
**COMPANY** (<u>id</u>, name, cnpj, {phone})<br>
**SERVICE** (<u>id</u>, title, description, {photo})<br>
**CATEGORY_SERVICE** (<u>id</u>, name)<br>
**CLIENT_EVALUATION** (<u>id</u>, note, comment)<br>

### Relacionamentos



## 2. Versionamento

| Versão | Data       | Modificação          | Autor(es)           |
| :----: | ---------- | -------------------- | --------------- |
|  0.1   | 14/01/2022 | Criação do documento | Luís Fernando Furtado de Araújo |