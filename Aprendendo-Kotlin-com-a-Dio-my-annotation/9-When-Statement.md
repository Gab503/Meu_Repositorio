<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <h1>When</h1><br>
   <p>Use When quando você tiver uma expressão condicional com múltiplas ramificações. When pode ser usado como uma declaração ou como uma expressão. É um pouco semelhante ao match case em Python, mas com uma flexibilidade maior.
  <h1>When statement / when declaração</h1><br>

    fun main() {
    cases("Hello")
    cases(1)
    cases(0L)
    cases(MyClass())
    cases("hello")
    }

    fun cases(obj: Any) {
    when (obj){
        1 -> println("One")
        "Hello" -> println("Greeting")
        is Long -> println("Long")
        !is String -> println("Not is string")
        else -> println("Unknow")
        // Saída:
        // Greeting
        // One
        // Long
        // Not is string
        // Unknow
    }
    }



    class MyClass

   </p>
</body>
</html>