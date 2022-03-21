# <center> GOFs Comportamentais

<div align="justify">

## 1. Introdução

Os padrões de projeto foram criados a partir da necessidade de se agilizar o projeto, no sentido de explicitar claramente padrões nos quais ja foram utilizados em outros projetos e de toda forma são recorrentes, assim evitando retrabalho. Portanto o uso de padrões de projetos ajuda a reduzir o tempo de desenvolvimento e aumentar a qualidade do código de maneira geral. Eles são divididos em tres frentes: criacionais, estruturais e comportamentais, nesse documento iremos falar dos padrões de projetos comportamentais que seguiremos no desenvolvimento desse projeto. Os padrões de projetos comportamentais focam nos algoritmos e na designação de responsabilidades entre os objetos. Sendo eles:

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

## 2. Chain of Responsibility

<div align="justify"> Esse padrão consiste na utilização de vários objetos(handlers) para tratar requisições. Portanto se trata de uma cadeia de objetos que vao tratando as requisições sequencialmente. Um exemplo de uso do padrão Chain of Responsibility é o tratamento de requisições de um banco de dados, onde cada requisição vai para um handler, e o handler vai tratar a requisição e enviar para o proximo handler, até chegar no ultimo handler que trata a requisição.  
</div>
<br>
<div align="justify"> Esse padrão pode ser utilizado para evitar o acoplamento do remetente com o destinatário, encadeando os handlers, passando a solicitação pela cadeia ate que a requisição seja tratada. Também pode ser utilizado quando a requisição precisa passar por uma sequencia de handlers, onde podem ocorre varias dinâmicas diferentes no jeito de utilizar os handlers que va de acordo com a logica da implementação, cada handler pode realizar uma operação e passar para o proximo, um handler pode também tratar a requisição e finaliza-la antes de terminar a sequencia, assim como também pode ocorrer de finalizar a sequencia visto que nao foi possível tratar a requisição ali e a sequencia nao iria mais funcionar, assim ja interrompendo a cadeia ali. Portanto resumindo em tópicos casos onde seriam interessante aplicar o chain of responsibility, seria:

- Evitar o acoplamento do remetente com o destinatário.
- Tratar requisições de forma sequencial de maneira menos rígida, visto que esse permite o remanejamento na ordem dos handlers.
- Quando se quer aplicar o principio de responsabilidade única, onde cada handler é responsável por uma única operação.
- Principio aberto/fechado, onde é possível adicionar novos handlers sem quebrar o código cliente existente.

</div>

<div align="justify"> Segue abaixo um exemplo de uso do padrão Chain of Responsibility, do site refactoring guru, em python:

```Python
from __future__ import annotations
from abc import ABC, abstractmethod
from typing import Any, Optional


class Handler(ABC):
    """
    The Handler interface declares a method for building the chain of handlers.
    It also declares a method for executing a request.
    """

    @abstractmethod
    def set_next(self, handler: Handler) -> Handler:
        pass

    @abstractmethod
    def handle(self, request) -> Optional[str]:
        pass


class AbstractHandler(Handler):
    """
    The default chaining behavior can be implemented inside a base handler
    class.
    """

    _next_handler: Handler = None

    def set_next(self, handler: Handler) -> Handler:
        self._next_handler = handler
        # Returning a handler from here will let us link handlers in a
        # convenient way like this:
        # monkey.set_next(squirrel).set_next(dog)
        return handler

    @abstractmethod
    def handle(self, request: Any) -> str:
        if self._next_handler:
            return self._next_handler.handle(request)

        return None


"""
All Concrete Handlers either handle a request or pass it to the next handler in
the chain.
"""


class MonkeyHandler(AbstractHandler):
    def handle(self, request: Any) -> str:
        if request == "Banana":
            return f"Monkey: I'll eat the {request}"
        else:
            return super().handle(request)


class SquirrelHandler(AbstractHandler):
    def handle(self, request: Any) -> str:
        if request == "Nut":
            return f"Squirrel: I'll eat the {request}"
        else:
            return super().handle(request)


class DogHandler(AbstractHandler):
    def handle(self, request: Any) -> str:
        if request == "MeatBall":
            return f"Dog: I'll eat the {request}"
        else:
            return super().handle(request)


def client_code(handler: Handler) -> None:
    """
    The client code is usually suited to work with a single handler. In most
    cases, it is not even aware that the handler is part of a chain.
    """

    for food in ["Nut", "Banana", "Cup of coffee"]:
        print(f"\nClient: Who wants a {food}?")
        result = handler.handle(food)
        if result:
            print(f"  {result}", end="")
        else:
            print(f"  {food} was left untouched.", end="")


if __name__ == "__main__":
    monkey = MonkeyHandler()
    squirrel = SquirrelHandler()
    dog = DogHandler()

    monkey.set_next(squirrel).set_next(dog)

    # The client should be able to send a request to any handler, not just the
    # first one in the chain.
    print("Chain: Monkey > Squirrel > Dog")
    client_code(monkey)
    print("\n")

    print("Subchain: Squirrel > Dog")
    client_code(squirrel)
```

