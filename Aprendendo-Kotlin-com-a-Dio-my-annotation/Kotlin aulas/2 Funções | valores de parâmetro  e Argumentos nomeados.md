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
