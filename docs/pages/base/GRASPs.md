# <center> GRASPs

<div align="justify">

## 1. Introdução

Padrões de atribuição geral de responsabilidades de software (da sigla em inglês GRASP) são diretrizes de projetos de software para melhor definir as responsabilidades específicas para classes e objetos de um projeto orientado a objetos.

Entre os diversos padrões de GRASP iremos abordar os seguintes princípios nesse documento:

    * Especialista
    * Alta Coesão
    * Baixo acoplamento


## 2. Especialista
Um questionamento muito comum no processo de desenvolvimento se refere à onde deve ser incluído uma nova funcionalidade ou método.
O GRASP de especialista define que devemos procurar pelos pedaços de informação necessários para completar a tarefa, de forma que o lugar que possua maior conhecimento sobre essas informações é o melhor candidato para essa funcionalidade.

Podemos ver esse padrão implementado no seguinte trecho de código do nosso projeto:

~~~Python
class ProviderViewSet(viewsets.ModelViewSet):
    queryset = Provider.objects.all().order_by('name')
    serializer_class = ProviderSerializers
    permission_classes = [permissions.IsAuthenticated]

    def retrieve(self, request, *args, **kwargs):
        params = kwargs
        print(params['pk'])

        providers = Provider.objects.filter(name__contains=params['pk'])
        serializer = ProviderSerializers(providers, many=True)

        return Response(serializer.data)
~~~

Nesse trecho temos a função retrieve, cujo papel é retornar a lista de provedores cujo o nome possuí a substring informada, é implementada dentro do viewset de provedores já que é o ambiente que possuí a maior quantidade de informação necessária para a execição da tarefa.

## 3. Referências

> What are General Responsibility Assignment Software Patterns? Level Up Coding, 2020. Disponível em: https://levelup.gitconnected.com/what-are-general-responsibility-assignment-software-patterns-6ad9635a44da. Acesso em: 18, março de 2022.
>
</div>

### Histórico de versão

|    Data    | Versão |    Autor    |      Descrição       |
| :--------: | :----: | :---------: | :------------------: |
| 18/03/2022 |  0.1   | Álvaro Gouvea <br> Lorrayne Cardozo <br> Pedro Henrique Campos | Criação do documento e <br> inclusão inicial dos padrōes utilizados |