# Linguagem de Programação C
file name: Hello.c

      # incluide <stdio.h>
      int main (void)
      {
          printf("Hello World !");
      }
#### Mas como executar esse código ? 
Interface de Linha de Comando, ou CLI, que é basicamente na janela do terminal. O contraste de uma interfacce gráfica de usuário, ou GUI. 

Lembrando que os computadores entendem apenas códigos binários, 1 e 0. Os computadores de hoje dia possuem a capacidade de imprimir (mostrar) vários coisas na tela. E essa nocão de impressão, essa função, essa funcionalidade, também está sendo representada sob o capô de um computador por assim dizer, por algum padrão de 0 e 1. 

Todo o código acima, apesar de ser mais ou menos perecido com o inglês, e como que diz claramente: " Hello World! ", o computador, ironicamente, não sabe o que foi digitado. 
Para que ele entenda o que está digitado, você precisa realmente converter para 0 e 1. 
Este código fonte em C, precisa ser em 0 e 1 para que o computador possa entender.

#### Como convertes este código fonte em binário ?
Precisará de um programa chamado compilador. Um compilador é um programa que você pode baixar gratuitamente, ou pode ser pago também, que é um programa projetado para converter o código fonte em códigos de que os computadores possam entender, isto é, em binário. Portanto, só precisa de acesso a um compilador.

E um desses existem dentro do CS50 IDE. Vamos descrever essa ferramenta como sendo algo simples, "make". Literalmente, se eu quiser que meu programa faça algo, e digito na janela do terminal "make hello". Não Hello.c; O compilador vai inferir a partir deste comando que eu pretendo compilar um arquivo chamado Hello.c

Agora para executar o programa em Hello.c você precisa digitar um comando diferente, que é o análogo do duplo clique em ícone em seu dispositivo. Digite literalmente: 

* ./Hello

Que é como dizer: Vá na pasta atual do computador que estou usando e procure por um programa chamado "Hello".  Após isso basta digitar enter e que executará o programa.

*  Uma função é como um miniprograma. É uma ação ou um verbo que você pode usar ao escrever seu próprio programa que faz algo. No scratc há por exemplo Say (dizer).
As funções também podem ter inputs, re-chamadas. Agora, vamos começar chamando inputs para argumentos de funções por assim dizer. Outro termo para isso é parâmetros. Mas são sinônimos. Os argumentos são as inputs para as funções.

No scratch, por exemplo, Say Hello World

* Em c, printf("Hello World")

printf é para imprimir algo formatado. 

* Repare que em C, há parênteses abertos e parênteses fechados. No meio desses parênteses estarão os inputs dessa função printf, também conhecidos como argumentos.

* Também à necessidade de acrescentar aspas duplas à esquerda e à direita.

* E também tem que acrescentar um ponto e vírgula ao final.

* As funções são apenas uma versão programada de um algoritmo, a implementação de um algoritmo em código, em software. Assim, uma função pode ser representada como sendo a tomada de inputs conhecida de outra forma como argumentos. Mas as funções podem fazer pelo menos dois tipos diferentes de coisas no mundo da programação.
Quando uma função recebe inputs, ou seja, argumentos, funções podem ter o que se chama efeitos colaterais.

* No scratch, quando usamos o bloco "Say" ele retornou um output. Mais tecnicamente tinha um efeito colateral. Quando usou o bloco say ou printf, apareceu algo na tela, ou melhor, teve um efeito colateral.
Portanto, um efeito colateral de uma função é frequentemente algo visual que acontece na tela, como texto ou áudio.

* Há outra característica de funções, conhecida como return values, onde uma função pode realmente devolver um valor. Vai apenas devolver para você de uma forma que você, o programador, pode reutilizar qual seja o output dessa função idealmente, armazenando em uma variável. Assim como um matemático armazenaria um número em uma variável, como X ou Y, ou Z.

* Bibliotecas: Uma biblioteca é um código que outra pessoa escreveu. A que será usada é chamada CS50.

      string answer = get_string( " What's your name ?");

  
* String: No mundo da programação, uma string é um texto.

* get_string é uma função que vai fornecer a você inputs. Perceba, por parêntes em C, ele pode rebecer entrada. A entrada / input será "What's your name ?".

