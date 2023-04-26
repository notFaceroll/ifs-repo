# Speedrun de Paradigma de Orientação a Objetos

## Conceitos

A orientação a objetos é um paradigma de programação que se baseia na ideia de que um programa pode ser modelado como um conjunto de objetos que interagem entre si. Cada objeto tem suas próprias características (atributos) e comportamentos (métodos), e pode se comunicar com outros objetos através de mensagens.

Um dos principais objetivos da orientação a objetos é facilitar a reutilização de código, já que os objetos podem ser criados a partir de classes existentes e herdar suas características e comportamentos. Além disso, a orientação a objetos também ajuda a organizar melhor o código, já que cada objeto é responsável por uma tarefa específica.

Existem alguns conceitos fundamentais da orientação a objetos, como encapsulamento, herança e polimorfismo. O encapsulamento refere-se à ideia de que os dados e comportamentos de um objeto devem ser protegidos de acesso não autorizado. A herança permite que uma classe herde as características de outra, o que pode simplificar o processo de criação de novas classes. O polimorfismo permite que um objeto seja tratado de várias formas diferentes, dependendo do contexto em que é utilizado.

## Tipos Abstratos de Dados (TAD)

Tipos abstratos de dados (TAD) são uma abstração que permite a definição de novos tipos de dados em um programa de computador, com suas próprias operações e comportamentos. Eles são "abstratos" no sentido de que as operações que eles definem são independentes da sua implementação concreta.

Em outras palavras, um TAD descreve um tipo de dado a partir de sua interface pública (métodos, funções) e das operações que podem ser realizadas com esse tipo de dado, sem expor os detalhes de sua implementação. Isso permite que a implementação subjacente possa ser modificada sem afetar o comportamento dos programas que utilizam o TAD.

Um exemplo comum de TAD é a pilha (stack), que pode ser definida como uma estrutura de dados em que a inserção e a remoção de elementos são realizadas apenas no topo da pilha. As operações básicas que podem ser realizadas em uma pilha são "push" (inserção) e "pop" (remoção), e a interface pública da pilha não precisa expor como essas operações são implementadas.

Os TAD são frequentemente utilizados em linguagens de programação orientadas a objetos, pois a orientação a objetos permite a definição de novos tipos de dados (classes) com suas próprias operações e comportamentos. No entanto, eles também podem ser implementados em linguagens que não são orientadas a objetos.

## Classes e Objetos

> Classe é uma descrição abstrata de um tipo de objeto, enquanto uma instância é uma representação concreta desse tipo de objeto com seus próprios valores de atributos e comportamentos. As instâncias são criadas a partir de classes e podem ser criadas e manipuladas em tempo de execução.

Uma classe é uma estrutura que define um tipo de objeto, especificando seus atributos (variáveis) e métodos (funções) que podem ser aplicados a esse tipo de objeto. Em outras palavras, uma classe é uma "planta" para criar objetos.

As classes são utilizadas para criar instâncias, que são objetos concretos criados a partir da classe. Cada instância é uma cópia da classe, com seus próprios valores de atributos, que podem ser acessados e modificados por meio dos métodos da instância.

Por exemplo, suponha que uma classe chamada "Cachorro" seja definida com os atributos "nome", "idade" e "raça", e os métodos "latir" e "andar". A partir dessa classe, podemos criar várias instâncias de cachorro, cada uma com seus próprios valores para os atributos "nome", "idade" e "raça", e que podem latir e andar.

## Tipos e Subtipos

> Tipos e subtipos se referem à relação de herança entre classes, em que uma subclasse é um tipo mais específico que herda atributos e métodos de uma classe pai mais geral. Essa relação permite a polimorfismo e a reutilização de código.

Uma classe é um tipo, e uma subclasse é um subtipo da classe pai. A subclasse herda os atributos e métodos da classe pai, e pode adicionar seus próprios atributos e métodos ou sobrescrever os da classe pai. Por exemplo, uma classe "Cachorro" pode ser uma subclasse de uma classe "Animal". Isso significa que a classe "Cachorro" herda os atributos e métodos da classe "Animal", como "nome" e "idade", mas pode adicionar seus próprios atributos e métodos, como "latir".

A relação de subtipo é importante porque permite a polimorfismo, ou seja, o uso de objetos de diferentes subtipos como se fossem do mesmo tipo. Por exemplo, se tivermos uma função que espera um objeto do tipo "Animal", podemos passar um objeto do tipo "Cachorro", pois "Cachorro" é um subtipo de "Animal". Isso ocorre porque a subclasse herda todos os atributos e métodos da classe pai, e portanto, pode ser tratada como a classe pai em algumas situações.

## Troca de mensagens entre objetos

> A troca de mensagens é a forma como os objetos interagem na programação orientada a objetos. Ela é utilizada para solicitar que um objeto execute um método ou função e retornar uma resposta ao objeto que enviou a mensagem. Essa troca de mensagens pode ser síncrona ou assíncrona e pode ser bidirecional.

