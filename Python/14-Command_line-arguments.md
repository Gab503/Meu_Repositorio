# Command line arguments
Argumentos de linha de comando, este recurso não é exclusivo do Python, também há em outras linguagens de programação. Em geral, permite fornecer entrada não quando solicitar dentro de um programa, como acontece sempre que chamamos a entrada da função em Python , mas sim, com esse recurso, argumentos de linha de comando de programas que permitem inserir no programa apenas quando você está executando na linha  de comando.

         import sys
         print("hello, my name is ", sys.argv[1]) # substitui a necessidade de criar uma variável com input e colocá-la em um format

No índice 0, vai estar o nome do arquivo, e se der enter sem escrever o nome no prompt / terminal, vai dar erro de índice

        import sys
        try:
            # substitui a necessidade de criar uma variável com input e colocá-la em um format
        print("hello, my name is ", sys.argv[1])
        except IndexError:
             print("Too new arguments")

Otimizando:

        import sys
        if len(sys.argv) < 2:
            print("Too few arguments")
        elif len(sys.argv) > 2:
             print("Too many arguments")
        else:
            print("hello, my name is ", sys.argv[1])


         import sys
         if len(sys.argv) < 2:
        ''' Se a condição for true, irá sair do programa'''
            sys.exit("Too few arguments")
        elif len(sys.argv) > 2:
            sys.exit("Too many arguments")
        print("hello, my name is ", sys.argv[1])