* Como na maioria das linguagens, se você quiser que algo seja armazenado em uma variável, você mesmo tem que fazer isso.
Para fazer isso, você simplesmente inventa o nome da variável que você deseja, seja X ou Y ouZ, ou de forma mais convincente, "aswer", e você usa um sinal de igual. E mesmo que em matemática isso geralmente implique igualdade, no contexto do C e na maioria das linguagens de programação, o sinal de igualdade na verdade significa o que chamaremos de atribuição. Significa, efetivamente, copiar o que estiver à direita no quer que esteja à esquerda. Portanto, se do lado direito houver uma função cujo propósito é perguntar a uma pessoa seu nome, esse nome vai ser copiado da direita para a esquerda para esta variável chamada resposta.

No mundo do C, você não pode ter apenas variáveis. Você tem que dizer ao computador, antecipadamente, que tipo de variável você deseja. Neste caso, uma string. 

E a convenção para fazer isso é você escrever literalmente o nome do tipo que você quer. Em seguida você escreve o nome da variável. E então, novamente, ára atribuir um valor a essa variável da direita para a esquerda, temos que usar o sinal de igual. 

Podemos fazer algo com o valor de retorno ou output da pesqunta.


    string answer = get_string("What's your name ?");
    printf(" Hello %s\n",answer);

* %s Isto é o que chamamos de formato de código, portanto o f em print. O printf não apenas imprime coisas. Ele também pode imprimir códigos de formato. E isto é apenas uma sintexe extravagante dizendo "coloque algum valo aqui". o s, é uma string. Se você usar uma vírgula no meio de parênteses como argumentos ou inputs para uma função, ou seja, separando o que há na esquerda do que está à direita. Note que, a vírgula está fora das aspas duplas;

* Lembre-se que, sempre que for alterar o código, não basta apenas salvar-lo, é preciso re-copilar. Usando neste caso, "make Hello". Isso acontece por causa da linguagem C, que é uma linguagem compilada e não interpretada.

      int main(void)
      {

      }
É assim que você começa a escrever um programa. Semelhante ao aberte a bandeira verde do scratch. 

Header file: Arquivos de cabeçalho. Um termo técnico que se refere a um arquivo escrito na linguagem de programação C, cujo nome termina não com .c mas com .h

 No scratch:

         When (bandeira verde) clicked.
         Say Hello World.

 Em c:    

         int main(void)
         {
             printf("Hello World");
         }
.

          # include <cs50.h>
          # include <stdio.h>

          int main (void)
          {
              string answer = get_string("What's your name ?");
              printf("Nice to meet you %s\n",answer);
          }   


         
* #include <stdio.h> Se refere a um arquivo chamado stdio.h, que é for standard input output ponto h. É um acrônimo no mundo dos computadores que se refere apenas a entrada e saída. Assim, o io.h é apenas um arquivo muito popular que é usado em C e que dá a capacidade de obter input e output do usuário. E o faz fornecer o printf, por exemplo, que permite que você gere alguma forma de output atráves desses efeitos colaterais.

* Para usar o get_string, acrescentamos um segundo arquivo de cabeçalho chamado CS50.h

##### Portanto, estes arquivos de cabeçalho apenas dão acesso a mais funções do que você pode obter automaticamente da linguagem que você está usando, neste caso, C.

É normal cometer alguns erros quando se está iniciando seu aprendizado, como esquecer um ; no final do código, ou aspas, ou parêntes etc... Há algumas ferramentas que podem ajudar a lidar com esses erros:

Qualquer umas das ferramentas cujos nomes terminam com 50 são especificamente orientadas para a educação, escritas pelo Staff da CS50, para treinamentos temporários que serem utilizadas neste curso.

* help50: help50 é um comando para permitir que você esolva problemas que de outra forma você não poderia ver com clareza em seu próprio código. Ele ajuda a saber o que deu errado. 
Para isso basta adicionar help50 antes do make dessa maneira:

            help50 make Hello

##### Lembre-se: Um bom código é correto, isto é, faz o que se espera que faça, possui design e estilo.

* style50: Esta é outra ferramenta orientada para a educação que está instalada no CS50 IDE, que permite que você descubra como melhorar seu código. 
  
