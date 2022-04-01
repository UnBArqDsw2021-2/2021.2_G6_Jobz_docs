# <center> Documento de Arquitetura

<div align="justify">

## 2. Representação Arquitetural

### 2.1. FrontEnd

O **ReactJS** é uma biblioteca da linguagem JavaScript que utiliza certos padrões de design baseados em Components. A aplicação React começa com um único componente raiz, que é construído usando um ou mais componentes, e cada um desses componentes pode ser aninhado com outro componente em qualquer nível.

### 2.2. BackEnd


### 2.3. Banco de Dados
O **PostgreSQL** é um Sistema Gerenciador de Banco de Dados (SGBD) Relacional, utilizado para armazenar informações de soluções de informática em todas as áreas de negócios existentes (Milani, André. PostgreSQL: Guia do Programador. Novatec. 2008).



## 3. Metas e Restrições Arquiteturais

### 3.1. Metas

#### 3.1.2 Portabilidade
A aplicação deve ser compatível e ser possível a execução com desempenho satisfatório nos navegadores mais utilizados e que possuem atualizacoes recentes.

#### 3.1.1 Escalabilidade
A aplicação deve ser estruturada com o objetivo de ser escalável o suficiente para ser possível futuras evoluções com o crescimento do projeto.

#### 3.1.2 Segurança

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

## 4.Visão de dados

### 4.1. Diagrama Entidade-Relacionamento (DE-R)
<p align='center'>
    <img src='assets/images/modelagemBanco/v2-DERR.jpg' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 1: Diagrama de entidade relacionamento</b>
        <br>
    </figcaption>
</p>

### 4.2. Diagrama Logico de Dados (DLD)

<p align='center'>
    <img src='assets/images/modelagemBanco/v2-DLDR.jpg' width=auto height=auto>
    <figcaption align='center'>
        <b>Figura 2: Diagrama lógico</b>
        <br>
    </figcaption>
</p>

### 4.3. Dicionário de dados

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

## 5. Referências

> ReactJS - Architecture. Disponível em: <https://www.tutorialspoint.com/reactjs/reactjs_architecture.htm#:~:text=Architecture%20of%20the%20React%20Application&text=Developers%20are%20free%20to%20choose,.%2C%20to%20write%20better%20code.>. Acesso em: 27 Mar. 2022.

>  Milani, André. PostgreSQL: guia do programador. São Paulo. Novatec, 2008. Disponível em: https://books.google.com.br/books?hl=pt-BR&lr=&id=eb7fXbM70F4C&oi=fnd&pg=PA19&dq=postgresql&ots=FWcgYx_Oo1&sig=8Qv1Kfrdfj9Bzqz7ywREjIgBYZM#v=onepage&q=postgresql&f=false Acesso em: 27/03/2022.‌

</div>

### Histórico de versão

|    Data    | Versão |          Autor(es)               |                Descrição                        |
| :--------: | :----: | :------------------------------: | :---------------------------------------------: |
| 27/03/2022 |  0.1   | Lorrayne Cardozo e Ariel Serafim | Criação do tópico de representação arquitetural. |
| 28/03/2022 |  0.2    | Pedro Campos e Luis Araujo       | Criação do tópico Metas e Restrições Arquiteturais.|
| 28/03/2022 |  0.3    | Pedro Campos e Luis Araujo       | Criação do tópico Visão de dados. |
| 28/03/2022 |  0.4    | Luis Araujo e Pedro Campos      | Criação dos subtópicos de Metas arquiteturais |