# Introdução

Kotlin é uma linguagem de programação um tanto quanto recente, mas já madura, destinada a tornar os desenvolvedores(as) 
mais felizes.

É concisa, segura, interoperável com java e outras linguagens, além de oferecer muitas maneiras de reutilizar código entre
várias plataformas para uma programação produtiva. <br> Vale ressaltar, que é importante ler a documentação oficial do kotlin 
que é super tranquilo de entender, lembrando inclusive que as informações contidas aqui, minhas anotações do curso da Dio.me,
também são baseados na documentação do Kotlin. 
  
## Hello World

    fun main()
    {
        println("Hello, world!")
        // Result = Hello, world! this is a comment
    }
    
Explicação: fun é como se fosse o def do Python, é usado para declarar uma função. 

A main() é a função onde seu programa começa. O Corpo de uma função em Kotlin, é escrito entre chaves { }.

 A função print( ) é usada para imprimir textos/string na tela. Quando não tem mais espaço na tela, será exibido na
 linha de baixo o restante. 
 
 Já a função println( ), pula linha. Basta lembrá-se do escraval do portugol.
 
 Outra semelhança com Python é que não precisa de ; (ponto vírgula) no final de cada "código".
    
Documentação ofical do Kotlin: https://kotlinlang.org/docs/kotlin-tour-hello-world.html

# Funções - Valores de Parâmetro e Argumentos Nomeados

## Funções

  
    fun sum(x: Int, y: Int): Int
    {
        return x + y
    }
    fun main() 
    {
        println(sum(1, 2))
        // 3
    }
    
    
Como mencionado anteriormente, você pode criar suas próprias funções em Kottlin usando o comando fun. 
Os parâmetros da função são escritos entre parênteses ( ). 

O tipo de retorno é escrito após os parênteses da função (),
separados por dois ponto : O corpo de uma função é escrito entre chaves { }.

A palavra-chave return é usada para sair ou 
retornar algo de uma função. 

Se você é iniciante assim como eu, pode ser ver preso no entendimento da função return, 
usando uma analogia eu conseguir entender, é mais ou menos assim:<br>Imagine um restaurante, nele há a cozinha, a mesa dos
cliente etc... nos concentraremos apenas nesses dois, a cozinha é onde são preparados os pratos para os clientes, então vem um 
garçom pegar na cozinha os pratos para levar aos cliente. Nessa analogia, a cozinha seria a função, o garçom é a função return, 
que vai "levar algo de fora da função", geralmemte um valor, ou melhor, retorna algo para o código. Exemplo de funções em
Kotlin:
  
*  1
  
* Declara uma função chamada de printMessage
  
* Possui um parâmetro chamado message do tipo String, isto é, recebe como parâmetro um texto para fazer algo
Neste caso é imprimir a mensagem recebida ( o parâmetro).

* Unit -> o tipo de return; Significa qualquer coisa, pode usar ou não, é opcional neste caso.

        // 1
        fun printMessage(message: String): Unit          
        {                                                                                                                  
            println(message)                    
        }
    
*  2

* Declara uma função chamada printMessageWithPrefix. Observe o prefixo, ele está recebendo uma atribuição de valor
 Um valor padrão. Caso não seja específicado o valor Será atribuido info

 * Interpolação de strings = ''%prefix'' -> Substituindo + para concadernar strings.

        // 2
        fun printMessageWithPrefix(message: String, prefix: String = "info")
        {      
            println("$prefix $message")
         }
    
*  3

* Uma função chamada soma (sum), vai receber valores inteiros e retorna um Int (número inteiro) também,
 com a função return, retorna o resultado.

        // 3
        fun sum(x: Int, y: Int):Int
        {                                               
            return x + y
        }

* 4
  
* Um função de multiplicação. Retornando x * y, o return está implícito neste caso.
  
      // 4 
      fun multiply(x: Int, y: Int) = x * y                                       
     .
    
       fun main(){        
        // 5- imprimir a mensagem ''Hello''
            printMessage("Hello")                                                  
        
        // 6- imprimir Log Hello
            printMessageWithPrefix("Hello", "Log")                                 
        
        // 7- Não foi específicado o prefixo = info Hello
        printMessageWithPrefix("Hello")                                        
        
        // 8 - O mesmo que a 6, mas para demostrar atribuição de variável.
        printMessageWithPrefix(prefix = "Log", message = "Hello")              
        
       // 9 soma  
        println(sum(1, 2))                                                     
        
        // Multiplicação
        println(multiply(2, 4))                                                // 10 
       }
  
Observação: Você deve ter notado o uso de do símbolo $, este símbolo é usado para acessar os valores dos parâmetros,
convertê-los em Stringtipo e concatená-los em uma String para impressão. Possui um uso semelhante ao format do Python. 

# Parâmetros Vararg

## Argumentos nomeados
Para um código conciso, ao chamar sua função, você não precisa incluir nomes de parâmetros. No entanto, incluir nomes 
de parâmetros torna seu código mais fácil de ler. Isso é chamado de uso de argumentos nomeados. Se você incluir nomes de 
parâmetros. poderá escrevê-los em qualquer ordem. 

## Vararg


    
    fun main(){
        // Vararg = receber quantas mensagens quiser, desde que sejam string. Ou melhor quantidade de parâmetros indefinida.
        fun printAll(vararg messages: String) {
            for (m in messages) println(m)
        }
        printAll("Hello", "Hello","Salut", "Hola")
        
        fun printAllWithPrefix(vararg messages: String, prefix: String) {
            for (m in messages) println(prefix + m)
        }
        // prefix = neste caso é um argumento nomeado.
        printAllWithPrefix("Hello", "Hallo", "Salut", "Hola", 
        prefix = "Greeting: ")

        fun log(vararg entries: String) {
            printAll(*entries)
        }
        }
        
  Observação, se tiver uma função, que chame outra, que também é um vararg, tem que usar * para ser um vararg também e não um Array. 
  
  Vararg = Basicamente, permite colocar uma quantidade de parâmetros indefinida. Permite ter quantos elementos necessários de um
  determinado tipo, neste caso, do tipo string. 


# Variáveis Var e val
Variáveis são como caixas na memória do seu computador, onde podem armazenar itens.

Var é uma váriavel mutável, podendo assim ser alterada se necessário e quando quiser. 
Enquanto val, é uma váriavel imutável, não podendo ser alterado. 
  
    fun main() 
    {
        var a: String = "Initial"
        println(a)
        val b: Int = 1
        val c = 3
        println(b) 
        println(c)
        a = "Banana"
        println(a)
    }

    fun SomeCondition() = false

    fun main() 
    {
    
      val d: Int
    
    if (SomeCondition())
    {
        d = 1
    }else 
    {
        d = 2
    }
    println(d)
    }