Para adicionar comentários em c:

            // This is a comment

* Um bom comentário, explica o objetivo da linha ( ou linhas) de código. Mas lembre-se de sempre buscar que seu código seja auto-descritivo.

* check50: Esta é uma ferramenta específica que vai verificar a exatidão de seu código. Então, enquanto help50 apenas ajuda você a compilar seu código normalmente, quando não está compilando nada, o style50 ajuda você a melhorar o estilo de seu código, check50 verificará a exatidão de seu código em alguns testes automatizados.

A IDE CS50 é, na verdade como se fosse seu próprio servidor ou seu próprio computador na nuve. Na janela do terminal, pode ser feito muito mais coisas do que somente help50 ... Também é possível manipular os arquivos.

* ls : É uma notação abreviada para listas. E simplesmente, ls lista os arquivos ou pastas em sua pasta atual. Você ter observado que Hello* está destacado e com um asterisco. E isso é apenas uma pista visual de que esse arquivo é executável. Ou seka, que esse é um programa que você pode rodar com ./Hello.

* É possível renomear o arquivo dentro da janela do terminal.  Se quiser o remover digite:

        $rm Hello
        rm: remove regular file 'Hello' ? yes
  Você pode olhar no canto esquerda onde se encontra seus arquivos, notará que o arquivo Hello foi removido, restando apenas Hello.c.

* Para renomear:

        mv Hello.c goodbye.c


  * mv é o camando para mudar. Novamente no cante superior esquerdo, notará que o arquivo mudou de nome.
 
Suponha que eu queira começar a organizar meus arquivos. Suponha que você queira criar uma pasta também conhecida como um diretório:

        mkdir lecture

* mkdir é o comando para cria um novo diretório. Após o comando digite o nome do diretório.

* Para mover hello.c para no o diretório:

        $ mv hello.c lecture/
  Se digitar ls novamente, verá somente o nome da pasta.

Semelhante a quando você quiser acessar uma arquivo que está dentro de uma pasta, primeiro você precisa acessar a pasta e depois o arquivo: 

       $ cd lecture
* cd é comando para acessar um diretório.

Se digitar ls novamente verá:

        lecture/ $ ls
        $ hello.c

Suponha que eu queira mudar hello.c para onde estava antes. 

* Há uma notação curta para o que chamaremos de pastas dos pais. Assim como nas árvores genealógicas, há noção de pais e filhos, e netos, e assim por diante. Isso também é verdade em sistemas de informática que possuem pastas. E pastas dentro de pastas. Há uma hierarquia muito parecida com uma árvore genealógica.

  Então, se eu quiser mover hello.c um nível acima, eu posso fazer:

      $mv hello.c ..
  
O código acima significa, mova este arquivo para a pasta acima. 

Como eu subo a mim mesmo um nível acima nessa árvore genealógica que são estas pastas ?

       cd ..
Isso vai mudar para o diretório principal. Ponto ponto significa apenas o principal, o primeiro, o "Pai". 

Para remover o lecture não é o mesmo como removeu o Hello.c:

       rmdir lecture

* Para executar o hello.c usá-se ./hello pois assim como o ponto se refere ao ponto do seu diretório pai, um único ponto se refere a seu diretório atual.

  Portanto, ponto barra (./) é apenas uma maneira explícita de dizer ao computador, execute o programa hello que está aqui mesmo em meu diretório atual.

## Tipos de dados
Já vimos as strings. Você pode ter não apenas strings de texto, mas que talvez sejam inteiros, como números, ou talvez valore de ponto flutuante como 3.14159, ou outros valores semelhantes. Você pode ter valore booleanos que são apenas True or False. Você pode ter caracteres ou chars, que são caracteres únicos. 

* bool
* char
* double
* float
* int
* long
* string
* ...

no CS50 IDE também há:

* get_char
* get_double
* get_float
* get_int
* get_long
* get_string
* ...

Mas acontece que cada um destes tipos de dados, como int e float, têm um número finito de bits. Cada um desses tipos de dados usa um número específico de bits. Int por exemplo, inteiros em C, usa apenas 32 bits. 

Printf, tem a capacidade de imprimir não apenas strings, mas também diferentes formatos de códigos de outros tipos de dados também. 

