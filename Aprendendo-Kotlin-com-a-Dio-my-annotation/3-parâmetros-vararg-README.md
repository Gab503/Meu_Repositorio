<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title></title>
</head>
<body>
  <h1>Parâmetros Vararg</h1<br<br>
<h2>Argumentos nomeados</h2>
<br> <p>Para um código conciso, ao chamar sua função, você não precisa incluir nomes de parâmetros. No entanto, incluir nomes de parâmetros torna seu código mais fácil de ler. Isso é chamado de uso de argumentos nomeados. Se você incluir nomes de parâmetros. poderá escrevê-los em qualquer ordem. </p>
<h2>Vararg</h2>


    <p>
    fun main(){
        // Vararg = receber quantas mensagens quiser, desde que sejam string.
        // Ou melhor quantidade de parâmetros indefinida.
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
        
  Observação, se tiver uma função, que chame outra, que também é um vararg, tem que usar * para ser um vararg também e não um Array. </p>
       
  </p>
  <p> Vararg = Basicamente, permite colocar uma quantidade de parâmetros indefinida. Permite ter quantos elementos necessários de um determinado tipo, neste caso, do tipo string. </p> 
</body>
</html>