Quando um objeto envia uma mensagem para outro objeto, ele está solicitando que o objeto receptor execute um determinado método ou função. Essa mensagem contém informações que o receptor usa para executar o método correto e retornar uma resposta ao objeto que enviou a mensagem.

Por exemplo, suponha que temos um objeto "Cachorro" com um método "latir". Quando um objeto "Pessoa" envia uma mensagem "latir" para o objeto "Cachorro", o objeto "Cachorro" executa seu método "latir" e retorna uma resposta, que pode ser um som de latido.

A troca de mensagens pode ser síncrona ou assíncrona. Na troca de mensagens síncrona, o objeto que envia a mensagem aguarda a resposta do objeto receptor antes de continuar sua execução. Na troca de mensagens assíncrona, o objeto que envia a mensagem não aguarda a resposta e pode continuar sua execução, enquanto o objeto receptor executa a mensagem em segundo plano.

Além disso, a troca de mensagens pode ser bidirecional, ou seja, os objetos podem enviar e receber mensagens um do outro. Essa troca de mensagens bidirecional permite a construção de sistemas complexos e interativos, onde vários objetos podem colaborar para realizar determinada tarefa.

## Os "Pilares" da orientação a objetos

A programação orientada a objetos é baseada em quatro pilares fundamentais, que são:

- Encapsulamento
- Herança
- Polimorfismo
- Abstração

Cada um desses pilares tem sua importância e juntos fornecem uma estrutura poderosa para desenvolver software modular, flexível e escalável.

> Os quatro pilares da programação orientada a objetos - encapsulamento, herança, polimorfismo e abstração - trabalham juntos para fornecer uma estrutura poderosa e flexível para o desenvolvimento de software. Ao aplicar esses princípios corretamente, os desenvolvedores podem criar código mais modular, escalável e fácil de manter.

### Encapsulamento

O encapsulamento é a técnica de esconder a complexidade interna de um objeto e expor apenas sua interface pública. Isso significa que o objeto controla o acesso aos seus atributos e métodos, permitindo que outros objetos possam interagir com ele de forma segura e consistente.

O encapsulamento é alcançado por meio da definição de atributos e métodos como públicos, privados ou protegidos. Os atributos privados só podem ser acessados pelos métodos da classe, enquanto os atributos públicos podem ser acessados por qualquer objeto que tenha uma referência para o objeto em questão.

O encapsulamento permite que os objetos possam ser alterados internamente sem afetar outros objetos que dependem deles. Ele também aumenta a segurança do sistema, pois evita que objetos externos possam modificar os atributos do objeto sem permissão.

### Herança

A herança é um mecanismo pelo qual uma classe pode herdar atributos e métodos de uma classe pai. Isso permite que as subclasses herdem o comportamento e a estrutura da classe pai, enquanto adicionam ou modificam suas próprias características.

Por exemplo, uma classe "Cachorro" pode herdar da classe "Animal", que pode ter atributos como "nome" e "idade" e métodos como "andar" e "respirar". A classe "Cachorro" pode adicionar seus próprios métodos como "latir", que são específicos para a classe "Cachorro".

A herança permite que o código seja reutilizado e ajuda a manter o código organizado e fácil de entender.

### Polimorfismo

O polimorfismo é a capacidade de objetos de diferentes classes responderem a uma mesma mensagem de diferentes maneiras. Isso significa que objetos diferentes podem executar o mesmo método de maneiras diferentes, de acordo com sua própria implementação.

Por exemplo, suponha que tenhamos uma classe "Animal" com um método "fazerSom". A classe "Cachorro" e a classe "Gato" podem ser subclasses de "Animal" e implementar seu próprio método "fazerSom" de acordo com sua própria implementação. Então, quando uma mensagem "fazerSom" é enviada para um objeto "Animal", o método "fazerSom" é executado de maneira diferente dependendo do tipo de objeto que recebe a mensagem.

O polimorfismo permite que o código seja flexível e adaptável a diferentes situações. Ele também ajuda a manter o código organizado e fácil de entender.

### Abstração

A abstração é a capacidade de representar objetos do mundo real em um modelo de software simplificado. Ela permite que as complexidades do mundo real sejam abstraídas em objetos simples e tratados como entidades independentes.

Ela ajuda a simplificar a complexidade do mundo real em um modelo de software que é mais fácil de entender e trabalhar. Isso significa que o código pode ser mais modular, o que facilita a manutenção e o desenvolvimento de novos recursos.

A abstração também permite que os desenvolvedores trabalhem em níveis diferentes de detalhes. Eles podem se concentrar em objetos de alto nível e ignorar os detalhes de implementação subjacentes, ou se concentrar em detalhes de implementação específicos e ignorar a complexidade do sistema como um todo.

