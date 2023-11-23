# Função de escopo Run
 Executa um bloco de código em um contexto específico (o receptor do run), podendo modificar o objeto e retornar um resultado opcional. Pode ser usado para configurar propriedades de um objeto durante sua criação.

Pode ser comparado a executar código dentro do próprio objeto, independente de ele ser nulo ou não.

    fun main()
    {
    
        fun getNullableLength(ns: String?) 
	{
            println("for \"$ns\":")
            ns?.run{
                println("\tis empty? " + isEmpty())
                println("\tlength = $length")
                length
            }
        }
        getNullableLength(null)
        getNullableLength("")
        getNullableLength("some string with Kotlin ")
    }

A função getNullableLength usa a extensão run da classe String?. A extensão run permite executar um bloco de código se a string não for nula.

 O bloco de código executado pela extensão run imprime se a string está vazia e o seu comprimento, e retorna o comprimento da string.

Saída:

    for "null":
    for "":
	is empty? true
	length = 0
    for "some string with Kotlin ":
	is empty? false
	length = 24

