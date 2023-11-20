As operator functions em Kotlin são funções que permitem que você use operadores como +, -, *, / e outros, 
de maneira personalizada em seus tipos definidos pelo usuário. Assim como as infix functions, as operator functions também 
são usadas para melhorar a legibilidade e expressividade do código.

Para criar uma operator function, você precisa usar uma palavra-chave específica, como operator, e fornecer uma 
implementação específica para o operador que você deseja sobrecarregar

    fun main()
    {
       operator fun Int.time(str: String) = str.repeat(this)
       println(2 * "Bye")
    
       operator fun String.get(range: IntRange) = substring(range)
       val str = "Always forgive your enemies; nothing annoys them so much"
       println(str[0..14])
    }

