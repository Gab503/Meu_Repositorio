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
    
    </p>
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
convertê-los em Stringtipo e concatená-los em uma String para impressão. Também possui um uso semelhante ao format do Python. 

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
Use When quando você tiver uma expressão condicional com múltiplas ramificações. When pode ser usado como uma declaração ou
como uma expressão. É um pouco semelhante ao match case em Python, mas com uma flexibilidade maior.

## When statement / when declaração

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
Pode ser usado para atribuir um valor através de uma estrutura condicional por exemplo.
    
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
  
  
  
  Semelhante a uma expressão matemática por assim dizer.

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


  # Ranges: Loops com int
A maneira mais comum de criar um intervalo em Kotlin, é usar o .. operador. Por exemplo,1..4 é equivalente a 1, 2, 3, 4.

Para declarar um intervalo na ordem inversa, use downTo. Por exemplo, 4 dowTo 1, é equivalente a 4, 3, 2, 1.

Para declarar um intervalo que aumente em uma  etapa que não seja 1, use step e o valor de incremento desejado. 

Por exemplo, 1..5 step 2, é o mesmo que ir de 1 até 5, pulando de dois em dois, ou seja, 1, 3, 5.

Para declarar um intervalo que não inclui o valor final, use o ..< operador. Por exemplo, 1..< 4 é equivalente a 1, 2, 3. 
  
        
      fun main() 
      {
            // de 0 até 3
            for (i in 0..3){
                print(i)
            }
            // print(" ") para dar espaço e não ficar grudado.
            print(" ")
            
            // não incluir o 3
            for (i in 0 until 3) {
                print(i)
            }
            
            print(" ")
            
            for(i in 3 downTo 0)
            {
                print(i)
            }
            print(" ")
            
            // de 2 até 8 pulando de 2 em dois.
            for (i in 2..8 step 2)
            {
                print(i)
            }
            
            print(" ")
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
É o mesmo processo, só que desta vez com "strings" ao invés de int. Vale ressaltar que os Rangers também são suportados 
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
O if é usado como expression.
        
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
    