Neste último exemplo, demonstra um uso de variável val, básicamente, se SomeCondition for true, irá ter 1 como saída de dados.
Mas se for false, irá ter 2.

# Null Safety Nulidade
Segurança nula, ou nulidade, é a característica do Kotlin que faz com que os desenvolvedores deixem de forma explícita,
se uma determinada variável vai receber ou não um valor nulo.
    
     fun main()
     {
            // Não pode ser nula, e sim uma string.
            // ao atribuir null, vai dar erro pois é uma string, não nula
            
            var neverNull: String = "This can't be null"
            
            neverNull = null
            
            // Strin? vai aceitar string ou nulo.
            var nullable: String? = "You can keep a null here"
            var nullable = null
            
            // Não foi específicada, vai automaticamente ser não nula
            var inferredNonNull = "The compiler assumes non-null"
            inferredNonNull = null
            
            fun strLength(notNull: String): Int
            {
                return notNull.length
            }
            strLength(neverNull)
            strLength(nullable)
        }

    
        // str?.lenght ? : 0 ->Se não for nula acesse isso
    fun strLength(str: String?): Int 
    {
       return str?.length ? : 0
    }
  Outro exemplo:
        
        fun describeString(maybeString: String?):String
        {
            if (maybeString != null && maybeString.length > 0)
            {
                return "String of length ${maybeString.length}"
            }
            else
            {
                return "empty or null string"
            }
        }
        
        fun main()
        {
            println(describeString(null))
            println(describeString(""))
            println(describeString("Dio.me"))
        
        }

# Classes
Classes são basicamente uma estrutura de dados que você pode moldar da forma que quiser.
A palavra reservada para definir uma classe em Kotlin (e na maioria das linguagens) é class. 
As classes são um modelo para a criação de objetos (POO). Exemplo:

    // Declarar uma classe chamada Customer
    class Customer
    
    // Uma classe contact, com dois parâmetros de construção personalizados
    class Contact(val id: Int, var email: String) 
    
    fun main () 
    {
        
        val customer = Customer()
        
        val contact = Contact(1, "may@gmail.com")
        
        println(contact.id)
        println(contact.email)
        contact.email = "Jane@gmail.com"
        println(contact.email)
        
    }
  
# Generics Class
A ideia principal de classes genéricas, é ter flexibilidade na tipagem das suas informações.
É muito comum ver sendo usada em coleções (variáveis compostas) do tipo Listas, Mapas, Conjuntos.
    
    // Vai receber vararg E, isto é, qualquer coisa.
    // Pois está como parâmetro genérico da classe MutableStack
  
    class MutableStack<E>(vararg items: E)
    {
    
    // Converte para uma lista os elementos. 
    private val elements = items.toMutableList()
    
    // Adiciona o elemento na lista
    fun push(element: E) = elements.add(element)
    
    // pegar o último mas sem remover.
    fun peek(): E = elements.last()
    
    // Remove o último elemento.
    fun pop(): E = elements.removeAt(elements.size -1)
    
    // Verificar se está vazia.
    fun isEmpty() = elements.isEmpty()
    
    // Tamanho
    fun size() = elements.size
    
    // Converter para texto.
    override fun toString() = "MutableStack(${elements.joinToString()})"
    
     }

    fun main () 
    {
    val stack = MutableStack(0.62, 3.14, 2.7)
    stack.push(9.87)
    println(stack)
    
    println("peek(): ${stack.peek()}")
    println(stack)
    
    for (i in 1..stack.size())
    {
        println("pop(): ${stack.pop()}")
        println(stack)
    }
    }

# Funções Genéricas
Utlizando o mesmo pricípio de classes genéricas, para parâmetizar um tipo de maneira generica, mas desta vez em uma função.
  
    interface Source<out T> 
    {
    fun nextT(): T
    }

    fun demo(strs: Source<String>) 
    {
     val objects: Source<Any> = strs // This is OK, since T is an out-parameter
    
    }
Observação, este exemplo acima não foi muito bom, mas é basicamente o mesmo de classes genericas, mas ao invés de
usar classes é funções. Exemplo 
        
          fun element<E>... 
  
https://kotlinlang.org/docs/generics.html#use-site-variance-type-projections

# When
Use When quando você tiver uma expressão condicional com múltiplas ramificações. 

Em Kotlin, when é uma estrutura que pode ser usada tanto como uma declaração (when statement) quanto como uma 
expressão (when expression). Ambas são usadas para substituir blocos switch encontrados em outras linguagens, 
mas o when do Kotlin é mais poderoso e expressivo.

O -> em Kotlin é usado para associar um bloco de código ou uma expressão a um ramo específico em uma estrutura when. 
Ele funciona de maneira semelhante ao case ou -> em outras linguagens de programação que têm uma construção switch ou case.



## When statement / when declaração
A forma mais básica de when é como uma declaração, semelhante a um switch em Java ou C.
 
    val x = 5

    when (x) 
    {
    1 -> println("Um")
    2 -> println("Dois")
    3 -> println("Três")
    else -> println("Outro valor")
    }

.

    fun main() 
    {
    cases("Hello")
    cases(1)
    cases(0L)
    cases(MyClass())
    cases("hello")
    }

    fun cases(obj: Any) 
    {
    when (obj)
    {
        1 -> println("One")
        "Hello" -> println("Greeting")
        is Long -> println("Long")
        !is String -> println("Not is string")
        else -> println("Unknow")
        // Saída:
        // Greeting
        // One
        // Long
        // Not is string
        // Unknow
    }
    }



    class MyClass

   # When Expression
A forma mais avançada e poderosa de when é usá-lo como uma expressão, que permite atribuir o resultado do when a uma
variável ou usá-lo em outros contextos de expressão    

    val result = when (x) 
    {
    1 -> "Um"
    2 -> "Dois"
    3 -> "Três"
    else -> "Outro valor"
    }

    println(result)
.


    fun main() 
    {
      println(whenAssign("Hello"))
      println(whenAssign(3.4))
      println(whenAssign(1))
      println(whenAssign(MyClass()))
      }
  
     fun whenAssign(obj: Any):Any
     {
      val result = when (obj)
      {
          1 -> "one"
          "Hello" -> 1
          is Long -> false
          else -> 42
      }
      return result
     }
  
     class MyClass

