# <center> GRASPs

<div align="justify">

## 1. Introdução

GRASP é acrônimo de **General Responsability Assignment Software Patterns**, que em tradução livre significa **Padrões de Atribuição Geral de Responsabilidades de Software**. Padrões GRASP são uma ajuda na hora de entender como desenhar um software orientado a objetos de maneira metódica, racional e explicável (LARMAN, 2004). Esta diretriz de projetos de software visa oferecer um guia bem estruturado para definir as responsabilidades específicas para classes e objetos de projetos orientados a objetos.

Entre os diversos padrões de GRASP, a equipe decidiu abordar os seguintes princípios:

- Especialista
- Alta Coesão
- Baixo acoplamento

Estes padrões foram escolhidos com o objetivo de melhor organizar e dividir os diferentes módulos do projeto de forma coerente, tornando o código mais flexível, facilitando sua compreensão, manutenção e reutilização.

## 2. Discussão preeliminar

Para ajudar a tomar as decisões sobre os padrões de projetos foi feita uma reunião para discutir sobre as vantagens e desvantagens de cada padrão.

Essa discussão pode ser encontrada [aqui](../extras/reuniao_padroes_projeto.md).


## 3. Especialista

Um questionamento muito comum no processo de desenvolvimento se refere à onde deve ser incluído uma nova funcionalidade ou método.
O GRASP de especialista define que devemos procurar pelos pedaços de informação necessários para completar a tarefa, de forma que o lugar que possua maior conhecimento sobre essas informações é o melhor candidato para essa funcionalidade.

Podemos ver esse padrão implementado no seguinte trecho de código do nosso projeto:

```Python
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
```

Nesse trecho temos a função retrieve, cujo papel é retornar a lista de provedores cujo o nome possuí a substring informada, é implementada dentro do viewset de provedores já que é o ambiente que possuí a maior quantidade de informação necessária para a execução da tarefa.

## 4. Baixo Acoplamento

Pode-se dizer que o conceito de acoplamento está ligado a uma medida de quão fortemente um elemento está conectado, tem algum tipo de conhecimento ou depende de outros elementos. Sabe-se então, de antemão, que tanto o baixo acoplamento (classes dependendo minimamente de outras classes) e a alta coesão (as classes devem procurar ter apenas uma responsabilidade) são objetivos gerais de todo sistema projetado de maneira adequada.

Sendo assim, o padrão de projeto denominado de baixo acoplamento é um padrão avaliativo que determina como se pode atribuir responsabilidades para apoiar:<br/>

<ul>
	<li>Uma menor dependência entre as classes;</li>
	<li>Mudanças em alguma classe sem ter algum impacto tão grande em outras classes;</li>
	<li>Um maior potencial de reutilização.</li>
</ul>
A grande dúvida que pode surgir então é como que faríamos para oferecer esse suporte ao baixo acoplamento, tendo assim uma baixa dependência, baixo impacto nas mudanças e maior reutilização.

A resposta para isso é mais óbvia do que parece. Para oferecer suporte para todas as essas questões basta que seja atribuida responsabilidades de modo que o acoplamento sempre permaneça baixo, tendendo a sempre atribuir uma única responsabilidade para cada classe, para que assim o acoplamento sempre permaneça baixo. O próprio padrão do _framework Django REST_ utilizado no backend do projeto já nos oferece um baixo acoplamento.

É importante ressaltar que sempre que houver subclasses essas serão fortemente acopladas às suas superclasses, sendo assim sempre que houver o uso de herança deve-se ter cuidado com a forma com que foi desenvolvida essa questão. Além disso, é relevante saber que não é ideial existir um grau de acomplamento nulo entre as classes, pois isso fere o fato de objetos conectados poderem trocar mensagens entre si.

Podemos ver a aplicação do baixo acoplamento no nosso código nos seguintes trechos de modelagem das nossas duas principais classes:
~~~Python
class Services(models.Model):
	datePurchase = models.DateField()
	dateSevice = models.DateField()
	serviceDesription = models.CharField(max_length=5000)
~~~
~~~Python
class Person(AbstractUser):
    name = models.CharField(max_length=500)
    cpf = models.BigIntegerField(primary_key=True)
    phone = models.BigIntegerField()
    email = models.EmailField(verbose_name="email", max_length=150, unique=True)

    USERNAME_FIELD = 'email'
    REQUIRED_FIELDS = []

    objects = PersonManager()

    def __str__(self):
        return self.name
