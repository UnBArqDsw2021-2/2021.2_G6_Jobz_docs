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
    <img src='assets/images/reutilizaçãoSoftware/axios.png' width=70% height=auto>
    <figcaption align='center'>
        <b>Figura 2: Trecho de código demonstrando a utilização da biblioteca Axios.</b>
        <br>
    </figcaption>
</p>


### 2.3 Reutilização no Docker



## 3. Referências

> REACT. React. Disponível em: https://pt-br.reactjs.org/. Acesso em: 26 de mar. de 2022.

> AXIOS. Introdução. Disponível em: https://axios-http.com/ptbr/docs/intro. Acesso em: 26 de mar. de 2022.
</div>

### Histórico de versão

|    Data    | Versão |    Autor           |        Descrição         |
| :--------: | :----: | :----------------: | :----------------------: |
| 26/03/2022 |  0.1   | Fernando e Antonio | Reutilização no FrontEnd |
| 26/03/2022 |  0.1.1   | Fernando e Antonio | Correção de links        |