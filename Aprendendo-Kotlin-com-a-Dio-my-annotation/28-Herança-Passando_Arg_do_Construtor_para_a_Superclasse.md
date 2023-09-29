<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>POO</title>
</head>
<body>
    <h1>Herança. Passando Argumentos do Construtor Para a Superclasse.</h1>

<p>Classe Lion<br>
A classe Lion é uma classe aberta que representa um leão. Ela tem dois atributos: name e origin. O atributo name representa o nome do leão e o atributo origin representa a origem do leão. Ela também tem um método sayHello() que imprime uma mensagem de saudação. </p>

<p>Atributo name<br>
O atributo name é um atributo de tipo String que representa o nome do leão.    
<br></p>

<p>Atributo origin<br>
O atributo origin é um atributo de tipo String que representa a origem do leão.</p>

<p>Método sayHello()<br>
O método sayHello() é um método de tipo Unit que imprime uma mensagem de saudação. A mensagem de saudação inclui o nome e a origem do leão. </p>

<p>Classe Asiatic<br>
A classe Asiatic é uma classe que herda da classe Lion. Ela tem um construtor que passa o valor do parâmetro name para o atributo name da classe Lion. Ela também passa o valor "India" para o atributo origin da classe Lion.</p>

<p>Função main()<br>
A função main() é a função principal do programa. Ela cria um objeto da classe Asiatic e chama o método sayHello() desse objeto.<br>

Saída
A saída do programa é a seguinte mensagem: </p>
    Rufo, the lion from India says: graoh!


  
<p>
Explicação
    <br>
O código funciona da seguinte forma:<br>

A classe Lion é declarada como uma classe aberta. Isso significa que ela pode ser herdada por outras classes.<br>
    
A classe Asiatic herda da classe Lion. <br>

O construtor da classe Asiatic passa o valor do parâmetro name para o atributo name da classe Lion. Ele também passa o valor "India" para o atributo origin da classe Lion.<br>

A função main() cria um objeto da classe Asiatic.<br>

O método sayHello() do objeto Asiatic é chamado. <br>
    
O método sayHello() imprime a mensagem de saudação.
</p>
</body>
</html>