# <center> Diagrama de Implementação

<div align="justify">

## 1. Introdução

O diagrama de implementação, também conhecido como Diagrama de Implantação ou Deployment Diagram, como descrito pela IBM, é um tipo de diagrama UML de estrutura, que mostra a estrutura estática do sistema e suas partes em diferentes níveis de abstração e implementação, assim como a maneira que essas partes são relacionadas umas com as outras, focando em expor os relacionamentos entre os componentes de sofware e hardware com o seu papel na distribuição do produto.

Com relação à descrição de componentes de hardware que serão implementados são descritos, de forma mais comum, sistemas de armazenamento de dados, processadores e outros sistemas que suportam o ambiente de execução do sistema, já ligados a exibir a maneira com que o produto será distribuído, como podemos na pagina da UML-Diagrams, são descritas as tecnologias presentes no sistema e as suas interconexões, em forma de relacionamentos entre os componentes no diagrama.

Um diagrama de implementação possui diversos elementos gráficos que representam os diferentes componentes que utilizados em um produto de software, entre estes elementos podemos destacar dois deles, os **nós**, **conexões** e os **Ambientes de Execução**, que segundo a IBM podem ser descritos da seguinte forma:

- **Nós**: representados graficamente em formato de cubos, os nós tem como objetivo descrever componentes presentes, componentes que representam recursos computacionais como dispositivos, servidores ou computadores pessoais. Os Nós podem ser conectados uns com os outros através de conexões, representando o relacionamento entre eles.

- **Conexões**: representam os mecanismos de comunicação entre os nós, podendo ser representado por meios físicos, como cabos de fibra ótica, ou por representação em forma de protocolos, como TCP/IP, HTTP e HTTPS.

- **Ambientes de Execução***: um tipo de ambiente que representa uma plataforma específica, como sistema operacional ou um sistema gerenciador de banco de dados.


Assim, a elaboração de um diagrama de implementação do processo de modelagem de um produto de software, irá apoiar a compreensão da integração dos sistemas utilizados, que serão base para a construção do produto de software em questão.

## 2. Diagrama de Implementação


<p align='center'>
    <img src='assets/images/diagramasEstaticos/diagramaImplementação.svg' width=40% height=auto>
    <figcaption align='center'>
        <b>Figura 1: Diagrama de implementação do produto. </b>
        <br>
    </figcaption>
</p>

## 3. Referências

> UML-DIAGRAMS. **Structure Diagrams**. Dispoível em: https://www.uml-diagrams.org/deployment-diagrams-overview.html. Acesso em: 8 fev. 2022.

> IBM. **Diagramas de Implementação**. Disponível em: https://www.ibm.com/docs/pt-br/rsas/7.5.0?topic=topologies-deployment-diagrams. Acesso em: 9 fev. 2022.

> ANIMALESCO. **Diagrama de Implementação**. Disponível em: https://unbarqdsw2021-1.github.io/2021.1_G01_Animalesco_docs/#/pages/diagrama-de-implementacao. Acesso em: 9 fev. 2022.

</div>

### Histórico de versão

|    Data    | Versão |       Autor      |              Descrição                    |
| :--------: | :----: | :--------------: | :---------------------------------------: |
| 09/02/2022 |  0.5   | Fernando Miranda |    Criação do documento e introdução      |
| 09/02/2022 |  1.0   | Fernando Miranda | Adicionado o diagrama de implementação    |
| 14/02/2022 |  1.1   | Lorrayne Cardozo | Revisão do documento                      |
| 19/02/2022 |  1.2   | Fernando Miranda | Melhoria de texto, padrões e link de referencias |