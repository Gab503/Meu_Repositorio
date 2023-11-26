# Programação Orientada a Objetos em Kotlin
https://play.kotlinlang.org/ IDE online de Kotlin ( um lugar online para rodar os códigos)

Documentação oficial: https://kotlinlang.org/

Um paradigma de programação é definido pela maneira como um determinado programador resolve um certo problema, 
fornecendo visão e determinando como o programador estrutura e executa este programa. De certa forma, é uma receita de como 
uma pessoa pode resolver um problema.  

Os quatro principais paradigmas de programação são: paradigma imperativo, declarativo, funcional e orientado a objetos.
A diferenciação entre os paradigmas de programação é feita através das técnicas que estes mesmos paradigmas permitem ou proíbem.

    fun main()
    {
        printf("Hello World !")
        
    }

**Para que serve os Paradigmas:** Reutilização de código. Os paradigmas da programação iram ajudar a reutilizar um código já escrito, com um modelo de como fazer várias coisas com um mesmo código. 

* Programadores devem buscar não gerar bugs (erros no código), escrever seu código e o reutilizar, escrever códigos limpos,
isto é, lembrar que outra pessoa ( ou você futuramente) poderá ler seu código e também que o computador possa entender e saber o que fazer.



**Princípios da POO (Programação Orientada a Objetos):** 

**Classes:** Em programação Orientada a Objetos (POO), uma classe é uma estrutura fundamental que representa um tipo de objeto. Ela é um modelo ou plano para criar objetos.

**Objetos:**É uma instância de uma classe. Um objeto é uma entidade concreta que existe em tempo de execução e possui valores específicos para seus atributos. uma instância (ou objeto) está "conectada" à classe a partir da qual foi criada. Ela herda as características e comportamentos definidos pela classe, mas pode ter valores específicos para seus próprios atributos.

**Instância:** Um objeto concreto criado a partir do uso de uma classe é chamado de instância dessa classe. Por exemplo, se temos uma classe "Cachorro", uma instância seria um cachorro específico, com características e comportamentos específicos.

**Atributos:**Uma classe define atributos que são características ou propriedades dos objetos dessa classe. Por exemplo, se estivermos falando sobre uma classe "Carro", os atributos podem incluir cor, modelo, ano de fabricaçãom etc.

**Propriedades:** O termo "propriedades" é muitas vezes usado de forma intercambiável com "atributos". Em alguns contextos, "propriedades" pode ser usado para se referir especificamente aos atributos de uma classe que têm métodos associados, chamados de "métodos de propriedade". Esses métodos são usados para obter ou definir o valor de um atributo e podem incluir lógica adicional.

**Métodos:** Além dos atributos, uma classe também define métodos. Métodos são funções ou procedimentos que podem ser executados pelos objetos da classe. No contecto "Carro", métodos podem incluir "ligar", "deligar", "acelerar", etc. Em termos simples, os métodos são ações que um objeto da classe pode realizar.
Basicamente, os métodos em Kotlin são funções definidas dentro de uma classe. Eles representam o comportamento associado a uma instância específica da classe.

* Encapsulamento.

Esse conceito refere-se à capacidade de uma classe de ocultar a implementação interna e expor apenas uma interface bem definida. Em outras palavras, os detalhes internos de como uma classe realiza suas operações são encapsulados, tornando mais fácilo para outros desenvolvedores utilizarem a classe sem precisar entender todos os detalhes internos.
  
* Herança

Uma classe pode herdar características (atributos e métodos) de outra classe. A classe que é herdada é chamada de classe pai ou classe base, e a classe que herda é chamada de classe filha ou subclasse. Isso promove a reutilização de código e facilita a organização hierárquica de classes.
  
* Abstração

A abstração é a capacidade de modelar objetos do mundo real de forma simplificada, destacando apenas os detalhes relevante para o contexto do problema. Em outras palavras, ela permite que você represente conceitos complexos de maneira mais simples, ignorando detalhes desncessários 
  
* Polimorfismo

O polimorfismo permite que objetos de diferentes classes sejam tratados de maneira uniforme. Isso significa que você pode usar um objeto de uma classe filha onde um objeto da classe pai é esperado. O polimorfismo é frequentemente alcançado através do uso de interfaces ou herança. 

**Construtores:** Os construtores são responsáveis por inicializar os atributos de uma classe quando um objeto dessa classe é criado. Eles definem como os atributos serão configurados quando uma instância da classe for instanciada. Em Kotlin, você pode ter um construtor primário diretamente na declaração da classe ou, se necessário, construtores secundários adicionais. São escritos entre parênteses após o nome da classe. 

**Parâmetros:** São basicamente os inputs de uma classe ou função. 
    
