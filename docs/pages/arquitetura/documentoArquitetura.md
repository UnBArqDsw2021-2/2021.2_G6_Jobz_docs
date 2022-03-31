# <center> Documento de Arquitetura

<div align="justify">

## 2. Representação Arquitetural

### 2.1. Tecnologias
Para o desenvolvimento da aplicação Jobz foi utilizado um conjunto de ferramentas, sendo elas o framework de desenvolvimento de API's web `Django Rest Framework` e a biblioteca `ReactJS` para a camada de visualização, além do sistema gerenciador de banco de dados relacional `PostgreSQL` e a virtualização do ambiente com  `Docker`.

#### 2.1.1. FrontEnd

O **ReactJS** é uma biblioteca da linguagem JavaScript que utiliza certos padrões de design baseados em Components. A aplicação React começa com um único componente raiz, que é construído usando um ou mais componentes, e cada um desses componentes pode ser aninhado com outro componente em qualquer nível. O framework foi escolhido porque alguns integrantes já possuíam experiência e a equipe julgou como uma boa opção para o projeto.

#### 2.1.2. BackEnd
Tanto o **Django** quanto o **Django Rest Framework** são escritos em [Python](https://www.python.org/), porém possuem finalidades diferentes.

O **Django** tem o propósito focado no desenvolvimento de aplicações web e sites, fazendo uso do *Don't Repeat Yourself* (DRY), que em tradução livre significa *Não Seja Repetitivo*, aproveitando ao máximo o código criado facilitando a reutilização. Além disso, utiliza o padrão *model-template-view* (MTV), onde a aplicação é dividida em camadas, tornando o código mais organizado.

O **Django Rest Framework** tem como objetivo o desenvolvimento de API's de forma simples e ágil, gerando uma API navegável que facilita na usabilidade para os desenvolvedores, além de possuir sistema de autenticação e serialização de dados.

O framework foi escolhido porque alguns integrantes já possuíam experiência, se disponibilizando para fornecer ajuda aos demais, além de que a ferramenta oferece um rápido desenvolvimento.

#### 2.1.3. Banco de Dados
O **PostgreSQL** é um Sistema Gerenciador de Banco de Dados (SGBD) Relacional, utilizado para armazenar informações de soluções de informática em todas as áreas de negócios existentes (Milani, André. PostgreSQL: Guia do Programador. Novatec. 2008). É um dos cinco SGDB's relacionais mais utilizados do mercado, e foi escolhido por ser um sistema open-source de fácil instalação que possui interfaces simples e intuitivas que facilitam o aprendizado, além de ser muito fácil de manter devido a sua estabilidade.

#### 2.1.4. Docker
O **Docker** foi utilizado porque facilita o desenvolvimento em equipe possibilitando a containerização do ambiente de execução, permitindo o compartilhamento de tecnologias e dependências em qualquer host que contenha o Docker instalado.

## 3. Referências

> ReactJS - Architecture. Disponível em: <https://www.tutorialspoint.com/reactjs/reactjs_architecture.htm#:~:text=Architecture%20of%20the%20React%20Application&text=Developers%20are%20free%20to%20choose,.%2C%20to%20write%20better%20code.>. Acesso em: 27 Mar. 2022.

>  Milani, André. PostgreSQL: guia do programador. São Paulo. Novatec, 2008. Disponível em: https://books.google.com.br/books?hl=pt-BR&lr=&id=eb7fXbM70F4C&oi=fnd&pg=PA19&dq=postgresql&ots=FWcgYx_Oo1&sig=8Qv1Kfrdfj9Bzqz7ywREjIgBYZM#v=onepage&q=postgresql&f=false Acesso em: 27/03/2022.‌

> ALURA. Django e Django Rest: Diferenças e aplicações. Alura. Disponível em: <https://www.alura.com.br/artigos/django-django-rest-diferencas>. Acesso em: 31 mar. 2022.


</div>

### Histórico de versão

|    Data    | Versão |          Autor(es)               |                Descrição                        |
| :--------: | :----: | :------------------------------: | :---------------------------------------------: |
| 27/03/2022 |  0.1   | Lorrayne Cardozo e Ariel Serafim | Criação do tópico de representação arquitetural |