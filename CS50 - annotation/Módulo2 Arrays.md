# Módulo 2 Arrays

Nas últimas aulas, vimos que para um código em C ser executado, precisa primeiro ser convertido em linguagem de máquina (código binário).
Para fazer isso usámos make hello por exemplo. 

Make esta automatizando um conjunto mais específico de etapas. Por exemplo ao fazer make hello irá aparecer na sua tela (ou não, na minha não apareceu, acho que é por causa da versão atual)

             
    clang - ggdb3 -00 -std=c11 -wall -werror - wextra -wno-sign-compare -Wno-used-parameter -Wno-unused-variable -wshadow hello.c -lcrypt -lcs50 -lm -o hello

#### O make está automatizando a execução de um comando, mais especificamente denominado clang. 
Clang é o compilador, um compilador sendo um programa que converte código-fonte em código de máquina. Temos usado Clang o tempo todo. Mas o Clang requer um pouco mais de sofisticação. 

Clang é outro programa instalado no CS50 IDE. É um compilador muito popular que você pode baixar em seu próprio dispositivo. Mas para executá-lo diretamente sem o make é um pouco diferente.          

* Digite clang
* Nome do arquivo que quer compilar.
* E aperte enter

      clang hello.c

  Se não aparecer nada na tela, é porque tudo ocorreu bem. Ao digitar ls agora, você não verá o programa hello, e sim a.out*.

      $ clang hello.c
      $ ls
      a.out* hello.c

Este é um resquício histórico. Anos atrás, quando os humanos usavam um compilador para compilar seu código, 
o nome do arquivo padrão que todo programa recebeu foi a.out para saída de assembly.
Mas esse não é um bom nome para um programa. Não é de forma alguma descritivo do que faz. 
Acontece que programas como o Clang podem ser configurados na linha de comando. 

    $ clang -o hello hello.c

Está fornecendo o que vamos chamar de argumento de linha de comando. Portanto esses comando, como make e rm, 
às vezes podem apenas ser executados por si próprios. Mas muitas vezes, vimos que eles aceitam informações em algum sentido
você digita make hello, rm hello. E a segunda palavra hello, nesses casos, é uma espécie de input para o comando, 
agora conhecido como um argumento de linha de comando. É um input para o comando.


Neste código temos mais de um argumento de linha de comando.

* Temos a palavra Clang, que é o compilador que vamos executar.
* -o uma notação abreviada para "output", "imprima o seguinte".
* O que deseja como output ? hello, portanto a palavra final é hello.c

Isso está dizend: Rode Clang, produza um arquivo chamado hello, e tome como arquivo de input o chamado hello.c.

    M2/ $ clang -o hello hello.c
    M2/ $ ls
    hello*  hello.c

Portanto, é assim que o Clang está ajudando a compilar o código. É uma espécie de automação de todos esses processos.

    #include <stdio.h>
    #include <cs50.h>

    int main(void)
    {
        string name = get_string("What's your name ? ")
        printf("Hello %s\n", name);
    }
Esta versão 2.0 do hello world envolvia solicita um input do usuário usando a função get_string do CS50, armazenado a saída em 
uma variável chamada nome. Mas lembre-se de que também tivemos que adicionar cs50.h no início do arquivo.



Ao usar uma biblioteca, não basta apenas incluí-la no cabeçalho no topo de seu próprio código. Às vezes, 
você também precisa dizer ao computador onde encontrar os 0 e 1 que alguém escreveu para implementar 
uma função como get_string.

Portanto, o arquivo de cabeçalho, como cs50, apenas informa ao compilador que a função existe. Há um segundo mecanismo 
que até agora foi automatizado para nós que diz ao computador onde encontrar 0 e 1 que implementam as funções no cabeçalho 
desse arquivo.

Portanto, será necessário adicionar outro argumento de linha de comando para este comando.

    $ clang -o hello hello.c -lcs50 

