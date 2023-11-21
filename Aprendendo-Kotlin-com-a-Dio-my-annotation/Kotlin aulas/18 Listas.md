# Listas(List)
As listas armazenam itens na ordem em que são adicionados e permitem itens duplicado. Ao criar listas, o 
Kotlin pode inferir o tipo de itens armazenados. Para declarar o itpo explicitamente, adicione-o entre conlchetes 
angulares, exemplo, <Int> após a declaração da lista.
    
A função listOf() vai criar uma lista imutável.

A função mutableListOf() vai criar uma lista mutável.

    

        val systemUsers: MutableList<Int> = mutableListOf(1, 2, 3)
            val sudoers: List<Int> = systemUsers
            
            fun addSystemUser(newUser: Int)
            {
                systemUsers.add(newUser)
            }
            
            fun getSysSudoers(): List<Int> {
                return sudoers
            }
            
            fun main()
            {
                addSystemUser(4)
                println("Tot sudoers: ${getSysSudoers().size}")
                getSysSudoers().forEach{
                    i -> println("Some useful info on user $i")
                }
              
            }
