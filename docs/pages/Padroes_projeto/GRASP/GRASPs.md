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

## 3. Baixo Acoplamento

Pode-se dizer que o conceito de acoplamento está ligado a uma medida de quão fortemente um elemento está conectado, tem algum tipo de conhecimento ou depende de outros elementos. Sabe-se então, de antemão, que tanto o baixo acoplamento (classes dependendo minimamente de outras classes) e a alta coesão (as classes devem procurar ter apenas uma responsabilidade) são objetivos gerais de todo sistema projetado de maneira adequado.

Sendo assim, o padrão de projeto denominado de baixo acoplamento é um padrão avaliativo que determina como se pode atribuir responsabilidades para apoiar:<br/>
<ul>
	<li>Uma menor dependência entre as classes;</li>
	<li>Mudanças em alguma classe sem ter algum impacto tão grande em outras classes;</li>
	<li>Um maior potencial de reutilização.</li>
</ul>
A grande dúvida que pode surgir então é como que faríamos para oferecer esse suporte ao baixo acoplamento, tendo assim uma baixa dependência, baixo impacto nas mudanças e maior reutilização.

A resposta para isso é mais óbvia do que parece. Para oferecer suporte para todas as essas questões basta que seja atribuida responsabilidades de modo que o acoplamento sempre permaneça baixo, tendendo a sempre atribuir uma única responsabilidade para cada classe, para que assim o acoplamento sempre permaneça baixo.

É importante ressaltar que sempre que houver subclasses essas serão fortemente acopladas às suas superclasses, sendo assim sempre que houver o uso de herança deve-se ter cuidado com a forma com que foi desenvolvida essa questão. Além disso, é relevante saber que não é ideial existir um grau de acomplamento nulo entre as classes, pois isso fere o fato de objetos conectados poderem trocar mensagens entre si.

## 4. Referências

> What are General Responsibility Assignment Software Patterns? Level Up Coding, 2020. Disponível em: https://levelup.gitconnected.com/what-are-general-responsibility-assignment-software-patterns-6ad9635a44da. Acesso em: 18, março de 2022.

> Videoaulas e materiais complementares presentes no moodle da disciplina Arquitetura e Desenho de Software. Disponível em: https://aprender3.unb.br/course/view.php?id=11018. Acesso em: 15/03/2022.

> Low Coupling GRASP Pattern. Source Code Examples,2018. Disponível em: https://www.sourcecodeexamples.net/2018/06/low-coupling-grasp-pattern.html. Acesso em 18, março de 2022.

> Coupling in Java with Example. Java Guides, 2018. Disponível em: https://www.javaguides.net/2018/08/coupling-in-java-with-example.html . Acesso em 19, março de 2022.  

### Histórico de versão

|    Data    | Versão |    Autor    |      Descrição       |
| :--------: | :----: | :---------: | :------------------: |
| 18/03/2022 |  0.1   | Álvaro Gouvea <br> Lorrayne Cardozo <br> Pedro Henrique Campos | Criação do documento e <br> inclusão inicial dos padrōes utilizados |
| 19/03/2022 |  0.5   | Álvaro Gouvea <br> Lorrayne Cardozo <br> Pedro Henrique Campos | Inclusão inicial baixo acoplamento|