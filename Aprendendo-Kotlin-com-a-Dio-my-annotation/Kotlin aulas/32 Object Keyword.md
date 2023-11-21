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
