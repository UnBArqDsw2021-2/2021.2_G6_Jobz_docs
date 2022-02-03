# MoSCoW

## 1. Introdução

<p style="text-indent: 40px; align="justify"> MoSCoW é uma técnica de análise de de requisitos, que tem como objetivo de atribuir valores, como representado na <a href="#Figura1">Figura 1</a>, que indicam qual a importância de cada funcionalidade, de acordo com o valor agregado a ela em relação ao produto final.  
  
Durante o processo de priorização, cada funcionalidade é avaliada com relação a sua importância e recebe uma atribuição que pode ser:</p>

- **M**ust: Funcionalidade tem alto valor agregadom, se o produto não contiver esta funcionalidade ele não terá sucesso, deve ter prioridade sobre as outras no processo de implementação.
- **S**hould: Requisito que tem importância mas não é essencial, caso não seja implementado impactará a satisfação do cliente.
- **C**ould: Requisito que é apenas desejável para o produto, requisito que deve ser implementado somente se ouver tempo e os recursos permitam.
- **W**ould ou **W**on't: Requisito dispensável, que pode ser adicionado em outro momento ou até mesmo em outros projetos, mesmo que seja marcado como não importante a atribuição ainda indica que a funcionalidade foi avaliada.<a href="#Bibliografia">[1]</a>

<a id="Figura1">></a>

<img width="550" src="../assets/images/moscow.png" class="center" alt="Método de priorização MoSCoW">
<figcaption class="center"><center> Figura 1 - Descrição de cada prioridade.<br>Fonte:[2] </center> </figcaption>

## 2. Metodologia

<p align="justify"> 
Na tabela foram identificados os metodos que originaram os requisitos, esses metodos são listados na coluna Técnica
</p>

|  ID  |                  Técnica                   |                              Requisito                               | Priorização |
| :--: | :----------------------------------------: | :------------------------------------------------------------------: | :---------: |
| RF01 | <a href="/introspeccao " >Introspecção</a> |                    Filtrar serviços por categoria                    |    COULD    |
| RF02 | <a href="/introspeccao " >Introspecção</a> |           Filtrar serviços por quantidade de contratações            |    COULD    |
| RF03 | <a href="/introspeccao " >Introspecção</a> |             Filtrar serviços por qualidade de avaliações             |    COULD    |
| RF04 | <a href="/introspeccao " >Introspecção</a> |         Receber notificação com lembrete do serviço marcado          |    WOULD    |
| RF05 | <a href="/introspeccao " >Introspecção</a> | Remarcar data do serviço, considerando certo período de antecedência |    MUST     |
| RF06 | <a href="/introspeccao " >Introspecção</a> |                       Cancelar serviço marcado                       |    MUST     |
| RF07 | <a href="/introspeccao " >Introspecção</a> |              Chat entre cliente e prestador de serviço               |    MUST     |
| RF08 | <a href="/introspeccao " >Introspecção</a> |                   Visualizar serviços disponíveis                    |    MUST     |
| RF09 | <a href="/introspeccao " >Introspecção</a> |                     Visualizar serviços marcados                     |    MUST     |
| RF10 | <a href="/introspeccao " >Introspecção</a> |                  Visualizar serviços já contratados                  |    MUST     |
| RF11 | <a href="/introspeccao " >Introspecção</a> |                   Favoritar prestador de serviços                    |   SHOULD    |
| RF12 | <a href="/introspeccao " >Introspecção</a> |                           Avaliar serviços                           |   SHOULD    |
| RF13 | <a href="/introspeccao " >Introspecção</a> |   Visualizar avaliações de clientes sobre um prestador de serviços   |   SHOULD    |
| RF14 | <a href="/introspeccao " >Introspecção</a> |                            Editar perfil                             |    COULD    |
| RF15 | <a href="/introspeccao " >Introspecção</a> |                    Denunciar prestador de serviço                    |   SHOULD    |
| RF16 | <a href="/introspeccao " >Introspecção</a> |                       Compartilhar um serviço                        |    WOULD    |
| RF17 | <a href="/introspeccao " >Introspecção</a> |                          Denunciar cliente                           |    COULD    |
| RF18 | <a href="/introspeccao " >Introspecção</a> |             Visualizar localização e endereço do cliente             |    MUST     |
| RF19 | <a href="/introspeccao " >Introspecção</a> |                  Visualizar seus serviços marcados                   |    COULD    |
| RF20 | <a href="/introspeccao " >Introspecção</a> |                  Cadastrar serviço e categorizá-lo                   |    MUST     |
| RF21 | <a href="/introspeccao " >Introspecção</a> |         Cadastrar horário disponivel para realizar o serviço         |    MUST     |
| RF22 | <a href="/introspeccao " >Introspecção</a> |             Visualizar localização e endereço do cliente             |    MUST     |

## 3 .Referências <a id="Bibliografia"></a>

[1] - VAZQUEZ, Carlos Eduardo; SIMÕES, Guilherme Siqueira; **Engenharia de Requisitos**: Software orientado ao negócio. 1. ed. Brasil: Brasport, 2016.  
[2] - CRRUX, @CrruxHQ. **he MoSCoW method is a prioritization technique used in management, business analysis, project management, and software development.** 17 out, 2019. Tweet.

## 4.Versionamento

<center>

|    Data    | Versão |      Autor      |                 Descrição                 |
| :--------: | :----: | :-------------: | :---------------------------------------: |
| 31/01/2022 |  0.1   | Antônio Aldisio | Criação do documento e adição dos itens 1 |
| 03/02/2022 |  0.2   | Antônio Aldisio |            Adição dos itens 2             |

</center>
