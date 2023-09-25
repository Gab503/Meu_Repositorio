<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <h1>Loops: Iterators</h1><br>
  <p>Iterators são as interações que dão a capacidade de algo ser interado. Poder percorrer os elementos de uma estrutura de dados. O Kotlin permite implementear operadores iterators personalizados.</p><br>
  <p>
    
    class Animal(val name: String)

    class Zoo (val animals: List<Animal>){
    
    // operator = cria a capacidade de ter iterações na classe zoo.
    operator fun iterator(): Iterator<Animal>{
       return animals.iterator()
    }
    }

    fun main(){
    val zoo = Zoo(listOf(Animal("Zebra"), Animal("Lion")))
    
    for (animal in zoo){
        println("Watch out, it's a ${animal.name}")
    }
    }


  </p>
</body>
</html>