# </center> Diagrama de Atividades

## 1. Introdução
O diagrama de atividades é um diagrama comportamental UML que tem como objetivo apresentar o fluxo entre um conjunto de atividades do sistema, demonstrando graficamente como as atividades são dependentes umas das outras. É de extrema importância para esclarecer o fluxo de trabalho entre usuários e o sistema, além de modelar elementos de arquitetura de software.

Para a construção dos diagramas, foram considerados os seguintes símbolos:

|                                Símbolo                                              |                                                                 Descrição                                                               |
|:-----------------------------------------------------------------------------------:|-----------------------------------------------------------------------------------------------------------------------------------------|
|<img src='assets/images/diagramaAtividades/inicio.png' width=100px height=auto>      | É chamado de nó inicial e representa o início de um fluxo ou processo no diagrama de atividades.                                        |
|<img src='assets/images/diagramaAtividades/fluxo.png' width=170px height=auto>       | Representa a direção do fluxo de uma atividade.                                                                                         |
|<img src='assets/images/diagramaAtividades/acao.png' width=170px height=auto>        | Representa uma atividade do fluxo, sendo considerado um dos principais elementos do diagrama de atividades.                             |
|<img src='assets/images/diagramaAtividades/condicao.png' width=300px height=auto>    | Representa uma decisão a ser tomada no fluxo, possui no mínimo duas ramificações de ações sendo que apenas uma será realizada. |
|<img src='assets/images/diagramaAtividades/pontoUniao.png' width=300px height=auto>  | Representa o ponto de união, em que duas ou mais atividades diferentes serão conduzidas ao mesmo destino.                               |
|<img src='assets/images/diagramaAtividades/divisaoFluxo.png' width=170px height=auto>| Representa a divisão de um único fluxo em duas ou mais atividades simultâneas.                                                          |
|<img src='assets/images/diagramaAtividades/juncaoFluxo.png' width=170px height=auto> | Representa a junção de dois ou mais fluxos diferentes, reintroduzindo-os em um único fluxo.                                             |
|<img src='assets/images/diagramaAtividades/fim.png' width=100px height=auto>         | É chamado de nó final e representa o fim de um fluxo no diagrama de atividades.                                                         |

## 2. Diagramas
### 2.1. Login
<center><img width="550px" src="assets/images/diagramaAtividades/diagramaLogin.png">
<figcaption>Figura 01 - Diagrama de Atividades representando o login.<br></figcaption></center>

### 2.2. Perfil Cliente
<center><img width="600px" src="assets/images/diagramaAtividades/diagramaCliente.png">
<figcaption>Figura 02 - Diagrama de Atividades representando o perfil de cliente.<br></figcaption></center>

### 2.4. Perfil Prestador de Serviço
<center><img width="500px" src="assets/images/diagramaAtividades/diagramaPrestador.png">
<figcaption>Figura 03 - Diagrama de Atividades representando o perfil de prestador de serviço.<br></figcaption></center>

## 3. Referências
>Diagrama de Atividades. Disponível em: https://homepages.dcc.ufmg.br/~amendes/GlossarioUML/glossario/conteudo/atividades/diagrama_de_atividades.htm. Acesso em 14 de fevereiro de 2022.

>Diagrama de Atividades. Disponível em: http://www.dsc.ufcg.edu.br/~jacques/cursos/map/html/uml/diagramas/atividades/diag_atividades.htm. Acesso em 14 de fevereiro de 2022.

## 4. Versionamento
|    Data    | Versão |    Autor(es)     |            Descrição             |
| :--------: | :----: | :--------------: | :------------------------------: |
| 13/02/2022 |  1.0   | Lorrayne Cardozo | Criação do documento de personas |