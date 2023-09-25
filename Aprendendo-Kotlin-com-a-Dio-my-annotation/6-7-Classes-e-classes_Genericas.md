<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <h1>Classes</h1>
  <p>Classes são basicamente uma estrutura de dados que você pode moldar da forma que quiser.<br>A palavra reservada para definir uma classe em Kotlin (e na maioria das linguagens) é class. <br>As classes são um modelo para a criação de objetos (POO). Exemplo:<br>
    // Declarar uma classe chamada Customer
    class Customer
    
    // Uma classe contact, com dois parâmetros de construção personalizados
    class Contact(val id: Int, var email: String) 
    
    fun main () {
        
        val customer = Customer()
        
        val contact = Contact(1, "may@gmail.com")
        
        println(contact.id)
        println(contact.email)
        contact.email = "Jane@gmail.com"
        println(contact.email)
        
    }
  </p><br><br>
  <h1>Generics Class</h1><br>
  <p> 
    A ideia principal de classes genéricas, é ter flexibilidade na tipagem das suas informações. É muito comum ver sendo usada em coleções (variáveis compostas) do tipo Listas, Mapas, Conjuntos.<br>
    
    // Vai receber vararg E, isto é, qualquer coisa.
    // Pois está como parâmetro genérico da classe MutableStack
  
    class MutableStack<E>(vararg items: E) {
    
    // Converte para uma lista os elementos. 
    private val elements = items.toMutableList()
    
    // Adiciona o elemento na lista
    fun push(element: E) = elements.add(element)
    
    // pegar o último mas sem remover.
    fun peek(): E = elements.last()
    
    // Remove o último elemento.
    fun pop(): E = elements.removeAt(elements.size -1)
    
    // Verificar se está vazia.
    fun isEmpty() = elements.isEmpty()
    
    // Tamanho
    fun size() = elements.size
    
    // Converter para texto.
    override fun toString() = "MutableStack(${elements.joinToString()})"
    
     }

    fun main () {
    val stack = MutableStack(0.62, 3.14, 2.7)
    stack.push(9.87)
    println(stack)
    
    println("peek(): ${stack.peek()}")
    println(stack)
    
    for (i in 1..stack.size()){
        println("pop(): ${stack.pop()}")
        println(stack)
    }
    }
  </p>
</body>
</html>