# <center> Backlog do Produto

<div align="justify">

## 1. Introdução

O Backlog do Produto, ou Backlog, foi introduzido pela primeira vez pelo método ágil Scrum é um artefato utilizado em projetos ágeis, artefato este que consiste em uma lista de pedidos ou requisições do cliente sobre quais comportamentos e funcionalidades o sistema deve possuir para este ser considerado como um produto finalizado. Um backlog pode ser implementado com diferentes níveis de detalhes, entre implementações diferentes, os principais pontos componentes de um backlog são:

- Tema(Theme);
- Épicos(Epics);
- Funcionalidades(Funcionalidades);
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

| ID  | Descrição                                                              |
| --- | ---------------------------------------------------------------------- |
| E01 | [Usuário](./pages/base/lexicos.md#l01-usuário)                         |
| E02 | [Agendamento](./pages/base/lexicos.md#l09-agendar-serviço) de serviços |
| E03 | [Avaliação](./pages/base/lexicos.md#l05-avaliar)                       |
| E04 | [Pesquisa](./pages/base/lexicos.md#l06-pesquisar)                      |
| E05 | Interação entre [usuários](./pages/base/lexicos.md#l01-usuário)        |

## 4. Funcionalidades

| Épico             | ID   | Descrição                                                                                      |
| ----------------- | ---- | ---------------------------------------------------------------------------------------------- |
| [E01](#_3-Épicos) | FT01 | Conta                                                                                          |
| [E01](#_3-Épicos) | FT02 | Perfil                                                                                         |
| [E02](#_3-Épicos) | FT03 | Agendamento de Serviços                                                                        |
| [E02](#_3-Épicos) | FT04 | Controle de Serviços                                                                           |
| [E03](#_3-Épicos) | FT05 | [Avaliações](./pages/base/lexicos.md#l05-avaliar)                                              |
| [E03](#_3-Épicos) | FT06 | Denúncias                                                                                      |
| [E04](#_3-Épicos) | FT07 | [Buscar](./pages/base/lexicos.md#l06-pesquisar)                                                |
| [E04](#_3-Épicos) | FT08 | [Categorias](./pages/base/lexicos.md#l07-categorias-de-serviço)                                |
| [E05](#_3-Épicos) | FT09 | [Chat](./pages/base/lexicos.md#l12-chat) entre [usuários](./pages/base/lexicos.md#l01-usuário) |
| [E05](#_3-Épicos) | FT10 | Compartilhar                                                                                   |

## 5. Histórias de Usuário

| Funcionalidade              | ID   | Descrição                                                                                                                                                                                                                                                                                                                                                                                     |
| --------------------------- | ---- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [FT01](#_4-Funcionalidades) | US01 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de me cadastrar, para que possa ter uma conta na plataforma.                                                                                                                                                                                                                                                                |
| [FT01](#_4-Funcionalidades) | US02 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de efetuar login no site, para que possa ter acesso as suas funcionalidades.                                                                                                                                                                                                                                                |
| [FT01](#_4-Funcionalidades) | US03 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de recuperar minha senha, para que possa acessar minha conta no caso que à tenha esquecido.                                                                                                                                                                                                                                 |
| [FT02](#_4-Funcionalidades) | US04 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de visualizar os serviços que ja contratei, para que possa ter controle sobre o meu histórico de uso.                                                                                                                                                                                                                       |
| [FT02](#_4-Funcionalidades) | US05 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de poder editar as informações de perfil, para que possa atualizar ou mudar minhas informações.                                                                                                                                                                                                                             |
| [FT02](#_4-Funcionalidades) | US06 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de favoritar um [prestador de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços), para que eu possa encontra-lo novamente com facilidade.                                                                                                                                                                          |
| [FT03](#_4-Funcionalidades) | US07 | Eu, como [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de cadastrar meus horários disponíveis, para que eu possa ter o controle dos horários que irei trabalhar.                                                                                                                                                                                       |
| [FT03](#_4-Funcionalidades) | US08 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de visualizar os horários que um [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços) está disponível, para que eu possa agendar um horário que me agrade.                                                                                                                                            |
| [FT03](#_4-Funcionalidades) | US09 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de agendar um compromisso, para que o [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços) que escolhi esteja alocado para me visitar no horário que eu desejo.                                                                                                                                       |
| [FT03](#_4-Funcionalidades) | US10 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de visualizar os meus agendamentos, para que eu possa ter um melhor controle sobre os meus compromissos marcados.                                                                                                                                                                                                           |
| [FT03](#_4-Funcionalidades) | US11 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de ser notificado sobre os meus agendamentos, para que não me esqueça dos compromissos marcados.                                                                                                                                                                                                                            |
| [FT04](#_4-Funcionalidades) | US12 | Eu, como [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de ter uma lista com as novas marcações de serviços, para que possa ter um bom controle dos novos pedidos.                                                                                                                                                                                      |
| [FT04](#_4-Funcionalidades) | US13 | Eu, como [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de ter a opção de aprovar, ou não, a solicitação de um novo serviço.                                                                                                                                                                                                                            |
| [FT04](#_4-Funcionalidades) | US14 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de poder remarcar um serviço, para que possa entrar em acordo com o horário de atendimento.                                                                                                                                                                                                                                 |
| [FT04](#_4-Funcionalidades) | US15 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de poder cancelar um serviço, para que possa evitar um desencontro no caso de um imprevisto.                                                                                                                                                                                                                                |
| [FT04](#_4-Funcionalidades) | US16 | Eu, como [prestador de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de cadastrar um serviço, para que possa ser oferecido pela plataforma.                                                                                                                                                                                                                           |
| [FT04](#_4-Funcionalidades) | US17 | Eu, como [prestador de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de visualizar as informações do meu [cliente](./pages/base/lexicos.md#l03-cliente), para que possa saber onde será executado o serviço.                                                                                                                                                          |
| [FT05](#_4-Funcionalidades) | US18 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de [avaliar](./pages/base/lexicos.md#l05-avaliar) um [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), para que outros [clientes](./pages/base/lexicos.md#l03-cliente) possam ter um melhor entendimento sobre a qualidade do serviço prestado por ele.                                           |
| [FT05](#_4-Funcionalidades) | US19 | Eu, como [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de [avaliar](./pages/base/lexicos.md#l05-avaliar) um [cliente](./pages/base/lexicos.md#l03-cliente), para que os outros [prestadores de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços) possam ter ideia da minha experiência com o [cliente](./pages/base/lexicos.md#l03-cliente). |
| [FT05](#_4-Funcionalidades) | US20 | Eu, como [usuário](./pages/base/lexicos.md#l01-usuário), gostaria de visualizar as [avaliações](./pages/base/lexicos.md#l05-avaliar) , para que possa ter uma noção sobre o seu comportamento.                                                                                                                                                                                                |
| [FT06](#_4-Funcionalidades) | US21 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de poder denunciar um [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), para que possa alertar outros usuários sobre algum problema na execução de um serviço.                                                                                                                                    |
| [FT06](#_4-Funcionalidades) | US22 | Eu, como [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de denunciar um [usuário](./pages/base/lexicos.md#l01-usuário), para que outros usuários sejam alertados sobre o seu comportamento.                                                                                                                                                             |
| [FT07](#_4-Funcionalidades) | US23 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de realizar [buscas](./pages/base/lexicos.md#l06-pesquisar) na plataforma, para que possa encontrar um [prestador de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços).                                                                                                                                           |
| [FT07](#_4-Funcionalidades) | US24 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de realizar [buscas](./pages/base/lexicos.md#l06-pesquisar) na plataforma, para que possa encontrar um [prestador de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços) por meio de seu nome ou serviço.                                                                                                           |
| [FT08](#_4-Funcionalidades) | US25 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de poder filtrar minha [busca](./pages/base/lexicos.md#l06-pesquisar) por localidade, para que possa encontrar um [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços) próximo à mim com maior facilidade.                                                                                            |
| [FT08](#_4-Funcionalidades) | US26 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de filtrar minha [busca](./pages/base/lexicos.md#l06-pesquisar) por quantidade de contratações, para poder escolher os [prestadores de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços) com maior experiência na plataforma.                                                                                     |
| [FT08](#_4-Funcionalidades) | US27 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de filtrar minha [busca](./pages/base/lexicos.md#l06-pesquisar) por [avaliações](./pages/base/lexicos.md#l05-avaliar) , para que possa escolher um [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços) que teve seu serviço elogiado por outros [clientes](./pages/base/lexicos.md#l03-cliente).     |
| [FT09](#_4-Funcionalidades) | US28 | Eu, como [clientes](./pages/base/lexicos.md#l03-cliente), gostaria de poder mandar uma mensagem para o [prestadores de serviço](./pages/base/lexicos.md#l02-prestador-de-serviços), para que possa discutir algum detalhe sobre um servico.                                                                                                                                                   |
| [FT09](#_4-Funcionalidades) | US29 | Eu, como [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de poder mandar uma mensagem para um [clientes](./pages/base/lexicos.md#l03-cliente), para que possa discutir algum detalhe sobre um servico.                                                                                                                                                   |
| [FT10](#_4-Funcionalidades) | US30 | Eu, como [cliente](./pages/base/lexicos.md#l03-cliente), gostaria de poder compartilhar o perfil de um prestador de serviços, para que possa indicar este [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços) para outro [cliente](./pages/base/lexicos.md#l03-cliente).                                                                                               |
| [FT10](#_4-Funcionalidades) | US31 | Eu, como [prestador de serviços](./pages/base/lexicos.md#l02-prestador-de-serviços), gostaria de poder compartilhar o meu serviço de forma premium, para que seja apresentada de forma destacada pela plataforma.                                                                                                                                                                             |

## 6. Tarefas

| IdFuncionalidades           | IdHistoriasDeUsuario             | Tarefas                                                                                                                                                                                                          |
| --------------------------- | -------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [FT01](#_4-Funcionalidades) | [US01](#_5-histórias-de-usuário) | - Criar página de cadastro de usuário <br>- Criar tela principal <br>- Criar model de usuário <br>- Disponibilizar endpoint de cadastro<br>- Implementar requisição POST para usuário                            |
| [FT01](#_4-Funcionalidades) | [US02](#_5-histórias-de-usuário) | - Criar tela de login<br>- Fazer requisição POST para login<br>- Disponibilizar endpoint de autenticação<br>- Armazenar de maneira local o token de autenticação                                                 |
| [FT01](#_4-Funcionalidades) | [US03](#_5-histórias-de-usuário) | - Criar página para recuperação de senha<br>- Gerar nova senha<br>- Enviar email com nova senha                                                                                                                  |
| [FT02](#_4-Funcionalidades) | [US04](#_5-histórias-de-usuário) | - Adicionar página que apresenta serviços já contratados do usuário <br> - Realizar uma requisição GET para pegar as informações dos serviços já contratados                                                     |
| [FT02](#_4-Funcionalidades) | [US05](#_5-histórias-de-usuário) | - Criar página do perfil<br>- Realizar a requisição GET com as informações do perfil                                                                                                                             |
| [FT02](#_4-Funcionalidades) | [US06](#_5-histórias-de-usuário) | - Adicionar botão para favoritar prestador<br>- Adicionar região de prestadores favoritados no próprio perfil<br>- Realizar a requisição POST para adicionar prestador                                           |
| [FT02](#_4-Funcionalidades) | [US07](#_5-histórias-de-usuário) | - Adição dos horários do Prestador no Perfil<br>- Adição da coluna de horários na tabela de prestador<br>- Realizar a requisição POST para cadastrar horário<br>- Disponibilizar endpoint para adição de horário |
| [FT03](#_4-Funcionalidades) | [US08](#_5-histórias-de-usuário) | - Realizar a requisição GET para visualizar os horários disponível do prestador                                                                                                                                  |
| [FT03](#_4-Funcionalidades) | [US09](#_5-histórias-de-usuário) | - Realizar requisição POST com horário do serviço                                                                                                                                                                |
| [FT03](#_4-Funcionalidades) | [US10](#_5-histórias-de-usuário) | - Realizar a requisição GET para visualizar o agendamento do próprio usuário em seu perfil                                                                                                                       |
| [FT03](#_4-Funcionalidades) | [US11](#_5-histórias-de-usuário) | - Adicionar o botão de notificações da NavBar<br> - Realizar a requisição GET de tempos em tempos para saber se o período do agendamento está próximo                                                            |
| [FT04](#_4-Funcionalidades) | [US12](#_5-histórias-de-usuário) | - Adicionar um botão de serviços na sideBar do perfil do prestador de serviço<br> - Realizar a requisição GET para recuperar a lista das marcações de serviço                                                    |
| [FT04](#_4-Funcionalidades) | [US13](#_5-histórias-de-usuário) | - Criação da página de aprovação de serviço<br> - Requisição GET de todos os serviços requisitados para o prestador<br>- Requisição POST com os serviços aceitos pelo prestador                                  |
| [FT04](#_4-Funcionalidades) | [US14](#_5-histórias-de-usuário) | - Adicionar a opção de remarcação de serviço na lista de serviços do usuário<br> - Realizar a requisição PUT para fazer a remarcação do serviço                                                                  |
| [FT04](#_4-Funcionalidades) | [US15](#_5-histórias-de-usuário) | - Disponbilizar endpoint para deletar serviços<br>- Implementar requisição de DELETE<br>- Adicionar opção de deleção de serviço                                                                                  |
| [FT04](#_4-Funcionalidades) | [US16](#_5-histórias-de-usuário) | - Criação da tela de Serviço <br> - Realizar a requisição POST das informações do serviço <br> - Disponibilizar endpoint de serviço                                                                              |
| [FT04](#_4-Funcionalidades) | [US17](#_5-histórias-de-usuário) | - Disponibilizar link para perfil do cliente                                                                                                                                                                     |
| [FT05](#_4-Funcionalidades) | [US18](#_5-histórias-de-usuário) | - Criação da página de avaliação do serviço na página do serviço <br> - Realizar uma requisição POST para adicionar a avaliação do cliente                                                                       |
| [FT05](#_4-Funcionalidades) | [US19](#_5-histórias-de-usuário) | - Criação da página de avaliação do cliente na página do perfil do cliente <br> - Realizar uma requisição POST para adicionar a avaliação ao cliente                                                             |
| [FT05](#_4-Funcionalidades) | [US20](#_5-histórias-de-usuário) | - Criação da seção de comentários dos usuários <br> - Realização da requisição GET para receber todas as avaliações realizadas                                                                                   |
| [FT06](#_4-Funcionalidades) | [US21](#_5-histórias-de-usuário) |  - Criar o botão que permita o cliente denunciar o prestador de serviço <br> - Realizar a requisição POST para adicionar uma denúncia ao prestador                                                               |
| [FT06](#_4-Funcionalidades) | [US22](#_5-histórias-de-usuário) | - Disponibilizar o botão de denunciar usuário, do ponto de vista do prestador <br> - Realizar a requisição de POST para adicionar uma denúncia ao cliente                                                        |
| [FT07](#_4-Funcionalidades) | [US23](#_5-histórias-de-usuário) | - Realizar a requisição GET para receber a lista de serviços de seus prestadores por meio da componente NavBar <br> - Filtrar lista de prestadores de acordo com as informações concedidas                       |
| [FT07](#_4-Funcionalidades) | [US24](#_5-histórias-de-usuário) | - Realizar a requisição GET utilizando o nome ou serviço para receber a busca                                                                                                                                    |
| [FT08](#_4-Funcionalidades) | [US25](#_5-histórias-de-usuário) | - Implementar API de localização <br> - Requisição GET de prestadores de serviço em localidades próximas <br> - Criação da Tag localização para filtrar a busca de serviço                                       |
| [FT08](#_4-Funcionalidades) | [US26](#_5-histórias-de-usuário) |  - Criação da Tag quantidade de contratações para filtrar a busca de serviço <br> - Realização da requisição GET por meio da quantidade de contratações                                                          |
| [FT08](#_4-Funcionalidades) | [US27](#_5-histórias-de-usuário) | - Criação da Tag avaliações para filtrar a busca de serviço <br>- Realização da requisição GET por meio das avaliações                                                                                           |
| [FT09](#_4-Funcionalidades) | [US28](#_5-histórias-de-usuário) | - Criação da página de chat entre o cliente e o prestador<br>- Realização da requisição POST da mensagem do ponto de vista do cliente para o Prestador                                                           |
| [FT09](#_4-Funcionalidades) | [US29](#_5-histórias-de-usuário) | - Implementar chat na aplicação <br>- Criação da página de chat entre o cliente e o prestador <br>- Realização da requisição POST da mensagem do ponto de vista do Prestador para o Cliente                      |
| [FT10](#_4-Funcionalidades) | [US30](#_5-histórias-de-usuário) | - Adicionar botão de compartilhar <br>- Gerar link do perfil do provedor                                                                                                                                         |
| [FT10](#_4-Funcionalidades) | [US31](#_5-histórias-de-usuário) | - Adicionar página de pagamento para conta premium do prestador de serviço <br> - Adicionar coluna <br> - Premium na tabela de provedor no Backend <br> - Priorizar resultados de provedores premium plataforma  |

## 7. Backlog Priorizado

| Épico             | Funcionalidade              | Histórias de Usuário             | Moscow | Rastreabilidade |
| ----------------- | --------------------------- | -------------------------------- | ------ | --------------- |
| [E01](#_3-Épicos) | [FT01](#_4-Funcionalidades) | [US01](#_5-histórias-de-usuário) | MUST   | RF01            |
| [E01](#_3-Épicos) | [FT01](#_4-Funcionalidades) | [US02](#_5-histórias-de-usuário) | MUST   | RF01            |
| [E01](#_3-Épicos) | [FT01](#_4-Funcionalidades) | [US03](#_5-histórias-de-usuário) | MUST   | RF01            |
| [E01](#_3-Épicos) | [FT02](#_4-Funcionalidades) | [US04](#_5-histórias-de-usuário) | MUST   | RF07            |
| [E01](#_3-Épicos) | [FT02](#_4-Funcionalidades) | [US05](#_5-histórias-de-usuário) | MUST   | RF20            |
| [E01](#_3-Épicos) | [FT02](#_4-Funcionalidades) | [US06](#_5-histórias-de-usuário) | MUST   | RF02            |
| [E01](#_3-Épicos) | [FT03](#_4-Funcionalidades) | [US07](#_5-histórias-de-usuário) | COULD  | RF15            |
| [E02](#_3-Épicos) | [FT04](#_4-Funcionalidades) | [US08](#_5-histórias-de-usuário) | MUST   | RF17            |
| [E02](#_3-Épicos) | [FT04](#_4-Funcionalidades) | [US09](#_5-histórias-de-usuário) | MUST   | RF09            |
| [E02](#_3-Épicos) | [FT04](#_4-Funcionalidades) | [US10](#_5-histórias-de-usuário) | MUST   | RF10            |
| [E02](#_3-Épicos) | [FT05](#_4-Funcionalidades) | [US11](#_5-histórias-de-usuário) | MUST   | RF07            |
| [E02](#_3-Épicos) | [FT05](#_4-Funcionalidades) | [US12](#_5-histórias-de-usuário) | MUST   | RF25            |
| [E02](#_3-Épicos) | [FT05](#_4-Funcionalidades) | [US13](#_5-histórias-de-usuário) | MUST   | RF25            |
| [E02](#_3-Épicos) | [FT05](#_4-Funcionalidades) | [US14](#_5-histórias-de-usuário) | SHOULD | RF04            |
| [E02](#_3-Épicos) | [FT05](#_4-Funcionalidades) | [US15](#_5-histórias-de-usuário) | COULD  | RF12            |
| [E02](#_3-Épicos) | [FT05](#_4-Funcionalidades) | [US16](#_5-histórias-de-usuário) | SHOULD | RF14            |
| [E03](#_3-Épicos) | [FT06](#_4-Funcionalidades) | [US17](#_5-histórias-de-usuário) | COULD  | RF13            |
| [E03](#_3-Épicos) | [FT06](#_4-Funcionalidades) | [US18](#_5-histórias-de-usuário) | COULD  | RF13            |
| [E03](#_3-Épicos) | [FT06](#_4-Funcionalidades) | [US19](#_5-histórias-de-usuário) | COULD  | RF21            |
| [E03](#_3-Épicos) | [FT07](#_4-Funcionalidades) | [US20](#_5-histórias-de-usuário) | SHOULD | RF22            |
| [E03](#_3-Épicos) | [FT07](#_4-Funcionalidades) | [US21](#_5-histórias-de-usuário) | SHOULD | RF22            |
| [E04](#_3-Épicos) | [FT08](#_4-Funcionalidades) | [US22](#_5-histórias-de-usuário) | MUST   | RF08            |
| [E04](#_3-Épicos) | [FT09](#_4-Funcionalidades) | [US23](#_5-histórias-de-usuário) | MUST   | RF08            |
| [E04](#_3-Épicos) | [FT09](#_4-Funcionalidades) | [US24](#_5-histórias-de-usuário) | MUST   | RF08            |
| [E04](#_3-Épicos) | [FT09](#_4-Funcionalidades) | [US25](#_5-histórias-de-usuário) | MUST   | RF08            |
| [E05](#_3-Épicos) | [FT10](#_4-Funcionalidades) | [US26](#_5-histórias-de-usuário) | COULD  | RF03            |
| [E05](#_3-Épicos) | [FT10](#_4-Funcionalidades) | [US27](#_5-histórias-de-usuário) | MUST   | RF09            |
| [E05](#_3-Épicos) | [FT11](#_4-Funcionalidades) | [US28](#_5-histórias-de-usuário) | WOULD  | RF05            |

## 8. Mapeamento das Histórias de Usuário

<p align='center'>
    <img src='assets/images/backlog/MapeamentoDeHistoriasDeusuario.png' width=100% height=auto>
   
    <figcaption align='center'>
        <b>Figura 2: Parte do mapeamento das histórias</b>
        <br>
    </figcaption>

Clique aqui para melhor visualizar nosso
[Mapeamento de Histórias de Usuário](https://miro.com/app/board/uXjVODr3z4g=/?invite_link_id=850072576590).

</p>

## 9. Requisitos Não Funcionais

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

## 10. Referências

> - LEFFINGWELL, Dean; Agile Software Requirements: Lean Requirements Practices for Teams, Programs, and Enterprise. 1. ed. Boston: Pearson, 2011.
> - WIEGERS, Karl; BEATTY, Joy; Software Requirements: Best practices. 3. ed; Microsoft Press, 2013
> - Backlog do Produto. Animalesco. Disponível em: https://unbarqdsw2021-1.github.io/2021.1_G01_Animalesco_docs/#/pages/backlog-do-produto (Último acesso em 01/02/2022)
>   [3] Lei Geral de Proteção de Dados Pessoais(LGPD). 14 de Agosto 2018. (http://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei/l13709.htm). Acesso em 18 de Fevereiro de 2022.

</div>

### Histórico de versão

|    Data    | Versão |              Autor              |                       Descrição                        |
| :--------: | :----: | :-----------------------------: | :----------------------------------------------------: |
| 01/02/2022 |  0.1   |        Fernando Miranda         |          Adicionada introdução e Referências           |
| 01/02/2022 |  1.0   |        Fernando Miranda         |          Adicionada versão inicial do Backlog          |
| 18/02/2022 |  2.0   |  Rodrigo Balbino e João Victor  |          Refatoração e priorização do backlog          |
| 19/02/2022 |  2.1   |        Fernando Miranda         |        Adicionados links entre tabelas/paginas         |
| 20/03/2022 |  2.2   | Rodrigo Balbino e Álvaro Gouvea |      Refatorando tabela das Histórias de usuário       |
| 20/03/2022 |  2.3   | Rodrigo Balbino e Álvaro Gouvea | Adicionando Tasks e Mapeamento de Histórias de usuário |
