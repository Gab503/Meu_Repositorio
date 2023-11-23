# Apply
 A função apply é usada para configurar as propriedades de um objeto durante sua criação. Ela retorna o próprio objeto 
 após as modificações.
 
Imagine comprar um carro e personalizá-lo na própria concessionária antes de dirigir para casa.


    data class Person(var name: String, var age: Int, var about: String)
    {
        constructor(): this("",0, "")
        
    }
    
    fun main()
    {
        val jake = Person()
        val stringDescription = jake.apply
        {
            name = "Jake"
            age = 30
            about = "Android developer"
        }.toString()
        
        println(stringDescription)
    }

O código acima define uma classe de dados chamada Person com três propriedades: name, age e about. A classe de dados
também tem dois construtores: um construtor primário que leva três parâmetros e um construtor secundário sem parâmetros.
    
A função main() cria uma nova instância da classe Person chamada jake. Em seguida, a função usa a função de escopo apply 
para modificar as propriedades do objeto jake. A função apply recebe um bloco de código como argumento e executa o bloco 
de código dentro do contexto do objeto especificado.

Neste caso, a função apply é usada para definir o nome, a idade e a descrição de Jake. 
    
Exemplo de saída:

    Person(name=Jake, age=30, about=Android developer)

Vantagens de usar a função apply:

A função apply pode ser usada para modificar as propriedades de um objeto de forma concisa e elegante. 
Ela também torna o código mais legível, porque fica claro que o código dentro do bloco de código apply está 
operando no objeto especificado.
        
  Desvantagens de usar a função apply
        
A função apply pode tornar o código menos legível, especialmente se o bloco de código for longo ou complexo. 
No entanto, esta desvantagem pode ser mitigada usando a função also, que é semelhante à função apply, mas o valor de
retorno da função é o próprio objeto, não o valor retornado pelo bloco de código.
        