# Estrutura de Repetição for
    
    fun main()
    {
    
    // criando uma lista de bolos
    // listOf  está dispônivel de forma implícita também.
    // tal função, vai cria uma lista imutável.
    val cakes = listOf("carrot", "cheese", "Chocolate")
    
    for (cake in cakes)
    {
        println("Yummy, it's a $cake cake!")
    }
    }

# Loops: While and do while
O laço de repetição while, vai executar algo, enquanto for true, enquanto a condição for verdadeira.

## Do while
Enquanto o while faz a condição sempre em primeiro, o do while primeiro executa o do, e depois passa a condição. Então irá executar
algo dentro do "Do" enquanto a condição for True ( verdadeira) 
  
    fun eatACake() = println("Eat a Cake")
    fun bakeACake() = println("Baker a Caker")

    fun main()
    {
    var cakesEaten = 0
    var cakesBaked = 0
    
    while (cakesEaten < 5) 
    {
        eatACake()
        cakesEaten ++
    }
    
    do
    {
        bakeACake() 
        cakesBaked++
    }   while (cakesBaked < cakesEaten)

    }

Loops: Iterators
Iterators são as interações que dão a capacidade de algo ser interado. Poder percorrer os elementos de uma estrutura de dados.
O Kotlin permite implementear operadores iterators personalizados.

É semelhante ao enumerate do Python.
    
    class Animal(val name: String)

    class Zoo (val animals: List<Animal>)
    {
    
    // operator = cria a capacidade de ter iterações na classe zoo.
    operator fun iterator(): Iterator<Animal>
    {
       return animals.iterator()
    }
    }

    fun main()
    {
    val zoo = Zoo(listOf(Animal("Zebra"), Animal("Lion")))
    
    for (animal in zoo){
        println("Watch out, it's a ${animal.name}")
    }
    }

# Rangers: Ifs e loops com Char
Além dos números, os Rangers também suportam caracteres.
    

        fun main()
        {
            for (c in 'a'..'d'){
                print(c)
            }
            print(" ")
            
            for (c in 'z' downTo 's' step 2)
            {
                print(c)
            }
            print(" ")
            
            }
É o mesmo processo, só que desta vez com "strings" ao invés de inteiros. Vale ressaltar que os Rangers também são suportados 
em estruturas de repetições e condicionais. 
  
         
      fun main()
      {
            val x = 2
            if (x in 1..5)
            {
                print("X is in range from 1 to 5")
            }
            println()
            
            if (x !in 6..10)
            {
                print("X is not in ranger from 6 to 10")
            }
            
        }  
  
  # Verificação de igualdade == e ===
  Existe duas formas de verificar a igualdade de dois objetos, uma seria uma comparação estrutural, 
  que é feita com a sintaxe ==, e a outra uma comparação referencial, com a sintaxe ===.
  
    fun main()
    {
    val authors = setOf ("Shakespeare", "Hemigway", "Twain")
    val writers = setOf("Twain", "Shakespeare", "Hemigway")
    
    // Comparação estrutural.
    println(authors == writers)

    // comparação referencial.
    println(authors === writers)
    }  
    // true
    // false

Ao invés de ser uma lista, são do tipo set, esse tipo não aceita duplicatas, se tiver um elemento duplicado,
ele simplesmente não aceita essa duplicata. 

Neste exemplo acima, você deve ter observado que possuem os mesmo items em ordens diferentes. 
Isto é, estruturalmente, possuem os mesmos valores, mas, possuem referencias diferentes (ordem diferentes = referencias 
diferentes). 

Podemos pensar assim, uma comparação estrutural, é para saber se possuem os mesmo elementos. 

Já uma comparação referencial é para ver se ambos são de fatos iguais, isto é, identicos.
  
# Expressão Condicional
O if é usado como expressão.
        
        fun main()
        {
        // está fazendo a verificação se a > b e retornando a, 
        // Senão vai retornar b
        
        fun max(a: Int, b: Int) = if (a > b) a else b
        println(max(99, -42))
        
        // Mesma coisa que fazer assim: 
        fun maxOld(a: Int, b: Int): Int
        {
            if (a > b)
            {
                return a
            }
            else
            {
                return b
            }
        }
    }
    
 Observe a diferença na quantidade de código.
  
# Listas(List)
As listas armazenam itens na ordem em que são adicionados e permitem itens duplicado. Ao criar listas, o 
Kotlin pode inferir o tipo de itens armazenados. Para declarar o itpo explicitamente, adicione-o entre conlchetes 
angulares, exemplo, <Int> após a declaração da lista.
    
A função listOf() vai criar uma lista imutável.

A função mutableListOf() vai criar uma lista mutável.

    

        val systemUsers: MutableList<Int> = mutableListOf(1, 2, 3)
            val sudoers: List<Int> = systemUsers
            
            fun addSystemUser(newUser: Int)
            {
                systemUsers.add(newUser)
            }
            
            fun getSysSudoers(): List<Int> {
                return sudoers
            }
            
            fun main()
            {
                addSystemUser(4)
                println("Tot sudoers: ${getSysSudoers().size}")
                getSysSudoers().forEach{
                    i -> println("Some useful info on user $i")
                }
              
            }
# Conjuntos Set
Enquanto as listas são ordenadas e permitem itens duplicados, os conjuntos não são ordenados (a ordem não importa) e
armazenam apenas itens únicos.

Para criar conjuntos imutáveis, utlize setOf().E para criar conjuntos mutáveis, use mutableSetOf()
Semelhante as lista, para criar uma variável somente para leitura, utlize apenas set (no caso das listas é List)

Ao criar conjuntos, o Kotlin pode inferir o tipo de itens armazenados. Para declarar o tipo explicitamente, adicione o tipo 
entre colchetes angulares, <>, após a declaração set.


        val openIssues: MutableSet<String> = mutableSetOf("uniqueDescr1", "uniqueDescr2", "uniqueDescr3")

            fun addIssue(uniqueDesc: String): Boolean
            {
                return openIssues.add(uniqueDesc)
            }
            
            fun getStatusLog(isAdded: Boolean): String
            {
                return if (isAdded) "registered correctly." else "marked as duplicate and rejected."
            }
            
            fun main()
            {
                val aNewIssue: String = "uniqueDescr4"
                val anIssueALreadyIn: String = "uniqueDescr2"
                
                println("Issue $aNewIssue ${getStatusLog(addIssue(aNewIssue))}")
                println("Issue $anIssueALreadyIn ${getStatusLog(addIssue(anIssueALreadyIn))}")
            }

