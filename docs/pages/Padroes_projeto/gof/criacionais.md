# <center> GoFs Criacionais

<div align="justify">

## 1. Introdução

Padrões de projeto são soluções para problemas comuns que encontramos no desenvolvimento ou manutenção de um software. Iremos abordar os padrões criacionais, estes são padrões que lidam com mecanismos de criação de objetos, voltados a criar objetos de maneira adequada à situação. Eles ajudam a tornar um sistema independente de como seus objetos são criados, compostos e representados.[1](./pages/Padroes_projeto/gof/criacionais.md#_4-referências)

Conforme o código da aplicação tem o seu foco direcionado para a maior utilização de composição de objetos a aplicação dos padrões criacionais tende a tomar maior enfase, com isso a estruturação de código deixa de ser focada em um comportamento fixo e se volta mais para a definição de comportamentos básicos e fundamentais para o comportamento do software.[2](./pages/Padroes_projeto/gof/criacionais.md#_4-referências)

"Existem dois temas recorrentes nesses padrões. Primeiro, todos eles encapsulam conhecimento sobre qual classe concreta o sistema usa. Segundo, eles escondem como instancias dessas classes são criadas e construidas." [(Gamma, 1994, p.94)](./pages/Padroes_projeto/gof/criacionais.md#_4-referências) Com isso os padrões criacionais criam flexibilidade na criação de objetos dentro de um software.

Neste documento iremos abordar os seguintes **GoFs Criacionais** que foram adotados pela equipe:

  - [Builder](./pages/Padroes_projeto/gof/criacionais.md#_3-builder)
  - [Factory](./pages/Padroes_projeto/gof/criacionais.md#_2-Factory)
  - [Singleton](./pages/Padroes_projeto/gof/criacionais.md#_4-Singleton)


## 2. Factory

O método de fábrica é um padrão de design criacional que resolve o problema de criar objetos de produto sem especificar suas classes concretas, tendo o objetivo de facilitar a criação de objetos. O padrão **factory** se baseia na ideia de que é mais simples encontrar onde um determinado objeto está sendo instanciado, se isso for feito através de uma função central.

<p align='center'>
    <img src='assets/images/gofsCriacionais/exFactory.png' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 1: Exemplo de Factory</b>
        <br>
        <small>Fonte: https://refactoring.guru/pt-br/design-patterns/factory-method</small>
    </figcaption>
</p>

Como podemos perceber na [imagem 1](./pages/Padroes_projeto/gof/criacionais.md#_2-Factory), no padrão **factory** nos passamos apenas uma função, não nos importando onde o objeto está implementado nem como foi implementado.

Podemos observar no [trecho de código](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_BackEnd/blob/master/jobz/user/models.py) a seguir, uma implementação que está sendo utilizada pela equipe.


<!--

If you realize that you cannot track the objects created by your application because the code that creates them is in many different places instead of a single function/method, you should consider using the Factory Method pattern [Eckel08, page 187]. The Factory Method centralizes an object creation and tracking your objects becomes much more easier. Note that it is absolutely fine to create more than one Factory Method, and this is how it is typically done in practice. Each Factory Method logically groups the creation of objects that have similarities. For example, one Factory Method might be responsible for connecting you to different databases (MySQL, SQLite), another Factory Method might be responsible for creating the geometrical object that you request (circle, triangle), and so on.
-->

<p align='center'>
    <img src='assets/images/gofsCriacionais/codigo 1.png' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 2: Chamada da classe Factory</b>
    </figcaption>
</p>

Onde podemos observar que a chamada da classe **PersonManager** irá cuidar da criação de usuários.

<p align='center'>
    <img src='assets/images/gofsCriacionais/codigo2.png' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 3: Classe Factory</b>
    </figcaption>
</p>

## 3. Builder


Se tratando de um padrão de projeto criacional, o padrão builder tem "o objetivo de construir um objeto complexo a partir da sua representação, de tal forma que o mesmo processo de construção possa criar representações diferentes" [(Gamma, 1994, p.110)](./pages/Padroes_projeto/gof/criacionais.md#_4-referências) com esta sentença podemos dizer que o padrão **Builder** é um padrão de projeto que permite a você construir objetos complexos passo a passo, permitindo que um único código possa nos atender em diversas tarefas.

Como no exemplo do [trecho de código](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_BackEnd/blob/master/jobz/jobz/urls.py), onde o código de criação de [usuários](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_BackEnd/blob/master/jobz/user/models.py) e [serviços](https://github.com/UnBArqDsw2021-2/2021.2_G6_Jobz_BackEnd/blob/master/jobz/service/models.py) da nossa aplicação são tratados da mesma forma, mesmo se tratando de objetos ligeiramente diferentes, por um único método **register** que disponibiliza o acesso, a recuperação e a criação destas tabelas.


<p align='center'>
    <img src='assets/images/gofsCriacionais/codigo3.png' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 4: Metodo Builder</b>
    </figcaption>
</p>

<p align='center'>
    <img src='assets/images/gofsCriacionais/registro.png' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 5: Modelo de acesso criado pelo método register.</b>
    </figcaption>
</p>

## 4. Singleton

O padrão criacional singleton especifica que apenas uma instância da classe pode existir, e esta será utilizada por toda a aplicação. Dessa forma temos apenas um ponto de acesso global a esta instância da classe.
Ao utilizar Singleton temos mais controle sobre o acesso às propriedades e métodos de uma classe, e também reduzimos o consumo de memória desnecessário por utilizar várias instancias desnecessárias de uma classe.

<p align='center'>
    <img src='assets/images/gofsCriacionais/exSingleton.png' width=100% height=auto>
    <figcaption align='center'>
        <b>Figura 6: Estrutura de um Singleton.</b>
        <br>
        <small>Fonte: https://refactoring.guru/pt-br/design-patterns/singleton</small>
    </figcaption>
</p>

A figura acima demonstra a estutura de um singleton, onde a classe Singleton possui o método estático _getInstance_ que retorna a mesma instancia de sua própia classe.

Um exemplo de código usando o singleton em python:

```
class SingletonMeta(type):
    """
    The Singleton class can be implemented in different ways in Python. Some
    possible methods include: base class, decorator, metaclass. We will use the
    metaclass because it is best suited for this purpose.
    """

    _instances = {}

    def __call__(cls, *args, **kwargs):
        """
        Possible changes to the value of the `__init__` argument do not affect
        the returned instance.
        """
        if cls not in cls._instances:
            instance = super().__call__(*args, **kwargs)
            cls._instances[cls] = instance
        return cls._instances[cls]


class Singleton(metaclass=SingletonMeta):
    def some_business_logic(self):
        """
        Finally, any singleton should define some business logic, which can be
        executed on its instance.
        """

        # ...


if __name__ == "__main__":
    # The client code.

    s1 = Singleton()
    s2 = Singleton()

    if id(s1) == id(s2):
        print("Singleton works, both variables contain the same instance.")
    else:
        print("Singleton failed, variables contain different instances.")
```

No nosso projeto esse padrão será utilizado para a conexão com o banco de dados, em que o própio _framework Django REST_ realiza esse controle.
<!--
## 4. Prototype (Duvida)

O Prototype é um padrão de projeto criacional que permite copiar objetos existentes sem fazer seu código ficar dependente de suas classes.

Pasta compomentes do frontend

~~~JavaScript
import React from 'react'
import * as S from './styles'

function Button(props) {
    return (
        <S.Container>
            <button className="button">
                <span> {props.title} </span>
            </button>
        </S.Container>
    )
}

export default Button

~~~
<-->


## 5. Referências

> Design Patterns. Refactoring Guru, 2014. Disponível em: https://refactoring.guru/pt-br/design-patterns/creational-patterns. Acesso em: 17 mar. de 2022.

> Gamma, E. et al. Design Patterns: Elements of Reusable Object-Oriented Software. 1. ed. Addison-Wesley, 1994.

> DEVMEDIA. Design Patterns - Factory. Disponível em: https://www.devmedia.com.br/design-patterns-factory/17158. Acesso em 17 mar. de 2022.

> REAL PYTHON. The Factory Method pattern and its implementation in python. Disponível em: https://realpython.com/factory-method-python/. Acesso em 17 mar. de 2022.

> Opus Software. Singleton Design Pattern – O que é, onde usar e quais as vantagens? Disponível em: https://www.opus-software.com.br/singleton-design-pattern/. Acesso em: 20/03/2022

</div>

### Histórico de versão

|    Data    | Versão |    Autor    |      Descrição       |
| :--------: | :----: | :---------: | :------------------: |
| 17/03/2022 |  0.1   | Antônio Aldísio <br> Fernando Miranda <br> João Victor | Criação do documento e <br> inclusão inicial dos padrōes utilizados |
| 18/03/2022 |  0.2   | Antônio Aldísio <br> Fernando Miranda <br> João Victor | Melhoria de introdução e descrição do metodo Factory |
| 19/03/2022 |  0.3   | Antônio Aldísio <br> Fernando Miranda <br> João Victor | Adicionado o conteudo correspondente ao padrão builder. |
| 20/03/2022 |  0.4   | Antônio Aldísio <br> Fernando Miranda <br> João Victor | Adicionado o conteudo correspondente ao padrão singleton. |
| 20/03/2022 |  0.5   | Antônio Aldísio <br> Fernando Miranda <br> João Victor | Adicionado exemplo de código do padrão singleton. |
| 21/03/2022 |  0.6   | Pedro Henrique | Revisão do documento |