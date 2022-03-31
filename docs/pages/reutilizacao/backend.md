# <center> Reutilização no BackEnd

<div align="justify">

## 1. Introdução
Segundo o [Perforce](https://www.perforce.com/blog/qac/what-code-reuse-code-reuse-best-practices), a reutilização de código é a prática de usar um código existente para uma nova função ou software. Porém, em seu desenvolvimento devem ser levados em consideração diversos fatores que garantam que o código tenha uma alta qualidade e possa ser reutilizado, por isso deve ser seguro, protegido e confiável. A ideia do reuso é evitar retrabalho no desenvolvimento de um novo projeto, levando em consideração trabalhos feitos anteriormente.

O desenvolvimento de um software é um processo que demanda bastante tempo e esforço, e a prática de reutilização de código é utilizada para otimizar esse processo, fazendo com que soluções previamente desenvolvidas sejam aproveitadas e implementadas em um novo contexto.

## 2. Django

O **Django** é utilizado para construção de aplicações web utilizando o padrão *model-template-view* (MTV) que mantém o código bem organizado em suas devidas camadas, e já oferece os padrões de projeto Alta Coesão e Baixo Acoplamento, organizando os métodos de forma bem definida e com suas respectivas responsabilidades. Desta forma, isso aumenta a qualidade do código e facilita sua reutilização. Além disso, sua principal convenção é o *Don't Repeat Yourself* (DRY), que em tradução livre significa *Não Seja Repetitivo*, visando aproveitar ao máximo o código criado, evitando duplicação e auxiliando em sua reutilização.

Já o **Django Rest Framework** é uma poderosa ferramenta para construção de API's, além de possuir um sistema de autenticação e serialização de dados. É de fácil reuso, pois os serviços fornecidos podem ser facilmente consumidos tanto por interfaces web quanto mobile.

<p align='center'>
    <img src='assets/images/reutilizacao/backend/django.png' width=25% height=auto>
    <figcaption align='center'>
        <b>Figura 1: Estrutura do BackEnd utilizando o framework Django.</b>
        <br>
        <small>Fonte: Autor</small>
    </figcaption>
</p>

## 3. Referências

> ALURA. Django e Django Rest: Diferenças e aplicações. Alura. Disponível em: <https://www.alura.com.br/artigos/django-django-rest-diferencas>. Acesso em: 27 Mar. 2022.

> DEVMEDIA. Reutilização de Software: Técnicas e Ferramentas. DevMedia. Disponível em: <https://www.devmedia.com.br/reutilizacao-de-software-revista-engenharia-de-software-magazine-39/21956>. Acesso em: 27 Mar. 2022.

> BELLAIRS, Richard. What Is Code Reuse? Code Reuse Best Practices. Perforce Software. Disponível em: <https://www.perforce.com/blog/qac/what-code-reuse-code-reuse-best-practices>. Acesso em: 27 Mar. 2022.


</div>

### Histórico de versão

|    Data    | Versão |           Autor(es)              |      Descrição       |
| :--------: | :----: | :------------------------------: | :------------------: |
| 27/03/2022 |  0.1   | Lorrayne Cardozo e Ariel Serafim | Criação do documento |