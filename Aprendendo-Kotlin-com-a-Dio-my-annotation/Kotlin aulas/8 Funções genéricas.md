# Funções Genéricas
Utlizando o mesmo pricípio de classes genéricas, para parâmetizar um tipo de maneira generica, mas desta vez em uma função.
  
    interface Source<out T> 
    {
    fun nextT(): T
    }

    fun demo(strs: Source<String>) 
    {
     val objects: Source<Any> = strs // This is OK, since T is an out-parameter
    
    }
Observação, este exemplo acima não foi muito bom, mas é basicamente o mesmo de classes genericas, mas ao invés de
usar classes é funções. Exemplo 
        
          fun element<E>... 
  
https://kotlinlang.org/docs/generics.html#use-site-variance-type-projections
