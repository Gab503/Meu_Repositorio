# Infix function
uma infix function é uma forma de escrever operações de uma maneira mais amigável e fácil de entender, 
especialmente quando se trata de ações que você faria naturalmente de forma "infixada", como somar, subtrair, etc.

A notação infix permite que você chame uma função sem usar o ponto (.), tornando a chamada da função mais concisa 
e sem a necessidade de parênteses. Com a notação infix, você pode escrever a chamada da função de uma maneira que se
assemelha mais a uma expressão direta. Essa abordagem pode tornar o código mais legível em alguns casos.

    fun main()
    {
        infix fun Int.time(str: String) = str.repeat(this)
        println(2 times "Bye")
    
        val pair = "Ferrari" to "Katrina"
        println(pair)
    
        infix fun String.onto(other: String) = Pair(this, other)
        val myPair = "McLaren" onto "Lucas"
        println(myPair)
    
        val sophia = Person("Sophia")
        val claudia = Person("Claudia")
        sophia likes claudia
    }

    class Person(val name: String) 
    {
        val likedPeople = mutableListOf<Person>()
        infix fun likes(other: Person) {likedPeople.add(other)}
    }



 1. fun main() : Início da função principal do programa.

2. infix fun Int.time(str: String) = str.repeat(this): Define uma função infix chamada time que estende a classe Int.
 Essa função concatena uma string (str) repetindo-a a quantidade de vezes especificada pelo valor do inteiro.

3. println(2 times "Bye"): Chama a função time de forma infixada, resultando na impressão de "ByeBye"
(a string "Bye" repetida duas vezes).

4. val pair = "Ferrari" to "Katrina": Cria um par de strings usando a notação to. O par resultante é armazenado na variável pair.

5. println(pair): Imprime o par de strings "Ferrari" e "Katrina".

6. infix fun String.onto(other: String) = Pair(this, other): Define uma função infix chamada onto que estende a
 classe String. Essa função cria um par (Pair) com o receptor da função (this) e o parâmetro other.

7. val myPair = "McLaren" onto "Lucas": Chama a função onto de forma infixada, criando um par de strings
 ("McLaren" e "Lucas"). O par resultante é armazenado na variável myPair.

8. println(myPair): Imprime o par de strings "McLaren" e "Lucas".

9. val sophia = Person("Sophia"): Cria uma instância da classe Person chamada sophia com o nome "Sophia".

10. val claudia = Person("Claudia"): Cria uma instância da classe Person chamada claudia com o nome "Claudia".

11. sophia likes claudia: Chama a função infix likes da instância sophia da classe Person, indicando que
 "Sophia" gosta de "Claudia". A função likes adiciona "Claudia" à lista de pessoas gostadas por "Sophia".

12. class Person(val name: String): Define uma classe Person com uma propriedade name e uma
lista likedPeople para armazenar pessoas gostadas.

13. infix fun likes(other: Person) { likedPeople.add(other) }: Define uma função infix chamada likes que adiciona uma pessoa
 à lista de pessoas gostadas (likedPeople).

