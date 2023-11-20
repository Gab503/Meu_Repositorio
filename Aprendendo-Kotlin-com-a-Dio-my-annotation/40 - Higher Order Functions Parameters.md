Higher-order functions (funções de ordem superior) em Kotlin são funções que recebem outras funções como parâmetros ou 
retornam funções. Elas são uma parte fundamental da programação funcional e proporcionam uma maneira flexível e poderosa de 
lidar com operações em coleções, abstrações e manipulações de funções.

    fun calculate(x: Int, y: Int, operation: (Int, Int) -> Int): Int
    {
        return operation(x, y)
    }

    fun sum(x: Int, y: Int) = x + y

    fun main()
    {
        val sumResult = calculate(4, 5, ::sum)
        val mulResult = calculate(4, 5) {a, b -> a * b}
        println("sumResult $sumResult, mulResult $mulResult")
    }

    