* lcs50: Simplesmente se refere ao link na biblioteca CS50.

Portanto o make automatiza tudo isso para nós.

Quando você compila seu código-fonte para o código de máquina, há mais etapas envolvidas. 
E quando dizemos compilar, na verdade queremos dizer essas quatro etapas:

**Preprocessing**

**Compiling**

**Assembling**

**Linking**

1. Pega seu próprio código-fonte, e ele pré-processa seu código, de cima a baixo, da esquerda para a direita.
Pré-processar seu código significa que procura todas as linhas que começam com um símbolo hash, como: 

       #include<cs50.h>
       #include<stdio.h>

E o que a etapa de pré-processamento faz é localizar e substituir. O hash include pela função da biblioteca que está sendo usado.

    #include<cs50.h>  -> string get_string(string prompt);
    #include<stdio.h> -> int printf(string format,...);

Lembrando que isto ocorre automaticamente. Está definindo todas as funções no código para que o computador saiba o que fazer, 
porque lembre-se de que encontramos este tipo de bug no módulo anterior, onde tentava implementar uma função chamada get_positive_int. 
quando foi implementado essa função na parte inferior do código, o compilador era meio burro por não perceber que ele existia
porque foi implementado até o final do arquivo. 

Ao colocar uma menção a esta função, uma dica, se preferir, bem no topo, é como treinar o compilador a saber de antemão que 
ainda não sei como está implementado, mas sei que get_String vai existir. Ainda não sei como está implementado
mas eu sei que printf vai existir. 

Portanto esses arquivos de cabeçalho que incluímos, contém todos os protótipos, ou seja, todas as dicas para todas as funções
que existem na biblioteca para que seu código, quando compilado, saiba, de cima a baixo que essas funções existirão. 

* Portanto o pré-processador apenas nos poupa o trabalho de ter que copiar e colar todos esses protótipos, ou se preferir assim,
* todas essas dicas, nós mesmos.

 2. Agora a compilação tem um significado mais preciso. Compilar seu código agora significa pegar este código C
e convertê-lo do código-fonte para outro tipo de código-fonte o que chamamos de código assembly.

Resumindo, há muitos computadores diferentes no mundo, e especificamente, há muitos tipos diferentes de CPUs, Unidade Central 
de Processamento, o cérebro de um computador. E uma CPU entende certos comandos. E esses comandos tendem a ser expressos
nesta linguagem chamada código assembly. 

Então você escreve o código em C e o computador, porém converte para uma linguagem mais amigável chamada código Assembly.

E decádas atrás, os humanos escreveram essas coisas. Humanos escreveram código assembly. Mas hoje em dia, temos C, e linguagens como 
Python mais fáceis de usar.

O código em assembly está um pouco mais próximo do que o próprio computador entende. 

3. Assembling (montar). Significa pegar o código assembly e finalmente convertê-lo em código de máquina ( código binário) 0s e 1s.

Então você escreve o código-fonte. O compilador o monta em código assembly. Em seguida, ele o compila em código assembly. 
Em seguida, ele o monta em código de máquina até que tenhamos os 0s e 1s.

Mas na verdade há uma etapa final. 

Só porque o código que você escreveu foi convertido em 0 e 1, ele ainda precisa ser vinculado aos 0s e 1s que o CS50 escreveu 
e que os designers da linguagem C escreveram anos atrás. Então quando você escreve um código, não está apenas incluindo os protótipos 
para funções como get_string e printf no topo, as demais linhas de código ( da função principal) são as finalmente
convertidas em 0s e 1s. 

Portanto há 3 arquivos sendo combinados em seu programa.

* O primeiro hello.c uma vez que é pré-processado e compilado e montado, fica na forma de 0s e 1s.

* Em algum lugar no CS50 IDE, há um monte de 0 e 1 representando CS50.c.

* Em algum lugar na IDE CS50 há outro arquivo representando os 0s e 1s para stdio.h.

