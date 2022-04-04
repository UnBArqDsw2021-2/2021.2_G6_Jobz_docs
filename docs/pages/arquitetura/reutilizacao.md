# <center> Reutilização de Software

<div align="justify">

## 1. Introdução
Segundo o [Perforce](https://www.perforce.com/blog/qac/what-code-reuse-code-reuse-best-practices), a reutilização de código é a prática de usar um código existente para uma nova função ou software. Porém, em seu desenvolvimento devem ser levados em consideração diversos fatores que garantam que o código tenha uma alta qualidade e possa ser reutilizado, por isso deve ser seguro, protegido e confiável. A ideia do reuso é evitar retrabalho no desenvolvimento de um novo projeto, levando em consideração trabalhos feitos anteriormente.

O desenvolvimento de um software é um processo que demanda bastante tempo e esforço, e a prática de reutilização de código é utilizada para otimizar esse processo, fazendo com que soluções previamente desenvolvidas sejam aproveitadas e implementadas em um novo contexto.

## 2. Aplicações

### 2.1 Reutilização no BackEnd
O **Django** é utilizado para construção de aplicações web utilizando o padrão *model-template-view* (MTV) que mantém o código bem organizado em suas devidas camadas, e já oferece os padrões de projeto Alta Coesão e Baixo Acoplamento, organizando os métodos de forma bem definida e com suas respectivas responsabilidades. Desta forma, isso aumenta a qualidade do código e facilita sua reutilização. Além disso, sua principal convenção é o *Don't Repeat Yourself* (DRY), que em tradução livre significa *Não Seja Repetitivo*, visando aproveitar ao máximo o código criado, evitando duplicação e auxiliando em sua reutilização.

Já o **Django Rest Framework** é uma poderosa ferramenta para construção de API's, além de possuir um sistema de autenticação e serialização de dados. É de fácil reuso, pois os serviços fornecidos podem ser facilmente consumidos tanto por interfaces web quanto mobile.

Na imagem abaixo conseguimos visualizar como é organizada a estrutura do backend utilizando o framework:

<p align='center'>
    <img src='assets/images/reutilizacao/django.png' width=25% height=auto>
    <figcaption align='center'>
        <b>Figura 1: Estrutura do BackEnd utilizando o framework Django.</b>
        <br>
    </figcaption>
</p>


### 2.2 Reutilização no FrontEnd

#### 2.2.1 Component

Para o desenvolvimento da parte de frontend da aplicação, o grupo optou pela adoção da biblioteca [React](https://reactjs.org/), a partir disso podemos apontar a presença do padrão [Component](./pages/Padroes_projeto/emergentes/emergentes.md#padrão-de-component) como reutilização de código na aplicação, já que a utilização do padrão visa dividir o código em componentes que podem ser reutilizados.

A seguir temos um exemplo de [código](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_FrontEnd/blob/Issue%2372_FrontEnd_CadastroDisponibilidade/src/components/Button/index.js) que utiliza o padrão [Component](./pages/Padroes_projeto/emergentes/emergentes.md#padrão-de-component), que foi retirado do [repositório de frontend](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_FrontEnd) da aplicação, onde podemos observar o exemplo de um botão que será reutilizado em várias partes do desenvolvimento das páginas da aplicação.

<p align='center'>
    <img src='assets/images/emergentes/component.png' width=70% height=auto>
    <figcaption align='center'>
        <b>Figura 2: Trecho de código demonstrando um componente que é reaproveitado.</b>
        <br>
    </figcaption>
</p>

#### 2.2.2 Axios

Além da biblioteca [React](https://reactjs.org/), também podemos apontar a utilização da biblioteca [Axios](https://axios-http.com/ptbr/docs/intro), cujo objetivo é criar configurações reutilizáveis para as conexões necessárias na aplicação.

Visando criar configurações para as conexões HTTP necessárias, a biblioteca [Axios](https://axios-http.com/ptbr/docs/intro) foi adotada no nosso desenvolvimento de frontend. No [trecho de código](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_FrontEnd/blob/master/src/views/collaboratorRegistrationPage/index.js), podemos ver um exemplo de utilização da biblioteca na nossa aplicação.

<p align='center'>
    <img src='assets/images/reutilizacao/axios.png' width=70% height=auto>
    <figcaption align='center'>
        <b>Figura 3: Trecho de código demonstrando a utilização da biblioteca Axios.</b>
        <br>
    </figcaption>
</p>


### 2.3 Reutilização no Docker

Com a intenção de isolar os ambientes criados para a aplicação, a equipe decidiu se utilizar da ferramenta [Docker](https://www.docker.com/), que possibilita o empacotamento da aplicação ou ambiente dentro de um container, facilitando o acesso para qualquer outro usuário.

Para o desenvolvimento do [Dockerfile do backend](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_BackEnd/blob/master/Dockerfile) e do [Dockerfile do frontend](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_FrontEnd/blob/master/Dockerfile) reutilizamos imagens já disponibilizadas no [Docker Hub](https://hub.docker.com/), o docker Hub é o maior repositório de imagens de container do mundo com uma variedade de fontes de conteúdo, incluindo desenvolvedores da comunidade de container, projetos de código aberto e fornecedores independentes de software (ISV) construindo e distribuindo seu código em container.

Na elaboração do projeto foram usadas as imagens do [python](https://hub.docker.com/_/python) e [node](https://hub.docker.com/_/node) para o backend e frontend, respectivamente.
Nas figuras abaixo apresentamos como é a utilização no projeto:


<p align='center'>
    <img src='assets/images/reutilizacao/dockerNode.png' width=70% height=auto>
    <figcaption align='center'>
        <b>Figura 4: Código demonstrando da utilização da imagem do node</b>
        <br>
    </figcaption>
</p>


<p align='center'>
    <img src='assets/images/reutilizacao/dockerPython.png' width=70% height=auto>
    <figcaption align='center'>
        <b>Figura 5: Código demonstrando da utilização da imagem do python</b>
        <br>
    </figcaption>
</p>

#### 2.3.2 Docker compose

Além do reaproveitamento de imagem dentro do **Dockerfile**, acontece também dentro do [docker-compose](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_BackEnd/blob/master/docker-compose.yml) para a construção do container do banco de dados, que utiliza a imagem do [postgres](https://hub.docker.com/_/postgres), como pode ser visto no trecho de código apresentado abaixo.


<p align='center'>
    <img src='assets/images/reutilizacao/dockerPostgres.png' width=70% height=auto>
    <figcaption align='center'>
        <b>Figura 6: Trecho de código demonstrando da utilização da imagem do postgres</b>
        <br>
    </figcaption>
</p>




## 3. Referências

> REACT. React. Disponível em: https://pt-br.reactjs.org/. Acesso em: 26 de mar. de 2022.

> AXIOS. Introdução. Disponível em: https://axios-http.com/ptbr/docs/intro. Acesso em: 26 de mar. de 2022.

> DOCKER HUB. Docker.  Disponível em: https://www.docker.com/products/docker-hub/. Acesso em: 26 de mar. de 2022.

> DOCKER. Docker. Disponível em: https://www.docker.com/. Acesso em: 26 de mar. de 2022.

> ALURA. Django e Django Rest: Diferenças e aplicações. Alura. Disponível em: <https://www.alura.com.br/artigos/django-django-rest-diferencas>. Acesso em: 27 Mar. 2022.

> DEVMEDIA. Reutilização de Software: Técnicas e Ferramentas. DevMedia. Disponível em: <
https://www.devmedia.com.br/reutilizacao-de-software-revista-engenharia-de-software-magazine-39/21956>. Acesso em: 27 Mar. 2022.

> BELLAIRS, Richard. What Is Code Reuse? Code Reuse Best Practices. Perforce Software. Disponível em: <https://www.perforce.com/blog/qac/what-code-reuse-code-reuse-best-practices>. Acesso em: 27 Mar. 2022.

> Design Patterns: Elements of Reusable Object-Oriented Software. Disponível em: <
https://www.amazon.com/gp/product/0201633612/ref=as_li_tl?ie=UTF8&camp=1789&creative=390957&creativeASIN=0201633612&linkCode=as2&tag=triatcraft-20&linkId=XRGUDJCGWC6AJNZM. Acesso em: 31 Mar. 2022.
</div>

### Histórico de versão

|    Data    | Versão |                     Autor                     |        Descrição         |
| :--------: | :----: | :-------------------------------------------: | :----------------------: |
| 26/03/2022 |  0.1   |              Fernando e Antonio               | Reutilização no FrontEnd |
| 26/03/2022 | 0.1.1  |              Fernando e Antonio               |    Correção de links     |
| 26/03/2022 |  0.2   | Fernando e Antonio | Correção de links        |
| 26/03/2022 |  0.3   | Fernando e Antonio | Reutilização no Docker   |
| 26/03/2022 |  0.3.1  | Fernando e Antonio | Correções no Documento   |
| 31/03/2022 |  0.4   | Rodrigo Balbino, Guilherme Braz e João Victor |    Revisão do tópico Reutilização no Frontend      |
| 31/03/2022 |  0.4.1   | João Victor, Álvaro e Luis Fernando |    Revisão do tópico Reutilização no Docker      |
| 03/04/2022 |  0.5   | Lorrayne Cardozo e Ariel Serafim | Adição do tópico do Backend |
| 04/04/2022| 0.5.1   | Pedro, Guilherme, Fernando e João | Revisão tópico Reutilização Backend|