</div>

<!-- Braz -->
<!-- Explicação do que é o Gof -->
<!-- Por quê utilizar o Gof -->
<!-- Exemplo do Gof aplicado em código -->

## 3. Iterator

 <div align= "justify">  Essa padrão permite que nós passemos por elementos de uma coleção sem evidenciar a representação dele, que poderia ser um vetor, árvore, pilha, lista e etc. A principal ideia é descobrir o comportamento de travessia da coleção no objeto que chamamos de Iterator.</div>

<div align= "justify"> O iterator guarda todos os detalhes da travessia, como por exemplo a posição atual e quantos elementos existem até o final. Assim vários iterators podem passar uns pelos outros ao mesmo tempo, independentemente.
</div>

 <div align= "justify"> Os iterators implementam uma mesma interface, isso torna o código do cliente compatível com qualquer tipo de coleção ou qualquer algoritmo de travessia desde que tenha um iterator adequado. Se for necessário uma travessia especial, deve-se criar uma nova classe iterator sem precisar mudar o cliente ou coleção</div>

<div align="justify"> Segue um exemplo de uso do iterator pattern em Golang, exemplo do site refactoring guru . </div>

```Golang
//collection.go: Collection
package main

type collection interface {
    createIterator() iterator
}


//userCollection.go: Concrete collection
package main

type userCollection struct {
    users []*user
}

func (u *userCollection) createIterator() iterator {
    return &userIterator{
        users: u.users,
    }
}

//iterator.go: Iterator
package main

type iterator interface {
    hasNext() bool
    getNext() *user
}

//userIterator.go: Concrete iterator
package main

type userIterator struct {
    index int
    users []*user
}

func (u *userIterator) hasNext() bool {
    if u.index < len(u.users) {
        return true
    }
    return false

}
func (u *userIterator) getNext() *user {
    if u.hasNext() {
        user := u.users[u.index]
        u.index++
        return user
    }
    return nil
}

//user.go: Client code
package main

type user struct {
    name string
    age  int
}

//main.go: Client code
package main

import "fmt"

func main() {

    user1 := &user{
        name: "a",
        age:  30,
    }
    user2 := &user{
        name: "b",
        age:  20,
    }

    userCollection := &userCollection{
        users: []*user{user1, user2},
    }

    iterator := userCollection.createIterator()

    for iterator.hasNext() {
        user := iterator.getNext()
        fmt.Printf("User is %+v\n", user)
    }
}
```

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

<div align="justify">   O Strategy é um padrão de projeto comportamental, o seu objetivo é permitir que diferentes algorítmos de uma mesma família, entende-se, resolvem o mesmo problema, sejam escolhidos e tempo de execução. </div>

<div align="justify">   De inicio isso pode parecer redundante, 'por que escolher entre diferentes algoritmos se todos resolvem o mesmo problema?'. De forma geral, o objetivo é otimização baseada em situações específicas e mmudança de contexto.
Para o primeiro caso podemos pensar em uma situação em que um algoritmo de exige ordenação de dados que são possivelmente todos inteiros ou não, caso todos os elementos são inteiros, usamos o gravity sort, caso tenha valores ponto flutuante, usamos o merge sort.
No caso de mudança de contexto podemos pensar em uma aplicação em que uma classe de forma geométrica que pode se especilizar em triangulo, quadrado e outras formas, podemos usar o strategy para definir o funcionamento de um método getArea(), que usará diferentes formulas, a depender do contexto da forma geométrica a que pertence.
</div>

<div align="justify"> Segue um exemplo de uso do strategy pattern em python, exemplo do site refactoring guru . </div>