4.  Esta quarta estapa final, conhecida como linking, que pega todos os 0s e 1s, todos do CS50, todos de printf, e os linka
todos em grande conjunto blob, se preferir, representando coletivamente o seu programa, hello.c


## Debugging

Os humanos cometem erros em todas as formas de vida. E isso é muito verdadeiro no contexto do código, onde, novamente, 
de acordo com os módulos anteriores, a precisão é muito importante, assim como a correção. E às é difícil alcançar esses dois objetivos. 

#### Como você pode depurar seu próprio código, ou seja, encontrar problemas em seu código ?
Um bug é um erro em um programa. Nos módulos anteriores, há o help50, style50, check50, mas há mais ferramentas que podem
ajudar você.

É uma ferramenta de depuração universal, chamada no contexto de C printf. Então printf, é claro é apenas uma função que 
imprime coisas na tela. Mas isso em si é uma ferramenta maravilhosamente poderosa por meio da qual você pode rastrear
problemas em seu código.

Quase todas as linguagens de programação que existem têm alguma forma de printf, print ou say do scrath por exemplo, mas será
alguma capacidade de exibir informações ou apresentar informações a um humano.

    #include <stdio.h>

    int main(void)
    {
        for (int i = 0; i <= 10; i++)
        {
            printf("i is now %i\n", i);
            printf("#\n");
        }
    }

Há um bug nesse programa, cujo objetivo é imprimir 10 hash verticalmente. E através do primeiro printf podemos analisar melho este bug.
Ao executar este programa, verá que começa no 0, e não no 1 para resolver isso:

    for (int i = 1; i <= 10; i++);

#### Mas e se o código tive muitas linhas, vai precisar colocar printf para cada variável ? Para cada operação que for feita etc ?
Para isso temos o debug50 construido em cima de uma ferramenta padrão da indústria conhecida como GDB, o GNU DeBugger, que é uma ferramenta
padrão que muitos sistemas de computador diferentes usam para fornecer a capacidade de depurar seu código de uma forma mais sofisticada do que usar apenas printf.

    #include <stdio.h>

    int main(void)
    {
        for (int i = 0; i <= 10; i++)
        {
            printf("#\n");
        }
    }

Um depurador, é uma ferramenta que permite que você execute seu código passo a passo e olhe para dentro de variáveis e outras partes da memória dentro do computador 
enquanto seu programa está em execução. No momento, quase todo programa que executamos leva uma fração de segundo para ser executado, isso é muito rápido para envolver 
nossa mente em torno do que está acontecendo passo a passo. Um depurador permite que você execute seu programa muito mais devagar, passo a passo, para que você possa ver
o que está acontecendo. 

File name = bug.c

    $ debug50 ./bug
    Looks like you haven't set any breakpoints. Set at least one breakpoint by clicking to the left of a line number an  d then re-run debug50!

Debug50 precisa que eu diga ao computador antes em que linha eu quero entrar e seguir passo a passo. Clique na numeração da linha que deseja (linha 6)

Após apertar enter, verá um novo painel a esquerda. 

* A linha 6 está destacada. E isso é porque o debug50 está fazendo, é executar o programa mas interrompe a execução na linha 6. Então faz tudo da linha 1 a 5.

* Ao clicar em Step Over, irá começar a pecorrer a linha de código

      #include<cs50.h>
      #include<stdio.h>


      int main(void)
      {
          int = i get_negative_int();
          printf("%i\n", i);
      }

      int get_negative_int(void)
      {
          int n;
          do
          {
              n = get_int("Negative Integer: ");
          }
          while (n < 0);
          return n
      }

O bug deste programa, é que não existe get_negative_int, pois está sendo declarado após a função principal. 

    1 #include<cs50.h>
    2 #include<stdio.h>
    3
    4 // Prototype
    5 int get_negative_int(void);
    6
    7 int main(void)
    8 {
    9
    10  int i = get_negative_int();
    11  printf("%i\n", i);
    12 }
    13
    14 int get_negative_int(void)
    15  {
    16  int n;
    17   do
    18  {
    19      n = get_int("Negative Integer: ");
    20  }
    21   while (n < 0);
    22   return n;
    23  }

