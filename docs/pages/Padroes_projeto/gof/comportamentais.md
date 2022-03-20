# <center> GOFs Comportamentais

<div align="justify">

## 1. Introdução

Os padrões de projeto foram criados a partir da necessidade de se agilizar o projeto, no sentido de explicitar claramente padrões os quais ja foram utilizados em outros projetos e de toda forma sao recorrentes, assim evitando retrabalho. Portanto o uso de padrões de projetos ajudam a reduzir o tempo de desenvolvimento e aumentar a qualidade do código de maneira geral. Eles sao divididos em tres frentes: criacionais, estruturais e comportamentais, nesse documento iremos falar dos padrões de projetos comportamentais que seguiremos no desenvolvimento desse projeto. Os padrões de projetos comportamentais focam nos algoritmos e na designação de responsabilidades entre os objetos. Sendo eles:

- Chain of Responsibility
- Command
- Iterator
- Mediator
- Memento
- Observer
- State
- Strategy
- Template Method
- Visitor

## 2. Chain of Responsability

<!-- Braz -->
<!-- Explicação do que é o Gof -->
<!-- Por quê utilizar o Gof -->
<!-- Exemplo do Gof aplicado em código -->

## 3. Iterator

<!-- Explicação do que é o Gof -->
<!-- Por quê utilizar o Gof -->
<!-- Exemplo do Gof aplicado em código -->

## 4. State

 <div align="">   O state é um padrão de projeto comportamental, o seu objetivo é permitir que um objeto seja capaz de mudar seu comportamento quando seu estado interno muda. É como se o objeto realizasse uma mudança de classes. Assim, esse padrão resolve o problema de como fazer um comportamento depender de um estado predeterminado e finito de opções. </div>
 <br>
 <div align="justify"> Especificamente em nosso projeto, foi utilizado o Framework React.js para o desenvolvimento do Front-end. Dessa forma, o React utiliza o padrão de projeto state por meio do react-hook, que permite utilizar esse padrão com o hook chamado 'useState', Esse hook é criado para modificar o valor interno de uma variável para assim conseguir mudar seu comportamento.</div> <br>
 Exemplo de uso do State em nosso projeto:

```Javascript

  const [data, setData] = useState({
    name: '',
    email: '',
    password: ''
  })

   axios.post(url, {
      name: data.name,
      email: data.email,
      password: data.password
    }).then(res => {
      console.log(res.data)
    })
  }

  function handle(e) {
    const newdata = { ...data }
    newdata[e.target.id] = e.target.value
    setData(newdata)
    console.log(newdata)
  }

<Input onChange={e => handle(e)} id="name" placeholder="NOME" type="text" required />
<Input onChange={e => handle(e)} id="email" placeholder="EMAIL" type="email" required />
<Input onChange={e => handle(e)} id="password" placeholder="SENHA" type="password" required />
```

<div align="justify"> Por meio desse código exemplo retirado de nosso projeto, conseguimos monitorar as adições feitas pelo usuário em cada um dos três campos de input: name, email e password. Sempre quando um caractere é escrito, a função handle recebe essa modificação e envia como um novo estado da varíavel interna de data. Para enfim, conseguirmos realizar a requisição POST de cadastro. </div>

## 5. Strategy

<!-- Ariel -->
<!-- Explicação do que é o Gof -->
<!-- Por quê utilizar o Gof -->
<!-- Exemplo do Gof aplicado em código -->

<!--
PADRÃO PARA ADICIONAR IMAGENS:

### 2.1 ADIÇÃO DE IMAGENS
<p align='center'>
    <img src='assets/images/guia_estilo/logo.png' width=40% height=auto>
    <figcaption align='center'>
        <b>Figura 1: DESCRIÇÃO DA IMAGEM</b>
        <br>
        <small>Fonte: FONTE DA IMAGEM (AUTOR)</small>
    </figcaption>
</p>
-->

## 6. Referências

> Padrões de projeto comportamentais. Refactoring Guru, 2014. Disponível em: <https://refactoring.guru/pt-br/design-patterns/behavioral-patterns>. Acesso em: 19 mar. de 2022.1
> Oseberg S., Fredrik. The modern guide to React state patterns, 2021. Disponível em:https://blog.logrocket.com/modern-guide-react-state-patterns/. Acesso em 20 mar. de 2022.1
> Source Making. State Design Pattern, 2021. Disponível em: https://sourcemaking.com/design_patterns/state. Acesso em 20 mar. de 2022.1
> GeeksforGeeks. State Design Pattern, 01 Sep, 2021. Disponível em: https://www.geeksforgeeks.org/state-design-pattern/. Acesso em 20 mar. de 2022.1

</div>

### Histórico de versão

|    Data    | Versão |                     Autor                     |      Descrição       |
| :--------: | :----: | :-------------------------------------------: | :------------------: |
| 19/03/2022 |  0.1   | Rodrigo Balbino, Ariel Vieira, Guilherme Braz | Criação do documento |
| 20/03/2022 |  0.2   | Rodrigo Balbino, Ariel Vieira, Guilherme Braz |   Adição do State    |
