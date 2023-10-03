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
