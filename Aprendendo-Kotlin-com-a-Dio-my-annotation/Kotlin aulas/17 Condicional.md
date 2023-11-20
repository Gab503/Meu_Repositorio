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
