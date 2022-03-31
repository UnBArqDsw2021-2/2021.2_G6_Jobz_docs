# <center> Reutilização de Software

<div align="justify">

## 1. Introdução

## 2. Aplicações

### 2.1 Reutilização no BackEnd

### 2.2 Reutilização no FrontEnd

#### 2.2.1 Component

Para o desenvolvimento da parte de frontend da aplicação, o grupo optou pela adoção da biblioteca [React](https://reactjs.org/), a partir disso podemos apontar a presença do padrão [Component](./pages/Padroes_projeto/emergentes/emergentes.md#padrão-de-component) como reutilização de código na aplicação, já que a utilização do padrão visa dividir o código em componentes que podem ser reutilizados.

A seguir temos um exemplo de [código](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_FrontEnd/blob/Issue%2372_FrontEnd_CadastroDisponibilidade/src/components/Button/index.js) que utiliza o padrão [Component](./pages/Padroes_projeto/emergentes/emergentes.md#padrão-de-component), que foi retirado do [repositório de frontend](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_FrontEnd) da aplicação, onde podemos observar o exemplo de um botão que será reutilizado em várias partes do desenvolvimento das páginas da aplicação.

<p align='center'>
    <img src='assets/images/emergentes/component.png' width=70% height=auto>
    <figcaption align='center'>
        <b>Figura 1: Trecho de código demonstrando um componente que é reaproveitado.</b>
        <br>
    </figcaption>
</p>

#### 2.2.2 Axios

Além da biblioteca [React](https://reactjs.org/), também podemos apontar a utilização da biblioteca [Axios](https://axios-http.com/ptbr/docs/intro), cujo objetivo é criar configurações reutilizáveis para as conexões necessárias na aplicação.

Visando criar configurações para as conexões HTTP necessárias, a biblioteca [Axios](https://axios-http.com/ptbr/docs/intro) foi adotada no nosso desenvolvimento de frontend. No [trecho de código](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_FrontEnd/blob/master/src/views/collaboratorRegistrationPage/index.js), podemos ver um exemplo de utilização da biblioteca na nossa aplicação.

<p align='center'>
    <img src='assets/images/reutilizacao/axios.png' width=70% height=auto>
    <figcaption align='center'>
        <b>Figura 2: Trecho de código demonstrando a utilização da biblioteca Axios.</b>
        <br>
    </figcaption>
</p>


### 2.3 Reutilização no Docker

Com a intenção de isolar os ambientes criados para a aplicação, a equipe decidiu se utilizar da ferramenta [Docker](https://www.docker.com/), que possibilita o empacotamento da aplicação ou ambiente dentro de um container, facilitando o acesso para qualquer outro usuário.

Para o desenvolvimento do [Dockerfile do backend](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_BackEnd/blob/master/Dockerfile) e do [Dockerfile do frontend](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_FrontEnd/blob/master/Dockerfile) reutilizamos imagens já disponibilizadas no [Docker Hub](https://hub.docker.com/), o docker Hub é o maior repositório de imagens de contêiner do mundo com uma variedade de fontes de conteúdo, incluindo desenvolvedores da comunidade de container, projetos de código aberto e fornecedores independentes de software (ISV) construindo e distribuindo seu código em container.

Na elaboração do projeto foram usadas as imagens do [python](https://hub.docker.com/_/python) e [node](https://hub.docker.com/_/node) para o backend e frontend, respectivamente.
Nas figuras abaixo apresentamos com é a utilização no projeto:


<p align='center'>
    <img src='assets/images/reutilizacao/dockerNode.png' width=70% height=auto>
    <figcaption align='center'>
        <b>Figura 3: Código demonstrando da utilização da imagem do node</b>
        <br>
    </figcaption>
</p>


<p align='center'>
    <img src='assets/images/reutilizacao/dockerPython.png' width=70% height=auto>
    <figcaption align='center'>
        <b>Figura 4: Código demonstrando da utilização da imagem do python</b>
        <br>
    </figcaption>
</p>

#### 2.3.2 Docker compose

Além do reaproveitamento de imagem dentro do **Dockerfile** acontece também dentro do [docker-compose](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_BackEnd/blob/master/docker-compose.yml) para a construção do continer do banco de dados, que utiliza a imagem do [postgres](https://hub.docker.com/_/postgres), como pode ser visto no trecho de código apresentado abaixo.


<p align='center'>
    <img src='assets/images/reutilizacao/dockerPostgres.png' width=70% height=auto>
    <figcaption align='center'>
        <b>Figura 5: Trecho de código demonstrando da utilização da imagem do postgres</b>
        <br>
    </figcaption>
</p>




## 3. Referências

> REACT. React. Disponível em: https://pt-br.reactjs.org/. Acesso em: 26 de mar. de 2022.

> AXIOS. Introdução. Disponível em: https://axios-http.com/ptbr/docs/intro. Acesso em: 26 de mar. de 2022.

> DOCKER HUB. Docker.  Disponível em: https://www.docker.com/products/docker-hub/. Acesso em: 26 de mar. de 2022.

> DOCKER. Docker. Disponível em: https://www.docker.com/. Acesso em: 26 de mar. de 2022.
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
