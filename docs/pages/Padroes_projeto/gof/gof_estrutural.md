# <center> GOFs Estruturais

<div align="justify">


## 1. Decorator

O Decorator é um GOF estrutural que tem como objetivo agregar comportamentos adicionais a um objeto. É uma alternativa flexivel à herança no momento de extender funcionalidades, já que com o decorator adiciona esse novo comportamento ao objeto e não à classe.

Exemplo do uso de decotators no código de exemplo do _framework Django REST_, que apesar de não ser um trecho do nosso código, se encaixa no nosso projeto:

```
from rest_framework.decorators import api_view
from rest_framework.response import Response

@api_view(['GET', 'POST'])
def hello_world(request):
    if request.method == 'POST':
        return Response({"message": "Got some data!", "data": request.data})
    return Response({"message": "Hello, world!"})
```

Nesse exemplo acima o decorator `@api_view` recebe uma lista de metodos HTTP que a view deve aceitar.

## 2. Facade
O Facade é um GOF estrutural que tem como objetivo esconder a complexidade de um conjunto de classes e reduzir o acoplamento entre as camadas do porjeto. É muito utilizado por bibliotecas e frameworks para produzir uma interface mais simplificada.

No nosso projeto serão utilizadas diversas bibliotecas que atuam com Facade de suas implementações.

## 3. Referências

> Padrões de Projeto. Refactoring Guru. Disponível em: https://refactoring.guru/pt-br. Acesso em: 20/03/2022.

> Videoaulas e materiais complementares presentes no moodle da disciplina Arquitetura e Desenho de Software. Disponível em: https://aprender3.unb.br/course/view.php?id=11018. Acesso em: 15/03/2022.

> http://www.csi.uneb.br/padroes_de_projetos/decorator.html. Acesso em: 20/03/2022.

> O Padrão Facade aplicado. Fábio Godoy DevMedia. Disponível em: https://www.devmedia.com.br/o-padrao-facade-aplicado/12683. Acesso em: 20/03/2022.

</div>

### Histórico de versão

|    Data    | Versão |    Autor    |      Descrição       |
| :--------: | :----: | :---------: | :------------------: |
| 20/03/2022 |  0.1   | João Victor e Ariel | Criação do documento e adição do GOF Decorator |
| 20/03/2022 |  0.2   | João Victor e Ariel | Adição do GOF Facade |
