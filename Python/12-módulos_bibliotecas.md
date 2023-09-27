# Libraries / bibliotecas
Arquivos de códigos que outras pessoas escreveram e que você pode usar em seus próprios programas ou o código de uma biblioteca que você escreveu e que pode usar em seu próprio programa, mas também em outros programas. 
     Uma capacidade de compartilhar códigos com outras pessoas e em seus próprios projetos.

 Isso é feito através dos módulos.
Um módulo em Python é apenas uma biblioteca que normalmente possui uma ou mais funções ou outros recursos integrados. Geralmente o objetivo de uma biblioteca é a reutilização do código, se você estiver usando os mesmos tipos de funções repetidamente, a mesma funcionalidade, provavelmente há uma oportunidade de fatorar esse código em uma biblioteca que você pode carregar em programas avançados.

Para usar esses módulos em seu código, use a palavra chave import.

  Para pegar somente um recurso ou função de um módulo,por exemplo choice da biblioteca random, utilize from random import choice

         import random
        coin = random.choice(["heads", "tails"])
        print(coin)

         from random import choice
         coin = choice(["heads", "tails"])
         print(coin)

Para saber mais sobre bibliotecas python, <a href="https://docs.python.org/3/library/index.html" target="_blank">clique aqui</a>

         import random
         for x in range(20):
             number_random = random.randint(1, 100)
            print(number_random, end=" ")


        import random
        cards = ["jack", "queen","king"]
         random.shuffle(cards)
         print(cards)
    
# statistics
Python também vem com uma biblioteca de estatísticas, ou seja, calcula a média, moda e mediana. 

