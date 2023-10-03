<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Funções de Escopo</h1>
    <h2>Let</h2>

    <p>A função let em Kotlin é uma função de escopo que permite executar um bloco de código com um objeto como contexto. O resultado do bloco de código é o valor retornado pela função let.<br>
    O argumento da função let é o objeto que será usado como contexto. O nome do argumento é it, mas pode ser nomeado de outra forma.
     O bloco de código é executado com o objeto como contexto. O objeto pode ser acessado usando o nome do argumento it.<br> 
    O resultado do bloco de código é o valor retornado pela função let.<br>Em geral, a função let é uma maneira conveniente de executar um bloco de código com um objeto como contexto. Pode ser usada para vários fins, incluindo validação, operações e transformações.</p>

    fun customPrint(s: String){
        print(s.uppercase())
    }
    
    fun main(){
        
        val empty = "test".let{
            customPrint(it)
            it.isEmpty()
        }
        println("is empty: $empty")
        
        fun printNonNull(str: String?){
            println("Printing \"$str\":")
            
            str?.let{
                print("\t")
                customPrint(it)
                println()
            }
        }
        
        fun printIfBothNonNull(strOne: String?, strTwo: String?){
            strOne?.let{firstString ->
                strTwo?.let{secondString ->
                    customPrint("$firstString : $secondString")
                    println()
                }
        }
    }
        
        printNonNull(null)
        printNonNull("my string")
        printIfBothNonNull("First", "Second")
        
    }

    <p>Função customPrint():<br>
    Esta função pega uma string como parâmetro e imprime a versão em maiúsculas da string.
    <br>
    Função let():<br>
        
    A função let() é uma função de escopo que permite executar um bloco de código com um objeto como contexto. O resultado do bloco de código é o valor retornado pela função let().
        
    Chamada da função let() na função main():
        
    A primeira chamada da função let() na função main() é usada para imprimir a string "test" em maiúsculas e verificar se ela está vazia. O resultado da verificação de vazio é retornado pela função let().
        
     A segunda chamada da função let() na função main() é usada para imprimir a string "my string" em maiúsculas, se ela não for nula.
        
     A terceira chamada da função let() na função main() é usada para imprimir a string "First : Second", se ambas as strings forem não nulas.
        
    Saída do programa:<br>        
    TEST is empty: false<br>
    Printing "null":<br>
    Printing "my string":<br>
        MY STRING<br>
    FIRST : SECOND

</p>

</body>
</html>