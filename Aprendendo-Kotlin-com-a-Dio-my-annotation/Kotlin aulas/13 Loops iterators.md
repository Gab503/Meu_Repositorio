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


  
