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


