<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Enum Class</h1>
    
    <p>Uma enum class é um tipo especial de classe em Kotlin que pode ser usada para representar um conjunto de valores constantes. As enum classes são declaradas usando a palavra-chave enum class seguida pelo nome da classe e os valores constantes.</p>

    enum class State{
        IDLE, RUNNING, FINISHED
    }
    
    fun main(){
        val state = State.RUNNING
        val message = when (state){
            State.IDLE -> "it's idle"
            State.RUNNING -> "it's running"
            State.FINISHED -> "it's finished"
        }
        println(message)
    }

    <p>Explicação do código:
    1. Declaração da enum class State com três valores: IDLE, RUNNING e FINISHED.
    2. Criação de uma variável state do tipo State e atribuição do valor RUNNING a ela.
    3. Declaração de uma variável message do tipo String.
    4. Atribuição do valor correto da variável message de acordo com o valor da variável state usando uma when expression.
    5. Impressão da variável message.</p>
       
    <p>Saída:</p> 
    <p> it's running</p>

    <p>Outro exemplo: </p>

    enum class Color(val rgb: Int ){
        RED(0xFF0000),
        GREEN(0x00FF00),
        BLUE(0x0000FF),
        YELLOW(0xFFFF00);
        
        fun containsRed() = (this.rgb and 0xFF0000 != 0)
    }
    
    fun main(){
        val red = Color.RED
        println(red)
        println(red.containsRed())
        println(Color.BLUE.containsRed())
        println(Color.YELLOW.containsRed())
    }
<p>
    Documentação do código<br>
    
    Este código define uma classe enum chamada Color que representa as quatro cores primárias: vermelho, verde, azul e amarelo. Cada cor é representada por uma constante da classe Color, que possui uma propriedade chamada rgb que armazena o valor RGB da cor.
    
    A função containsRed() verifica se a cor contém vermelho. Ela faz isso realizando uma operação AND bit a bit entre a propriedade rgb da cor e o valor inteiro 0xFF0000, que representa a máscara de vermelho. Se o resultado da operação AND bit a bit não for zero, então a cor contém vermelho.
    
    A função main() cria uma variável chamada red e a atribui ao valor da constante Color.RED. Em seguida, imprime a variável red no console. Em seguida, chama a função containsRed() na variável red e imprime o resultado no console. Por fim, chama a função containsRed() nas constantes Color.BLUE e Color.YELLOW e imprime os resultados no console.
    
    Saída:
    
    RED
    true
    false
    true</p>
</body>
</html>