* %c Será o local a ser ocupado para impressão de um único caractere. Porcentagem c para char por assim dizer.
  
* %f  Vai ser para um valor de ponto flutuante. Portanto se você quiser imprimir um número real com um ponto decimal, você vai usar %f
  
* %i Se quiser imprimir um número inteiro, use %i. 
  
* %li Se você quiser imprimir um número inteiro longo, também conhecido como long, use %li
  
* %s Para imprimir strings
  
* ...

Também há peradores aritméticos:

* Adição + 
* Subtração -
* Multiplicação *
* divisão /
* Módulo ou resto da divisão %

* File name: addition.c
  
            # include <cs50.h>
            # include <stdio.h>

            int main(void)
            {
                int x = get_int("What is X ? ");

                int y = get_int("What is Y ? ");

                printf("%i \n", x + y );

             }

  * Deta vez, digite make addition
  * ./addition

  * Caso digite qualquer coisa que não seja um número inteiro, irá novamente fazer a pergunta what is x ( or y) até receber um número inteiro.

Sem precisar cria estruturas condicionais para verificar se recebeu um número inteiro ou uma um loop while. 

* Ints usam apenas 32 bits no total. Com 32 bits, poder contar até aproximadamente até 4 bilhões. Mas get_int suporta inteiros de forma ampla, o que inclui não apenas números positivos, mas também números negativos e zero. Se você quiser suportar ambos os números positivos e números negativos, você pode representar 4 bilhões ou mais de valores totais possíveis. Mas se quiser ir mais longe, você pode contar tão alto quanto 2 bilhões na direção positiva e 2 bilhões na direção negativa.

Para receber um número mais alto, precisará utilizar um outro tipo de dados sem ser int. Neste caso, long, um número inteiro longo.

             # include <cs50.h>
             # include <stdio.h>

             int main(void)
             {
                 long x = get_long("What is X ? ");

                 long y = get_long("What is Y ? ");

                 printf("%li \n", x + y );

             }


* Casting:Cast ou Typecast. Covencer o computador a converter um tipo de dado em outro. Entre parênteses, apenas colocando o novo tipo de dados que você deseja.

        # include <cs50.h>
        # include <stdio.h>

        int main (void)
        {
            // Get  numbers from user
            int x = get_int("what is X ? ");
            int y = get_int("What is Y ? ");

            // Divide x by y, and Convert X and Y to Float. Remember, x and y are integer variables
            float z = (float) x / (float) y;
            printf("%f\n", z);

        }

  ####  Syntatic sugar:
  * counter = 0
    
  * int counter = 0;
    
  * counter = counter +1;
    
  * counter += 1;
 
  * counter ++;
 
  ## Estruturas Condicionais
  Uma condição é como uma bifurcação na estrada que poderia permitir que você fizesse isso, esta outra coisa ou algo mais. Por exemplo:

        if (x < y)
        {
             printf("x is less than y"); 
        }
  
Você não precisa destas duas chaves se você só tem uma linha de código dentro da condição. No entanto, estilisticamente, é recomendado. 

E podemos ir em um outro sentido na bifurcação. Com o else.

    if (x < y)
    {
        printf("x is less than y"); 
    }
    
    else if (x > y)
    {
         printf("x is greater than y");
    }

    else  (x == y)
    {
         printf("x is equal to y");
    }

* Vale ressaltar que C diferencia letra maiúsculas e minúsculas. para isso continue na estrutura condiciona, e coloque ou, isto é || para fazer duas perguntas ao mesmo tempo. 

      # include <cs50.h>
      # include <stdio.h>

      int main(void)
      {
  
      // chars são caracteres individuais.
      char c = get_char("Do you agree ? ");
  
      // Use aspas simples quando você está comparando caracteres individuais.
      if (c == 'y' || c == 'Y')
      {
           printf("Agreed.\n");
      }

      else if ( c == 'n' || c == 'N')
      {
           printf("Not agreed.\n");
      }


      }

  ## Loops

      while
      {

      } 
