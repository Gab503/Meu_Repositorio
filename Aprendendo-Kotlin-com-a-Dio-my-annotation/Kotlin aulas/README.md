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
  
  
  

  
