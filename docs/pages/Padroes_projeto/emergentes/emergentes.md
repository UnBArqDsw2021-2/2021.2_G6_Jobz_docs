# <center> TEMPLATE

<div align="justify">

## 1. Padrão de Component

Amplamente utilizado na biblioteca React de desenvolvimento de interfaces de usuário, este padrão de projeto tem como o objetivo separar os componentes que serão utilizados em duas categorias  container e de apresentação:

* **Componentes de Apresentação**: Componentes que têm preocupação com a aparência das coisas, não têm dependências do resto da aplicação e vão receber seus dados exclusivamente através do retorno de uma entrada arbitrária. Ex: Sidebar e UserInfo
* **Componentes Container**: maior preocupação em como as coisas funcionam, vem para ditar o funcionamento de outros componentes(containers ou de apresentação) e tendem a ter estados e serem utilizados como fontes de dados. Ex: UserPage e FollowedUserList.

Vantagens da utilização do padrão:
Com a utilização desse padrão é possível obter uma melhor separação de interesses, podendo entender melhor sua interface de usuário.
Uma das principais características do uso desse padrão é o potencial de reutilização que se pode obter, podendo utilizar os componentes criados em vários ambientes distintos.

## 2. Aplicações em código

Na [figura 1](./pages/Padroes_projeto/emergentes/emergentes?id=figura1) que foi retirada do [repotisório de frontend](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_FrontEnd/blob/Issue%2372_FrontEnd_CadastroDisponibilidade/src/components/Navbar/navbar.js) da aplicação, podemos ver um exemplo de container, que se preocupa com o funcionamento da pagina.

<a id="figura1"></a>

<p align='center'>
    <img src='assets/images/emergentes/container.png' width=70% height=auto>
    <figcaption align='center'>
        <b>Figura 1: Trecho de código demonstrando um component container</b>
        <br>
    </figcaption>
</p>


Agora a [figura 2](./pages/Padroes_projeto/emergentes/emergentes?id=figura2) que também foi retirada do [repotisório de frontend](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_FrontEnd/blob/Issue%2372_FrontEnd_CadastroDisponibilidade/src/components/Button/index.js) da aplicação, podemos ver o exemplo de um component de apresentação, que se preocupa com a apresentação visual do componente.

<a id="figura2"></a>
<p align='center'>
    <img src='assets/images/emergentes/component.png' width=70% height=auto>
    <figcaption align='center'>
        <b>Figura 2: Trecho de código demonstrando um component de apresentação</b>
        <br>
    </figcaption>
</p>

## 3. Referências

> OPENREPLAY. 3 React component Design Patterns you should know about. Disponível em: https://blog.openreplay.com/3-react-component-design-patterns-you-should-know-about. Acesso em: 17/03/2022.

> MEDIUM. Presentational and Container Components. Disponível em: https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0. Acesso em: 17/03/2022


> LOGROCKET. React component design patterns for 2022. Disponível em: https://blog.logrocket.com/react-component-design-patterns-2022/. Acesso em: 19/03/2022.
</div>

### Histórico de versão

|    Data    | Versão |    Autor    |      Descrição       |
| :--------: | :----: | :---------: | :------------------: |
| 20/03/2022 |  1.0   | Fernando e pedro | Construção do documento |