**Variáveis:**

       fun main()
       {
       val name: String = "Gab" // variável imutável do tipo String ("semelhante a uma tupla no Python")

       var idade: Int? // Variável mutável que pode ser nula

       idade = 19
       println("Olá $name, você tem $idade anos")
       // $name == pegar o que estiver na variável name, parecido com o format do Python ou % do C
       
       }
       
* Por padrão, após a palavra-chave **class** se coloca o nome da classe cujo primeira letra é maiúscula, e crie um arquivo com o mesmo nome da classe e o defina nele. Ex:

 file: Dog

     class Dog
     {
         var name: String? = null
         // variável mutável chamada name do tipo(Isso que significa :) string, o ponto de interrogação significa que pode ser nulo ("vazio"). 
     }

Arquivo em execução:

    fun main()
    {
        val dog = Dog( )
        dog.name = "Linux"
        println(" Ola ${dog.name}")
    }

Em Kotlin, os dois pontos são usados para denotar o tipo de uma variável, o tipo de retorno de uma função, a herança de uma classe, a implementação de interfaces e para associar anotações.
    
Em Kotlin, cada instância de uma classe possui suas próprias cópias das propriedades da classe.

crio a classe Dog com um atributo name, dela instâncio dog ( crio um objeto chamado dog da classe Dog), e faço dog.name = "Linux" então o atributo name de dog recebe "Linux", e é imprimido Olá Linux.

 * Dentro da classe Dog há uma variável name, como está em uma classe chamamos ela de atributo / propriedade.

       class Dog // Classe Dog
       {
           var name: String? = null  // Propriedade da classe
    
           fun sayHi() // Método da classe
           {
                println("Hi my name's $name")
           }
   
       }  

       fun main()
       {
           val dog = Dog() // Instância / objeto criado a partir da classe
    
           dog.name = "Linux" // Atribuir Linux a propriedade name da intância dog.
    
           dog.sayHi() // chamando o método sayHi
       }

*  Em kotlin funções são declaradas com a palavra-chave fun. 

**Características das funções:**

* Possuem entrada, input

* Processa algo / faz alguma coisa.

* Tem um retorno (saída)

      class Dog 
      {
          var name: String? = null  
    
    
          fun sayHi(ownerName: String) 
         {
             println("Hi $ownerName, my name's $name")
         }
      }

      fun main()
      {
          val dog = Dog() 
    
          dog.name = "Linux" 
          dog.sayHi(ownerName = "Bilbo Bouseiro")

          val dogSara = Dog()
          dogSara.name = "Android"
         dogSara.sayHi(ownerName = "Sara")
      }

O método sayHi agora recebe um parâmetro ownerName do tipo String. Isso permite que o método saúda o proprietário do cachorro usando o nome do proprietário passado como argumento

ownerName é um parâmetro do método sayHi. Quando você chama o método sayHi e fornece um valor para ownerName, esse valor é usado dentro do método para personalizar a saudação.

**Getter (get):**

O método get é utilizado para obter o valor de uma propriedade. Quando você acessa o valor de uma propriedade, implicitamente ou explicitamente, o método get correspondente é chamado.

**Setter (set):**

O método set é utilizado para atribuir um novo valor a uma propriedade. Quando você atribui um valor a uma propriedade, implicitamente ou explicitamente, o método set correspondente é chamado.

Em muitas linguagens de programação, você precisa definir explicitamente os métodos get e set. No entanto, em Kotlin, esses métodos são gerados automaticamente para propriedades, a menos que você precise de um comportamento personalizado.

    class Dog constructor(private val ownerName: String)
    {
        var name: String? = null  
    
        fun sayHi() 
        {
            println("Hi my name's $name and my owner is $ownerName")
        }
    }

    fun main()
    {
        val dog = Dog(ownerName ="Bilbo Bouseiro") 
    
        dog.name = "Linux" 
        dog.sayHi() 
    }

**Private:** Quando você marca um membro de uma classe como private, você está dizendo que esse membro só deve ser acessado dentro da própria classe em que foi declarado. Ou seja, ele é "escondido" do código externo à classe.

Isso proporciona encapsulamento, que é um dos princípios fundamentais da programação orientada a objetos. O encapsulamento permite que você controle o acesso aos detalhes internos de uma classe, fornecendo uma interface externa (métodos públicos e propriedades) enquanto mantém os detalhes internos (membros privados) ocultos e seguros.





1. Declaração da classe Dog:

É declarada uma classe chamada Dog que tem uma propriedade ownerName (inicializada pelo construtor) e uma propriedade opcional name.

2. Construtor e Propriedade ownerName:

O construtor primário da classe Dog recebe um parâmetro ownerName e o marca como private (acesso restrito à própria classe). Isso significa que ownerName é uma propriedade da classe e está acessível apenas dentro dela.

3. Propriedade name:

É declarada uma propriedade name, que é uma variável que pode armazenar um valor do tipo String ou null. Inicialmente, está configurada como null.

