# Def

Para definir suas próprias funções, utilize o comando def, que significa definir.
 
    def hello():
         print("Hello")
    name = str(input("What's your name ? "))
    hello()
    print(name)
    def hello(to):
        print("Hello", to)

Definir uma função é muito útil, pois assim não precisa ficar repetindo várias vezes a mesma coisa.

Outro exemplo:

      def greeting(name):
          print("welcome, " + name)
     greeting("Augusto")
Para definir uma função, usamos a palavra-chave def. O nome da função é o que vem após a palavra-chave. Neste exemplo, o nome da função é saudação. Então, para chamar a função mais tarde no script, vamos usar a palavra saudação (observe que está em inglês). 
Após o nome, temos os parâmetros da função, que são escritos entre parênteses. Neste exemplo, temos apenas um parâmetro, nome, seguido de dois pontos no final da linha. Após o cólon ( : ), temos o corpo da função. É aí que declaramos o que queremos que nossa função faça. Tenha em mente que o corpo da função deve estar à direita da definição. Nesse exemplo, o corpo contém apenas uma linha que chama de impressão. 

Parâmetro é a variável que irá receber um valor em uma função (ou método) enquanto que um argumento é o valor (que pode originar de uma variável ou expressão) que você passa para a função (ou método).

Usamos a palavra-chave return para dizer ao Python que este é o valor de retorno de uma função, armazenamos esse valor em uma variável.
Retornando valores usando funções
A função return nos permite combinar chamadas para funções e operações mais complexas que tornam seu código mais reutilizável. 


# Scope / Escopo 
É uma variável existente apenas em um contexto que você definiu. Mas se definir no escopo global, isto é,
no programa principal, irá ser "universal" essa variável, mas se definir apenas em uma função, irá esxistir somente na função(escopo local).

# Return

Retornar algo
Com uma analogia eu conseguir entender, pense em um restaurante, há uma cozinha, as mesas dos clientes etc. se concentre apenas nessas duas.
Na cozinha são feitos os pratos, então vem um garçom, pega os pratos e leva para a mesa dos cliente. 
Nessa analogia, a cozinha seria a função, o garçom seria a função return, mas ao invés de levar os pratos aos clientes, a função return retornaria algo ao código.

Às vezes não queremos que uma função simplesmente execute e termine. Podemos querer que uma função manipule os dados que lhe passamos e depois nos devolva o resultado. É aqui que o conceito de valores de retorno é útil. Utilizamos a palavra-chave return numa função, que diz à função para passar os dados de volta. Quando chamamos a função, podemos armazenar o valor devolvido numa variável. Os valores de retorno permitem que as nossas funções sejam mais flexíveis e poderosas, para que possam ser reutilizadas e chamadas várias vezes