~~~
Nesses trechos podemos ver que as definições das duas classes não possuem uma relação direta, mesmo que existam dependências entre elas em partes do código, elas conseguem trabalhar também de forma independente.

## 5. Alta Coesão

Um elemento com responsabilidades altamente relacionadas que não faz uma grande quantidade de trabalho tem alta coesão. Esses elementos incluem classes, subsistemas e assim por diante (LARMAN, 2004). Classes que possuem muitas responsabilidades não relacionadas dificultam sua compreensão, manutenibilidade e reutilização, além de aumentar sua fragilidade. Devido a isso, a alta coesão é utilizada pois possui o objetivo de manter os objetos adequadamente focados, compreensíveis e gerenciáveis, além de, consequentemente, com um baixo acoplamento.

Além de fornecer um baixo acoplamento, o próprio padrão do _framework Django REST_ utilizado no backend do projeto também oferece uma alta coesão, visto que cada um dos seus arquivos tem suas próprias responsabilidades e métodos bem definidos de forma que não trabalhem demais, assim como é apresentado na Figura 1.

<p align='center'>
    <img src='assets/images/grasps/altaCoesao.png' width=20% height=auto>
    <figcaption align='center'>
        <b>Figura 1: Estrutura das responsabilidades de cada classe do projeto. </b>
        <br>
    </figcaption>
</p>

Além disso, o diagrama de classes desenvolvido pela equipe apresentado abaixo também é uma solução:

<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramaClasses/classDiagramV2.svg' width=40% height=auto>
    <figcaption align='center'>
        <b>Figura 2: Diagrama de classes do produto. </b>
        <br>
    </figcaption>
</p>

## 6. Referências

> What are General Responsibility Assignment Software Patterns? Level Up Coding, 2020. Disponível em: https://levelup.gitconnected.com/what-are-general-responsibility-assignment-software-patterns-6ad9635a44da. Acesso em: 18, março de 2022.

> Videoaulas e materiais complementares presentes no moodle da disciplina Arquitetura e Desenho de Software. Disponível em: https://aprender3.unb.br/course/view.php?id=11018. Acesso em: 15/03/2022.

> Low Coupling GRASP Pattern. Source Code Examples,2018. Disponível em: https://www.sourcecodeexamples.net/2018/06/low-coupling-grasp-pattern.html. Acesso em 18, março de 2022.

> Coupling in Java with Example. Java Guides, 2018. Disponível em: https://www.javaguides.net/2018/08/coupling-in-java-with-example.html . Acesso em 19, março de 2022.

> LARMAN, Craig. Utilizando UML e Padrões: Uma introdução à análise e ao projeto orientados a objetos e ao desenvolvimento iterativo. 3. ed. [S. l.: s. n.], 2004.

### Histórico de versão

|    Data    | Versão |                             Autor                              |                                   Descrição                                    |
| :--------: | :----: | :------------------------------------------------------------: | :----------------------------------------------------------------------------: |
| 18/03/2022 |  0.1   | Álvaro Gouvea <br> Lorrayne Cardozo <br> Pedro Henrique Campos |      Criação do documento e <br> inclusão inicial dos padrōes utilizados       |
| 19/03/2022 |  0.2   | Álvaro Gouvea <br> Lorrayne Cardozo <br> Pedro Henrique Campos |                       Inclusão inicial baixo acoplamento                       |
| 20/03/2022 |  0.3   | Álvaro Gouvea <br> Lorrayne Cardozo <br> Pedro Henrique Campos | Adição do tópico de Alta Coesão, complementando Baixo Acoplamento e introdução |
| 20/03/2022 |  0.4   | Rodrigo Balbino <br> Ariel Serafim <br> Guilherme Braz         |                        Realizando revisão do documento                         |
| 20/03/2022 |  0.5   | Álvaro Gouvea <br> Lorrayne Cardozo <br> Pedro Henrique Campos |                        Adição de código sobre baixo acoplamento                |
| 21/03/2022 |  1.0   | João Victor e Fernando |                        Adição da discussão preeliminar                |
