<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <h1>Funções Genéricas</h1><br>
  <p>Utlizando o mesmo pricípio de classes genéricas, para parâmetizar um tipo de maneira generica, mas desta vez em uma função.<br>
  
    interface Source<out T> {
    fun nextT(): T
    }

    fun demo(strs: Source<String>) {
     val objects: Source<Any> = strs // This is OK, since T is an out-parameter
    // ...
    }
<p>Observação, este exemplo acima não foi muito bom, mas é basicamente o mesmo de classes genericas, mas ao invés de usar classes é funções. Exemplo 
        
          fun element<E>... </p>
  
<a href="https://kotlinlang.org/docs/generics.html#use-site-variance-type-projections" target="_blank"> 
  clique aqui para mais informações: </a>
  </p>
</body>
</html>