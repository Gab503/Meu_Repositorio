<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Listas(List)</h1><br>
    <p>As listas armazenam itens na ordem em que são adicionados e permitem itens duplicado. Ao criar listas, o Kotlin pode inferir o tipo de itens armazenados. Para declarar o itpo explicitamente, adicione-o entre conlchetes angulares, exemplo, <Int> após a declaração da lista.</p>
    
  <p>A função listOf() vai criar uma lista imutável.<br>
    A função mutableListOf() vai criar uma lista mutável.</p> 

    <p>

        val systemUsers: MutableList<Int> = mutableListOf(1, 2, 3)
            val sudoers: List<Int> = systemUsers
            
            fun addSystemUser(newUser: Int){
                systemUsers.add(newUser)
            }
            
            fun getSysSudoers(): List<Int> {
                return sudoers
            }
            
            fun main() {
                addSystemUser(4)
                println("Tot sudoers: ${getSysSudoers().size}")
                getSysSudoers().forEach{
                    i -> println("Some useful info on user $i")
                }
              
            }

    </p>
</body>
</html>