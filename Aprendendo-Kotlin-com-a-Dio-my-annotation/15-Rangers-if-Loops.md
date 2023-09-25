<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Rangers: Ifs e loops com Char</h1><br>
    <p>Além dos números, os Rangers também suportam caracteres.</p>
    <p>

        fun main(){
            for (c in 'a'..'d'){
                print(c)
            }
            print(" ")
            
            for (c in 'z' downTo 's' step 2){
                print(c)
            }
            print(" ")
            
            }
    </p>
<p>É o mesmo processo, só que desta vez com "strings" ao invés de int.<br>Vale ressaltar que os Rangers também são suportados em estruturas de repetições e condicionais. </p>
    <p>
         
      fun main(){
            val x = 2
            if (x in 1..5){
                print("X is in range from 1 to 5")
            }
            println()
            
            if (x !in 6..10){
                print("X is not in ranger from 6 to 10")
            }
            
        }  
    </p>

</body>
</html>