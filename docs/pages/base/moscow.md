# <center> MoSCoW

<div align="justify">

## 1. Introdução

MoSCoW é uma técnica de análise de de requisitos, que tem como objetivo de atribuir valores, como representado na Figura 1, que indicam qual a importância de cada funcionalidade, de acordo com o valor agregado a ela em relação ao produto final.

Durante o processo de priorização, cada funcionalidade é avaliada com relação a sua importância e recebe uma atribuição que pode ser:

- **M**ust: Funcionalidade tem alto valor agregadom, se o produto não contiver esta funcionalidade ele não terá sucesso, deve ter prioridade sobre as outras no processo de implementação.
- **S**hould: Requisito que tem importância mas não é essencial, caso não seja implementado impactará a satisfação do cliente.
- **C**ould: Requisito que é apenas desejável para o produto, requisito que deve ser implementado somente se ouver tempo e os recursos permitam.
- **W**ould ou **W**on't: Requisito dispensável, que pode ser adicionado em outro momento ou até mesmo em outros projetos, mesmo que seja marcado como não importante a atribuição ainda indica que a funcionalidade foi avaliada.[[1]](./pages/base/moscow?id=3.-referências)

<p align='center'>
    <img src='assets/images/moscow.png' width=40% height=auto>
    <figcaption align='center'>
        <b>Figura 1: Descrição MoSCoW</b>
        <br>
        <small>Fonte: CRRUX, @CrruxHQ</small>
    </figcaption>
</p>

## 2. Requisistos funcionais

|  ID  |                   Técnica                    |                 Requisito                 | Priorização |
| :--: | :------------------------------------------: | :---------------------------------------: | :---------: |
| RF01 |   [Brainstorm](./pages/base/brainstorm.md)   |             Cadastrar usuário             |    MUST     |
| RF02 | [Introspecção](./pages/base/introspeccao.md) |               Editar perfil               |    MUST     |
| RF03 | [Introspecção](./pages/base/introspeccao.md) | Chat entre cliente e prestador de serviço |    COULD    |
| RF04 |   [Brainstorm](./pages/base/brainstorm.md)   |        Notificação de agendamento         |   SHOULD    |
| RF05 |   [Brainstorm](./pages/base/brainstorm.md)   |           Compartilhar serviços           |    WOULD    |
| RF06 | [Questionário](./pages/base/questionario.md) |          Tutorial da plataforma           |   SHOULD    |
| RF07 |   [Brainstorm](./pages/base/brainstorm.md)   |     Visualizar histórico de serviços      |    MUST     |
| RF08 | [Questionário](./pages/base/questionario.md) |        Filtro de busca de serviços        |    MUST     |
| RF09 | [Introspecção](./pages/base/introspeccao.md) |      Visualizar serviços disponíveis      |    MUST     |
| RF10 |   [Brainstorm](./pages/base/brainstorm.md)   |              Agendar serviço              |    MUST     |
| RF11 | [Introspecção](./pages/base/introspeccao.md) |         Cancelar serviço marcado          |    MUST     |
| RF12 | [Introspecção](./pages/base/introspeccao.md) |         Remarcar data do serviço          |    COULD    |
| RF13 | [Introspecção](./pages/base/introspeccao.md) |             Avaliar serviços              |    COULD    |
| RF14 | [Introspecção](./pages/base/introspeccao.md) |      Denunciar prestador de serviço       |   SHOULD    |
| RF15 | [Introspecção](./pages/base/introspeccao.md) |      Favoritar prestador de serviços      |    COULD    |
| RF16 | [Questionário](./pages/base/questionario.md) | Favoritar categorias de serviço preferido |    COULD    |
| RF17 | [Introspecção](./pages/base/introspeccao.md) |             Cadastrar serviço             |    MUST     |
| RF18 |   [Brainstorm](./pages/base/brainstorm.md)   |           Categorizar serviços            |    COULD    |
| RF19 | [Introspecção](./pages/base/introspeccao.md) |   Visualizar serviços próprios marcados   |    MUST     |
| RF20 | [Introspecção](./pages/base/introspeccao.md) |     Visualizar informações do usuário     |    MUST     |
| RF21 | [Introspecção](./pages/base/introspeccao.md) |     Visualizar avaliações do usuário      |    COULD    |
| RF22 | [Introspecção](./pages/base/introspeccao.md) |             Denunciar usuário             |   SHOULD    |
| RF23 | [Questionário](./pages/base/questionario.md) |  Visualizar estatísticas sobre o serviço  |    COULD    |
| RF24 | [Questionário](./pages/base/questionario.md) |  Recomendação de serviços na plataforma   |    WOULD    |
| RF25 | [Questionário](./pages/base/questionario.md) |     Visualizar informações do Serviço     |    MUST     |

## 3. Referências

> [1] VAZQUEZ, Carlos Eduardo; SIMÕES, Guilherme Siqueira; **Engenharia de Requisitos**: Software orientado ao negócio. 1. ed. Brasil: Brasport, 2016

> [2] CRRUX, @CrruxHQ. **he MoSCoW method is a prioritization technique used in management, business analysis, project management, and software development.** 17 out, 2019. Tweet.

</div>

### Histórico de versão

|    Data    | Versão |             Autor             |                         Descrição                          |
| :--------: | :----: | :---------------------------: | :--------------------------------------------------------: |
| 31/01/2022 |  0.1   |        Antônio Aldisio        |         Criação do documento e adição dos itens 1          |
| 03/02/2022 |  0.2   |        Antônio Aldisio        |                     Adição dos itens 2                     |
| 04/02/2022 |  1.0   |        Antônio Aldisio        | Adição dos RF e RNF do questionário e brainstorm no item 2 |
| 18/02/2022 |  2.0   | Rodrigo Balbino e João Victor |                 Refatoração dos requisitos                 |
