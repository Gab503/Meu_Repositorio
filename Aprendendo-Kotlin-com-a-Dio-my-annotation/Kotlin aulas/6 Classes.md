# Classes
Classes são basicamente uma estrutura de dados que você pode moldar da forma que quiser.
A palavra reservada para definir uma classe em Kotlin (e na maioria das linguagens) é class. 
As classes são um modelo para a criação de objetos (POO). Exemplo:

    // Declarar uma classe chamada Customer
    class Customer
    
    // Uma classe contact, com dois parâmetros de construção personalizados
    class Contact(val id: Int, var email: String) 
    
    fun main () 
    {
        
        val customer = Customer()
        
        val contact = Contact(1, "may@gmail.com")
        
        println(contact.id)
        println(contact.email)
        contact.email = "Jane@gmail.com"
        println(contact.email)
        
    }
