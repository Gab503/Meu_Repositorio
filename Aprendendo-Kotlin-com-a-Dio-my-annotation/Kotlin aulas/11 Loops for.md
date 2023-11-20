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
