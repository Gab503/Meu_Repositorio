# Herança simples
       
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
