# Also
A função also permite fazer modificações ou realizar operações no objeto, mas ela retorna o próprio objeto original.
Ela é útil para fazer anotações ou realizar ações enquanto mantém o objeto inalterado.

Pode ser comparada a fazer anotações em um mapa enquanto mantém o mapa original sem alterações.

A função also oferece uma flexibilidade adicional, pois permite que você faça modificações no objeto e, 
ao mesmo tempo, mantenha o objeto original intacto. Assim, você pode realizar uma variedade de ações, incluindo aquelas 
que envolvem o objeto original e/ou a versão modificada, conforme necessário.

    
    data class Person(var name: String, var age: Int, var about: String)
    {
        constructor(): this("",0, "")
        
    }
    
    fun writeCreationLog(p: Person)
    {
        println("A new person ${p.name} was created.")
    }
    
    fun main()
    {
        
        val jake = Person("Jeke", 30, "Adroid developer")
        .also{
            writeCreationLog(it)
        }
    }

O código acima define uma classe de dados chamada Person com três propriedades: name, age e about. A classe 
de dados também tem dois construtores: um construtor primário que leva três parâmetros e um construtor secundário 
sem parâmetros.

A função writeCreationLog() imprime uma mensagem para o console informando que uma nova pessoa foi criada.

A função main() cria uma nova instância da classe Person chamada jake com os valores fornecidos para as propriedades name,
age e about.

Em seguida, a função main() usa a função de escopo also para executar a função writeCreationLog() com o objeto jake 
como argumento. A função also recebe um bloco de código como argumento e executa o bloco de código dentro do 
contexto do objeto especificado.

Neste caso, a função also é usada para imprimir uma mensagem para o console informando que uma nova pessoa chamada 
Jake foi criada.

Exemplo de saída:

    A new person Jake was created.
