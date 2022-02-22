# </center> Diagrama de Atividades

<div align="justify">

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
|<img src='assets/images/diagramaAtividades/fim.png' width=100px height=auto>         | É chamado de nó final e representa o fim de um fluxo no diagrama de atividades.                                                     |

A partir da implementação do diagrama de atividades, podemos descrever as etapas que ocorrem quando um determinado cenário é iniciado, até que este cenário seja encerrado, ajudando a compreensão do processo que será executado, para que os envolvidos na produção do software possam identificar as necessidades do sistema com maior precisão.
A partir do exposto acima, esperamos atingir com o uso desse diagrama, uma maior compreensão dos fluxos de atividades no nosso projeto, isso é, detalhar os processos necessários para a correta execução do nosso produto. Temos então o detalhamento dos fluxos de login, perfil do cliente e perfil do prestador de serviço.


## 2. Diagramas
### 2.1. Login

<p align='center'>
    <img src='assets/images/diagramaAtividades/diagramaLogin.png' width=40% height=auto>
    <figcaption align='center'>
        <b>Figura 01 - Diagrama de Atividades representando o login. </b>
        <br>
    </figcaption>
</p>

### 2.2. Perfil Cliente

<p align='center'>
    <img src='assets/images/diagramaAtividades/diagramaCliente.png' width=40% height=auto>
    <figcaption align='center'>
        <b>Figura 02 - Diagrama de Atividades representando o perfil de cliente.</b>
        <br>
    </figcaption>
</p>

### 2.4. Perfil Prestador de Serviço

<p align='center'>
    <img src='assets/images/diagramaAtividades/diagramaPrestador.png' width=40% height=auto>
    <figcaption align='center'>
        <b>Figura 03 - Diagrama de Atividades representando o perfil de prestador de serviço.</b>
        <br>
    </figcaption>
</p>

</p>

## 3. Referências
> Diagrama de Atividades. Disponível em: https://homepages.dcc.ufmg.br/~amendes/GlossarioUML/glossario/conteudo/atividades/diagrama_de_atividades.htm. Acesso em 14 de fevereiro de 2022.

> Diagrama de Atividades. Disponível em: http://www.dsc.ufcg.edu.br/~jacques/cursos/map/html/uml/diagramas/atividades/diag_atividades.htm. Acesso em 14 de fevereiro de 2022.

> Diagramas de Atividades. Disponível em: https://www.ibm.com/docs/pt-br/rsm/7.5.0?topic=diagrams-activity. Acesso em 19 de fevereiro de 2022.

### Histórico de versão

|    Data    | Versão |    Autor         |          Descrição                      |
| :--------: | :----: | :--------------: | :------------------------------------:  |
| 13/02/2022 |  1.0   | Lorrayne Cardozo |   Criação do documento de personas      |
| 19/02/2022 |  1.1   | Fernando Miranda | Revisão e padronização do documento     |
| 20/02/2022 |  1.1   | Ariel Serafim    | Adição do impacto da tecnica no projeto |