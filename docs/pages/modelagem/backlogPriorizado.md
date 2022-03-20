# <center> Backlog do Produto

<div align="justify">

## 1. Introdução

O Backlog do Produto, ou Backlog, foi introduzido pela primeira vez pelo método ágil Scrum é um artefato utilizado em projetos ágeis, artefato este que consiste em uma lista de pedidos ou requisições do cliente sobre quais comportamentos e funcionalidades o sistema deve possuir para este ser considerado como um produto finalizado. Um backlog pode ser implementado com diferentes níveis de detalhes, entre implementações diferentes, os principais pontos componentes de um backlog são:

- Tema(Theme);
- Épicos(Epics);
- Funcionalidades(Features);
- Histórias de usuário(User Stories);
- Tarefas(Tasks);

O **Tema** em um backlog do produto é o componente que possui a granularidade mais alta em um backlog, tratando de uma relação direta entre o backlog e o objetivo do projeto, pode-se dizer que o tema descreve a visão do produto, representando os princípios que agregam valor da aplicação.

**Épicos** são formados por um conjunto de funcionalidades, os épicos são representações expressadas em alto nível, ou mais próxima das necessidades reais, de um grupo de funcionalidades que o cliente precisa que o software execute. Os Épicos também podem ser descritos como histórias de usuário que são grandes demais para serem implementadas em um único ciclo de desenvolvimento Mike Cohn(2010), que deverão ser subdivididas em histórias até estas poderem ser implementadas em um único ciclo.

**Funcionalidades** - Enquanto os épicos tratam de um nível superior das necessidades do cliente com um produto de software, as funcionalidades são especificações de processos que se decompõem em histórias de usuário e vão descrever melhor quais as responsabilidades do software.

As **Histórias de usuário** são descrições focadas na visão do usuário, em que as funcionalidades serão necessárias, descrições que devem ser entendidas tanto por clientes, quanto pelos desenvolvedores e tem o objetivo de contextualizar o desenvolvimento de uma funcionalidade que o sistema precisa atender.

As **Tarefas** representam o menor nível de granularidade nas descrições de requisitos registradas no backlog do produto. As tarefas são pré-requisitos para que uma história de usuário possa ser completada.

## 2. Tema

Site aglomerador de [prestadores de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços).

## 3. Épicos