4. Método sayHi():

Um método chamado sayHi é declarado dentro da classe Dog. Este método imprime uma mensagem no console usando interpolação de strings, referenciando os valores das propriedades name e ownerName.

5. Função main():

Na função main, é criada uma instância da classe Dog chamada dog com o nome do proprietário definido como "Bilbo Bouseiro".

6. Atribuição de Valor à Propriedade name:

O valor da propriedade name do objeto dog é alterado para "Linux".

7. Chamada do Método sayHi():

O método sayHi do objeto dog é chamado. Este método imprime a mensagem formatada que inclui os valores de name e ownerName


    class Dog 
    {
        var owner: Human? = null 
        var name: String? = null  
    
        fun sayHi() 
        {
            println("Hi my name's $name and my owner is ${owner?.name}")
        }
    }

    class Human
    {
        var name: String? = null
    }

    fun main()
    {
        val gab = Human()
        gab.name = "Gabriela"
    
        val dog = Dog()
        dog.owner = gab
        dog.name = "Linux" 
        dog.sayHi() 
    
        val sara = Human()
        sara.name = "Sara"
        dog.owner = sara
        dog.sayHi()

    }

Saída:

Hi my name's Linux and my owner is Gabriela

Hi my name's Linux and my owner is Sara

**Observação!** O mais importante em POO, é que cada classe tenha um objetivo, cada classe tem que ter um propósito. 

**Data class:** Em Kotlin, uma "data class" (classe de dados) é uma classe especializada que é frequentemente usada para representar dados imutáveis. Ela é projetada para armazenar dados de maneira concisa e fornecer funcionalidades úteis automaticamente. Para criar uma data class em Kotlin, você pode usar a palavra-chave data antes da palavra-chave class.

Uma data class em Kotlin é uma forma concisa de criar uma classe que é principalmente usada para armazenar dados. A palavra-chave data fornece automaticamente várias funcionalidades úteis que, de outra forma, você teria que escrever manualmente, economizando assim linhas de código e tornando o código mais legível.

Ao usar uma data class, o Kotlin automaticamente gera implementações padrão para os seguintes métodos com base nas propriedades declaradas na classe:

1. equals(): Compara os valores das propriedades de duas instâncias e verifica se são iguais.

2. hashCode(): Gera um código de hash para a instância, útil ao usar a classe em estruturas de dados que dependem de hash.

3. toString(): Cria uma representação de string da instância, útil para depuração.

4. componentN(): Fornece funções de desestruturação para acessar as propriedades individualmente.

Além disso, uma data class também inclui uma função copy(), que permite criar uma cópia modificada da instância com a capacidade de alterar alguns valores.

Isso torna as data classes ideais para situações em que você precisa criar classes simples para armazenar dados e realizar operações comuns, sem a necessidade de escrever manualmente os métodos mencionados acima.


    class Motor
    {
        private var ligado: Boolean = false
        private var nivelCombustivel: Int = 2
    
        fun ligar()
        {
            ligado = true 
        }
    
        fun desligar()
        {
            ligado = false
        }
    
        fun estaLigado() : Boolean
        {
            return ligado
        }
    
        fun temCombustivel() : Boolean
        {
            return nivelCombustivel > 0
        }
    
        fun gastandoCombustivel()
        {
            println("Gastando Combustível, nível atual do tanque: $nivelCombustivel litros")
            nivelCombustivel--
        }
    }

    class Carro constructor (private val motor: Motor) 
    {
        var cor: String? = null
    
        fun ligar()
        {
            println("Ligando o carro...")
            motor.ligar()
        }
    
        fun desligar()
        {
            motor.desligar()
            println("Carro desligado")
        }
    
        fun anda()
        {
            if (motor.estaLigado() && motor.temCombustivel())
            {
                println("Carro andando: vruun vrruuunnn! ")
            }
            else if (!motor.temCombustivel())
            {
                println("Precisa de combustével! ")
            }
            else
            {
                println("Pro carro andar, precisa ligar o carro primeiro né!")
            }
        
            motor.gastandoCombustivel()
        }
    
        fun freia()
        {
            println("Freiando o Carro")
        }
    
        fun buzina()
        {
            println("Bi-Bi Bi-Bi ")
        }
    
    }


    fun main()
    {
        var motor = Motor()
        val meu_carro = Carro(motor)
        meu_carro.ligar()
        meu_carr0.anda()
    }

