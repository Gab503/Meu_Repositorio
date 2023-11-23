# Função de escopo Run
A função with não é uma extensão de objeto, mas permite que você acesse as propriedades do objeto sem usar o 
operador de acesso (.).

Ela não retorna o objeto após as modificações; você acessa as propriedades diretamente.


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

função getNullableLength usa a extensão run da classe String?. A extensão run permite executar um
bloco de código se a string não for nula.

O bloco de código executado pela extensão run imprime se a string está vazia e o seu comprimento,
e retorna o comprimento da string.

Saída:

    for "null":
    for "":
	is empty? true
	length = 0
    for "some string with Kotlin ":
	is empty? false
	length = 24