| ID                | Descrição                                                              |
| ----------------- | ---------------------------------------------------------------------- |
| E01 | [Usuário](./pages/base/lexicos.md#l01-usuário)                         |
| E02 | [Agendamento](./pages/base/lexicos.md#l09-agendar-serviço) de serviços |
| E03 | [Avaliação](./pages/base/lexicos.md#l05-avaliar)                       |
| E04 | [Pesquisa](./pages/base/lexicos.md#l06-pesquisar)                      |
| E05 | Interação entre [usuários](./pages/base/lexicos.md#l01-usuário)        |

## 4. Features

| Épico             | ID                   | Descrição                                                                                      |
| ----------------- | -------------------- | ---------------------------------------------------------------------------------------------- |
| [E01](#_3-Épicos) | FT01               | Conta                                                                                          |
| [E01](#_3-Épicos) | FT02               | Perfil                                                                                         |
| [E02](#_3-Épicos) | FT03               | Agendamento de Serviços                                                                        |
| [E02](#_3-Épicos) | FT04               | Controle de Serviços                                                                           |
| [E03](#_3-Épicos) | FT05               | [Avaliações](./pages/base/lexicos.md#l05-avaliar)                                              |
| [E03](#_3-Épicos) | FT06               | Denúncias                                                                                      |
| [E04](#_3-Épicos) | FT07               | [Buscar](./pages/base/lexicos.md#l06-pesquisar)                                                |
| [E04](#_3-Épicos) | FT08               | [Categorias](./pages/base/lexicos.md#l07-categorias-de-serviço)                                |
| [E05](#_3-Épicos) | FT09               | [Chat](./pages/base/lexicos.md#l12-chat) entre [usuários](./pages/base/lexicos.md#l01-usuário) |
| [E05](#_3-Épicos) | FT10               | Compartilhar                                                                                   |

## 5. Histórias de Usuário

| Feture               | ID                               | Descrição                                                                                                                                                                                                                                                                                                                                                                                     |
| -------------------- | -------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [FT01](#_4-features) | US01 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de me cadastrar, para que possa ter uma conta na plataforma.                                                                                                                                                                                                                                                                |
| [FT01](#_4-features) | US02 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de efetuar login no site, para que possa ter acesso as suas funcionalidades.                                                                                                                                                                                                                                                |
| [FT01](#_4-features) | US03 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de recuperar minha senha, para que possa acessar minha conta no caso que à tenha esquecido.                                                                                                                                                                                                                                 |
| [FT02](#_4-features) | US04 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de visualizar os serviços que ja contratei, para que possa ter controle sobre o meu histórico de uso.                                                                                                                                                                                                                       |
| [FT02](#_4-features) | US05 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de poder editar as informações de perfil, para que possa atualizar ou mudar minhas informações.                                                                                                                                                                                                                             |
| [FT02](#_4-features) | US06 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de favoritar um [prestador de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços), para que eu possa encontra-lo novamente com facilidade.                                                                                                                                                                          |
| [FT03](#_4-features) | US08 | Eu, como [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de cadastrar meus horários disponíveis, para que eu possa ter o controle dos horários que irei trabalhar.                                                                                                                                                                                       |
| [FT03](#_4-features) | US08 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de visualizar os horários que um [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços) está disponível, para que eu possa agendar um horário que me agrade.                                                                                                                                            |
| [FT03](#_4-features) | US09 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de agendar um compromisso, para que o [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços) que escolhi esteja alocado para me visitar no horário que eu desejo.                                                                                                                                       |
| [FT03](#_4-features) | US10 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de visualizar os meus agendamentos, para que eu possa ter um melhor controle sobre os meus compromissos marcados.                                                                                                                                                                                                           |
| [FT03](#_4-features) | US11 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de ser notificado sobre os meus agendamentos, para que não me esqueça dos compromissos marcados.                                                                                                                                                                                                                            |
| [FT04](#_4-features) | US12 | Eu, como [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de ter uma lista com as novas marcações de serviços, para que possa ter um bom controle dos novos pedidos.                                                                                                                                                                                      |
| [FT04](#_4-features) | US13 | Eu, como [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de ter a opção de aprovar, ou não, a solicitação de um novo serviço.                                                                                                                                                                                                                            |
| [FT04](#_4-features) | US14 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de poder remarcar um serviço, para que possa entrar em acordo com o horário de atendimento.                                                                                                                                                                                                                                 |
| [FT04](#_4-features) | US15 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de poder cancelar um serviço, para que possa evitar um desencontro no caso de um imprevisto.                                                                                                                                                                                                                                |
| [FT04](#_4-features) | US16 | Eu, como [prestador de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de cadastrar um seviço, para que possa ser oferecido pela plataforma.                                                                                                                                                                                                                            |
| [FT04](#_4-features) | US17 | Eu, como [prestador de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de visualizar as informações do meu [cliente](./pages/base/lexicos.md#l03-cliente), para que possa saber onde será executado o serviço.                                                                                                                                                          |
| [FT05](#_4-features) | US18 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de [avaliar](./pages/base/lexicos.md#l05-avaliar) um [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), para que outros [clientes](./pages/base/lexicos.md#l03-cliente) possam ter um melhor entendimento sobre a qualidade do serviço prestado por ele.                                           |
| [FT05](#_4-features) | US19 | Eu, como [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de [avaliar](./pages/base/lexicos.md#l05-avaliar) um [cliente](./pages/base/lexicos.md#l03-cliente), para que os outros [prestadores de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços) possam ter ideia da minha experiência com o [cliente](./pages/base/lexicos.md#l03-cliente). |
| [FT05](#_4-features) | US20 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de visualizar as [avaliações](./pages/base/lexicos.md#l05-avaliar) , para que possa ter uma noção sobre o seu comportamento.                                                                                                                                                                                                |
| [FT06](#_4-features) | US21 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de poder denunciar um [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), para que possa alertar outros usuários sobre algum problema na execução de um serviço.                                                                                                                                    |
| [FT06](#_4-features) | US22 | Eu, como [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de denunciar um [usuário](./pages/base/lexicos.md#l01-usuário), para que outros usuários sejam alertados sobre o seu comportamento.                                                                                                                                                             |
| [FT07](#_4-features) | US23 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de realizar [buscas](./pages/base/lexicos.md#l06-pesquisar) na plataforma, para que possa encontrar um [prestador de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços).                                                                                                                                            |
| [FT07](#_4-features) | US24 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de realizar [buscas](./pages/base/lexicos.md#l06-pesquisar) na plataforma, para que possa encontrar um [prestador de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços) por meio de seu nome ou serviço.                                                                                                           |
| [FT08](#_4-features) | US25 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de poder filtrar minha [busca](./pages/base/lexicos.md#l06-pesquisar) por localidade, para que possa encontrar um [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços) próximo à mim com maior facilidade.                                                                                            |
| [FT08](#_4-features) | US26 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de filtrar minha [busca](./pages/base/lexicos.md#l06-pesquisar) por quantidade de contratações, para poder escolher os [prestadores de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços) com maior experiência na plataforma.                                                                                     |
| [FT08](#_4-features) | US27 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de filtrar minha [busca](./pages/base/lexicos.md#l06-pesquisar) por [avaliações](./pages/base/lexicos.md#l05-avaliar) , para que possa escolher um [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços) que teve seu serviço elogiado por outros [clientes](./pages/base/lexicos.md#l03-cliente).     |
| [FT09](#_4-features) | US28 | Eu, como [clientes](./pages/base/lexicos.md#l03-cliente), gostaria de poder mandar uma mensagem para o [prestadores de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços), para que possa discutir algum detalhe sobre um servico.                                                                                                                                                  |
| [FT09](#_4-features) | US29 | Eu, como [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de poder mandar uma mensagem para um [clientes](./pages/base/lexicos.md#l03-cliente), para que possa discutir algum detalhe sobre um servico.                                                                                                                                                   |
| [FT10](#_4-features) | US30 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de poder compartilhar o perfil de um prestador de serviços, para que possa indicar este [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços) para outro [cliente](./pages/base/lexicos.md#l03-cliente).                                                                                               |
| [FT10](#_4-features) | US31 | Eu, como [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de poder compartilhar o meu serviço de forma premium, para que seja apresentada de forma destacada pela plataforma.                                                                                                                                                                             |

## 6. Backlog Priorizado

| Épico             | Feature              | História de Usuário              | Moscow | Rastreabilidade |
| ----------------- | -------------------- | -------------------------------- | ------ | --------------- |
| [E01](#_3-Épicos) | [FT01](#_4-features) | [US01](#_5-histórias-de-usuário) | MUST   | RF01            |
| [E01](#_3-Épicos) | [FT01](#_4-features) | [US02](#_5-histórias-de-usuário) | MUST   | RF01            |
| [E01](#_3-Épicos) | [FT01](#_4-features) | [US03](#_5-histórias-de-usuário) | MUST   | RF01            |
| [E01](#_3-Épicos) | [FT02](#_4-features) | [US04](#_5-histórias-de-usuário) | MUST   | RF07            |
| [E01](#_3-Épicos) | [FT02](#_4-features) | [US05](#_5-histórias-de-usuário) | MUST   | RF20            |
| [E01](#_3-Épicos) | [FT02](#_4-features) | [US06](#_5-histórias-de-usuário) | MUST   | RF02            |
| [E01](#_3-Épicos) | [FT03](#_4-features) | [US07](#_5-histórias-de-usuário) | COULD  | RF15            |
| [E02](#_3-Épicos) | [FT04](#_4-features) | [US08](#_5-histórias-de-usuário) | MUST   | RF17            |
| [E02](#_3-Épicos) | [FT04](#_4-features) | [US09](#_5-histórias-de-usuário) | MUST   | RF09            |
| [E02](#_3-Épicos) | [FT04](#_4-features) | [US10](#_5-histórias-de-usuário) | MUST   | RF10            |
| [E02](#_3-Épicos) | [FT05](#_4-features) | [US11](#_5-histórias-de-usuário) | MUST   | RF07            |
| [E02](#_3-Épicos) | [FT05](#_4-features) | [US12](#_5-histórias-de-usuário) | MUST   | RF25            |
| [E02](#_3-Épicos) | [FT05](#_4-features) | [US13](#_5-histórias-de-usuário) | MUST   | RF25            |
| [E02](#_3-Épicos) | [FT05](#_4-features) | [US14](#_5-histórias-de-usuário) | SHOULD | RF04            |
| [E02](#_3-Épicos) | [FT05](#_4-features) | [US15](#_5-histórias-de-usuário) | COULD  | RF12            |
| [E02](#_3-Épicos) | [FT05](#_4-features) | [US16](#_5-histórias-de-usuário) | SHOULD | RF14            |
| [E03](#_3-Épicos) | [FT06](#_4-features) | [US17](#_5-histórias-de-usuário) | COULD  | RF13            |
| [E03](#_3-Épicos) | [FT06](#_4-features) | [US18](#_5-histórias-de-usuário) | COULD  | RF13            |
| [E03](#_3-Épicos) | [FT06](#_4-features) | [US19](#_5-histórias-de-usuário) | COULD  | RF21            |
| [E03](#_3-Épicos) | [FT07](#_4-features) | [US20](#_5-histórias-de-usuário) | SHOULD | RF22            |
| [E03](#_3-Épicos) | [FT07](#_4-features) | [US21](#_5-histórias-de-usuário) | SHOULD | RF22            |
| [E04](#_3-Épicos) | [FT08](#_4-features) | [US22](#_5-histórias-de-usuário) | MUST   | RF08            |
| [E04](#_3-Épicos) | [FT09](#_4-features) | [US23](#_5-histórias-de-usuário) | MUST   | RF08            |
| [E04](#_3-Épicos) | [FT09](#_4-features) | [US24](#_5-histórias-de-usuário) | MUST   | RF08            |
| [E04](#_3-Épicos) | [FT09](#_4-features) | [US25](#_5-histórias-de-usuário) | MUST   | RF08            |
| [E05](#_3-Épicos) | [FT10](#_4-features) | [US26](#_5-histórias-de-usuário) | COULD  | RF03            |
| [E05](#_3-Épicos) | [FT10](#_4-features) | [US27](#_5-histórias-de-usuário) | MUST   | RF09            |
| [E05](#_3-Épicos) | [FT11](#_4-features) | [US28](#_5-histórias-de-usuário) | WOULD  | RF05            |

<!--
<table class="backlogTable">
    <thead>
        <th class="backlogHeader">Tema</th>
        <th class="backlogHeader">Épicos</th>
        <th class="backlogHeader">Funcionalidades</th>
        <th class="backlogHeader">ID</th>
        <th class="backlogHeader">Histórias de usuário</th>
        <th class="backlogHeader">Tarefas</th>
    </thead>
    <tbody>
        Épico de Usuário

         Feature de Conta
        <tr>
            <td rowspan="50" class="backlogTheme">Site aglomerador de prestadores de Serviço</td>
            <td rowspan="16" class="user2-2"><a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a></td>
            <td rowspan="7" class="user2-2">Conta</td>
            <td rowspan="4" class="user2-2">[US01](#_5-histórias-de-usuário)</d>
            <td rowspan="4"class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de me cadastrar, para que possa ter uma conta na plataforma.</td>
            <td class="user2-2">Criar modelo de <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a></td>
        </tr>
        <tr>
            <td class="user2-2">Criar modelo de <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>.</td>
        </tr>
            <td class="user2-2">Criar página de registro.</td>
        <tr>
            <td class="user2-2">Criar persistência de dados do <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>.</td>
        </tr>
        <tr>
            <td class="user2">[US02](#_5-histórias-de-usuário)</d>
            <td class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de efetuar <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l04-login">login</a> no site, para que possa ter acesso as suas funcionalidades.</td>
            <td class="user2">Criar página de <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l04-login">login</a>.</td>
        </tr>
        <tr>
            <td rowspan="2" class="user2-2">[US03](#_5-histórias-de-usuário)</d>
            <td rowspan="2" class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de recuperar minha senha, para que possa acessar minha conta no caso que à tenha esquecido.</td>
            <td class="user2-2">Criar página de recuperação de senha.</td>
        </tr>
        <tr>
            <td class="user2-2">Criar funcionalidade de requisição de recuperação de senha.</td>
        </tr>
        <tr>
            <td rowspan="6" class="user2">Perfil</td>
            <td rowspan="4" class="user2">[US04](#_5-histórias-de-usuário)</d>
            <td rowspan="4" class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de visualizar os serviços que ja contratei, para que possa ter controle sobre o meu histórico de uso.</td>
            <td class="user2">Criar página de histórico de serviços.</td>
        </tr>
        <tr>
            <td class="user2">Criar página de perfil.</td>
        </tr>
        <tr>
            <td class="user2">Criar modelo de histórico de serviços</a>
        </tr>
        <tr>
            <td class="user2">Criar persistência de dados dos serviços contratados.</td>
        </tr>
        <tr>
            <td class="user2-2">[US05](#_5-histórias-de-usuário)</d>
            <td class="user2-2">Eu, como Prestador de Serviço, gostaria de visualizar a localização do meu <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, para que possa saber onde será executado o serviço.</td>
            <td class="user2-2">Criar modo de visualização de perfil de outro <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a></td>
        </tr>
        <tr>
            <td class="user2">[US06](#_5-histórias-de-usuário)</d>
            <td class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de poder editar as informações de perfil, para que possa atualizar ou mudar minhas informações.</td>
            <td class="user2">Criar página de edição de perfil.</td>
        </tr>
       Feature de Favoritos

        <tr>
            <td rowspan="3" class="user2-2">Favoritos</td>
            <td rowspan="3" class="user2-2">[US07](#_5-histórias-de-usuário)</d>
            <td rowspan="3" class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de favoritar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, para que eu possa encontralo novamento com facilidade.</td>
            <td class="user2-2">Criar lista de favoritos.</td>
        </tr>
        <tr>
            <td class="user2-2">Criar persistência da lista de favoritos.</td>
        </tr>
        <tr>
            <td class="user2-2">Criar pagina de favoritos.</td>
        </tr>
        Epico de Agendamento
        Feature de Disponibilidade
        <tr>
            <td rowspan="12" class="user2">Agendamento</td>
            <td rowspan="5" class="user2">Disponibilidade</td>
            <td rowspan="2" class="user2">[US08](#_5-histórias-de-usuário)</d>
            <td rowspan="2" class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, gostaria de cadastrar meus horários disponíveis, para que eu possa ter o controle dos horários que irei trabalhar.</td>
            <td class="user2">Criar página de horáriode disponíveis.</td>
        </tr>
        <tr>
            <td class="user2">Criar persistência de dados de horário disponível.</td>
        </tr>
        <tr>
            <td class="user2-2">[US09](#_5-histórias-de-usuário)</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de visualizar os horários que um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a> está disponível, para que eu possa agendar um horário que me agrade.</td>
            <td class="user2-2">Criar página de visualização de agendamentos.</td>
        </tr>
        <tr>
            <td rowspan="2" class="user2">[US10](#_5-histórias-de-usuário)</d>
            <td rowspan="2" class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de agendar um compromisso, para que o <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a> que escolhi esteja alocado para me visitar no horário que eu desejo.</td>
            <td class="user2">Criar página solicitação de agendamentos.</td>
        </tr>
        <tr>
            <td class="user2">Criar persistência de dados de agendamentos.</td>
        </tr>
        Feature de Controle de Compromissos
        <tr>
            <td rowspan="7" class="user2-2">Controle de Compromissos</td>
            <td class="user2-2">[US11](#_5-histórias-de-usuário)</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de visualizar os meus agendamentos, para que eu possa ter um melhor controle sobre os meus compromissos marcados.</td>
            <td class="user2-2">Criar página de lista de agendamentos.</td>
        </tr>
        <tr>
            <td class="user2">[US12](#_5-histórias-de-usuário)</d>
            <td class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, gostaria de ter uma lista com as novas marcações de serviços, para que possa ter um bom controle dos novos pedidos.</td>
            <td class="user2">Criar página de novas solicitações de serviço.</td>
        </tr>
        <tr>
            <td class="user2-2">[US13](#_5-histórias-de-usuário)</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, gostaria de ter a opção de aprovar, ou não, a solicitação de um novo serviço.</td>
            <td class="user2-2">Adicionar à pagina de solicitação de serviços a opção de aceitar/regeitar serviço</td>
        </tr>
        <tr>
            <td rowspan="2" class="user2">[US14](#_5-histórias-de-usuário)</d>
            <td rowspan="2" class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de ser notificado sobre os meus agendamentos, para que não me esqueça dos compromissos marcados.</td>
            <td class="user2">Criar modelo de notificações.</td>
        </tr>
        <tr>
            <td class="user2">Criar sistema de notificações.</td>
        </tr>
        <tr>
            <td class="user2-2">[US15](#_5-histórias-de-usuário)</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de poder remarcar um compromisso, para que possa entrar em acordo com o horário de atendimento.</td>
            <td class="user2-2">Criar opção de alterar data e horário de um serviço já marcado.</td>
        </tr>
        <tr>
            <td class="user2">[US16](#_5-histórias-de-usuário)</d>
            <td class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de poder cancelar um compromisso, para que possa evitar um desencontro no caso de um imprevisto.</td>
            <td class="user2">Criar opção de cancelamento de serviço já marcado.</td>
        </tr>
        Épico de Avaliação
         Feature de Avaliações
        <tr>
            <td rowspan="9" class="user2-2">Avaliação</td>
            <td rowspan="5" class="user2-2">Avaliações</td>
            <td rowspan="2" class="user2-2">[US17](#_5-histórias-de-usuário)</d>
            <td rowspan="2" class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de avaliar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, para que outros <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">clientes</a> possam ter um melhor entendimento sobre a qualidade do serviço prestado por ele.</td>
            <td class="user2-2">Criar opção de avaliar <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>.</td>
        </tr>
        <tr>
            <td class="user2-2">Criar persistência de dados de avaliações de um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>.</td>
        </tr>
        <tr>
            <td rowspan="2" class="user2">[US18](#_5-histórias-de-usuário)</d>
            <td rowspan="2" class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, gostaria de avaliar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, para que os outros prestadores de serviço possam ter ideia da minha experiência com o <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>.</td>
            <td class="user2">Criar opção de avaliar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>.</td>
        </tr>
        <tr>
            <td class="user2">Criar opção de avaliar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>.</td>
        </tr>
        <tr>
            <td class="user2-2">[US10](9_5-histórias-de-usuário)</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de visualizar as avaliações do <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a> com quem irei interagir, para que possa ter uma noção sobre o seu comportamento.</td>
            <td class="user2-2">Adicionar a pagina de visualização de perfil a lista de avaliações do <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>.</td>
        </tr>
        Feature de Denúncias
        <tr>
            <td rowspan="4"class="user2">Denúncias</td>
            <td rowspan="2" class="user2">[US10]20_5-histórias-de-usuário)</d>
            <td rowspan="2" class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de poder denúnciar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, para que possa alertar outros <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuários</a> sobre algum problema na execução de um serviço.</td>
            <td class="user2">Criar página de denúncia de <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuários</a>.</td>
        </tr>
            <td class="user2">Criar opção de denúncia de <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a> no respectivo perfil.</td>
        <tr>
        </tr>
        <tr>
            <td class="user2-2">[US20]21_5-histórias-de-usuário)</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, gostaria de denúnciar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, para que outros <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuários</a> sejam alertados sobre o seu comportamento.</td>
            <td class="user2-2">Criar opção de denúncia de <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a> no respectivo perfil.</td>
        </tr>
        - Épico de Pesquisa
         Feature de Busca
        <tr>
            <td rowspan="5" class="user2">Pesquisa</td>
            <td rowspan="2" class="user2">Busca</td>
            <td rowspan="2" class="user2">[US20](2_5-histórias-de-usuário)</d>
            <td rowspan="2" class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de realizar buscas na plataforma, para que possa encontrar um prestador de serviço que atenda as minhas necessidades.</td>
            <td class="user2">Criar opção de busca de <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestadores de serviços</a>.</td>
        </tr>
        <tr>
            <td class="user2">Criar pagina de resultado de busca.</td>
        </tr>
        Feature de Categorias
        <tr>
            <td rowspan="3" class="user2-2">Categorias</td>
            <td class="user2-2">[US20](3_5-histórias-de-usuário)</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de poder filtrar minha busca por localidade, para que possa encontrar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a> próximo à mim com maior facilidade.</td>
            <td class="user2-2">Criar categoria de pesquisa ligada à localidade do <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>.</td>
        </tr>
        <tr>
            <td class="user2">[US20](4_5-histórias-de-usuário)</d>
            <td class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de filtrar minha busca por quantidade de contratações, para poder escolher os prestadores de serviço com maior experiência na plataforma.</td>
            <td class="user2">Criar categoria de pesquisa ligada à numero de serviços prestados do <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>.</td>
        </tr>
        <tr>
            <td class="user2-2">[US20](5_5-histórias-de-usuário)</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de filtrar minha busca por avaliações, para que possa escolher um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a> que teve seu serviço elogiado por outros <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">clientes</a>.</td>
            <td class="user2-2">Criar categoria de pesquisa ligada à avaliação geral do <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>.</td>
        </tr>
        Épico de Interação entre usuários
         Feature de Chat entre usuários
        <tr>
            <td rowspan="7" class="user2-2">Interação entre <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuários</a></td>
            <td rowspan="5" class="user2-2">Chat entre <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuários</a></td>
            <td rowspan="4" class="user2-2">[US20](6_5-histórias-de-usuário)</d>
            <td rowspan="4" class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de poder mandar uma mensagem para outro <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, para que possa discutir algum detalhe sobre um compromisso.</td>
            <td class="user2-2">Criar sistema de chat entre usuários.</td>
        </tr>
        <tr>
            <td class="user2-2">Criar notificação de mensagens.</td>
        </tr>
        <tr>
            <td class="user2-2">Criar ambiente de mensagen direta.</td>
        </tr>
        <tr>
            <td class="user2-2">Criar opção de mandar mensagens na pagina de perfil de um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>.</td>
        </tr>
        <tr>
            <td class="user2">[US20](_5-histórias-de-usuário)</d>
            <td class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de poder visualizar as informações de contato de um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, para que possa ter contato com ele fora da plataforma.</td>
            <td class="user2">---</td>
        </tr>
        <tr>
            <td class="user2">Compartilhar</td>
            <td class="user2">US28</d>
            <td class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de poder compartilhar o perfil de um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, para que possa indicar este <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a> para outro <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>.</td>
            <td class="user2">Criar opção de compartilhar informações entre <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuários</a>.</td>
        </tr>
    </tbody>

</table>

        -->

## 7. Requisitos Não Funcionais

|  ID   |                   Técnica                    |                                                 Requisito                                                  |
| :---: | :------------------------------------------: | :--------------------------------------------------------------------------------------------------------: |
| RNF01 | [Questionário](./pages/base/questionario.md) |                               A plataforma deve ter uma interface intuitiva                                |
| RNF02 |   [Brainstorm](./pages/base/brainstorm.md)   |                      A plataforma deve ser estável para múltiplos acessos simultâneos                      |
| RNF03 |   [Brainstorm](./pages/base/brainstorm.md)   |           A plataforma deve ser executada por meio de navegadores web com suporte ao JavaScript            |
| RNF04 |   [Brainstorm](./pages/base/brainstorm.md)   |                      O sistema deve ser desenvolvido utilizando Orientação a Objetos                       |
| RNF05 |   [Brainstorm](./pages/base/brainstorm.md)   |                           O sistema deve ter seu sistema organizado com o docker                           |
| RNF06 |   [Brainstorm](./pages/base/brainstorm.md)   | O sistema deve se adaptar a [LGPD](http://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm) |
| RNF07 |   [Brainstorm](./pages/base/brainstorm.md)   |   O usuário deve ser capaz de compreender as funcionalidades disponíveis em até 30 minutos de utilização   |
| RNF08 |   [Brainstorm](./pages/base/brainstorm.md)   |                   A interface deve ser adaptativa para telas acima de 320px de resolução                   |

## 8. Referências

> - LEFFINGWELL, Dean; Agile Software Requirements: Lean Requirements Practices for Teams, Programs, and Enterprise. 1. ed. Boston: Pearson, 2011.
> - WIEGERS, Karl; BEATTY, Joy; Software Requirements: Best practices. 3. ed; Microsoft Press, 2013
> - Backlog do Produto. Animalesco. Disponível em: https://unbarqdsw2021-1.github.io/2021.1_G01_Animalesco_docs/#/pages/backlog-do-produto (Último acesso em 01/02/2022)
>   [3] Lei Geral de Proteção de Dados Pessoais(LGPD). 14 de Agosto 2018. (http://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm). Acesso em 18 de Fevereiro de 2022.

</div>

### Histórico de versão

|    Data    | Versão |             Autor             |                Descrição                |
| :--------: | :----: | :---------------------------: | :-------------------------------------: |
| 01/02/2022 |  0.1   |       Fernando Miranda        |   Adicionada introdução e Referências   |
| 01/02/2022 |  1.0   |       Fernando Miranda        |  Adicionada versão inicial do Backlog   |
| 18/02/2022 |  2.0   | Rodrigo Balbino e João Victor |  Refatoração e priorização do backlog   |
| 19/02/2022 |  2.1   |       Fernando Miranda        | Adicionados links entre tabelas/paginas |
| 20/03/2022 |  2.2   |       Rodrigo Balbino e Álvaro Gouvea        | Refatorando tabela das Histórias de usuário |