# Mapas (Map)
Os mapas armazenam itens como pares de valores-chaves. Você acessa o valor referenciando a chave. 
Os mapas são úteis se você quiser um valor sem usar um índice numerado, como uma lista. Semelhantes as bibliotecas do Python.
    
Para criar um mapa imutável use: mapOf()

Para criar um mapa mutável use: mutableMapOf()
    
        
        // Uma constante imutável com valor 15
        const val POINTS_X_PASS: Int = 15
        
        // contas com um mapa mutável, o 1 tem 100, o 2 100, e o terceiro 100.
        val EZPassAccounts: MutableMap<Int, Int> = mutableMapOf(1 to 100, 2 to 100, 3 to 100)
        
        // Uma cópia somente para leitura.
        val EZPassReport: Map<Int, Int> = EZPassAccounts
        
        // update doss pontos,vai receber um Id da conta
        fun updatePointsCredit(accountId: Int)
        {
            
            //Vai ver se tem o accountId
            if (EZPassAccounts.containskey(accountId))
            {
              
                // se true, faz o update, adicionando os pontos ao que ele já tem
                println("updating $accountId...")
                EZPassAccounts[accountId] = EZPassAccounts.getValue(accountId) + POINTS_X_PASS
            } else
            {
                println("Error: Trying to update a non-existing account (id: $accountId)")
            }
        }
        
        fun accountsReport() 
        {
            println("EZ-Pass report: ")
            EZPassReport.forEach{
                k, v -> println("ID $k: credit $v")
            }
        }
        
        fun main()
        {
            accountsReport()
            updatePointsCredit(1)
            updatePointsCredit(1)
            updatePointsCredit(5)
            accountsReport()
        }


# Funções úteis
A primeira é a filter, uma vez que você cria uma variável que seja uma coleção, ela permite filtrar os elementos dela,
baseado em um predicado ( uma regra de filtro)
    
        fun main()
        {
        val numbers = listOf(1, -2, 3, -4, 5, -6)
        val positives = numbers.filter{x -> x >0}
        val negatives = numbers.filter{it <0}
        println(positives)
        println(negatives)
       }


## Expressões Lambda
Kotlin permite escrever códigos ainda mais concisos para funções usando expressões lambda. Dentro da expressão Lambda,
você escreve: Os parâmetros seguidos por um ->.O corpo da função após o ->.

    
        fun main() 
        {
            println({ string: String -> string.uppercase() }("hello"))
            // HELLO
        }
    

  A filter() aceita uma expressão lambda como predicado.

  {x -> x > 0} pega cada elemento da lista e retorna apenas aqueles que são positivos. Ou usa it como no exemplo acima.
    

A função map() também aceita uma expressão lambda como predicado.

    
        fun main()
        {
    
            val numbers = listOf(1, -2, 3, -4, 5, -6)
            val doubled = numbers.map { x -> x * 2 }
            val tripled = numbers.map { it * 3 }
            println(doubled)
            // [2, -4, 6, -8, 10, -12]
            println(tripled)
            // [3, -6, 9, -12, 15, -18]
            
        }

  Neste exemplo acima, irá transformar todos os elementos da coleção. 
    
        fun main()
        {
            val numbers = listOf(1 , -2, 3, -4, 5, -6)
            val anyNegative = numbers.any { it < 0 }
            val anyGT6 = numbers.any{it > 6}
            
            println(numbers)
            println(anyNegative)
            println(anyGT6)
        }
 flatMap.
      
     fun main() 
     {
            val fruitsBag = listOf("apple", "orange", "banana", "grapes")
            val clothesBag = listOf("Shirts", "pants", "jeans")
            val cart = listOf(fruitsBag, clothesBag)
            val mapBag = cart.map{it}
            val flatMapBag = cart.flatMap{it}
            
            println("Your bags are: $mapBag")
            println("The things you bought are: $flatMapBag")
            // Your bags are: [[apple, orange, banana, grapes], [Shirts, pants, jeans]]
            // The things you bought are: [apple, orange, banana, grapes, Shirts, pants, jeans]
        
        }
    

    # Orientação a Objetos e Tipos de Classes - POO

## Abstração
Habilidade de concentrar-se nos apesctos essenciais de um domínio, ignorando características menos importantes ou acidentais.

Nesse contexto, classes e objetos são abstrações de entidade existentes no domínio/problema em questão.
 
Pensar em como seria aquele problema no mundo real. Abstrair a solução, em como ela seria no mundo real.
Semelhante ao pensamento computacional.

## Encapsulamento
Encapsular significa esconder a implementação dos objetos, criando assim interfaces de uso mais concisas 
e fáceis de usar/entender.

O encapsulamento favore principalmente dois aspectos de um sistema: a mutenção e a evulação.

Não necessáriamente, quando você projeto ou modela um sistema orientado a objetos, todo os seus métodos, no caso do 
Kotlin funções, vão ser públicos. 

## Herança
Permite que as classes compartilhem suas características (propriedades) e comportamentos (funções) entre si

A herança é usada na intenção de promover o recuo de código através de estruturas mais genéricas e flexíveis.

Pense como se fosse uma árvore, o troco seria a classe (superclasse), os galhos (subclasses) seriam sua herança.
Os galhos teriam suas próprias características, mas aida assim, também teriam as características do tronco. 

A herança permite que várias classes reutilizem um comportamento em comum.

## Polimorfismo
Capacidade de um objeto poder ser referenciado de várias formas, ou seja, é capaz de tratar objetos criados a 
partir das classes específicas como objetos de uma classe genérica.

Esse conceito nos oferece possibilidade incríveis para a criação de soluções mais génericas.

O polimorfismo permite que objetos de diferentes classes sejam tratados de maneira uniforme, por exemplo, várias classes podem
ter um método chamado "apresentar", e cada uma implementará esse método de forma diferente.

## Herança simples
       
    // Para que uma classe base, que possa ser uma classe de herença, "pai"de outra classe
    // ela precisa do comando open class, que diz que ela pode ser usada como extensão de outra classe
    // Tanto a classe quanto a função estão abertas.
    // Isso significa que a classe Dog pode ser alvo de uma hierarquia
    open class Dog{
        open fun sayHello()
        {             
            println("Wow Wow")
        }
    }
    // Uma classe de do cachorro Yokshire está herdando a classe Dog, todas as suas características e comportamentos da classe
    // Dog.
    class Yorkshire : Dog()
    {             
        override fun sayHello()
        {      // Override = sobrescrever a função sayHello que é uma função aberta 
            println("Wif Wif! ")      // se não fosse aberta, não seria possível. 
        }
    }
    
    // Polimorfismo. 
    // instânciar um cachorro, do tipo Dog, tratando-o como um cachorro.
    fun main()
    {
        val dog: Dog = Yorkshire()
        dog.sayHello()
    }
    
    // Saída: Wif Wif!

