# <center> Metodologia do Projeto

<div align="justify">

## 1. Introdução

Este documento tem como objetivo definir as abordagens, metodologias e processos utilizados durante o desenvolvimento do projeto. Aqui estão descritas as metodologias usadas como referencias e quais artefatos foram selecionados destas.

## 2. Metodologias

### 2.1 SCRUM

O Scrum é um framework de gerenciamento de projetos, da etapa da organização ao desenvolvimento ágil de produtos complexos e adaptativos buscando o valor máximo, utilizado desde 1990, atualmente é utilizado em mais de 60% dos projetos ágeis em todo o mundo. [[1]](https://pt.wikipedia.org/wiki/Scrum)

Dentro dessa metodologia existe diversas atividades que ocorrem durante o processo de desenvolvimento, e as seguintes foram selecionadas de acordo com nosso contexto: Product Backlog, Sprints, Sprint Planning, Sprint Review.

O product Backlog é uma lista com as funcionalidades a serem implementadas em um projeto. Para nosso contxto iremos utilizar as [issues criadas no nosso repositorio](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_docs/issues) como lista de funcionalidades.

No Scrum, os projetos são dividos em ciclos (de uma semana a um mês) chamados de Sprints. O Sprint representa um Time Box dentro do qual um conjunto de atividades deve ser executado. No nosso projeto foi defino uma duração de 5 a 7 dias para as sprints.

No início de cada Sprint, faz-se uma Sprint Planning Meeting, ou seja, uma reunião de planejamento e a equipe seleciona as atividades que ela será capaz de implementar durante a Sprint que se inicia. As tarefas alocadas em uma Sprint são transferidas do Product Backlog para o Sprint Backlog. Essa reunião ficou definida para acontecer a cada segunda-feira às 18h.

Ao final de uma Sprint, a equipe apresenta as funcionalidades implementadas em uma Sprint Review Meeting, que é uma reunião para a verificação e validação das entregas da sprint anterior.

### 2.2 XP

O XP é um método de desenvolvimento de software, leve, não é prescritivo, e procura fundamentar as suas práticas por um conjunto de valores que são: comunicação, simplicidade, feedback e coragem. O objetivo principal do XP é levar ao extremo um conjunto de práticas que são ditas como boas na engenharia de software.

Para um melhor proveito dessa metodologia, uma adaptação será feita para nosso contexto. Com isso foi definido que todas as tarefas do projeto serão planejadas para serem pequenas entregas, para que uma pessoa consiga entregar dentro do prazo definido. A programação em pares será utilizada para que buscar uma integração melhor entre a equipe e criar um sentimento de posse sobre os artefatos produzidos.

## 2.3. Kanban

O Kanban é uma uma forma de fazer a gestão dos fluxos de desenvolvimento de um projeto, com foco no aumento de produtividade. É um sistema visual de gestão de trabalho que busca conduzir cada tarefa por um fluxo predefinido de trabalho.

Para a aplicação do Kanban, será utilizado o plugin Zenhub, onde as tarefas serão dispostas em cards que correspondem as issues do GitHub.

As pipelines padrões de um Kanban são: `To do`,`Doing`,`Done`. Para nosso contexto serão utilizados as seguintes pipelines:

-   Product Backlog: Todas as tarefas à serem realizadas
-   Sprint Backlog: Tarefas que devem ser realizadas na Sprint atual
-   In Progress: Tarefas em andamento
-   Review/QA: Tarefas aguardando revisão
-   Closed: Tarefas finalizadas

### Referências

> Scrum. Disponível em https://pt.wikipedia.org/wiki/Scrum
> Introdução ao Extreme Programming (XP). Disponível em https://www.devmedia.com.br/introducao-ao-extreme-programming-xp/29249

</div>

### Histórico de versão

|    Data    | Versão | Autor (es)  |      Descrição       |
| :--------: | :----: | :---------: | :------------------: |
| 28/01/2022 |  1.0   | João Victor | Criação do documento |
