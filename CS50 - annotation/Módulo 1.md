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

* Uma função é como um miniprograma. É uma ação ou um verbo que você pode usar ao escrever seu próprio programa que faz algo. No scratc há por exemplo Say (dizer).
As funções também podem ter inputs, re-chamadas. Agora, vamos começar chamando inputs para argumentos de funções por assim dizer. Outro termo para isso é parâmetros. Mas são sinônimos. Os argumentos são as inputs para as funções.

No scratch, por exemplo, Say Hello World

Em c, printf("Hello World")