## Mecanismos de Classificação: Classes Abstratas e Interfaces

> Classes abstratas e interfaces são dois mecanismos de classificação que ajudam a definir tipos de objetos comuns e relacioná-los hierarquicamente. Classes abstratas são usadas para definir a estrutura comum para classes relacionadas, enquanto as interfaces são usadas para definir uma funcionalidade comum para classes não relacionadas.

Uma classe abstrata é uma classe que não pode ser instanciada, mas pode ser usada como uma superclasse para outras classes. Ela pode conter métodos concretos e abstratos, além de variáveis de instância e de classe. Métodos abstratos são aqueles que não possuem implementação e devem ser implementados por classes derivadas. Ao herdar de uma classe abstrata, uma classe derivada pode ter métodos adicionais, variáveis e outras funcionalidades. Classes abstratas são úteis para definir uma estrutura comum para classes relacionadas, enquanto permitindo que cada classe derivada forneça sua própria implementação.

Uma interface é uma coleção de métodos abstratos e constantes, mas sem implementação. Ela define um conjunto de operações que uma classe pode implementar, mas não contém nenhuma implementação concreta em si mesma. As interfaces são usadas para definir um conjunto comum de funcionalidades para várias classes que não estão necessariamente relacionadas por herança. Uma classe pode implementar várias interfaces, o que permite que ela forneça uma funcionalidade específica em diferentes contextos.

A diferença fundamental entre classes abstratas e interfaces é que as classes abstratas podem ter tanto métodos abstratos quanto concretos, enquanto as interfaces podem ter apenas métodos abstratos. Além disso, as classes abstratas são usadas para definir a estrutura comum para classes relacionadas, enquanto as interfaces são usadas para definir uma funcionalidade comum para classes não relacionadas.

## Vinculação Dinâmica e Polimorfismo de Herança

A vinculação dinâmica é o processo pelo qual um método é selecionado em tempo de execução, com base no tipo real do objeto em questão. Em outras palavras, quando um método é chamado em um objeto, o compilador não sabe exatamente qual método deve ser chamado, pois pode haver várias classes que implementam esse método. A decisão sobre qual método deve ser chamado é tomada em tempo de execução, com base no tipo real do objeto em questão. Isso permite que as classes derivadas substituam o comportamento dos métodos herdados de sua classe base, sem alterar o comportamento da classe base.

O polimorfismo de herança, por sua vez, é a capacidade de objetos de classes derivadas serem tratados como objetos de sua classe base. Isso significa que, se uma classe derivada for uma subclasse de uma classe base, ela pode ser usada onde quer que seja esperada uma instância da classe base. Isso é possível porque a classe derivada tem todas as propriedades e comportamentos da classe base, além de seus próprios recursos adicionais.

Juntos, a vinculação dinâmica e o polimorfismo de herança permitem a criação de código mais flexível e reutilizável em programação orientada a objetos. Por exemplo, imagine que você tem uma classe de Animal, com sub-classes como Cachorro e Gato, cada uma com seus próprios métodos específicos. Se você tiver uma lista de animais, poderá chamar métodos comuns, como "andar", em cada objeto, mas a vinculação dinâmica garantirá que a implementação correta do método "andar" seja chamada para cada objeto, com base no tipo real do objeto. Isso permite que você crie um código genérico que possa ser aplicado a muitas situações diferentes, ao mesmo tempo em que se beneficia das implementações específicas de cada subclasse.

## Tratamento de Exceções

> O tratamento de exceções é uma técnica importante em programação orientada a objetos, pois ajuda a tornar o código mais robusto e confiável, reduzindo o impacto de falhas inesperadas e melhorando a experiência do usuário.

O tratamento de exceções é um mecanismo fundamental em programação orientada a objetos para lidar com situações excepcionais que possam ocorrer durante a execução de um programa.

As exceções podem ocorrer por diversos motivos, como entrada de dados inválidos, falta de memória, erros de rede, entre outros. Sem um tratamento adequado, essas exceções podem interromper a execução do programa e causar falhas ou comportamentos indesejados.

Quando ocorre uma exceção, o sistema lança um objeto de exceção correspondente. Esse objeto contém informações sobre o tipo de exceção que ocorreu e uma mensagem de erro que pode ser usada para depuração.

Em seguida, o programa tenta tratar a exceção, por meio de blocos "try-catch". Um bloco "try" envolve o código que pode gerar uma exceção, enquanto um bloco "catch" contém o código que lida com a exceção, caso ocorra. Quando ocorre uma exceção dentro de um bloco "try", o controle do programa é transferido para o primeiro bloco "catch" correspondente à exceção.

É importante lembrar que o tratamento de exceções deve ser usado com cuidado e apenas em situações em que é realmente necessário, pois um uso excessivo pode tornar o código mais complexo e difícil de manter.