Melhorando a leitura deste código / Otimizando:

    class Motor
    {
        private var ligado: Boolean = false
        private var nivelCombustivel: Int = 2
    
        fun ligar()
        {
            println("Ligando o motor...)
            ligado = true 
        }
    
        fun desligar()
        {
            println("Desligando o motor ...")
            ligado = false
        }
    
        fun estaLigado() : Boolean
        {
            return ligado
        }
    
        fun temCombustivel() : Boolean
        {
            return nivelCombustivel > 0
        }
    
        fun gastandoCombustivel()
        {
            println("Gastando Combustível, nível atual do tanque: $nivelCombustivel litros")
            nivelCombustivel--
        }
    }

    class Carro constructor (private val motor: Motor) 
    {
    
        fun ligar()
        {
            motor.ligar()
        }
    
        fun desligar()
        {
            motor.desligar()
        }
    
        fun anda()
        {
            when
            {
                !motor.estaLigado() -> println("Pro carro andar, precisa ligar o carro primeiro né!")
                !motor.temCombustivel() -> 
                {
                    println("Precisa de combustível! ") 
                    motor.desligar()
                }
                else ->
                {
                    motor.gastandoCombustivel()
                    println("Carro andando: vruun vrruuunnn! ") 
                }
            }
        }
    
        fun freia()
        {
            println("Freiando o Carro")
        }
    
        fun buzina()
        {
            println("Bi-Bi Bi-Bi ")
        } 
    }

    fun main()
    {
        var motor = Motor()
        val meu_carro = Carro(motor)
        meu_carro.ligar()
        meu_carro.anda()
        meu_carro.anda()
        meu_carro.anda()
    }


* Saída:

      Ligando o carro...
      Gastando Combustível, nível atual do tanque: 2 litros
      Carro andando: vruun vrruuunnn!
  
      Gastando Combustível, nível atual do tanque: 1 litros
      Carro andando: vruun vrruuunnn!
  
      precisa de combustível!

 **código passo a passo:**

1. **Classe `Motor`:**
   - A classe `Motor` representa um motor de um veículo e possui as seguintes propriedades privadas:
      - `ligado`: Indica se o motor está ligado (`true`) ou desligado (`false`).
      - `nivelCombustivel`: Representa o nível de combustível no tanque do veículo.
   - Métodos da classe `Motor`:
      - `ligar()`: Liga o motor, configurando a propriedade `ligado` para `true`.
      - `desligar()`: Desliga o motor, configurando a propriedade `ligado` para `false`.
      - `estaLigado()`: Retorna `true` se o motor estiver ligado, `false` caso contrário.
      - `temCombustivel()`: Retorna `true` se houver combustível suficiente, `false` caso contrário.
      - `gastandoCombustivel()`: Simula o gasto de combustível, reduzindo o `nivelCombustivel` em 1 e imprimindo uma mensagem.

2. **Classe `Carro`:**
   - A classe `Carro` possui uma propriedade privada `motor` do tipo `Motor` (injetada através do construtor). Isso representa a composição de um carro contendo um motor.
   - Métodos da classe `Carro`:
      - `ligar()`: Liga o carro chamando o método `ligar()` do motor.
      - `desligar()`: Desliga o carro chamando o método `desligar()` do motor.
      - `anda()`: Verifica se o carro pode andar (está ligado e tem combustível) e simula o consumo de combustível chamando o método `gastandoCombustivel()` do motor.
      - `freia()`: Simula a ação de frear o carro.
      - `buzina()`: Simula o som da buzina do carro.

3. **Função `main()`:**
   - Cria uma instância de `Motor` chamada `motor`.
   - Cria uma instância de `Carro` chamada `meu_carro`, passando a instância de `motor` como argumento para o construtor.
   - Liga o carro, chama o método `anda()` três vezes, imprimindo mensagens correspondentes ao funcionamento do carro.


**Funções Abstratas:** Funções abstratas são funções que são declaradas em uma classe, mas não são implementadas nessa classe. A implementação real da função é fornecida pelas subclasses dessa classe. Em outras palavras, uma função abstrata define uma assinatura (nome, parâmetros e tipo de retorno), mas não fornece uma implementação concreta.

Em linguagens de programação que suportam programação orientada a objetos, como Java, C++, ou Kotlin, as funções abstratas são muitas vezes usadas em conjunto com o conceito de classes abstratas ou interfaces.

Esse mecanismo permite definir comportamentos comuns em uma classe base enquanto fornece flexibilidade para implementações específicas em subclasses. Isso é uma parte importante do polimorfismo, que é a capacidade de tratar objetos de diferentes classes de maneira uniforme.

A utilização da palavra-chave override (sobrescrever) em uma linguagem de programação orientada a objetos, como Kotlin, é uma forma de indicar explicitamente que você está fornecendo uma implementação específica para uma função que foi declarada como abstrata na classe base (superclasse) ou definida em uma interface.

Ao marcar uma função com override, você está informando ao compilador que está substituindo a implementação da função da classe pai. Isso é uma garantia para o compilador e para quem está lendo o código, indicando que a função na subclasse tem a mesma assinatura (nome, parâmetros e tipo de retorno) que a função na classe base.






