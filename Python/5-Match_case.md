# Match case:
Vai facilitar a sua escrita, pois vai diminuir a repetição das estruturas condicionais e vai deixar o código mais fácil de ser entendido, pois já é mais intuitivo que ao usar uma estrutura dessa, temos as condições que podemos ter nesse caso específico.

Devemos utilizar quando queremos comparar a mesma variável ou expressão com várias opções:

A instrução switch (match em outras linguagens) é similar a uma série de instruções IF sobre a mesma expressão. Em muitas ocasiões, você pode querer comparar a mesma variável (ou expressão) com muitos valores diferentes, executando uma peça diferente do código dependendo de qual valor ele se encaixar. Este é exatamente o que a instrução switch faz.

      name = input("What's your name ? ")
          if name =="Harry" or name =="Hermione" or name == "Rone":
              print('Grifinória')
          else:
              print('Quem ?')
Usando match case:

      name = input("What's your name ? ")
      match name:
          case "Harry":
              print("Gryffindor")
          case "Hermione":
              print("Gryffindor")
          case "Ron":
              print("Gryffindor")
          case "Draco":
              print("Slytherin")
         case _:
              print("Who ? ")
O código acima basicamente faz:

1. Recebe uma entrada de um nome.
2. Utilizando o comando match para decidir qual case será executado
3. Caso o nome seja Harry, imprima Gryffindor. E assim por diante.