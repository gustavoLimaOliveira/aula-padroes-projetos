# Padrões de Projeto no Spring

Ao trabalhar com o Spring, é importante seguir padrões de projeto para organizar seu código e facilitar o desenvolvimento e a manutenção de aplicativos. Nesta seção, abordaremos alguns dos padrões de projeto mais comuns no contexto do Spring.

## MVC - Model-View-Controller

O padrão MVC (Model-View-Controller) é fundamental ao desenvolver aplicativos com o Spring. Ele ajuda a organizar a estrutura de seu projeto em camadas lógicas distintas, separando as responsabilidades da aplicação da seguinte maneira:

- **Controlador (Controller)**: Responsável por receber as requisições do cliente, interagir com o cliente e encaminhar as solicitações para a camada de serviço.

- **Camada de Serviço (Service)**: Orquestra a lógica de negócios da aplicação e interage com a camada de acesso a dados.

- **Camada de Acesso a Dados (Repository)**: Comunica-se com o banco de dados e executa operações de persistência.

- **Entidades (Entities)**: Responsáveis por manter a integridade dos dados a serem armazenados.

Para aplicar o padrão MVC em seu projeto Spring:

1. Crie pacotes para `controller`, `service`, `repository`, `entities`, e `exception`.

2. Organize seus arquivos dentro desses pacotes, seguindo as responsabilidades de cada camada.

Com essa estrutura, seu projeto estará alinhado com o padrão MVC, ou Arquitetura de Camadas, facilitando a organização e manutenção do código.

## Inversão de Controle

A Inversão de Controle (IoC) é um conceito importante no Spring. Ela se baseia no princípio de que, em vez de você controlar todos os detalhes em seu código, o controle é transferido para algo externo. Isso é semelhante a um chef de restaurante que não busca ingredientes, mas recebe ingredientes entregues a ele. No contexto do Spring, você pode observar a IoC em ação em suas classes de repository, service e controller.

## Padrão Repository

O padrão Repository é usado para abstrair a camada de acesso a dados em um projeto Spring. Geralmente, o Spring Data JPA é usado para implementar esse padrão. O uso do padrão Repository permite escrever código mais modular e fácil de testar, além de simplificar o acesso a dados.

## Padrão DTO (Data Transfer Object)

O padrão DTO é usado para transferir dados entre camadas de um aplicativo. Ao construir APIs, é importante evitar que dados maliciosos ou indesejados fluam livremente entre as camadas. Com o uso de DTOs, você pode controlar quais dados são transferidos e como eles são formatados, tornando seu aplicativo mais seguro.

## Padrões de Projeto Criacionais

Os padrões de projeto criacionais são um grupo de padrões que se concentram na maneira como os objetos são criados e instanciados em um programa.

### Abstract Factory

O padrão Abstract Factory ajuda a criar grupos de objetos relacionados que se encaixam em um estilo ou configuração específica, tudo isso sem precisar saber exatamente quais objetos estão sendo criados.

[Exemplo do Abstract Factory](https://gist.github.com/gustavoLimaOliveira/6de50ba837e40df7215f5270752e9ca1)

### Builder

O padrão Builder é usado para criar objetos complexos passo a passo, permitindo que você crie diferentes variações de um objeto sem precisar lidar com muitos construtores complicados.

[Exemplo do Builder](https://gist.github.com/gustavoLimaOliveira/ed6a5bcdc5ee6ba99c6240bf73456dd6)

### Factory Method

O padrão Factory Method é usado para criar objetos por meio de um método chamado "factory method". Esse método sabe como criar diferentes tipos de objetos, permitindo que você crie objetos de maneira flexível, de acordo com suas necessidades.

[Exemplo do Factory Method](https://gist.github.com/gustavoLimaOliveira/044077d944dc8d3840510405b14db4b0)

### Singleton

O padrão Singleton garante que uma classe tenha apenas uma instância e fornece um ponto de acesso global para essa instância.

[Exemplo do Singleton](https://gist.github.com/gustavoLimaOliveira/044077d944dc8d3840510405b14db4b0)

## Padrões Estruturais

Os padrões de projeto estruturais são um grupo de padrões que se concentram em como classes e objetos são organizados para formar estruturas maiores e mais complexas.

### Adapter

O padrão Adapter é usado quando você tem duas classes com interfaces incompatíveis, mas deseja que elas trabalhem juntas. O adaptador age como um intermediário entre essas classes, permitindo que elas se comuniquem.

[Exemplo do Adapter](https://gist.github.com/gustavoLimaOliveira/0f4b8f31df327422c01f378ba6f373e5)

### Bridge

O padrão Bridge é usado para separar duas dimensões diferentes de uma classe, permitindo que elas variem independentemente. Ele é útil quando você tem várias formas de uma entidade e várias maneiras de tratá-la, como diferentes formas e diferentes cores.

[Exemplo do Bridge](https://gist.github.com/gustavoLimaOliveira/ed195ef90b4da02a0c780e39b1eb8780)

### Facade

O padrão Facade é usado para fornecer uma interface única e simplificada para um conjunto complexo de subsistemas ou classes. Ele ajuda a esconder a complexidade do sistema subjacente e oferece uma maneira fácil de interagir com ele.

[Exemplo do Facade](https://gist.github.com/gustavoLimaOliveira/344765c58fc32307886cc9aa8e32b65d)

## Padrões Comportamentais

Os padrões de projeto comportamentais são um grupo de padrões que se concentram nas interações e responsabilidades entre objetos.

### Chain of Responsibility

O padrão Chain of Responsibility é usado quando você tem uma série de objetos que podem lidar com uma solicitação, mas você não sabe qual deles irá tratá-la até o momento em que a solicitação é feita. Cada objeto na cadeia tem a opção de tratar a solicitação ou passá-la para o próximo objeto na cadeia.

[Exemplo do Chain of Responsibility](https://gist.github.com/gustavoLimaOliveira/c138ed5d3c7014c6a7412c5327b58801)

### Observer

O padrão Observer é usado para criar uma relação de dependência um-para-muitos entre objetos. Quando um objeto (chamado de "sujeito" ou "observável") muda de estado, todos os seus "observadores" (ou "ouvintes") são notificados e atualizados automaticamente.

[Exemplo do Observer](https://gist.github.com/gustavoLimaOliveira/5fa983e197e0d5f98c696da306c65ea7)

### Strategy

O padrão Strategy é usado para definir uma família de algoritmos, encapsulá-los e torná-los intercambiáveis. Isso permite que um objeto mude seu comportamento de maneira flexível, escolhendo um algoritmo dentre vários disponíveis durante a execução do programa.

Espero que esses exemplos de padrões de projeto tenham sido úteis para entender como aplicá-los em seu código. Para obter mais informações e detalhes, consulte os links fornecidos.

[Exemplo do Strategy](https://gist.github.com/gustavoLimaOliveira/ec286e0313e934c9001d4d31cdc95702)
