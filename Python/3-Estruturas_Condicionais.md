     if, elif, else:
se,senão se, senão

      Ex:       
    n = int(input(‘Digite um número: ‘))
      if n % 2 ==0: (# se o número digitado for divisível por 2 e de resto 0 faça:)
          print(f ‘O número {número} digitado é par.)
      else: (#senão, se a primeira condição for falsa:)
          print(‘Ele é ímpar’)

O elif é usado para quando possui muitas condicionais, 

     if numero != 0: (“se número for diferente de 0”)
        print(“Você digitou um número positivo”)
     elif número < 0: (“senão se o número for menor que zero faça:)
        print(“Você digitou um número negativo”) # a partir de agora o else é opcional, mas somente se tiver apenas 1 elif, caso tenha mais de um, não é usado o else
    else: (“Senão, se todas as estrutura anteriores não forem verdadeiras/atendidas”)
         print(“Talvez você digitou um número neutro, isto é, o zero”)

    n = int(input('Digite um número: '))
        if n > 0:
            print('Você digitou um número positivo.')
        elif n < 0:
           print('Você digitou um número negativo.')
        else:
           print('Você digitou um número neutro, isto é, o zero........')

Aviso ! O python é sensível a letras maiúsculas e minúsculas, e também a identação. 
No Python, a identação é usada para indicar o nível de código aninhado, cada nível de identação é representado por uma certa quantidade de espaços ou tabulações no início de uma linha.