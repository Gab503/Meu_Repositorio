<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <h1>When Expression</h1><br>
  <p>Pode ser usado para atribuir um valor através de uma estrutura condicional por exemplo.<br>
    
    fun main() {
      println(whenAssign("Hello"))
      println(whenAssign(3.4))
      println(whenAssign(1))
      println(whenAssign(MyClass()))
      }
  
     fun whenAssign(obj: Any):Any{
      val result = when (obj) {
          1 -> "one"
          "Hello" -> 1
          is Long -> false
          else -> 42
      }
      return result
     }
  
     class MyClass
  
  
  
  Semelhante a uma expressão matemática por assim dizer.
  </p>
</body>
</html>