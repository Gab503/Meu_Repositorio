<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Also</h1>
    
    data class Person(var name: String, var age: Int, var about: String){
        constructor(): this("",0, "")
        
    }
    
    fun writeCreationLog(p: Person){
        println("A new person ${p.name} was created.")
    }
    
    fun main(){
        
        val jake = Person("Jeke", 30, "Adroid developer")
        .also{
            writeCreationLog(it)
        }
    }

    <p>O código acima define uma classe de dados chamada Person com três propriedades: name, age e about. A classe de dados também tem dois construtores: um construtor primário que leva três parâmetros e um construtor secundário sem parâmetros.
     A função writeCreationLog() imprime uma mensagem para o console informando que uma nova pessoa foi criada.
     A função main() cria uma nova instância da classe Person chamada jake com os valores fornecidos para as propriedades name, age e about.
    Em seguida, a função main() usa a função de escopo also para executar a função writeCreationLog() com o objeto jake como argumento. A função also recebe um bloco de código como argumento e executa o bloco de código dentro do contexto do objeto especificado.
    Neste caso, a função also é usada para imprimir uma mensagem para o console informando que uma nova pessoa chamada Jake foi criada.
    Exemplo de saída:<br>
    A new person Jake was created.</p>
</body>
</html>