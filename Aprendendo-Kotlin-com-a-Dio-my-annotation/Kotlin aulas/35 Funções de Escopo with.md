# with

A função with em Kotlin permite que você execute um bloco de código dentro do contexto de um objeto. Isso 
significa que você pode acessar as propriedades e métodos do objeto dentro do bloco de código sem ter que especificar 
explicitamente o nome do objeto.

A função with recebe dois argumentos: o objeto no qual você deseja executar o bloco de código e o próprio bloco de código. 
O bloco de código pode ser uma expressão ou uma declaração.

 É como ter uma conversa com alguém e referenciar diretamente o que a pessoa está dizendo, sem usar "você disse" a cada frase.

    class Configuration(var host: String, var port: Int)

    fun main()
    {
        val configuration = Configuration(host = "127.0.0.1", port = 9000)
    
    with(configuration)
    {
        println("$host:$port")
    }
    
    // instead of: 
    println("${configuration.host}:${configuration.port}")
     } 


