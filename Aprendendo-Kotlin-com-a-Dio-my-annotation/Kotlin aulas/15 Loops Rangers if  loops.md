# Rangers: Ifs e loops com Char
Além dos números, os Rangers também suportam caracteres.
    

        fun main()
        {
            for (c in 'a'..'d'){
                print(c)
            }
            print(" ")
            
            for (c in 'z' downTo 's' step 2)
            {
                print(c)
            }
            print(" ")
            
            }
É o mesmo processo, só que desta vez com "strings" ao invés de int. Vale ressaltar que os Rangers também são suportados 
em estruturas de repetições e condicionais. 
  
         
      fun main()
      {
            val x = 2
            if (x in 1..5)
            {
                print("X is in range from 1 to 5")
            }
            println()
            
            if (x !in 6..10)
            {
                print("X is not in ranger from 6 to 10")
            }
            
        }  
  
