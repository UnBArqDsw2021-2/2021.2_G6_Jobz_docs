# <center> Backlog do Produto

<div align="justify">

## 1. Introdução

O Backlog do Produto, ou Backlog, foi introduzido pela primeira vez pelo método ágil Scrum é um artefato utilizado em projetos ágeis, artefato este que consistem em uma lista de pedidos ou requisições do cliente sobre quais comportamentos e funcionalidades o sistema deve possuir para este ser considerado como um produto finalizado. Um backlog pode ser implementado com diferentes níveis de detalhes, entre implementações diferentes, os principais pontos componentes de um backlog são:

 - Tema(Theme);
 - Épicos(Epics);
 - Funcionalidades(Features);
 - Histórias de usuário(User Stories);
 - Tarefas(Tasks);

O **Tema** em um backlog do produto é o componente que possui a granularidade mais alta em um backlog, tratando de uma relação direta entre o backlog e o objetivo do projeto, pode-se dizer que o tema descreve a visão do produto, representando os princípios que agregam valor à aplicação.


**Épicos** são formados por um conjunto de funcionalidades, os épicos são representações expressadas em alto nível, ou mais próxima as necessidades reais, de um grupo de funcionalidades que o cliente precisa que o software execute. Os Épicos também podem ser descritos como histórias de usuário que são grandes demais para serem implementadas em um único ciclo de desenvolvimento Mike Cohn(2010), que deverão ser subdivididas em histórias até estas poderem ser implementadas em um único ciclo.


**Funcionalidades** - Enquanto os épicos tratam de um nível superior das necessidades do cliente com um produto de software, as funcionalidades são especificações de processos que se decompões em histórias de usuário e vão descrever melhor quais responsabilidades do software.


As **Histórias de usuário** são descrições focadas na visão do usuário, em que as funcionalidades serão necessárias, descrições que devem ser entendidas tanto por clientes, quanto pelos desenvolvedores e tem o objetivo de contextualizar o desenvolvimento de uma funcionalidade que o sistema precisa atender.

As **Tarefas** representam o menor nível de granularidade nas descrições de requisitos registradas no backlog do produto. As tarefas são pré-requisitos para que uma história de usuário possa ser completada.


## 2. Conteudo

Com a aplicação das técnicas de elicitação de requisitos, a equipe pode montar o backlog do produto com as funcionalidades que foram levantadas como necessárias para o produto.

