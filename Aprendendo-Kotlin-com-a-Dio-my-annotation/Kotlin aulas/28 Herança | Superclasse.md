# Herança. Passando Argumentos do Construtor Para a Superclasse.

       open class Lion(val name: String, val origin: String) 
       {
           fun sayHello()
           {
               println("$name, the lion from $origin says: graoh!")
           }
    }

    class Asiatic(name: String) : Lion(name = name, origin = "India")

    fun main()
    {
        val lion: Lion = Asiatic("Rufo")
        lion.sayHello()
    }

**Classe Lion**

A classe Lion é uma classe aberta que representa um leão. Ela tem dois atributos: name e origin. O atributo name representa
o nome do leão e o atributo origin representa a origem do leão. Ela também tem um método sayHello() que imprime uma mensagem
de saudação. 

**Atributo name**

O atributo name é um atributo de tipo String que representa o nome do leão.    

**Atributo origin**

O atributo origin é um atributo de tipo String que representa a origem do leão.

**Método sayHello()**

O método sayHello() é um método de tipo Unit que imprime uma mensagem de saudação. A mensagem de saudação inclui o nome 
e a origem do leão. 

**Classe Asiatic**

A classe Asiatic é uma classe que herda da classe Lion. Ela tem um construtor que passa o valor do parâmetro name para 
o atributo name da classe Lion. Ela também passa o valor "India" para o atributo origin da classe Lion.

**Função main()**

A função main() é a função principal do programa. Ela cria um objeto da classe Asiatic e chama o método sayHello() 
desse objeto.

**Saída**

A saída do programa é a seguinte mensagem: 
Rufo, the lion from India says: graoh!

**O código funciona da seguinte forma:**

A classe Lion é declarada como uma classe aberta. Isso significa que ela pode ser herdada por outras classes.
    
A classe Asiatic herda da classe Lion. 

O construtor da classe Asiatic passa o valor do parâmetro name para o atributo name da classe Lion. Ele também passa o valor 
"India" para o atributo origin da classe Lion.

A função main() cria um objeto da classe Asiatic.

O método sayHello() do objeto Asiatic é chamado. 
    
O método sayHello() imprime a mensagem de saudação.
