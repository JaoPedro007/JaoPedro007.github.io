# Contexto

![diagrama](https://www.plantuml.com/plantuml/svg/0/TLDDRzim3Bq7o7_WV4g1Dhxij5EpB6iBfAknE1Xs2bXPIpN8eYVAMRT_C-pG7v8_DifVIThrP8bwV7oFf2yve0zrQI7tw5YxGllnw8rnojQ5XeSGAdwNfXv_JhScFDJtDMklo0NjmbHHcMBX3RgThQiwdR-zo2owiBvTfXQ3vY2XpJoY7yEqaYhZqNYqd7szM-URBpVvzMQvk5fy-Z0vY_5CUoOtKTO8jpw7PDwU4ZdUGHS69ckK2GYAl3S5CZW2h2I8mUmeEHk8AYy2i20l-Lb_1Z4b3dPc_qGjyG03KIpsWNX0y52k83wYng8qpd3m7Vti-DxGCfnWDCDMU-sKmH88MEAwnAJnlVeLBvCk9ibn4gjc4f5AIfOcDBAw7XnKULqUj9v7oE16KAsVY6coNnCaW2YabR5PF8R9FJf5Klfz_1vh-54B4rIunLA44CJs3tDW_HtXcpQ1dj6LM8cuv8feQpNSoYroVYJljDA0O4cXDRzn_xJ_In23pFi_ibPIoUFfF7f_tFRkixQ7XJbqSCrDR-FhqHRyz_tPA5zW-Yh3G-Tc7KpKBF9dsKtSAebZO-mwpxDLJp-azJrzaJTqypHvFBgKwJM_p3y0)

**Nível 1: Diagrama de Contexto do Sistema**

Um Diagrama de Contexto do Sistema é um bom ponto de partida para diagramar e documentar um sistema de software, permitindo que você dê um passo para trás e veja o quadro geral. Desenhe um diagrama mostrando seu sistema como uma caixa no centro, cercada por seus usuários e pelos outros sistemas com os quais interage.

Detalhes não são importantes aqui, pois esta é a sua visão ampla mostrando uma imagem geral do panorama do sistema. O foco deve estar nas pessoas (atores, funções, personas, etc.) e nos sistemas de software, em vez de tecnologias, protocolos e outros detalhes de baixo nível. É o tipo de diagrama que você poderia mostrar a pessoas não técnicas.

**Escopo**: Um único sistema de software

**Elementos principais**: O sistema de software em questão.
Elementos de suporte: Pessoas (por exemplo, usuários, atores, funções ou personas) e sistemas de software (dependências externas) diretamente conectados ao sistema de software em questão. Normalmente, esses outros sistemas de software ficam fora do escopo ou limite do seu próprio sistema de software, e você não tem responsabilidade ou propriedade sobre eles.

**Público-alvo**: Todos, tanto pessoas técnicas quanto não técnicas, dentro e fora da equipe de desenvolvimento de software.

# Contexto

# Introdução

Esse projeto foi criado usando [c4builder](https://adrianvlupu.github.io/C4-Builder/)

Dê uma olhada em 

- [PlantUml](http://plantuml.com/) cria diagramas a partir de texto simples.

- [Markdown](https://guides.github.com/features/mastering-markdown/) cria documentos de texto enriquecido a partir de texto simples.

- [C4Model](https://c4model.com/) a ideia por trás dos mapas do seu código

- [C4-PlantUML](https://github.com/RicardoNiepel/C4-PlantUML) suporte à sintaxe C4 para gerar diagramas PlantUML

- [vscode-plantuml](https://github.com/qjebbs/vscode-plantuml) plugin para o Visual Studio Code para visualizar diagramas durante o design

Abra o terminal e execute os seguintes comandos para começar a compilar a documentação

```bash
npm i -g c4builder
c4builder
```

> Observação sobre o uso de imagens locais dentro de arquivos markdown
>
> As imagens devem ser colocadas ao lado do arquivo markdown que as utiliza.
>
> Todas elas serão copiadas para a pasta docs, seja em / (no caso de um único arquivo MD/PDF) ou seguindo a mesma estrutura de pasta que em src, portanto, certifique-se de que elas tenham nomes únicos. 

# Abstrações usadas

![C4Model](https://c4model.com/img/abstractions.png)

### Pessoa

Independentemente de como você pensa sobre seus usuários (como atores, funções, personas, etc.), as pessoas são os vários usuários humanos do seu sistema de software.

### Sistema de Software

Um sistema de software é o mais alto nível de abstração e descreve algo que entrega valor aos seus usuários, sejam eles humanos ou não. Isso inclui o sistema de software que você está modelando e os outros sistemas de software nos quais seu sistema de software depende (ou vice-versa).

### Contêiner

Um contêiner representa algo que hospeda código ou dados. Um contêiner é algo que precisa estar em execução para que o sistema de software como um todo funcione. Em termos reais, um contêiner é algo como: 

- Aplicação web no servidor: uma aplicação web Java EE em execução no Apache Tomcat, uma aplicação ASP.NET MVC em execução no Microsoft IIS, uma aplicação Ruby on Rails em execução no WEBrick, uma aplicação Node.js, etc.

- Aplicação web do lado do cliente: uma aplicação JavaScript em execução em um navegador da web usando Angular, Backbone.JS, jQuery, etc.

- Aplicação de desktop do lado do cliente: uma aplicação de desktop Windows escrita usando WPF, uma aplicação de desktop OS X escrita usando Objective-C, uma aplicação de desktop multiplataforma escrita usando JavaFX, etc.
- Aplicativo móvel: um aplicativo iOS da Apple, um aplicativo Android, um aplicativo Windows Phone da Microsoft, etc.

- Aplicação de console do lado do servidor: uma aplicação independente (por exemplo, "public static void main")

- etc

### Componente

Componente
A palavra "componente" é um termo extremamente sobrecarregado na indústria de desenvolvimento de software, mas, neste contexto, um componente é simplesmente um agrupamento de funcionalidades relacionadas encapsuladas por uma interface bem definida. Se você está usando uma linguagem como Java ou C#, a maneira mais simples de pensar em um componente é que ele é uma coleção de classes de implementação por trás de uma interface. Aspectos como como esses componentes são empacotados (por exemplo, um componente vs muitos componentes por arquivo JAR, DLL, biblioteca compartilhada, etc.) são uma preocupação separada e ortogonal.

Um ponto importante a ser observado aqui é que todos os componentes dentro de um contêiner geralmente são executados no mesmo espaço de processo. 