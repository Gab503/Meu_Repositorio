<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <h1>Loops: While and do while</h1><br>
  <p>
    O laço de repetição while, vai executar algo, enquanto for true, enquanto a condição for verdadeira.<br>
  <h1>Do while</h1><br>
  Enquanto o while faz a condição sempre em primeiro, o do while primeiro executa o do, e depois passa a condição.<br>
  
    fun eatACake() = println("Eat a Cake")
    fun bakeACake() = println("Baker a Caker")

    fun main(){
    var cakesEaten = 0
    var cakesBaked = 0
    
    while (cakesEaten < 5) {
        eatACake()
        cakesEaten ++
    }
    
    do {
        bakeACake() 
        cakesBaked++
    }   while (cakesBaked < cakesEaten)

    }
  </p>
</body>
</html>