A herança entre classes é declarada por dois pontos ( : ). Para tornar uma classe herdável, marque-a como open.

## Herança com Construtor Parametrizado
Imagine que você está cozinhando uma torta. Você pode ter uma receita básica para torta que você usa para todas as
tortas que você faz. No entanto, você pode querer fazer diferentes tipos de tortas, como torta de chocolate ou torta de maçã.
Para fazer isso, você pode criar uma receita para cada tipo de torta.

A receita básica para torta é como um construtor parametrizado. Ele fornece uma estrutura básica para todas as tortas.
As receitas para tortas específicas são como construtores de subclasses. Elas fornecem implementações específicas para
os parâmetros do construtor parametrizado.

    // Observe que a função não é open. Então não pode ser sobrescrita 
    open class Tiger(val origin: String)
    {
        fun sayHello()
        {
            println("A tiger from $origin says: grrhhhh!")
        }
    }

    // Herdar uma classe passando uma parâmetro padrão.
    // A classe SiberianTiger, é um Tiger passando sua origem como "Siberia"
    class SiberianTiger : Tiger("Siberia")

    fun main()
    {
        val tiger : Tiger = SiberianTiger()
        tiger.sayHello()
 
    }
    // Saída: A tiger from Siberia says: grrhhhh!
 
  
### Classe Tiger
A classe Tiger é uma classe aberta que representa um tigre. Ela tem um atributo "origin" que representa a origem do tigre. 
Ela também tem um método `sayHello()` que imprime uma mensagem de saudação.

**Atributo "origin"**

O atributo "origin" é um atributo de tipo "String" que representa a origem do tigre.

**Método "sayHello()"**

O método "sayHello()" é um método de tipo "Unit" que imprime uma mensagem de saudação. A mensagem de saudação inclui a
origem do tigre.


**Classe SiberianTiger**

A classe SiberianTiger é uma classe que herda da classe Tiger. Ela tem um construtor que passa o valor "Siberia" para
o atributo "origin" da classe Tiger.


**Função "main()"**

A função "main()" é a função principal do programa. Ela cria um objeto da classe SiberianTiger e chama o método "sayHello()" 
desse objeto.

**Saída:**

A saída do programa é a seguinte mensagem:
"A tiger from Siberia says: grrhhhh!"

**Explicação**

O código funciona da seguinte forma:

* A classe Tiger é declarada como uma classe aberta. Isso significa que ela pode ser herdada por outras classes.
* A classe SiberianTiger herda da classe Tiger.
* O construtor da classe SiberianTiger passa o valor "Siberia" para o atributo "origin" da classe Tiger.
* A função "main()" cria um objeto da classe SiberianTiger.
* O método "sayHello()" do objeto SiberianTiger é chamado.
* O método "sayHello()" imprime a mensagem de saudação.

# Herança. Passando Argumentos do Construtor Para a Superclasse.

       open class Lion(val name: String, val origin: String) 
       {
           fun sayHello()
           {
               println("$name, the lion from $origin says: graoh!")
           }
    }

    class Asiatic(name: String) : Lion(name = name, origin = "India")

    fun main()
    {
        val lion: Lion = Asiatic("Rufo")
        lion.sayHello()
    }

**Classe Lion**

A classe Lion é uma classe aberta que representa um leão. Ela tem dois atributos: name e origin. O atributo name representa
o nome do leão e o atributo origin representa a origem do leão. Ela também tem um método sayHello() que imprime uma mensagem
de saudação. 

**Atributo name**

O atributo name é um atributo de tipo String que representa o nome do leão.    

**Atributo origin**

O atributo origin é um atributo de tipo String que representa a origem do leão.

**Método sayHello()**

O método sayHello() é um método de tipo Unit que imprime uma mensagem de saudação. A mensagem de saudação inclui o nome 
e a origem do leão. 

**Classe Asiatic**

A classe Asiatic é uma classe que herda da classe Lion. Ela tem um construtor que passa o valor do parâmetro name para 
o atributo name da classe Lion. Ela também passa o valor "India" para o atributo origin da classe Lion.

**Função main()**

A função main() é a função principal do programa. Ela cria um objeto da classe Asiatic e chama o método sayHello() 
desse objeto.

**Saída**

A saída do programa é a seguinte mensagem: 
Rufo, the lion from India says: graoh!

**O código funciona da seguinte forma:**

A classe Lion é declarada como uma classe aberta. Isso significa que ela pode ser herdada por outras classes.
    
A classe Asiatic herda da classe Lion. 

O construtor da classe Asiatic passa o valor do parâmetro name para o atributo name da classe Lion. Ele também passa o valor 
"India" para o atributo origin da classe Lion.

A função main() cria um objeto da classe Asiatic.

O método sayHello() do objeto Asiatic é chamado. 
    
O método sayHello() imprime a mensagem de saudação.

# Data Class    

      // uma data class com duas propriedades, nome e id
     data class User(val name: String, val id: Int)
     {
    
    // Dizendo que não gostaria de fazer a comparação de todas as propriedades deste tipo, apenas ao do id 
    // se são iguais ou não
    override fun equals(other: Any?) =
    other is User && other .id == this.id
     }

    fun main()
    {
    // criação do usuário Alex, com id 1 e sua impressão.
    val user = User ("Alex", 1)
    println(user)
    
    // criação de outros dois usuários, o secondUser e o thirdUser.
    val secondUser = User("Alex", 1)
    val thirdUser = User("Max", 2)
    // Comparando eles estruturalmente:
    println("user == secondUser: ${user == secondUser}") 
    println("user == thirdUser: ${user == thirdUser}")
    
    // hascode pega as propriedades da estrutura de dados,do objeto, e gera um valor. 
    // hashCode() function
    println(user.hashCode())
    println(secondUser.hashCode())
    println(thirdUser.hashCode())
    
    // criar uma cópia com uma nova instância, mas com os mesmos valores estruturais
    // copy() function
    println(user.copy())
    // comparação referencial: 
    println(user === user.copy())
    // copiar user, mas o name será Max:
    println(user.copy("Max"))
    // copiar o User mudando o id
    println(user.copy(id = 3))
    
    // pode acessar as propriedades por ordem de declaração do construtor
    println("name = ${user.component1()}")
    println("id = ${user.component2()}")
    
    // Saída
    
    // User(name=Alex, id=1)
    
    // user == secondUser: true
    // user == thirdUser: false
    
    // 63347075 
    // 63347075
    // 2390846
    
    // User(name=Alex, id=1)
    // false
    
    // User(name=Max, id=1)
    // User(name=Alex, id=3)
    
    // name = Alex
    // id = 1
  
    }

