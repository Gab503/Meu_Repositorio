<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Função de escopo Run</h1>

    fun main(){
    
        fun getNullableLength(ns: String?) {
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

    <p>A função getNullableLength usa a extensão run da classe String?. A extensão run permite executar um bloco de código se a string não for nula.
    O bloco de código executado pela extensão run imprime se a string está vazia e o seu comprimento, e retorna o comprimento da string.</p>

    <p>Saída:</p>

    for "null":
for "":
	is empty? true
	length = 0
for "some string with Kotlin ":
	is empty? false
	length = 24

</body>
</html>