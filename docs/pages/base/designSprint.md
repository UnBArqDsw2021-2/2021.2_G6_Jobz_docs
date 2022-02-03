<style>
* { margin: 0; padding: 0; }
.slider {
    display: block;
    height: auto;
    width: 200;
    margin: auto;
    margin-top: 20px;
    position: relative;
}

.slider li {
    list-style: none;
    position: absolute;
}

.slider img {
    margin: auto;
    height: 100%;
    width: 100%;
    vertical-align: top;
}

.slider input {
    display: none;
}

.slider label {
    background-color: #000;
    bottom: 10px;
    cursor: pointer;
    display: block;
    height: 10px;
    position: absolute;
    width: 10px;
    z-index: 10;
}

.slider li:nth-child(1) label {
    left: 10px;
}

.slider li:nth-child(2) label {
    left: 40px;
}

.slider li:nth-child(3) label {
    left: 70px;
}

.slider img {
    opacity: 0;
    visibility: hidden;
}

.slider li input:checked ~ img {
    opacity: 1;
    visibility: visible;
    z-index: 10;
}

</style>
# <center>Design Sprint

## 1. Introdução
O Design Sprint é um método desenvolvido pelo [Google Ventures](https://www.gv.com/sprint/) com o objetivo de realizar algumas etapas de suma importância para o projeto de forma ágil. O processo é feito durante de 5 dia, sendo que em cada dia é concluído um artefato, sendo eles:
- Unpack (entender);
- Sketch (esboçar);
- Decision (decidir);
- Prototype (protótipo);
- Test (testar).

## 2. Processo
Devido ao curto prazo para o desenvolvimento do projeto, a metodologia foi utilizada de forma que se adaptasse a realidade do grupo, produzindo o Design Sprint em um menor período de tempo e desconsiderando a etapa de teste devido ao fato de que a equipe não possui clientes reais.

### 2.1. Unpack
A etapa de entendimento do projeto foi feita durante cerca de 30 minutos utilizando a técnica de [Brainstorming]() com todos os integrantes da equipe, levantando funcionalidades e ideias sobre o projeto.

### 2.2. Sketch
Após a discussão sobre o Brainstorming foram levantadas diversas ideias que serviram como inspiração para a próxima etapa. Foi reservado cerca de 1 hora para a etapa de esboço, em que cada integrante da equipe produziu um Rich Picture.

<ul class="slider">
    <li>
        <input type="radio" id="slide1" name="slide" checked>
        <label for="slide1"></label>
        <img src="../../../assets/images/rich-Alvaro.jpeg" />
    </li>
    <li>
        <input type="radio" id="slide2" name="slide">
        <label for="slide2"></label>
        <img src="../../../assets/images/rich-antonio.jpeg" />
    </li>
    <li>
        <input type="radio" id="slide3" name="slide">
        <label for="slide3"></label>
        <img src="../../../assets/images/rich-ariel.png" />
    </li>
</ul>

### 2.3. Decision
Na etapa de decisão, a equipe voltou a se reunir por volta de 30 minutos e escolheu o [Rich Picture]() que melhor se adequa ao projeto, além de desenvolver um [Storyboard]().

### 2.4. Prototype
Por fim, a equipe trabalhou cerca de 2 horas na construção de um [Protótipo de Baixa/Média Fidelidade](), afim de representar as ideias levantadas pela equipe.


## 3. Referências 
>SERRANO, Milene. Design Sprint, 2021. Material apresentado na Disciplina de Arquitetura e Desenho de Software do curso de engenharia de software da UnB, FGA. Acesso em: 29 de janeiro de 2022.

>The Design Sprint - GV. Disponível em: <https://www.gv.com/sprint/>. Acesso em: 29 de janeiro de 2022.


## 4. Versionamento 
|    Data    | Versão |     Modificação      |    Autor(res)    |
|:----------:|:------:|:--------------------:|:----------------:|
| 30/01/2022 |   1.0  | Criação do documento | Lorrayne Cardozo |