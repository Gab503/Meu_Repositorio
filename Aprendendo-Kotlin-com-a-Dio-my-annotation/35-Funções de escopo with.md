<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>with</h1>
    <p> A função with em Kotlin permite que você execute um bloco de código dentro do contexto de um objeto. Isso significa que você pode acessar as propriedades e métodos do objeto dentro do bloco de código sem ter que especificar explicitamente o nome do objeto.
    A função with recebe dois argumentos: o objeto no qual você deseja executar o bloco de código e o próprio bloco de código. O bloco de código pode ser uma expressão ou uma declaração.</p>

    class Configuration(var host: String, var port: Int)

    fun main(){
        val configuration = Configuration(host = "127.0.0.1", port = 9000)
    
    with(configuration){
        println("$host:$port")
    }
    
    // instead of: 
    println("${configuration.host}:${configuration.port}")
     } 


</body>
</html>
