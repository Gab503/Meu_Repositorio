<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>POO</title>
</head>
<body>
    <h1>Herança com Construtor Parametrizado</h1>

<p> Imagine que você está cozinhando uma torta. Você pode ter uma receita básica para torta que você usa para todas as tortas que você faz. No entanto, você pode querer fazer diferentes tipos de tortas, como torta de chocolate ou torta de maçã. Para fazer isso, você pode criar uma receita para cada tipo de torta.
<br>
A receita básica para torta é como um construtor parametrizado. Ele fornece uma estrutura básica para todas as tortas. As receitas para tortas específicas são como construtores de subclasses. Elas fornecem implementações específicas para os parâmetros do construtor parametrizado.</p>

// Observe que a função não é open. Então não pode ser sobrescrita 
open class Tiger(val origin: String){
    fun sayHello(){
        println("A tiger from $origin says: grrhhhh!")
    }
}

// Herdar uma classe passando uma parâmetro padrão.
// A classe SiberianTiger, é um Tiger passando sua origem como "Siberia"
class SiberianTiger : Tiger("Siberia")

fun main(){
    val tiger : Tiger = SiberianTiger()
    tiger.sayHello()
 
}
// Saída: A tiger from Siberia says: grrhhhh!
    
</body>
</html>