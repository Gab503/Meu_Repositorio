<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Verificação de igualdade == e ===</h1><br>
    <p>Existe duas formas de verificar a igualdade de dois objetos, uma seria uma comparação estrutural, que é feita com a sintaxe ==, e a outra uma comparação referencial, com a sintaxe ===.</p>

    <p>
        
        fun main(){
    val authors = setOf ("Shakespeare", "Hemigway", "Twain")
    val writers = setOf("Twain", "Shakespeare", "Hemigway")
    
    // Comparação estrutural.
    println(authors == writers)

    // comparação referencial.
    println(authors === writers)
    }  
    // true
    // false
</p>
<p>Ao invés de ser uma lista, são do tipo set, esse tipo não aceita duplicatas, se tiver um elemento duplicado, ele simplesmente não aceita essa duplicata. <br></p>

<p>Neste exemplo acima, você deve ter observado que possuem os mesmo items em ordens diferentes. Isto é, estruturalmente, possuem os mesmos valores, mas, possuem referencias diferentes (ordem diferentes = referencias diferentes). </p>

<p>Podemos pensar assim, uma comparação estrutural, é para saber se possuem os mesmo elementos. <br>Já uma comparação referencial é para ver se ambos são de fatos iguais, isto é, identicos.</p>
</body>
</html>
