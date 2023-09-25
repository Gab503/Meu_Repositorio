    frase = 'Curso em Vídeo Python'
    print(frase[9]) # saída: V
    print(frase[9:13]) # saída: Víde:, 9 é V e 13 é 'o'
    print(frase[9:21:2]) # Do índice 9 até o 21 em dois em dois, mas não há posição 21, mas é sempre 1 a menos, então vai até o 20
    print(frase[:5]) #Do caractere 0 até a letra 4
    print(frase[15:]) # Do 15 até o final
    print(frase[9::3]) # DO 9 até o final, pulando de trê em três

    # This is a comment in Python

# Análise de String:
len(frase) == Vai mostrar o comprimento da frase (21).

frase.count(‘o’) == Dentro da variável frase, quantas vezes aparece a letra o (3)

frase.count(‘o’,0,13) == Quantas vezes aparece a letra ‘o’, do 0 até 13/12.

 frase.find(‘deo’) ==  find( encontrar). Quantas vezes encontrou ‘deo’ na variável frase, irá indicar 11 (começou na posição 11).

frase.find(‘android’) == Não há a string android na variável frase, então irá mostrar -1, ou seja, não há.

‘Curso’ in frase == Existe a string Curso na frase; irá mostrar True or False.

# Transformação de String
frase.replace(‘Python’, ‘Android’) == Vai substituir a string Python por Android.

frase.upper( ) == Vai colocar toda a variável frase em letras maiúsculas. Pega as letras minúsculas e coloca em maiúscula.

frase.lower( ) == Vai colocar toda a variável frase em letras minúsculas. Pega as letras maiúsculas e coloca em minúscula.

frase.capitalize( ) == Vai colocar todos os caracteres em minúsculo, e somente o primeiro irá ficar em maiúscula.

rase.title( ) == Vai analisar quantas palavras há na string, pelas posições dos espaços, e vai fazer um capitalize em cada palavra, isto é, a primeira letra de cada caractere irá ficar em maiúsculo. 

frase.strip( ) == Vai remover os espaços “inúteis”; do começo e no final da string

frase.rstrip( )== right /direita, remove os espaços a direita ( os últimos)

frase.lstrip( ) == left/esquerda, remove os espaços à esquerda, ou seja no início. 

# Divisão de String
       frase.split( ) == Vai ocorrer uma divisão dentro da sua string, considerando os espaços.

        Ex: C/u/r/s/o/ /e/m/ /V/i/d/e/o/ / P/y/t/h/o/n/
     0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 

agora:  

     frase.split( ) ==
     C-u-r-s-o   e-m    V-i-d-e-o    P-y-t-h-o-n
     0-1-2-3-4   0-1     0-1-2-3-4  0-1-2-3-4-5
      0          1             2                3

Cada palavra recebe uma indexação nova; e cada palavra ficará dentro de um “bloco maior”. 


# Junção de String  
    ‘-’.join(frase) == Se eu tenho palavras separadas em “blocos maiores”/lista ( com o split), ficando:

     Curso-em-Vídeo-Python


Sep='separator' == Específica como os objetos serão separados, se houver mais do que um. O padrão é um espaço em branco.

end='caractere' == Específica o caractere que é impresso no final da linha. O padrão é \n, uma quebra de linha, mas, é muito utilizado para juntar duas frases, desse jeito: end=" " .