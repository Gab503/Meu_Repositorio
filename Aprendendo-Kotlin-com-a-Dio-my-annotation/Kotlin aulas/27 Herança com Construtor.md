# Herança com Construtor Parametrizado
Imagine que você está cozinhando uma torta. Você pode ter uma receita básica para torta que você usa para todas as
tortas que você faz. No entanto, você pode querer fazer diferentes tipos de tortas, como torta de chocolate ou torta de maçã.
Para fazer isso, você pode criar uma receita para cada tipo de torta.

A receita básica para torta é como um construtor parametrizado. Ele fornece uma estrutura básica para todas as tortas.
As receitas para tortas específicas são como construtores de subclasses. Elas fornecem implementações específicas para
os parâmetros do construtor parametrizado.

    // Observe que a função não é open. Então não pode ser sobrescrita 
    open class Tiger(val origin: String)
    {
        fun sayHello()
        {
            println("A tiger from $origin says: grrhhhh!")
        }
    }

    // Herdar uma classe passando uma parâmetro padrão.
    // A classe SiberianTiger, é um Tiger passando sua origem como "Siberia"
    class SiberianTiger : Tiger("Siberia")

    fun main()
    {
        val tiger : Tiger = SiberianTiger()
        tiger.sayHello()
 
    }
    // Saída: A tiger from Siberia says: grrhhhh!
 
  
## Classe Tiger
A classe Tiger é uma classe aberta que representa um tigre. Ela tem um atributo "origin" que representa a origem do tigre. 
Ela também tem um método `sayHello()` que imprime uma mensagem de saudação.

**Atributo "origin"**

O atributo "origin" é um atributo de tipo "String" que representa a origem do tigre.

**Método "sayHello()"**

O método "sayHello()" é um método de tipo "Unit" que imprime uma mensagem de saudação. A mensagem de saudação inclui a
origem do tigre.


**Classe SiberianTiger**

A classe SiberianTiger é uma classe que herda da classe Tiger. Ela tem um construtor que passa o valor "Siberia" para
o atributo "origin" da classe Tiger.


**Função "main()"**

A função "main()" é a função principal do programa. Ela cria um objeto da classe SiberianTiger e chama o método "sayHello()" 
desse objeto.

**Saída:**

A saída do programa é a seguinte mensagem:
"A tiger from Siberia says: grrhhhh!"

**Explicação**

O código funciona da seguinte forma:

* A classe Tiger é declarada como uma classe aberta. Isso significa que ela pode ser herdada por outras classes.
* A classe SiberianTiger herda da classe Tiger.
* O construtor da classe SiberianTiger passa o valor "Siberia" para o atributo "origin" da classe Tiger.
* A função "main()" cria um objeto da classe SiberianTiger.
* O método "sayHello()" do objeto SiberianTiger é chamado.
* O método "sayHello()" imprime a mensagem de saudação.



