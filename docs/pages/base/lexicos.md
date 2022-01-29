# <center>Léxicos


## 1. Introdução

<p align = "justify"> &emsp;&emsp; Uma das principais técnicas utilizadas para a modelagem de um projeto é chamada de léxico. Esse artefato tem como objetivo igualar o conhecimento da equipe, descrevendo os símbolos e termos específicos relacionados ao tema de nossa aplicação. Sendo assim, o léxico é uma fonte de consulta para compreender todas as terminologias utilizadas pelo grupo durante o período de desenvolvimento do projeto.</p>
<p align = "justify"> &emsp;&emsp; Para esse projeto será utilizado a descrição de termos via léxico LAL(Léxico Ampliado da Linguagem), na qual serve para descrever os termos relacionados ao projeto. Assim, nossos léxicos serão apresentados seguindo a seguinte estrutura:
</p>

- **Classificação** determina se o léxico é do tipo objeto, verbo, ou estado.
- **Noção** apresenta o significado do símbolo, ou melhor, sua denotação.
- **Impacto** apresenta o efeito do símbolo na aplicação, ou melhor, sua conotação.

| Número Léxico     | Nome do léxico          |
| ----------------- | ----------------------- |
| **Classificação** | Objeto / Verbo / Estado |
| **Noção**         | Denotação               |
| **Impacto**       | Conotação               |
| **Sinônimo**      | Opcional                |

## 2. Léxicos

### L01 - Usuário <a id="Usuario"></a>

| L01               | Usuário                                          |
| ----------------- | ------------------------------------------------ |
| **Classificação** | Objeto                                          |
| **Noção**         | Indivíduo que pretende utilizar o sistema.       |
| **Impacto**       | O usuário pode fazer <a href="#Login">login</a>. |
| **Sinônimo**      | -                                                |

### L02 - Prestador de Serviços <a id="Prestador"></a>

| L02               | Prestador de Serviços                                                                                                                          |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Objeto                                                                                                                                        |
| **Noção**         | <a href="#Usuario">Usuário</a> que oferece serviços para outros usuários da plataforma.                                                        |
| **Impacto**       | <a href="#Prestador">Prestador de serviços</a> pode gerar anúncios.<br><a href="#Prestador">Prestador de serviços</a> pode cadastrar serviços. |
| **Sinônimo**      | -                                                                                                                                              |

### L03 - Cliente <a id="Cliente"></a>

| L03               | Cliente                                                                                                                                                                                                                                                                                                                            |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Objeto                                                                                                                                                                                                                                                                                                                            |
| **Noção**         | <a href="#Usuario">Usuário</a> que utiliza o sistema com o intuito de contratar serviços de um <a href="#Prestador">prestador de serviços</a>.                                                                                                                                                                                     |
| **Impacto**       | <a href="#Cliente">Cliente</a> pode efetuar pagamentos.<br><a href="#Cliente">Cliente</a> pode deixar avaliações.<br><a href="#Cliente">Cliente</a> pode <a href="#Recomendar">recomendar</a> <a href="#Prestador">prestadores de serviços</a>.<br><a href="#Cliente">Cliente</a> pode realizar <a href="#Pesquisar">pesquisas</a>. |
| **Sinônimo**      | -                                                                                                                                                                                                                                                                                                                                  |

### L04 - Login <a id="Login"></a>

| L04               | Login                                                                                                                        |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Verbo                                                                                                                        |
| **Noção**         | Ato de ligação com a estrutura do site, que dá acesso ao perfil individual correspondente ao <a href="#Usuario">usuário</a>. |
| **Impacto**       | Usuário pode se utilizar das funcionalidades do site.                                                                        |
| **Sinônimo**      | -                                                                                                                            |

### L05 - Avaliar <a id="Avaliar"></a>

| L05               | Avaliar                                                                                                       |
| ----------------- | ------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Verbo                                                                                                         |
| **Noção**         | Ato de mensurar o nível de satisfação que o <a href="#Cliente">Cliente</a> obteve com o serviço prestado.     |
| **Impacto**       | <a href="#Cliente">Cliente</a> altera a avaliação geral de um <a href="#Prestador">prestador de serviços</a>. |
| **Sinônimo**      | -                                                                                                             |

### L06 - Pesquisar <a id="Pesquisar"></a>

