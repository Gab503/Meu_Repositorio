# Parâmetros Vararg

## Argumentos nomeados
Para um código conciso, ao chamar sua função, você não precisa incluir nomes de parâmetros. No entanto, incluir nomes 
de parâmetros torna seu código mais fácil de ler. Isso é chamado de uso de argumentos nomeados. Se você incluir nomes de 
parâmetros. poderá escrevê-los em qualquer ordem. 

## Vararg


    
    fun main(){
        // Vararg = receber quantas mensagens quiser, desde que sejam string. Ou melhor quantidade de parâmetros indefinida.
        fun printAll(vararg messages: String) {
            for (m in messages) println(m)
        }
        printAll("Hello", "Hello","Salut", "Hola")
        
        fun printAllWithPrefix(vararg messages: String, prefix: String) {
            for (m in messages) println(prefix + m)
        }
        // prefix = neste caso é um argumento nomeado.
        printAllWithPrefix("Hello", "Hallo", "Salut", "Hola", 
        prefix = "Greeting: ")

        fun log(vararg entries: String) {
            printAll(*entries)
        }
        }
        
  Observação, se tiver uma função, que chame outra, que também é um vararg, tem que usar * para ser um vararg também e não um Array. 
  
  Vararg = Basicamente, permite colocar uma quantidade de parâmetros indefinida. Permite ter quantos elementos necessários de um
  determinado tipo, neste caso, do tipo string. 