```Python
from __future__ import annotations
from abc import ABC, abstractmethod
from typing import List


class Context():
    """
    The Context defines the interface of interest to clients.
    """

    def __init__(self, strategy: Strategy) -> None:
        """
        Usually, the Context accepts a strategy through the constructor, but
        also provides a setter to change it at runtime.
        """

        self._strategy = strategy

    @property
    def strategy(self) -> Strategy:
        """
        The Context maintains a reference to one of the Strategy objects. The
        Context does not know the concrete class of a strategy. It should work
        with all strategies via the Strategy interface.
        """
        return self._strategy

    @strategy.setter
    def strategy(self, strategy: Strategy) -> None:
        """
        Usually, the Context allows replacing a Strategy object at runtime.
        """

        self._strategy = strategy

    def do_some_business_logic(self) -> None:
        """
        The Context delegates some work to the Strategy object instead of
        implementing multiple versions of the algorithm on its own.
        """
        # ...

        print("Context: Sorting data using the strategy (not sure how it'll do it)")
        result = self._strategy.do_algorithm(["a", "b", "c", "d", "e"])
        print(",".join(result))

        # ...

class Strategy(ABC):
    """
    The Strategy interface declares operations common to all supported versions
    of some algorithm.

    The Context uses this interface to call the algorithm defined by Concrete
    Strategies.
    """

    @abstractmethod
    def do_algorithm(self, data: List):
        pass

"""
Concrete Strategies implement the algorithm while following the base Strategy
interface. The interface makes them interchangeable in the Context.
"""

class ConcreteStrategyA(Strategy):
    def do_algorithm(self, data: List) -> List:
        return sorted(data)


class ConcreteStrategyB(Strategy):
    def do_algorithm(self, data: List) -> List:
        return reversed(sorted(data))


if __name__ == "__main__":
    # The client code picks a concrete strategy and passes it to the context.
    # The client should be aware of the differences between strategies in order
    # to make the right choice.

    context = Context(ConcreteStrategyA())
    print("Client: Strategy is set to normal sorting.")
    context.do_some_business_logic()
    print()

    print("Client: Strategy is set to reverse sorting.")
    context.strategy = ConcreteStrategyB()
    context.do_some_business_logic()
```
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
> Oseberg S., Fredrik. The modern guide to React state patterns, 2021. Disponível em:<https://blog.logrocket.com/modern-guide-react-state-patterns/>. Acesso em 20 mar. de 2022.1
> Source Making. State Design Pattern, 2021. Disponível em: <https://sourcemaking.com/design_patterns/state>. Acesso em 20 mar. de 2022.1
> GeeksforGeeks. State Design Pattern, 01 Sep, 2021. Disponível em: <https://www.geeksforgeeks.org/state-design-pattern/>. Acesso em 20 mar. de 2022.1
> Refactoring Guru. Strategy in python:
<https://refactoring.guru/design-patterns/strategy/python/example#example-0--main-py>. Acesso em 20 mar. de 2022.1
> Refactoring Guru. Iterator in Golang:
<https://refactoring.guru/design-patterns/iterator/go/example>. Acesso em 20 mar. de 2022.1

</div>

### Histórico de versão

|    Data    | Versão |                     Autor                     |              Descrição              |
| :--------: | :----: | :-------------------------------------------: | :---------------------------------: |
| 19/03/2022 |  0.1   | Rodrigo Balbino, Ariel Vieira, Guilherme Braz |        Criação do documento         |
| 20/03/2022 |  0.2   | Rodrigo Balbino, Ariel Vieira, Guilherme Braz |           Adição da Introdução      |
| 20/03/2022 |  0.3   | Rodrigo Balbino, Ariel Vieira, Guilherme Braz |           Adição do State           |
| 20/03/2022 |  0.4   | Rodrigo Balbino, Ariel Vieira, Guilherme Braz | Adição do texto inicial do Iterator |
| 20/03/2022 |  0.5   | Rodrigo Balbino, Ariel Vieira, Guilherme Braz | Adição do strategy pattern |
| 20/03/2022 |  0.6   | Rodrigo Balbino, Ariel Vieira, Guilherme Braz | Adição do exemplo do iterator pattern |
| 20/03/2022 |  0.7   | Rodrigo Balbino, Ariel Vieira, Guilherme Braz | Adição do chain of responsibility |