| L06               | Pesquisar                                                                                                |
| ----------------- | -------------------------------------------------------------------------------------------------------- |
| **Classificação** | Verbo                                                                                                    |
| **Noção**         | Ato de recolhimento de informações relevantes ao desejo de um <a href="#Usuario">usuário</a> do sistema. |
| **Impacto**       | Melhora a visibilidade de áreas de aptitude e <a href="#Prestador">prestadores de serviços</a>.          |
| **Sinônimo**      | Buscar                                                                                                   |

### L07 - Categorias de Serviço <a id="Categorias"></a>

| L07               | Categorias de Serviço                                                                      |
| ----------------- | ------------------------------------------------------------------------------------------ |
| **Classificação** | Objeto                                                                                    |
| **Noção**         | Categoria que tem como objetivo de aglomerar serviços de propósito semelhante ou identico. |
| **Impacto**       | Facilita a busca do <a href="#Cliente">cliente</a> por um serviço específico.              |
| **Sinônimo**      | -                                                                                          |

### L08 - Filtro de Busca <a id="Filtro"></a>

| L08               | Filtro de Busca                                                                                                                                    |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Objeto                                                                                                                                             |
| **Noção**         | <a href="#Categorias">Categorias de serviço</a> que tem como objetivo auxiliar o <a href="#Usuario">usuário</a> em uma busca refinada de serviços. |
| **Impacto**       | Facilita que o <a href="#Cliente">cliente</a> encontre o <a href="#Prestador">Prestador de serviços</a> que atende as suas exigências.             |
| **Sinônimo**      | -                                                                                                                                                  |

### L09 - Agendar Serviço <a id="Agendar"></a>

| L09               | Agendar Serviço                                                                                                                   |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Verbo                                                                                                                             |
| **Noção**         | Ato de marcar dia e horário em que o <a href="#Prestador">prestador de serviços</a> irá visitar o <a href="#Cliente">cliente</a>. |
| **Impacto**       | -                                                                                                                                 |
| **Sinônimo**      | Marcar visita<br>Agendamento                                                                                                      |

### L10 - Recomendar Serviço <a id="Recomendar"></a>

| L10               | Recomendar Serviço                                                                                                                        |
| ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Verbo                                                                                                                                     |
| **Noção**         | Ato de indicar um <a href="#Prestador">prestador de serviços</a> específico para outro <a href="#Cliente">cliente</a> cadastrado no site. |
| **Impacto**       | <a href="#Cliente">Cliente</a> pode recomendar diretamente para outro usuário, o prestador de serviço que já o atendeu.                   |
| **Sinônimo**      | -                                                                                                                                         |

### L11 - Notificar Usuário <a id="Notificar"></a>

| L11               | Notificar Usuário                                                                                                                                  |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Verbo                                                                                                                                              |
| **Noção**         | Ato de alertar os <a href="#Usuario">usuários</a> atrelados a um serviço agendado sobre a sua existencia.                                          |
| **Impacto**       | Ajuda o <a href="#Cliente">cliente</a> e o <a href="#Prestador">prestador de serviços</a> a não se esqueçam do <a href="#Agendar">agendamento</a>. |
| **Sinônimo**      | -                                                                                                                                                  |

### L12 - Chat <a id="Chat"></a>

| L12               | Chat                                                                                                                               |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| **Classificação** | Objeto                                                                                                                             |
| **Noção**         | Ferramenta de conversa informal e direta entre usuários da plataforma.                                                             |
| **Impacto**       | <a href="#Cliente">Cliente</a> pode se comunicar pela plataforma diretamente com o <a href="#Prestador">prestador de serviços</a>. |
| **Sinônimo**      | -                                                                                                                                  |

## 3. Referências

> SERRANO, Milene; Requisitos - Aula - PROJETO E DESENHO DE SOFTWARE;

> SAYÃO, Miriam; DE CARVALHO, Gustavo R. Construção do léxico de aplicações – PUC-Rio. Rio de Janeiro. 2006. Disponível em: http://www.nilc.icmc.usp.br/til/til2006/0030.pdf

## 4. Versionamento

| Versão | Data       | Modificação                                    | Autor            |
| :----: | ---------- | ---------------------------------------------- | ---------------- |
|  1.0   | 26/01/2022 | Criação do documento                           | Fernando Miranda |
|  1.1   | 28/01/2022 | Adição dos textos de introdução e Bibliografia | Rodrigo Balbino  |
|  1.2   | 28/01/2022 | Correções de hyperlinks e classificação        | Fernando Miranda |
| 1.3 | 29/01/2022 | Revisão do documento | Lorrayne Cardozo