Este código Kotlin demonstra o uso de uma data class. Uma data class é uma classe que fornece algumas funcionalidades
básicas, como equals(), hashCode() e toString(), sem que o programador precise implementá-las.

**Explicação do código**

1.  Declaração da data class User com duas propriedades, nome e id.
2.  Sobrescrita do método equals() para comparar dois objetos User apenas pelo id.
3.   Criação do usuário Alex, com id 1.
4.   Impressão do usuário Alex.
5.   Criação de dois outros usuários, o secondUser e o thirdUser.
6.   Comparação do usuário Alex com o secondUser. Como os dois usuários têm o mesmo id, o resultado é true.
7.   Comparação do usuário Alex com o thirdUser. Como os dois usuários têm o id diferente, o resultado é false.
8.   Impressão do hashcode do usuário Alex.
9.   Impressão do hashcode do secondUser.
10.  Impressão do hashcode do thirdUser.
11.  Criação de uma cópia do usuário Alex.
12.  Comparação do usuário Alex com a cópia. Como são objetos diferentes, o resultado é false.
13.  Criação de uma cópia do usuário Alex, mas com o nome alterado para Max.
14.  Criação de uma cópia do usuário Alex, mas com o id alterado para 3.
15.  Impressão das propriedades name e id do usuário Alex.

# Enum Class
Uma enum class é um tipo especial de classe em Kotlin que pode ser usada para representar um conjunto de 
valores constantes. As enum classes são declaradas usando a palavra-chave enum class seguida pelo nome da
classe e os valores constantes.

    enum class State
    {
        IDLE, RUNNING, FINISHED
    }
    
    fun main()
    {
        val state = State.RUNNING
        val message = when (state){
            State.IDLE -> "it's idle"
            State.RUNNING -> "it's running"
            State.FINISHED -> "it's finished"
        }
        println(message)
    }

**Explicação do código:**
1. Declaração da enum class State com três valores: IDLE, RUNNING e FINISHED.
    
2. Criação de uma variável state do tipo State e atribuição do valor RUNNING a ela.

3. Declaração de uma variável message do tipo String.
   
4. Atribuição do valor correto da variável message de acordo com o valor da variável state usando uma when expression.
  
5. Impressão da variável message.
       
**Saída:**

it's running

Outro exemplo: 

    enum class Color(val rgb: Int )
    {
        RED(0xFF0000),
        GREEN(0x00FF00),
        BLUE(0x0000FF),
        YELLOW(0xFFFF00);
        
        fun containsRed() = (this.rgb and 0xFF0000 != 0)
    }
    
    fun main()
    {
        val red = Color.RED
        println(red)
        println(red.containsRed())
        println(Color.BLUE.containsRed())
        println(Color.YELLOW.containsRed())
    }


    
 Este código define uma classe enum chamada Color que representa as quatro cores primárias: 
 vermelho, verde, azul e amarelo. Cada cor é representada por uma constante da classe Color,
 que possui uma propriedade chamada rgb que armazena o valor RGB da cor.
    
 A função containsRed() verifica se a cor contém vermelho. Ela faz isso realizando uma operação 
 AND bit a bit entre a propriedade rgb da cor e o valor inteiro 0xFF0000, que representa a máscara de 
 vermelho. Se o resultado da operação AND bit a bit não for zero, então a cor contém vermelho.
 
 A função main() cria uma variável chamada red e a atribui ao valor da constante Color.RED. Em seguida, 
 imprime a variável red no console. Em seguida, chama a função containsRed() na variável red e imprime o 
 resultado no console. Por fim, chama a função containsRed() nas constantes Color.BLUE e Color.YELLOW e imprime os
 resultados no console.
    
Saída:
  
RED
true
false
true

# Sealed class
Uma sealed class no Kotlin é como uma caixa lacrada de objetos. Você só pode criar novos objetos
da sealed class dentro do próprio arquivo onde a sealed class foi definida. E você só pode usar objetos da sealed
class em expressões when, o que garante que você sempre considere todos os casos possíveis.
        
Uma analogia para sealed classes é um restaurante de fast food. O restaurante tem um menu fixo de itens, 
e você só pode pedir itens do menu. Você não pode trazer sua própria comida ou criar novos itens de menu. E 
quando você faz um pedido, o restaurante garante que você receba o que pediu.

    sealed class Mammal(val name: String)
    class Cat(val catName: String) : Mammal(catName)
    class Human(val humanName: String, val job: String) : Mammal(humanName)

    fun greetMammal(mammal: Mammal) : String
    {
        when (mammal)
        {
            is Human -> return "Hello ${mammal.name}; you're working as a ${mammal.job}"
            is Cat -> return "Hello ${mammal.name}"
        }
    }

    fun main()
    {
        println(greetMammal(Cat("Snowy")))
    }

Este código define uma classe sealed chamada Mammal com uma única propriedade, name. A classe sealed Mammal só 
pode ser estendida por classes definidas no mesmo arquivo.

 Duas classes são derivadas da classe sealed Mammal: Cat e Human. A classe Cat possui uma propriedade adicional, catName. 
 A classe Human possui duas propriedades adicionais, humanName e job.
        
 A função greetMammal() recebe um objeto Mammal como parâmetro e retorna uma string de saudação. A função usa uma expressão 
 when para determinar o tipo do objeto Mammal e retornar a string de saudação apropriada.
        
 A função main() cria um objeto Cat chamado Snowy e chama a função greetMammal() para saudar o gato. A 
 saída do programa é a seguinte:
 
  Hello Snowy

  # Object Keyword
A palavra-chave object em Kotlin tem dois usos principais:

Para declarar uma classe singleton. Uma classe singleton é uma classe que só pode ter uma instância. 
Para declarar uma classe singleton, use a palavra-chave object em vez de class.
    
Para declarar um objeto anônimo. Um objeto anônimo é um objeto que é criado sem um nome. Para declarar um objeto anônimo, 
use a palavra-chave object seguida de um bloco de código.

    // Declara uma classe singleton
    object Logger
    {
        fun log(message: String) 
        {
            println(message)
        }
    }

    // Usa a classe singleton
    Logger.log("Hello, world!")

    // Declara um objeto anônimo
    val myObject = object
    {
        val name = "John Doe"
        val age = 30
     }

    // Usa o objeto anônimo
    println(myObject.name) // Imprime "John Doe"
    println(myObject.age) // Imprime 30

