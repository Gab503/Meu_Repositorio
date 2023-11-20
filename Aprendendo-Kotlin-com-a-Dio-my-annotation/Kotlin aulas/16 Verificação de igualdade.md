# Verificação de igualdade == e ===
  Existe duas formas de verificar a igualdade de dois objetos, uma seria uma comparação estrutural, 
  que é feita com a sintaxe ==, e a outra uma comparação referencial, com a sintaxe ===.

    
        
    fun main()
    {
    val authors = setOf ("Shakespeare", "Hemigway", "Twain")
    val writers = setOf("Twain", "Shakespeare", "Hemigway")
    
    // Comparação estrutural.
    println(authors == writers)

    // comparação referencial.
    println(authors === writers)
    }  
    // true
    // false

Ao invés de ser uma lista, são do tipo set, esse tipo não aceita duplicatas, se tiver um elemento duplicado,
ele simplesmente não aceita essa duplicata. 

Neste exemplo acima, você deve ter observado que possuem os mesmo items em ordens diferentes. 
Isto é, estruturalmente, possuem os mesmos valores, mas, possuem referencias diferentes (ordem diferentes = referencias 
diferentes). 

Podemos pensar assim, uma comparação estrutural, é para saber se possuem os mesmo elementos. 

Já uma comparação referencial é para ver se ambos são de fatos iguais, isto é, identicos.

