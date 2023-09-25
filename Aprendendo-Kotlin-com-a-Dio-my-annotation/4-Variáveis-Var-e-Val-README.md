<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
<h1>Variáveis Var e val</h1><br>
<p>Var é uma váriavel mutável, podendo assim ser alterada se necessário e quando quiser. <br> 
  Enquanto val, é uma váriavel imutável, não podendo ser alterado. <br></p>
  
    fun main() {
        var a: String = "Initial"
        println(a)
        val b: Int = 1
        val c = 3
        println(b) 
        println(c)
        a = "Banana"
        println(a)
    }

    fun SomeCondition() = false

    fun main() {
    
      val d: Int
    
    if (SomeCondition()){
        d = 1
    }else {
        d = 2
    }
    println(d)
}
<p>Neste último exemplo, demonstra um uso de variável val, básicamente, se SomeCondition for true, irá ter 1 como saída de dados.<br>
Mas se for false, irá ter 2.</p>
</body>
</html>
