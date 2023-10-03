      // uma data class com duas propriedades, nome e id
     data class User(val name: String, val id: Int){
    
    // Dizendo que não gostaria de fazer a comparação de todas as propriedades deste tipo, apenas ao do id 
    // se são iguais ou não
    override fun equals(other: Any?) =
    other is User && other .id == this.id
     }

    fun main(){
    // criação do usuário Alex, com id 1 e sua impressão.
    val user = User ("Alex", 1)
    println(user)
    
    // criação de outros dois usuários, o secondUser e o thirdUser.
    val secondUser = User("Alex", 1)
    val thirdUser = User("Max", 2)
    // Comparando eles estruturalmente:
    println("user == secondUser: ${user == secondUser}") 
    println("user == thirdUser: ${user == thirdUser}")
    
    // hascode pega as propriedades da estrutura de dados,do objeto, e gera um valor. 
    // hashCode() function
    println(user.hashCode())
    println(secondUser.hashCode())
    println(thirdUser.hashCode())
    
    // criar uma cópia com uma nova instância, mas com os mesmos valores estruturais
    // copy() function
    println(user.copy())
    // comparação referencial: 
    println(user === user.copy())
    // copiar user, mas o name será Max:
    println(user.copy("Max"))
    // copiar o User mudando o id
    println(user.copy(id = 3))
    
    // pode acessar as propriedades por ordem de declaração do construtor
    println("name = ${user.component1()}")
    println("id = ${user.component2()}")
    
    // Saída
    
    // User(name=Alex, id=1)
    
    // user == secondUser: true
    // user == thirdUser: false
    
    // 63347075 
    // 63347075
    // 2390846
    
    // User(name=Alex, id=1)
    // false
    
    // User(name=Max, id=1)
    // User(name=Alex, id=3)
    
    // name = Alex
    // id = 1
  
    }

Este código Kotlin demonstra o uso de uma data class. Uma data class é uma classe que fornece algumas funcionalidades básicas, como equals(), hashCode() e toString(), sem que o programador precise implementá-las.

Explicação do código

1.  Declaração da data class User com duas propriedades, nome e id.
2.  Sobrescrita do método equals() para comparar dois objetos User apenas pelo id.
3.   Criação do usuário Alex, com id 1.
4.   Impressão do usuário Alex.
5.   Criação de dois outros usuários, o secondUser e o thirdUser.
6.   Comparação do usuário Alex com o secondUser. Como os dois usuários têm o mesmo id, o resultado é true.
7.   Comparação do usuário Alex com o thirdUser. Como os dois usuários têm o id diferente, o resultado é false.
8.   Impressão do hashcode do usuário Alex.
9.   Impressão do hashcode do secondUser.
10.  Impressão do hashcode do thirdUser.
11.  Criação de uma cópia do usuário Alex.
12.  Comparação do usuário Alex com a cópia. Como são objetos diferentes, o resultado é false.
13.  Criação de uma cópia do usuário Alex, mas com o nome alterado para Max.
14.  Criação de uma cópia do usuário Alex, mas com o id alterado para 3.
15.  Impressão das propriedades name e id do usuário Alex.
