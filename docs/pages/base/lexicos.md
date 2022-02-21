# <center>Léxicos


## 1. Introdução

<p align = "justify"> &emsp;&emsp; Uma das principais técnicas utilizadas para a modelagem de um projeto é chamada de léxico. Esse artefato tem como objetivo igualar o conhecimento da equipe, descrevendo os símbolos e termos específicos relacionados ao tema de nossa aplicação. Sendo assim, o léxico é uma fonte de consulta para compreender todas as terminologias utilizadas pelo grupo durante o período de desenvolvimento do projeto.</p>
<p align = "justify"> &emsp;&emsp; Para esse projeto será utilizado a descrição de termos via léxico LAL(Léxico Ampliado da Linguagem), na qual serve para descrever os termos relacionados ao projeto. Assim, nossos léxicos serão apresentados seguindo a seguinte estrutura:
</p>

- **Classificação** determina se o léxico é do tipo objeto, verbo, ou estado.
- **Noção** apresenta o significado do símbolo, ou melhor, sua denotação.
- **Impacto** apresenta o efeito do símbolo na aplicação, ou melhor, sua conotação.

| Elemento          | Descrição               | Status      |
| ----------------- | ----------------------- |--------     | 
| **Classificação** | Objeto / Verbo / Estado | Obrigatório |
| **Noção**         | Denotação               | Obrigatório |
| **Impacto**       | Conotação               | Obrigatório |
| **Sinônimo**      | Termo sinõnimo          | Opcional    |

## 2. Léxicos

### L01 - Usuário

