# <center> GoFs Criacionais

<div align="justify">

## 1. Introdução

Padrões de projeto são soluções para problemas comuns que encontramos no desenvolvimento ou manutenção de um software. Iremos abordar os padrões criacionais, estes são padrões que lidam com mecanismos de criação de objetos, voltados a criar objetos de maneira adequada à situação. Eles ajudam a tornar um sistema independente de como seus objetos são criados, compostos e representados.[1](./pages/Padroes_projeto/gof/criacionais.md#_4-referências)

Conforme o código da aplicação tem o seu foco direcionado para a maior utilização de composição de objetos a aplicação dos padrões criacionais tende a tomar maior enfase, com isso a estruturação de código deixa de ser focada em um comportamento fixo e se volta mais para a definição de comportamentos básicos e fundamentais para o comportamento do software.[2](./pages/Padroes_projeto/gof/criacionais.md#_4-referências)

"Existem dois temas recorrentes nesses padrões. Primeiro, todos eles encapsulam conhecimento sobre qual classe concreta o sistema usa. Segundo, eles escondem como instancias dessas classes são criadas e construidas." [(Gamma, 1994, p.94)](./pages/Padroes_projeto/gof/criacionais.md#_4-referências) Com isso os padrões criacionais criam flexibilidade na criação de objetos dentro de um software.

Neste documento iremos abordar os seguintes **GoFs Criacionais** que foram adotados pela equipe:

  - [Builder](./pages/Padroes_projeto/gof/criacionais.md#_3-builder)
  - [Factory](./pages/Padroes_projeto/gof/criacionais.md#_2-Factory)


## 2. Factory

O método de fábrica é um padrão de design criacional que resolve o problema de criar objetos de produto sem especificar suas classes concretas, tendo o objetivo de facilitar a criação de objetos. O padrão **factory** se baseia na ideia de que é mais simples encontrar onde um determinado objeto está sendo instanciado, se isso for feito através de uma função central.

<p align='center'>
    <img src='assets/images/gofsCriacionais/exFactory.png' width=40% height=auto>
    <figcaption align='center'>
        <b>Figura 1: Exemplo de Factory</b>
        <br>
        <small>Fonte: https://refactoring.guru/pt-br/design-patterns/factory-method</small>
    </figcaption>
</p>

Como podemos perceber na [imagem 1](./pages/Padroes_projeto/gof/criacionais.md#_2-Factory), no padrão **factory** nos passamos apenas uma função, não nos importando onde o objeto está implementado nem como foi implementado.

Podemos ver no trecho de codigo a seguir, uma implementação que está sendo utilizada pela equipe.

<!--

If you realize that you cannot track the objects created by your application because the code that creates them is in many different places instead of a single function/method, you should consider using the Factory Method pattern [Eckel08, page 187]. The Factory Method centralizes an object creation and tracking your objects becomes much more easier. Note that it is absolutely fine to create more than one Factory Method, and this is how it is typically done in practice. Each Factory Method logically groups the creation of objects that have similarities. For example, one Factory Method might be responsible for connecting you to different databases (MySQL, SQLite), another Factory Method might be responsible for creating the geometrical object that you request (circle, triangle), and so on.
-->
~~~BackEnd

class PersonManager(BaseUserManager):
    def _create_user(self, username, name, email, password, cpf, phone, is_staff, is_superuser):
        if not name:
            raise ValueError('Usuario deve possuir nome')
        email = self.normalize_email(email)
        user = self.model(username=username, name=name, email=email, is_staff=is_staff, is_active=True, is_superuser=is_superuser, cpf=cpf, phone=phone)
        user.set_password(password)
        user.save(using=self._db)
        return user

    def create_user(self, username, name, cpf, phone, email=None, password=None):
        return self._create_user(username, name, email, password, cpf, phone, False, False)

    def create_superuser(self,username, name, cpf, phone, email=None, password=None):
        user=self._create_user(username, name, email, password, cpf, phone, True, True)
        user.is_active=True
        user.save(using=self._db)
        return user

~~~

~~~ FrontEnd

function HomePage() {
  let navigate = useNavigate()

  function navigateToServicesPage() {
    navigate('/servicePage')
  }

  function navigateToServiceCreate() {
    navigate('/serviceCreatePage')
  }

  function navigateToUserRegistration() {
    navigate('/userRegistrationPage')
  }

  function navigateToLogin() {
    navigate('/login')
  }


~~~

## 3. Builder

O Builder é um padrão de projeto criacional que permite a você construir objetos complexos passo a passo. O padrão permite que você produza diferentes tipos e representações de um objeto usando o mesmo código de construção.

~~~Python
from django.urls import include, path
from rest_framework import routers
from service import views
from service.views import ServiceViewSet
from user.views import UserViewSet, ProviderViewSet

router = routers.DefaultRouter()
router.register(r'service', ServiceViewSet)
router.register(r'user', UserViewSet)
router.register(r'provider', ProviderViewSet)

# Wire up our API using automatic URL routing.
# Additionally, we include login URLs for the browsable API.
urlpatterns = [
    path('', include(router.urls)),
    path('api-auth/', include('rest_framework.urls', namespace='rest_framework'))
]
~~~

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


## 4. Referências

> Design Patterns. Refactoring Guru, 2014. Disponível em: https://refactoring.guru/pt-br/design-patterns/creational-patterns. Acesso em: 17 mar. de 2022.

> Gamma, E. et al. Design Patterns: Elements of Reusable Object-Oriented Software. 1. ed. Addison-Wesley, 1994. p. 94-96.

> DEVMEDIA. Design Patterns - Factory. Disponível em: https://www.devmedia.com.br/design-patterns-factory/17158. Acesso em 17 mar. de 2022.

> REAL PYTHON. The Factory Method pattern and its implementation in python. Disponível em: https://realpython.com/factory-method-python/. Acesso em 17 mar. de 2022.


</div>

### Histórico de versão

|    Data    | Versão |    Autor    |      Descrição       |
| :--------: | :----: | :---------: | :------------------: |
| 17/03/2022 |  0.1   | Antônio Aldísio <br> Fernando Miranda <br> João Victor | Criação do documento e <br> inclusão inicial dos padrōes utilizados |
| 18/03/2022 |  0.2   | Antônio Aldísio <br> Fernando Miranda <br> João Victor | Melhoria de introdução e descrição do metodo Factory |