Uso de classes singleton:
  
Classes singleton são úteis para representar recursos compartilhados, como um banco de dados ou uma conexão com a 
internet. Elas também são úteis para representar estados, como o estado de um jogo ou a configuração de um aplicativo.
Uso de objetos anônimos:

Objetos anônimos são úteis para criar objetos rapidamente sem precisar declarar uma classe. Eles também são úteis 
para representar objetos que são usados apenas temporariamente.

# Funções de Escopo LET 

**Funções de Escopo:** Let, Run, With, Apply, Also.

Permite que você execute um bloco de código se o objeto não for nulo, retornando um resultado opcional.
Pode ser útil para operações em um objeto não nulo.

Pode ser comparado a uma estrutura condicional que executa um bloco de código se uma condição
(o objeto não ser nulo) for verdadeira.

A função let em Kotlin é uma função de escopo que permite executar um bloco de código com um objeto como contexto.
O resultado do bloco de código é o valor retornado pela função let.

 O argumento da função let é o objeto que será usado como contexto. O nome do argumento é it, mas pode ser nomeado de 
 outra forma.
 
O bloco de código é executado com o objeto como contexto. O objeto pode ser acessado usando o nome do argumento it. 
    
O resultado do bloco de código é o valor retornado pela função let.<br>Em geral, a função let é uma maneira conveniente 
de executar um bloco de código com um objeto como contexto. Pode ser usada para vários fins, incluindo validação,
operações e transformações.

      
    fun customPrint(s: String)
    {
        print(s.uppercase())
    }
    
    fun main()
    {
        
        val empty = "test".let{
            customPrint(it)
            it.isEmpty()
        }
        println("is empty: $empty")
        
        fun printNonNull(str: String?)
        {
            println("Printing \"$str\":")
            
            str?.let
            {
                print("\t")
                customPrint(it)
                println()
            }
        }
        
        fun printIfBothNonNull(strOne: String?, strTwo: String?)
        {
            strOne?.let{firstString ->
                strTwo?.let{secondString ->
                    customPrint("$firstString : $secondString")
                    println()
                }
        }
    }
        
        printNonNull(null)
        printNonNull("my string")
        printIfBothNonNull("First", "Second")
        
    }

**Função customPrint():**

Esta função pega uma string como parâmetro e imprime a versão em maiúsculas da string.
    
**Função let():**
        
A função let() é uma função de escopo que permite executar um bloco de código com um objeto como contexto.
O resultado do bloco de código é o valor retornado pela função let().
        
**Chamada da função let() na função main():**
        
 A primeira chamada da função let() na função main() é usada para imprimir a string "test" em maiúsculas e 
 verificar se ela está vazia. O resultado da verificação de vazio é retornado pela função let().
        
  A segunda chamada da função let() na função main() é usada para imprimir a string "my string" em maiúsculas, 
  se ela não for nula.
        
 A terceira chamada da função let() na função main() é usada para imprimir a string "First : Second", se ambas 
 as strings forem não nulas.
        
  Saída do programa:
    TEST is empty: false
    Printing "null":
    Printing "my string":
        MY STRING
    FIRST : SECOND

# Função de escopo Run
 Executa um bloco de código em um contexto específico (o receptor do run), podendo modificar o objeto e retornar um resultado opcional. Pode ser usado para configurar propriedades de um objeto durante sua criação.

Pode ser comparado a executar código dentro do próprio objeto, independente de ele ser nulo ou não.

    fun main()
    {
    
        fun getNullableLength(ns: String?) 
	{
            println("for \"$ns\":")
            ns?.run{
                println("\tis empty? " + isEmpty())
                println("\tlength = $length")
                length
            }
        }
        getNullableLength(null)
        getNullableLength("")
        getNullableLength("some string with Kotlin ")
    }

A função getNullableLength usa a extensão run da classe String?. A extensão run permite executar um bloco de código se a string não for nula.

 O bloco de código executado pela extensão run imprime se a string está vazia e o seu comprimento, e retorna o comprimento da string.

Saída:

    for "null":
    for "":
	is empty? true
	length = 0
    for "some string with Kotlin ":
	is empty? false
	length = 24


 # with

A função with em Kotlin permite que você execute um bloco de código dentro do contexto de um objeto. Isso 
significa que você pode acessar as propriedades e métodos do objeto dentro do bloco de código sem ter que especificar 
explicitamente o nome do objeto.

A função with recebe dois argumentos: o objeto no qual você deseja executar o bloco de código e o próprio bloco de código. 
O bloco de código pode ser uma expressão ou uma declaração.

 É como ter uma conversa com alguém e referenciar diretamente o que a pessoa está dizendo, sem usar "você disse" a cada frase.

    class Configuration(var host: String, var port: Int)

    fun main()
    {
        val configuration = Configuration(host = "127.0.0.1", port = 9000)
    
    with(configuration)
    {
        println("$host:$port")
    }
    
    // instead of: 
    println("${configuration.host}:${configuration.port}")
     } 


# Apply
 A função apply é usada para configurar as propriedades de um objeto durante sua criação. Ela retorna o próprio objeto 
 após as modificações.
 
Imagine comprar um carro e personalizá-lo na própria concessionária antes de dirigir para casa.


    data class Person(var name: String, var age: Int, var about: String)
    {
        constructor(): this("",0, "")
        
    }
    
    fun main()
    {
        val jake = Person()
        val stringDescription = jake.apply
        {
            name = "Jake"
            age = 30
            about = "Android developer"
        }.toString()
        
        println(stringDescription)
    }

O código acima define uma classe de dados chamada Person com três propriedades: name, age e about. A classe de dados
também tem dois construtores: um construtor primário que leva três parâmetros e um construtor secundário sem parâmetros.
    
A função main() cria uma nova instância da classe Person chamada jake. Em seguida, a função usa a função de escopo apply 
para modificar as propriedades do objeto jake. A função apply recebe um bloco de código como argumento e executa o bloco 
de código dentro do contexto do objeto especificado.

Neste caso, a função apply é usada para definir o nome, a idade e a descrição de Jake. 
    
Exemplo de saída:

    Person(name=Jake, age=30, about=Android developer)

Vantagens de usar a função apply:

A função apply pode ser usada para modificar as propriedades de um objeto de forma concisa e elegante. 
Ela também torna o código mais legível, porque fica claro que o código dentro do bloco de código apply está 
operando no objeto especificado.
        
  Desvantagens de usar a função apply
        