| L01               | Usuário                                          |
| ----------------- | ------------------------------------------------ |
| **Classificação** | Objeto                                          |
| **Noção**         | Indivíduo que pretende utilizar o sistema.       |
| **Impacto**       | O usuário pode fazer [login](#l04-login). |
| **Sinônimo**      | -                                                |

### L02 - Prestador de Serviços

| L02               | Prestador de Serviços                                                                                                                          |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Objeto                                                                                                                                        |
| **Noção**         | [Usuário](#l01-usuário) que oferece serviços para outros usuários da plataforma.                                                        |
| **Impacto**       | Prestador de serviços pode gerar anúncios.<br>Prestador de serviços  pode cadastrar serviços. |
| **Sinônimo**      | -                                                                                                                                              |

### L03 - Cliente

| L03               | Cliente                                                                                                                                                                                                                                                                                                                            |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Objeto                                                                                                                                                                                                                                                                                                                            |
| **Noção**         | [Usuário](#l01-usuário) que utiliza o sistema com o intuito de contratar serviços de um [prestador de serviços](#l02-prestador-de-serviços).                                                                                                                                                                                     |
| **Impacto**       | Cliente pode efetuar pagamentos.<br>Cliente pode deixar avaliações.<br>Cliente pode [recomendar](#l10-recomendar-serviço) [prestadores de serviço](#l02-prestador-de-serviços).<br>Cliente pode realizar [pesquisas](#l06-pesquisar). |
| **Sinônimo**      | -                                                                                                                                                                                                                                                                                                                                  |

### L04 - Login

| L04               | Login                                                                                                                        |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Verbo                                                                                                                        |
| **Noção**         | Ato de ligação com a estrutura do site, que dá acesso ao perfil individual correspondente ao [usuário](#l01-usuário). |
| **Impacto**       | [Usuário](#l01-usuário) pode se utilizar das funcionalidades do site.                                                                        |
| **Sinônimo**      | -                                                                                                                            |

### L05 - Avaliar

| L05               | Avaliar                                                                                                       |
| ----------------- | ------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Verbo                                                                                                         |
| **Noção**         | Ato de mensurar o nível de satisfação que o [cliente](#l03-cliente) obteve com o serviço prestado.     |
| **Impacto**       | [Cliente](#l03-cliente) altera a avaliação geral de um [prestador de serviços](#l02-prestador-de-serviços). |
| **Sinônimo**      | -                                                                                                             |

### L06 - Pesquisar

| L06               | Pesquisar                                                                                                |
| ----------------- | -------------------------------------------------------------------------------------------------------- |
| **Classificação** | Verbo                                                                                                    |
| **Noção**         | Ato de recolhimento de informações relevantes ao desejo de um [usuário](#l01-usuário) do sistema. |
| **Impacto**       | Melhora a visibilidade de áreas de aptitude e [prestadores de serviço](#l02-prestador-de-serviços).          |
| **Sinônimo**      | Buscar                                                                                                   |

### L07 - Categorias de Serviço

| L07               | Categorias de Serviço                                                                      |
| ----------------- | ------------------------------------------------------------------------------------------ |
| **Classificação** | Objeto                                                                                    |
| **Noção**         | Categoria que tem como objetivo de aglomerar serviços de propósito semelhante ou idêntico. |
| **Impacto**       | Facilita a busca do [cliente](#l03-cliente) por um serviço específico.              |
| **Sinônimo**      | -                                                                                          |

### L08 - Filtro de Busca

| L08               | Filtro de Busca                                                                                                                                    |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Objeto                                                                                                                                             |
| **Noção**         | [Categorias de serviço](#l07-categorias-de-serviço) que tem como objetivo auxiliar o [usuário](#l01-usuário) em uma busca refinada de serviços. |
| **Impacto**       | Facilita que o [cliente](#l03-cliente) encontre o [prestador de serviços](#l02-prestador-de-serviços) que atende as suas necessidades.             |
| **Sinônimo**      | -                                                                                                                                                  |

### L09 - Agendar Serviço

| L09               | Agendar Serviço                                                                                                                   |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Verbo                                                                                                                             |
| **Noção**         | Ato de marcar dia e horário em que o [prestador de serviços](#l02-prestador-de-serviços) irá visitar o [cliente](#l03-cliente). |
| **Impacto**       | [Cliente](#l03-cliente) e [prestador de serviços](#l02-prestador-de-serviços) receberão [notificações](#l11-notificar-usuário) sobre o evento.                                                                                                                                 |
| **Sinônimo**      | Marcar visita<br>Agendamento                                                                                                      |

### L10 - Recomendar Serviço

| L10               | Recomendar Serviço                                                                                                                        |
| ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Verbo                                                                                                                                     |
| **Noção**         | Ato de indicar um [prestador de serviços](#l02-prestador-de-serviços) específico para outro [cliente](#l03-cliente) cadastrado no site. |
| **Impacto**       | [Cliente](#l03-cliente) pode recomendar diretamente para outro [usuário](#l01-usuário), o [prestador de serviços](#l02-prestador-de-serviços) que já o atendeu.                   |
| **Sinônimo**      | -                                                                                                                                         |

### L11 - Notificar Usuário

| L11               | Notificar Usuário                                                                                                                                  |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Verbo                                                                                                                                              |
| **Noção**         | Ato de alertar os [usuários](#l01-usuário) atrelados a um [serviço agendado](#l09-agendar-serviço) sobre a sua existencia.                                          |
| **Impacto**       | Ajuda o [cliente](#l03-cliente) e o [prestador de serviços](#l02-prestador-de-serviços) a não se esqueçam do [agendamento](#l09-agendar-serviço). |
| **Sinônimo**      | -                                                                                                                                                  |

### L12 - Chat

| L12               | Chat                                                                                                                               |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Objeto                                                                                                                             |
| **Noção**         | Ferramenta de conversa informal e direta entre [usuários](#l01-usuário) da plataforma.                                                             |
| **Impacto**       | [Cliente](#l03-cliente) pode se comunicar, pela plataforma, diretamente com o [prestador de serviços](#l02-prestador-de-serviços). |
| **Sinônimo**      | -                                                                                                                                  |

## 3. Referências

> SERRANO, Milene; Requisitos - Aula - PROJETO E DESENHO DE SOFTWARE;

> SAYÃO, Miriam; DE CARVALHO, Gustavo R. Construção do léxico de aplicações – PUC-Rio. Rio de Janeiro. 2006. Disponível em: http://www.nilc.icmc.usp.br/til/til2006/0030.pdf

  
  
### Histórico de versão


|    Data    | Versão |    Autor    |      Descrição       |
| :--------: | :----: | :---------: | :------------------: |
| 26/01/2022 |  0.1   | Fernando Miranda |  Criação do documento   |  
| 28/01/2022 |  1.0   | Rodrigo Balbino | Adição dos textos de introdução e Bibliografia    | 
| 28/01/2022 |  1.1   | Fernando Miranda | Correções de hyperlinks e classificação   |  
| 29/01/2022 |  1.3   | Lorrayne Cardozo | Revisão do documento       |    
| 29/01/2022 |  1.4   | Fernando Miranda | Correções de hyperlinks e revisão de texto        |  
| 04/02/2022 |  1.5   | Ariel Serafim | Correções de hyperlinks e revisão de texto        |  
| 21/02/2022 |  1.6   | Antonio Aldisio | Adequação do padrão      |  