Ao depurar este código:

* Call stack é uma maneira sofisticada de se referir a todas as funções que seu programa neste momento executou e ainda não retornou.
No momento a [unica função que há é main. Porque eu definir um ponto de interrupção na linha 10, que está por definição dentro do main.

* Step into. Salta para a função get_negative_int, e se concentra na primeira linha de código, a linha 19. Agora em Call Stack apareceu a função get_negative_int


* Verá que o bug está no loop while, para corrigílo basta fazer n > 0.

## Depuração do Pato de borracha
A depuração do pato de borracha (ou rubber ducking ) é um método de depuração de código articulando um problema em linguagem natural falada ou escrita . O nome é uma referência a uma história do livro The Pragmatic Programmer , na qual um programador carregava um pato de borracha e depurava seu código, forçando-se a explicá-lo, linha por linha, para o pato. Existem muitos outros termos para esta técnica, muitas vezes envolvendo diferentes objetos inanimados (geralmente) ou animais de estimação, como um cachorro ou um gato.


* Types: Cada um dos tipos de dados ( int, float etc) é definido em um sistema de computador típico como ocupando uma quantidade
fixa de espaço. E isso depende do seu dispositivo, apenas quanto espaço é usado normalmente por esses tipos de dados.
Mas no CS50 IDE o tamanho deles são:

* bool 1 byte

* char 1 byte

* double 8 bytes

* float 4 bytes

* int 4 bytes

* long 8 bytes

* string ? bytes

* ...

É na memória RAM que os programas são armazenados enquanto estão em execução. E é onde os arquivos
são armazenados quando abertos. 

Então, normalmente, se você salvar, instalar programas ou salvar aquivos, são salvos no que geralmente é chamado de disco rígido, HD, ou SSD, CD ou algum outro meio físico. 

E eles não precisam de eletricidade para armazenar seus dados a longo prazo. Mas com RAM é diferentes, é mais volátil. 
Mas é mais veloz que um HD ou até um SSD. É muito mais rápido porque é puramente eletrônica, e não existem peças móveis. 

Com RAM, você tem a capacidade de abrir arquivos e executar programas mais rapidamente porque você clica duas vezes em um
programa para executá-lo, ou você abre um arquivo para visualizá-lo ou editá-lo, ele é armazenado temporariamente na RAM. 
se a bateria do seu laptop acabou, ou se seu computador foi desconectado ou seu telefone estragou, enquanto estava escrevendo um e-mail por exemplo,  a razão para qual você e eu tendemos a perder dados, é porque a memória RAM, é volátil. Ou seja requer eletricidade para continuar alimentá-la

Cada um retângulas da memória RAM é um tipo de chip. E nesses chips são armazenados todos os 0 e 1, os pequenos interruptores
mencionado no módulo 0. 

Eu não sei o tamanho de um pente de RAM, podemos pensar neste dispositivo físico, nesta memória, como sendo uma grade, de cima para baixo, da esquerda para a direita. E cada um dos quadrados desta grade, pode representar um byte individual. E talvez possa ter mais deles, talvez menos, mas não importa quantos existem, podemos pensar em cada um deles como tendo um local. 

**Então o que significa que um char ocupe 1 byte ?**
Isso significa que se a memória do seu computador está executando um programa, que talvez você escreveu usando uma variável char
em algum lugar dele, o char que você está armazenando nessa variável pode muito bem ser armazenado do quadrado do canto superior
da grade fisicamente desta parte da RAM. 

Se você estiver armazenando algo como um int, que ocupa 4 bytes, pode ocupar todos os quatro quadrados ao longo do topo, ou em um outro lugar, 