* While: Enquanto uma condição for verdadeira, irá ficar em um loop, ou melhor, em ciclo. Repetindo o código nele várias vezes.

      while
      {
           printf("Hello World\n");
      }

  Semelhante a uma estrutura condicional, while está constantemente se perguntando se deve ou não continuar. Semelhante a uma condição com sua própria expressão booleana. Assim, em C, precisa colocar parênteses após a palavra-chave while, e você tem de perguntar algo dentro desses parênteses.

  ##### Mas e se quiser fazer algo eternamente, você só quer que a resposta seja eternamente True, ou melhor, yes. Isso é chamado de loop infinito.


      while (true)
      {
           printf("Hello World\n"); 
      }


 .

E se quisermos fazer algo finitamente, isto é, que não seja feito para sempre. Usá-se um loop "for" ou um loop while até que a condição seja false. 

      int counter = 0; 
      while ( counter < 50 )
      {
           printf("Hello World\n");
           counter ++;
      }
      
Dessa forma como está, irá contar do 0 até 49. Para corrigir isso:

      int counter = 1;
      while (counter <= 50 )
      {
           printf("Hello World\n");
           counter ++;
           
      }

loop for não se trata de uma expressão booleana. Comece dizendo o ponto de partida. Depois, coloque a condição que será verificada repetidas vezes. E a última coisa no parênteses de um loop for é uma autalização, ou uma incrementação ou decrementação pela qual você pode fazer counter = counter + 1

      for ( int counter = 0; counter < 50; counter ++) 
      {
           printf("Hello World\n");
      }

#### Abstração
Este princípio de solução de problemas onde você pode simplificar de outra forma detalhes mais complicados. E a abstração é uma simplificação além de detalhes mais complicados ou detalhes de implementação. 

      # include <cs50.h>
      # include <stdio.h>

      int main(void)
      {
          for (int i =0; i < 3; i++)
          {
              printf("Meow\n");
          }
      }

* Para criar suas próprias funções:

      # include <stdio.h>

      void meow(void)
      {
          printf("Meow\n");
      }

      int main(void)
      {
          for (int i =0; i < 3; i++)
          {
              meow();
          }
      }

Por convenção, normalmente colocamos funções personalizadas na parte inferior do arquivo. Por que ? Somente para quando um programador, ou neste caso, um professor quiser entender seu código de cima a baixo. É apenas uma convenção humana para colocar o programa principal, a função main na parte superior de seu arquivo. 

      # include <stdio.h>

      int main(void)
      {
          for (int i =0; i < 3; i++)
          {
              meow();
          }

      void meow(void)
      {
          printf("Meow\n");
      }

      }



O problema é que quando você fazer isso, você vai ter criado um problema para si mesmo. Lembre-se que o computar fará tudo literalmente como está escrito para ele fazer. E o problema no momento é que quando o compilador ler o código de cima a baixo, à esquerda ou direit, não antes da declaração da função meow, a função meow não existirá. E no entanto, no loop for, a função meow está sendo chamada. Portanto o compilador simplesmente não sabe o que é a função meow, porque não encontrou meow ainda. Para resolver isso: 

    # include <stdio.h>

    // Prototype
    void meow(void);

    int main(void)
    {
        for (int i =0; i < 3; i++)
        {
            meow();
        }

    {
        printf("Meow\n");
    }

    }

É uma espécie de forma inteligente de dizer ao compilador que existirá uma função chamada meow mas que ainda não há mas vai ter. E é uma alternativa bem comum, para resolver esse problema.

    # include <stdio.h>

    int main(void)
    {
        meow(5);
    }
        void meow(void)
        {
            printf("Meow\n");
        }

* void meow (void): O primeiro void refere-se ao valor de retorno ou saída desta função. Resumindo, minha função personalizada meow não tem valor de retorno. Não produz nada por si só, em vez disso apenas tem um efeito colateral de impressão visualmente na tela. Mas tem uma entrada (void). E se você quiser que uma função em C aceite inputs ou argumentos, você pode literalmente fazer algo como:

      void meow(int n )

O nome do tipo que você quer, e o nome da variável que você deseja. Então suponha que eu queira que meow pegue como input algum número, vamos chamar de n. 

        
* Do while: É quase o mesmo que um loop while, exceto wue faz cegamente uma coisa primeiro antes de verificar uma condição. 

