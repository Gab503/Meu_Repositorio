<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Funções úteis</h1><br>
    <p>A primeira é a filter, uma vez que você cria uma variável que seja uma coleção, ela permite filtrar os elementos dela, baseado em um predicado ( uma regra de filtro)</p>
    <p>
      
        fun main(){
        val numbers = listOf(1, -2, 3, -4, 5, -6)
        val positives = numbers.filter{x -> x >0}
        val negatives = numbers.filter{it <0}
        println(positives)
        println(negatives)
    </p>
    <br>

  <h1>Expressões Lambda</h1><br>
    <p>Kotlin permite escrever códigos ainda mais concisos para funções usando expressões lambda. Dentro da expressão Lambda, você escreve: <br>Os parâmetros seguidos por um ->.<br>O corpo da função após o ->.<br></p>

    <p>
        fun main() {
            println({ string: String -> string.uppercase() }("hello"))
            // HELLO
        }
    </p>

   <p>A filter() aceita uma expressão lambda como predicado.<br>
    {x -> x > 0} pega cada elemento da lista e retorna apenas aqueles que são positivos. Ou usa it como no exemplo acima.
    </p><br>

   <p>A função map() também aceita uma expressão lambda como predicado.</p><br>

    <p>
        fun main() {
    
            val numbers = listOf(1, -2, 3, -4, 5, -6)
            val doubled = numbers.map { x -> x * 2 }
            val tripled = numbers.map { it * 3 }
            println(doubled)
            // [2, -4, 6, -8, 10, -12]
            println(tripled)
            // [3, -6, 9, -12, 15, -18]
            
        }
    </p><br>

  <p>Neste exemplo acima, irá transformar todos os elementos da coleção. .</p>
    <br>

    <p>
        fun main() {
            val numbers = listOf(1 , -2, 3, -4, 5, -6)
            val anyNegative = numbers.any { it < 0 }
            val anyGT6 = numbers.any{it > 6}
            
            println(numbers)
            println(anyNegative)
            println(anyGT6)
        }
    </p><br>
   <p>flatMap.<br>
      
     fun main() {
            val fruitsBag = listOf("apple", "orange", "banana", "grapes")
            val clothesBag = listOf("Shirts", "pants", "jeans")
            val cart = listOf(fruitsBag, clothesBag)
            val mapBag = cart.map{it}
            val flatMapBag = cart.flatMap{it}
            
            println("Your bags are: $mapBag")
            println("The things you bought are: $flatMapBag")
            // Your bags are: [[apple, orange, banana, grapes], [Shirts, pants, jeans]]
            // The things you bought are: [apple, orange, banana, grapes, Shirts, pants, jeans]
        
        }
    </p>

    

</body>
</html>