A função apply pode tornar o código menos legível, especialmente se o bloco de código for longo ou complexo. 
No entanto, esta desvantagem pode ser mitigada usando a função also, que é semelhante à função apply, mas o valor de
retorno da função é o próprio objeto, não o valor retornado pelo bloco de código.

# Also
A função also permite fazer modificações ou realizar operações no objeto, mas ela retorna o próprio objeto original.
Ela é útil para fazer anotações ou realizar ações enquanto mantém o objeto inalterado.

Pode ser comparada a fazer anotações em um mapa enquanto mantém o mapa original sem alterações.

A função also oferece uma flexibilidade adicional, pois permite que você faça modificações no objeto e, 
ao mesmo tempo, mantenha o objeto original intacto. Assim, você pode realizar uma variedade de ações, incluindo aquelas 
que envolvem o objeto original e/ou a versão modificada, conforme necessário.

    
    data class Person(var name: String, var age: Int, var about: String)
    {
        constructor(): this("",0, "")
        
    }
    
    fun writeCreationLog(p: Person)
    {
        println("A new person ${p.name} was created.")
    }
    
    fun main()
    {
        
        val jake = Person("Jeke", 30, "Adroid developer")
        .also{
            writeCreationLog(it)
        }
    }

O código acima define uma classe de dados chamada Person com três propriedades: name, age e about. A classe 
de dados também tem dois construtores: um construtor primário que leva três parâmetros e um construtor secundário 
sem parâmetros.

A função writeCreationLog() imprime uma mensagem para o console informando que uma nova pessoa foi criada.

A função main() cria uma nova instância da classe Person chamada jake com os valores fornecidos para as propriedades name,
age e about.

Em seguida, a função main() usa a função de escopo also para executar a função writeCreationLog() com o objeto jake 
como argumento. A função also recebe um bloco de código como argumento e executa o bloco de código dentro do 
contexto do objeto especificado.

Neste caso, a função also é usada para imprimir uma mensagem para o console informando que uma nova pessoa chamada 
Jake foi criada.

Exemplo de saída:

    A new person Jake was created.

# Infix function
uma infix function é uma forma de escrever operações de uma maneira mais amigável e fácil de entender, 
especialmente quando se trata de ações que você faria naturalmente de forma "infixada", como somar, subtrair, etc.

A notação infix permite que você chame uma função sem usar o ponto (.), tornando a chamada da função mais concisa 
e sem a necessidade de parênteses. Com a notação infix, você pode escrever a chamada da função de uma maneira que se
assemelha mais a uma expressão direta. Essa abordagem pode tornar o código mais legível em alguns casos.

    fun main()
    {
        infix fun Int.time(str: String) = str.repeat(this)
        println(2 times "Bye")
    
        val pair = "Ferrari" to "Katrina"
        println(pair)
    
        infix fun String.onto(other: String) = Pair(this, other)
        val myPair = "McLaren" onto "Lucas"
        println(myPair)
    
        val sophia = Person("Sophia")
        val claudia = Person("Claudia")
        sophia likes claudia
    }

    class Person(val name: String) 
    {
        val likedPeople = mutableListOf<Person>()
        infix fun likes(other: Person) {likedPeople.add(other)}
    }



 1. fun main() : Início da função principal do programa.

2. infix fun Int.time(str: String) = str.repeat(this): Define uma função infix chamada time que estende a classe Int.
 Essa função concatena uma string (str) repetindo-a a quantidade de vezes especificada pelo valor do inteiro.

3. println(2 times "Bye"): Chama a função time de forma infixada, resultando na impressão de "ByeBye"
(a string "Bye" repetida duas vezes).

4. val pair = "Ferrari" to "Katrina": Cria um par de strings usando a notação to. O par resultante é armazenado na variável pair.

5. println(pair): Imprime o par de strings "Ferrari" e "Katrina".

6. infix fun String.onto(other: String) = Pair(this, other): Define uma função infix chamada onto que estende a
 classe String. Essa função cria um par (Pair) com o receptor da função (this) e o parâmetro other.

7. val myPair = "McLaren" onto "Lucas": Chama a função onto de forma infixada, criando um par de strings
 ("McLaren" e "Lucas"). O par resultante é armazenado na variável myPair.

8. println(myPair): Imprime o par de strings "McLaren" e "Lucas".

9. val sophia = Person("Sophia"): Cria uma instância da classe Person chamada sophia com o nome "Sophia".

10. val claudia = Person("Claudia"): Cria uma instância da classe Person chamada claudia com o nome "Claudia".

11. sophia likes claudia: Chama a função infix likes da instância sophia da classe Person, indicando que
 "Sophia" gosta de "Claudia". A função likes adiciona "Claudia" à lista de pessoas gostadas por "Sophia".

12. class Person(val name: String): Define uma classe Person com uma propriedade name e uma
lista likedPeople para armazenar pessoas gostadas.

13. infix fun likes(other: Person) { likedPeople.add(other) }: Define uma função infix chamada likes que adiciona uma pessoa
 à lista de pessoas gostadas (likedPeople).

# Operator Function
As operator functions em Kotlin são funções que permitem que você use operadores como +, -, *, / e outros, 
de maneira personalizada em seus tipos definidos pelo usuário. Assim como as infix functions, as operator functions também 
são usadas para melhorar a legibilidade e expressividade do código.

Para criar uma operator function, você precisa usar uma palavra-chave específica, como operator, e fornecer uma 
implementação específica para o operador que você deseja sobrecarregar

    fun main()
    {
       operator fun Int.time(str: String) = str.repeat(this)
       println(2 * "Bye")
    
       operator fun String.get(range: IntRange) = substring(range)
       val str = "Always forgive your enemies; nothing annoys them so much"
       println(str[0..14])
    }

# Higher Order Function
As operator functions em Kotlin são funções que permitem que você use operadores como +, -, *, / e outros, 
de maneira personalizada em seus tipos definidos pelo usuário. Assim como as infix functions, as operator functions também 
são usadas para melhorar a legibilidade e expressividade do código.

Para criar uma operator function, você precisa usar uma palavra-chave específica, como operator, e fornecer uma 
implementação específica para o operador que você deseja sobrecarregar

    fun main()
    {
       operator fun Int.time(str: String) = str.repeat(this)
       println(2 * "Bye")
    
       operator fun String.get(range: IntRange) = substring(range)
       val str = "Always forgive your enemies; nothing annoys them so much"
       println(str[0..14])
    }


