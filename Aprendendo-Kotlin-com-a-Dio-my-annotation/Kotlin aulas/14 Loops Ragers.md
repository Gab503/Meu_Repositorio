# Ranges: Loops com int
A maneira mais comum de criar um intervalo em Kotlin, é usar o .. operador. Por exemplo,1..4 é equivalente a 1, 2, 3, 4.

Para declarar um intervalo na ordem inversa, use downTo. Por exemplo, 4 dowTo 1, é equivalente a 4, 3, 2, 1.

Para declarar um intervalo que aumente em uma  etapa que não seja 1, use step e o valor de incremento desejado. 

Por exemplo, 1..5 step 2, é o mesmo que ir de 1 até 5, pulando de dois em dois, ou seja, 1, 3, 5.

Para declarar um intervalo que não inclui o valor final, use o ..< operador. Por exemplo, 1..< 4 é equivalente a 1, 2, 3. 
  
        
      fun main() 
      {
            // de 0 até 3
            for (i in 0..3){
                print(i)
            }
            // print(" ") para dar espaço e não ficar grudado.
            print(" ")
            
            // não incluir o 3
            for (i in 0 until 3) {
                print(i)
            }
            
            print(" ")
            
            for(i in 3 downTo 0)
            {
                print(i)
            }
            print(" ")
            
            // de 2 até 8 pulando de 2 em dois.
            for (i in 2..8 step 2)
            {
                print(i)
            }
            
            print(" ")
        }
    
