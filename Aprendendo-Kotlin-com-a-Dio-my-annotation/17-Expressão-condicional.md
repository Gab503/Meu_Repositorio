<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Expressão Condicional</h1><br>
    <p>O if é usado como expression.</p>

    <p>
        
        fun main(){
        // está fazendo a verificação se a > b e retornando a, 
        // Senão vai retornar b
        fun max(a: Int, b: Int) = if (a > b) a else b
        println(max(99, -42))
        
        // Mesma coisa que fazer assim: 
        fun maxOld(a: Int, b: Int): Int{
            if (a > b){
                return a
            }
            else{
                return b
            }
        }
    }
    
    // Observe a diferença na quantidade de código.</p>
</body>
</html>