<table class="backlogTable">
    <thead>
        <th class="backlogThemeH">Tema</th>
        <th class="backlogEpics">Épicos</th>
        <th class="backlogFeatures">Funcionalidades</th>
        <th class="backlogID">ID</th> 
        <th class="backlogUserStories">Histórias de usuário</th>
        <th class="backlogTasks">Tarefas</th>
    </thead>
    <tbody>
        <!-- Épico de Usuário -->
        <!-- Feature de Conta -->
        <tr>
            <td rowspan="50" class="backlogTheme">Site aglomerador de prestadores de Serviço</td>
            <td rowspan="16" class="backlogEpic1"><a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a></td>
            <td rowspan="7" class="user1">Conta</td>
            <td rowspan="4" class="user1">US01</d>
            <td rowspan="4"class="user1">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de me cadastrar, para que possa ter uma conta na plataforma.</td>
            <td class="user1">Criar modelo de <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a></td>
        </tr>
        <tr>
            <td class="user1">Criar modelo de <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>.</td>
        </tr>
            <td class="user1">Criar página de registro.</td>
        <tr>
            <td class="user1">Criar persistência de dados do <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>.</td>
        </tr>
        <tr>
            <td class="user1-2">US02</d>
            <td class="user1-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de efetuar <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l04-login">login</a> no site, para que possa ter acesso as suas funcionalidades.</td>
            <td class="user1-2">Criar página de <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l04-login">login</a>.</td>
        </tr>
        <tr>
            <td rowspan="2" class="user1">US03</d>
            <td rowspan="2" class="user1">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de recuperar minha senha, para que possa acessar minha conta no caso que à tenha esquecido.</td>
            <td class="user1">Criar página de recuperação de senha.</td>
        </tr>
        <tr>
            <td class="user1">Criar funcionalidade de requisição de recuperação de senha.</td>
        </tr>
        <tr>
            <td rowspan="6" class="user2">Perfil</td>
            <td rowspan="4" class="user2">US04</d>
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
            <td class="user2-2">US05</d>
            <td class="user2-2">Eu, como Prestador de Serviço, gostaria de visualizar a localização do meu <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, para que possa saber onde será executado o serviço.</td>
            <td class="user2-2">Criar modo de visualização de perfil de outro <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a></td>
        </tr>
        <tr>
            <td class="user2">US06</d>
            <td class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de poder editar as informações de perfil, para que possa atualizar ou mudar minhas informações.</td>
            <td class="user2">Criar página de edição de perfil.</td>
        </tr>
        <!-- Feature de Favoritos -->
        <tr>
            <td rowspan="3" class="user1">Favoritos</td>
            <td rowspan="3" class="user1">US07</d>
            <td rowspan="3" class="user1">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de favoritar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, para que eu possa encontralo novamento com facilidade.</td>
            <td class="user1">Criar lista de favoritos.</td>
        </tr>
        <tr>
            <td class="user1">Criar persistência da lista de favoritos.</td>
        </tr>
        <tr>
            <td class="user1">Criar pagina de favoritos.</td>
        </tr>
        <!-- Epico de Agendamento -->
        <!-- Feature de Disponibilidade -->
        <tr>
            <td rowspan="12" class="user2">Agendamento</td>
            <td rowspan="5" class="user2">Disponibilidade</td>
            <td rowspan="2" class="user2">US08</d>
            <td rowspan="2" class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, gostaria de cadastrar meus horários disponíveis, para que eu possa ter o controle dos horários que irei trabalhar.</td>
            <td class="user2">Criar página de horáriode disponíveis.</td>
        </tr>
        <tr>
            <td class="user2">Criar persistência de dados de horário disponível.</td>
        </tr>
        <tr>
            <td class="user2-2">US09</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de visualizar os horários que um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a> está disponível, para que eu possa agendar um horário que me agrade.</td>
            <td class="user2-2">Criar página de visualização de agendamentos.</td>
        </tr>
        <tr>
            <td rowspan="2" class="user2">US10</d>
            <td rowspan="2" class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de agendar um compromisso, para que o <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a> que escolhi esteja alocado para me visitar no horário que eu desejo.</td>
            <td class="user2">Criar página solicitação de agendamentos.</td>
        </tr>
        <tr>
            <td class="user2">Criar persistência de dados de agendamentos.</td>
        </tr>
        <!-- Feature de Controle de Compromissos -->
        <tr>
            <td rowspan="7" class="user2-2">Controle de Compromissos</td>
            <td class="user2-2">US11</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de visualizar os meus agendamentos, para que eu possa ter um melhor controle sobre os meus compromissos marcados.</td>
            <td class="user2-2">Criar página de lista de agendamentos.</td>
        </tr>
        <tr>
            <td class="user2">US12</d>
            <td class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, gostaria de ter uma lista com as novas marcações de serviços, para que possa ter um bom controle dos novos pedidos.</td>
            <td class="user2">Criar página de novas solicitações de serviço.</td>
        </tr>
        <tr>
            <td class="user2-2">US13</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, gostaria de ter a opção de aprovar, ou não, a solicitação de um novo serviço.</td>
            <td class="user2-2">Adicionar à pagina de solicitação de serviços a opção de aceitar/regeitar serviço</td>
        </tr>
        <tr>
            <td rowspan="2" class="user2">US14</d>
            <td rowspan="2" class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de ser notificado sobre os meus agendamentos, para que não me esqueça dos compromissos marcados.</td>
            <td class="user2">Criar modelo de notificações.</td>
        </tr>
        <tr>
            <td class="user2">Criar sistema de notificações.</td>
        </tr>
        <tr>
            <td class="user2-2">US15</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de poder remarcar um compromisso, para que possa entrar em acordo com o horário de atendimento.</td>
            <td class="user2-2">Criar opção de alterar data e horário de um serviço já marcado.</td>
        </tr>
        <tr>
            <td class="user2">US16</d>
            <td class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de poder cancelar um compromisso, para que possa evitar um desencontro no caso de um imprevisto.</td>
            <td class="user2">Criar opção de cancelamento de serviço já marcado.</td>
        </tr>
        <!-- Épico de Avaliação -->
        <!-- Feature de Avaliações -->
        <tr>
            <td rowspan="9" class="user2-2">Avaliação</td>
            <td rowspan="5" class="user2-2">Avaliações</td>
            <td rowspan="2" class="user2-2">US17</d>
            <td rowspan="2" class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de avaliar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, para que outros <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">clientes</a> possam ter um melhor entendimento sobre a qualidade do serviço prestado por ele.</td>
            <td class="user2-2">Criar opção de avaliar <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>.</td>
        </tr>
        <tr>
            <td class="user2-2">Criar persistência de dados de avaliações de um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>.</td>
        </tr>
        <tr>
            <td rowspan="2" class="user2">US18</d>
            <td rowspan="2" class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, gostaria de avaliar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, para que os outros prestadores de serviço possam ter ideia da minha experiência com o <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>.</td>
            <td class="user2">Criar opção de avaliar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>.</td>
        </tr>
        <tr>
            <td class="user2">Criar opção de avaliar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>.</td>
        </tr>
        <tr>
            <td class="user2-2">US19</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, gostaria de visualizar as avaliações do <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a> com quem irei interagir, para que possa ter uma noção sobre o seu comportamento.</td>
            <td class="user2-2">Adicionar a pagina de visualização de perfil a lista de avaliações do <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>.</td>
        </tr>
        <!-- Feature de Denúncias -->
        <tr>
            <td rowspan="4"class="user2">Denúncias</td>
            <td rowspan="2" class="user2">US20</d>
            <td rowspan="2" class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de poder denúnciar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, para que possa alertar outros <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuários</a> sobre algum problema na execução de um serviço.</td>
            <td class="user2">Criar página de denúncia de <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuários</a>.</td>
        </tr>
            <td class="user2">Criar opção de denúncia de <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a> no respectivo perfil.</td>
        <tr>
        </tr>
        <tr>
            <td class="user2-2">US21</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>, gostaria de denúnciar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuário</a>, para que outros <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuários</a> sejam alertados sobre o seu comportamento.</td>
            <td class="user2-2">Criar opção de denúncia de <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a> no respectivo perfil.</td>
        </tr>
        <!-- Épico de Pesquisa -->
        <!-- Feature de Busca -->
        <tr>
            <td rowspan="5" class="user2">Pesquisa</td>
            <td rowspan="2" class="user2">Busca</td>
            <td rowspan="2" class="user2">US22</d>
            <td rowspan="2" class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de realizar buscas na plataforma, para que possa encontrar um prestador de serviço que atenda as minhas necessidades.</td>
            <td class="user2">Criar opção de busca de <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestadores de serviços</a>.</td>
        </tr>
        <tr>
            <td class="user2">Criar pagina de resultado de busca.</td>
        </tr>
        <!-- Feature de Categorias -->
        <tr>
            <td rowspan="3" class="user2-2">Categorias</td>
            <td class="user2-2">US23</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de poder filtrar minha busca por localidade, para que possa encontrar um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a> próximo à mim com maior facilidade.</td>
            <td class="user2-2">Criar categoria de pesquisa ligada à localidade do <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>.</td>
        </tr>
        <tr>
            <td class="user2">US24</d>
            <td class="user2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de filtrar minha busca por quantidade de contratações, para poder escolher os prestadores de serviço com maior experiência na plataforma.</td>
            <td class="user2">Criar categoria de pesquisa ligada à numero de serviços prestados do <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>.</td>
        </tr>
        <tr>
            <td class="user2-2">US25</d>
            <td class="user2-2">Eu, como <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">cliente</a>, gostaria de filtrar minha busca por avaliações, para que possa escolher um <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a> que teve seu serviço elogiado por outros <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l03-cliente">clientes</a>.</td>
            <td class="user2-2">Criar categoria de pesquisa ligada à avaliação geral do <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l02-prestador-de-servi%c3%a7os">prestador de serviços</a>.</td>
        </tr>
        <!-- Épico de Interação entre usuários -->
        <!-- Feature de Chat entre usuários -->
        <tr>
            <td rowspan="7" class="user2-2">Interação entre <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuários</a></td>
            <td rowspan="5" class="user2-2">Chat entre <a class="linkBacklog" href="https://unbarqdsw2021-2.github.io/2021.2_G6_Jobz_docs/#/./pages/base/lexicos?id=l01-usu%c3%a1rio">usuários</a></td>
            <td rowspan="4" class="user2-2">US26</d>
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
            <td class="user2">US27</d>
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

## 3. Referências


> - LEFFINGWELL, Dean; Agile Software Requirements: Lean Requirements Practices for Teams, Programs, and Enterprise. 1. ed. Boston: Pearson, 2011.
> - WIEGERS, Karl; BEATTY, Joy; Software Requirements: Best practices. 3. ed; Microsoft Press, 2013
> - Backlog do Produto. Animalesco. Disponível em: https://unbarqdsw2021-1.github.io/2021.1_G01_Animalesco_docs/#/pages/backlog-do-produto (Último acesso em 01/02/2022)

</div>

### Histórico de versão

|    Data    | Versão |       Autor      |              Descrição               |
| :--------: | :----: | :--------------: | :----------------------------------: |
| 01/02/2022 |  0.1   | Fernando Miranda | Adicionada introdução e Referências  |
| 01/02/2022 |  0.5   | Fernando Miranda | Adicionada versão inicial do Backlog |
