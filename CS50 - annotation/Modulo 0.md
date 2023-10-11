* What ultimately matters in this course is not so much where you end up relative to your classmates but where you end up relative to yourself when you began

* O que importa neste curso não é tanto onde você termina em relação aos seus colegas de classe, mas onde você termina em relação a si mesmo quando começou.

## O que é exatamente Ciência da Computação ?
Resposta: Resolver problemas.

Os dígitos decimais, ou base decimal, são 10 dígitos que nós usamos regularmente, 0, 1, 2, 3, 4, 5, 6, 7, 8, 9. Usando estes dígitos podemos obter qualquer número, 11, 45, 5000, ou qualquer outro que quisermos. 

* Mas os computadores não falam a mesma lingua que nós. Em certo sentido, eles são mais simples do que nós, apesar de parecerem complicados ou sofisticados e muito rápidos, mas no fim das contas, são dispositivos criados pelo homem, ele são relativamente simples em sus essência.

* Qual linguagem que os computadores falam ?

Sistema binário. É chamado assim, pois há apenas dois dígitos, 0 e 1, também conhecido como bits. Os computadores fala em binário, usando estas coisas chamadas bits.
O que os computadores usam como input (entrada) é apenas a eletricidade. Provalvemente a única coisa que todos nós fazemos diariamente, ou quase, com nosso laptop ou desktop, ou telefone, é certificar-se de que ainda está plugado na tomada, ou então carregando.

Portanto, o único input físico para nossos dispositivos hoje em dia é a eletricidade, de alguma forma. E assim, se aproveitamos esta eletricidade, talvez nós possamos começar a representar informações com ela. Um bom exemplo é uma lâmpada, se você permitir que a eletricidade flua, ligando um abaju na tomada ou apertando o interruptor, ela irá acender, e se desconectar seu abaju da tomada, irá desligar. 

A implicação desta ideia é muito simples. Podemos pegar um dispositivo físico, como uma única lâmpada, e ao plugar ou desplugar, podemos representar a informação, ligar, ou desligar. Podemos chamar esse comportamento de 0 e 1. Esse é o germinar de uma ideia, que nos deu computadores, e com ele, seu uso do sistema binário. 

* No fim das contas, tudo que os computadores têm é o input físico como eletricidade, vamos usar isso para manter um registro de informação. Vamos armazenar um pouco de eletricidade quando quisermos representar 1, e vamos deixar essa eletricidade pra lá, sem armazenar, quando quisermos representar um 0 em seu lugar. E é assim o input de computadores, nos dando os 0 e 1, que usamos hoje em dia.

* Há um pequeno problema, se tivermos apenas uma lâmpada ou um interruptor, se estiver desligada, pode ser 0, e se estiver ligada pode ser 1. Mas e se eu quiser contar mais do que 1, por exemplo, 5 ?

Bem, eu poderia, é claro, usar mais lâmpadas. E se utilizarmos três lâmpadas até qual número poderiamos contar ? <br>
Assim, com uma lâmpada, podemos contar de zero a um, duas possibilidades. Mas com três lâmpadas, até que ponto poderiamos contar ?

Inicialmente as três lâmpadas representam 0, pois estão desligadas. Ao ligar uma teremos 1, em seguida, 2 e por fim 3. Bem, não é bem assim.<br>
* Porque está errado ?

Bom, a resposta é 8 no total. Os cientistas da computação e os computadores, normalmente começam a contar a partir de zero, só porque faz sentido, porque quando tudo está desligado então você também pode chamar de zero. Portanto, se começarmos a contar do zero, temos 8 padrões possíveis. Isso permitiria que contássemos até sete. Então 7 é o mais alto que podemos contar com três lâmpadas. 

##### Pra entender a lógica por trâs: Vamos chamar as lâmpadas de A B e C. então teremos:
* A-0 B-1 C-2.
* A-3 B-4 C-5.
* A-6 B-7 C-8.

No mundo da informática, por conversão, comece a contar a partir de 0. Mas está correto dizer que há 8 possibilidades possíveis. 

##### Mas como podemos realmente chegar a esses 0 e 1  que o computador usa ?

Porque o que está dentro de um computador, no fim das contas, não são lâmpadas, mas pequenos e minúsculos interruptores, milhões de pequenos interruptores que podem ou ter status de ligado, 1, ou deligado,0.

* Esses interruptores são chamados de transistores.
E hoje em dia os computadores têm milhões deles, podendo estarem ON e OFF, em padrões diferentes.
O que podemos afirmar sobre representação, quando se trata de usar esses interruptores ? Como vamos representar informações com eles ?

Não precisa pensar muito nisso, nem voltar às origens das coisas. Se considerarmos por um momento, não apenas 0 e 1, mas o sistema decimal inteiro, de 0 a 9. 

* Como funciona esse sistema ?

123 ( não é cento e vinte e três!!! ). Três dígitos. Vamos considerar que cada um destes dígitos ou símbolos representam. o 3 é unidades, o 2 é dezenas, e o 1 é centena. E assim, Como chegamos destes três símbolos ou dígitos, 123, para a ideia matemática de "cento e vinte e três" ? <br> Automaticamente respondemos que 100 * 1 ( o símbolo * é igual a vezes ) + 10 * 2 + 1*3, que é o mesmo que 100 + 20 +3, ou o valor que conhecemos como cento e vinte e três. 

Bem, acontece que no mundo dos computadores, o sistema que eles usam é exatamente o mesmo. A única diferença é que os computadores só têm acesso a 0 e 1, não zero até nove. Se considerarmos agora, apenas três digitos possíveis representados por #(100) #(10) #(1), vamos considerar por um momento por que essas colunas são lugares de números de 1, 10, e 100, e assim por diante. o porquê dessa forma, é que havia um padrão, e isso apenas tem a ver com expoentes ou multiplicação. 

Portanto a coluna mais à direita, tecnicamente, é:
* 10 na potência de zero 10°, que é igual a 1.
*  O do meio é 10¹, que é apenas 10.
*  e 10² (ao quadrado) que é 100.

##### Percebeu algo ? é basicamente elevado a 0 1 2.
O que é interessante sobre esse tipo de representação é que ela intuitivamente nos diz que o 10 está envolvido. Há 10 dígitos, de zero a nove, portanto as colunas estão usando esta base de 10. Considerando que, se no sistema binário que os computadores usam você tem dois dígitos, 0 e 1, provavelmente a única coisa que vai mudar é o significado dessas colunas.  #(2²) #(2¹) #(2°) 

Se nós fizermos essas contas apenas, no mundo bibário, que os computadores utilizam, temos os lugares 1,2,4 e assim por diante

#### Voltando as três lâmpadas:
* A 2² -> 4
* B 2¹ -> 2
* C 2° -> 1
* Somando tudo temos 7. Observação, 2 é a quantidade de dígitos, ou melhor, código binário, 1 e 0.

Podemos considerar que se todas as lâmpadas estão desligadas, vamos começar novamente como zeros. Então, isso seria um padrão de símbolos ou dígitos que são 000 binários. 
Mas em nosso mundo humano, a matemática mental que você aplica instantaneamente, seria é claro, que 4 vezes 0 mais 2 vezes 0 mais 1 vezes zero -> 4 * 0 + 2 * 0 + 1 * 0, ou é claro, zero em decimal. 

##### Mas como um computador representa o número 1, por exemplo ?
Bem, isso é só mudar o bit mais à direita, de o até 1, "ligando a lâmpada mais à direita":
* Vai ser 001 em binário. Lembre-se 4 2 1 -> 001
  
Como represento o 2 ?

* Vai ser 010 em binário.
  
Como represento o 3 ?

* 100 ? Errado !!! 
  
Para representar o 3 é:
* 011  Lembre-se 4-2-1 o número três é 2 +1, ou 011 -> 02+1
  
  Lembre-se das posições 4-2-1

Agora há dois interruptores, porque eu preciso de algo nos lugar do 2 e do 1, que me retorne matematicamente o 3. Se formos em frente e escolhermos contar até 4, vai resultar em 100 (4+0+0) 

Se eu quiser contar até cinco, será 101. (4+0+1)

Seis será 110 (4+2+0)

Sete 111 -> 4+2+1

* Portanto, parece que usando três bits, onde cada um pode ser 0 ou 1, você pode permutá-los ("combinações possíveis) de 8 maneiras diferente. Duas possibilidades para as primeiras vezes Duas para as segundas vezes e Duas para as terceiras vezes, você pode permutá-los de oito maneiras diferentes. Lembre-se de começar a contar do 0.

  * Espaço amostral = { (1.1) (1.2) (1.3) (2.1) (2.2) (2.3) (3.1) (3.2) (3.3)} Lembre-se de começar a contar pelo 0. Espaço amostral é o conjunto formado por todos os resultados possíveis de um experimento aleatório. Pense como se tivesse dois dados, ao jogá-los, pode cair um dado com o número 1, e outro também com o número 1, ou um com o número 1, e outro com o 2, um cair 1 e o outro 3, um cair 2 e outro 1, assim por diante.
 
##### E se houver mais do que três lâmpadas ?

* Qual número este binário representa 110010 ? 
 
A resposta é 50. Lembra dos lugares 4-2-1 ? É so apliar um pouco mais. 1-2-4-8-16-32...
Portanto, 110010 é o mesmo que 32 + 16 + 0 + 0 + 2 + 0 = 50.

Parece que a única coisa que os computadores podem fazer é computar. Ou seja, comportar-se como calculadoras. E na verdade, isso é exatamente o que os computadores foram projetados para fazer, para facilitar a matemática de cálculos que, de outra forma, era bastante entediante ou impossível para os seres humanos. Mas obiviamente os dispositivos de hoje em dia são muito mais sofisticado. 

##### Como os computadores poderiam representar não apenas números, mas letras do alfabeto ?
Podemos atribuir os números específicos em binário a letras do alfabeto. A letra A maiúscula por exemplo é 65, ou melhor -> 01000001.( 0 + 64 + 0 + 0 + 0 + 0 + 0 +1)
Portanto, este é o padrão de bits que um computador usa para representar o decimal 65, e agora o que o computador está fazendo é apenas estar atento ao tipo de programa que você está usando. 

Se você estiver usando uma calculadora ou talvez usando algo como Excel para jogar número, bem, nesse contexto ao executar o software, como uma calculadora ou uma planilha de cálculo fazendo análise númerica, o programa vai ser dentro do hardware do computador o padrão de interruptores que representa o número decimal 65. E porque está no contexto de uma calculadora ou planilha de cálculo, o que você, o humano, pode ver na tele literalmente o número decimal 65. Mas se você estiver usando mensagens de texto ou e-mails ou qualquer aplicativo de mídia social, onde estamos nos comunicando não numericamente, mas em letras, nesse contexto, seu computado vai ser inteligente o suficiente para conhecer esse mesmo padrão de bits que representam 65, no contexto de uma mensagem de texto ou em um e-mail ou similiar, realmente representa a letra maiúscula A.

Portanto, o padrão é o mesmo.

* O sistema que nós criamos que mapeia 65 para A, 66 para B, 67 para C, é chamado ASCII, o padrão americano de código de Intercâmbio de Informações.

* ... A 65
* B 66
* C 67
* D 68
* E 69
* F 70
* G 71
* H 72
* I 73 ...

Há um mapeamento completo, também para pontuação, para letras minúsculas, símbolos etc.

Supondo que você recebeu uma mensagem de texto contendo um padrão de bits, ou na verdade, apenas uma sequência de números decimais que seja assim: 72, 73,33. Suponha que você tenha recebido uma mensagem de texto contendo estes padrões de números. 

##### Qual mensagem você acabou de receber ? 
Resposta: Hi! ->  01001000 01001001 0100001. Portanto, temos, 8 bits + 8 bits + 8bits, o que significa que, para receber a mensagem HI!, você está enviando ou recebendo 24 bits ao todo.

##### Vale ressaltar que o ANCII é o padrão americano, existem diversos outros, como por exemplo o brasileiro, é UTF-8.

Mas, os bits não são uma unidade de medida muito útil, normalmente por serem muito pequenos. Apenas 0 e 1. Mas cada um destes padrões (HI! 8 + 8 + 8 = 24 bits) de 8 bits, na verdade tem um vocabulário, se você preferir, que é bytesm neste caso 8 bits é 1 bytes. 
Geralmente usamos no contexto de magabytes ou gigabytes. Quando você fala sobre o tamanho de seus arquivos hoje em dia, você está falando em bytes, em alguns milhões ou bilhões de bytes. Mas cada um desses bytes, de forma simples, é um padrão de oito 0 e 1. 

Com 8 bits, no ANCII, você pode  representar 256 possibilidades de símbolos, entre eles letras minúsculas, maiúscula, pontuação etc. Basta fazer as contas, se você tiver 8 bits, cada um do quais pode ser 0 ou 1, isso significa que você tem duas possibilidades para o primeiro, vezes duas possibilidades para o segundo, vezes duas vezes dois. Acontece que são 2 até 8, ou 256. 

Até mesmo os emojis são na verdade padrões de 0 e 1. Estes são apenas caracteres em um alfabeto, o alfabeto emoji. 

* Hoje em dia, existe um sistema chamado Unicode, que os humanos elaboraram suportando não apenas o inglês, mas também todas as linguas humanas, que é a meta aspiracional, de forma escrita e impressa, ou mesmo eletrônica é o objetivo.

Por exmplo o emoji de chorando de alegria ( ou de rir ) 😂, o decimal que o representa é 128.514. 
Você está tecnicamente apenas enviando um padrão de bits assim: 000000011111011000000010

##### Como um computador registra cores ?
Você apenas atribui números para diferentes cores.

Há diferentes maneiras de fazer isso, acrônimos RGB, o RGB representa o vermelho, verde e azul, podemos conseguir cada cor do arco-íris misturando alguma quantidade de vermelho, verde e azul. Portanto, isso nos leva a perguntar como representamos a quantidade de vermelho, verde ou azul, e nós temos os bits à nossa disposição. 

Suponha que recebemos um padrão de bits, 72, 73, 33 novamente, mas desta vez não é um e-mail, nem uma mensagem de texto. Está no contexto de um arquivo aberto no Photoshop. O que isso está representando neste caso ?

No contexto de um e-mail ou uma mensagem de texto, ainda é HI!, Mas no contexto de Photoshop ou Instagram ou qualquer coisa que seja orientado em torno de  imagens, na verdade, ele vai representar uma quantidade de vermelho, alguma quantidade de verde e azul. O número total de possibilidades que você pode representar com 8 bits é 256. O valor mais alto que você pode representar é 255, se começarmos a contar a partir de zero. Então isso quer dizer que cada um destes três números (72, 73, 33) é um número entre 0 e 255. 

Portanto, 72 parece ser uma quantidada média de vermelho, 73 é como uma quantidade média de verde, e 33 é um pouco de azul. E se você combinar essas três quantidades de cor, 8 bits mais 8 bits mais 8 bits, usando um total de 24 bits, você te, um ponto que se parece com um ponto amarelo. Quando o emoji aparece na tela, é o resultado da interpretação do computador do valor de 128.514. Mas quando se trata de exibir informações na tela, o seu computador vai usar diferentes padrões de bits para controlar as cores dos pontos na tela. 

Os pontos que você e eu vemos em nosso computador, nas telas de celulares, ou mesmo nas TVs são chamados pixels.
São quadradinhos minúsculos que representam alguma cor, se você der bastante zoom em uma imagem, verá o que chamamos de pixelação. E é grande a chance de você já ter visto isto no Facebook, Instagram, onde quer que você esteja redimensionando ou editando fotos que não são bem exemplos de boa resolução. 

A resolução de uma imagem é quantos pixels ou pontos há horizontalmente e verticalmente. Portanto, se você realmente ampliar uma imagem, você eventualmente verá esses pixels. Um pixel está usando, 24 bits ou três bytes. Agora você pode imaginar que, provavelmente, há centenas, talvez milhares de pontos nessa imagem, se desfizermos o zoom e olharmos para o todo novamente. 

Então se cada um desses pontos ou pixels é de três bytes, é por isso que as fotografias que eu e você tiramos e as imagens que você e eu baixamos da internet geralmente não são medidas nem mesmo em bytes, por si só, mas em Kilobytes, por milhares de bytes, ou megabytes por milhões de bytes, ou se for um arquivo de vídeo, ele pode ser ainda maior, bilhões, ou gigabytes. 

##### Como os computadores representam arquivos de vídeo ?
Se você apenas continuar mudando as cores desses pontos uma vez por segundo ou um monte de vezes por segundo, nós teremos a ilusão de uqe há realmente movimento na tela, um vídeo.

Portanto, realmente, um vídeo, em algum sentido, é apenas um monte de imagens voando atráves da tela muito rapidamente ( semelhante a Stop Motion) 

##### Como os computadores representam as musicas ?
Poderia ser representada de diferentes maneiras, como, se você toca um piano, por exemplo, talvez você saiba que existem notas como A até G. Mas também há sustenidos e bemol, e assim por diante. Talvez precisemos apenas de um número para representar cada uma dessas notas possíveis. E talvez também pudéssemos usar outro número, assim como as imagens utilizam múltiplos números para representar os pontos, poderíamos usar um número para representar as notas de uma canção, mas também outro número para representar a duração dessa nota. Quantos segundo ou milissegundos ou batidas você deve ouvir com tal nota. 
Para que você pudesse inventar outras formulações, também, mas a música, na verdade, pode ser quantificada no mundo dos computadores em apenas pequenos trechos de informação. E desde que você e eu concordemos sobre como representá-la, é assim que todas essas coisas funcionam. 

E se você já se perguntou por que há JPEGs e PNGs e GIFs e Word documents e arquivos Excel e todos os diferentes formatos de arquivos ou ainda extensões em computadores, ou formatos de arquivos apenas que representam um grupo inteiro de humanos concordando como armazenar padrões de 0 e 1 em um arquivo de modo que quando esses 0 e 1 são carregados em um computador para exibição ou para interpretação, ele sabe o que esses padrões representam. 

As imagens são representadas de forma um pouco diferente, som e vídeo são representados um pouco diferente. Mas é tudo 0 e 1 no fim das contas. 

* Portanto, tudo isto é para dizer, que desde que nós concordemos com padrões, mundialmente, para representar a informação, agora podemos representar inputs para o problemas e, esperemos resolver problemas e ober resultados.
Portanto, tudo o que resta na solução de problemas, ou, na verdade, informática de modo geral, é olhar dentro desta caixa ( do seu computador) e considerar a forma como você recebe os inputs, se são números, cartas, imagens, vídeos, som, e convertê-los em soluções reais.
E assim em seu computador, é o que normalmente faríamos, que é descrever como algoritmos.

* Algoritmos são instruções passo a passo para a solução de problemas. Eles não têm que sequer envolver computadores. Nós humanos, podemos executar algoritmos apenas seguindo as instruções de outra pessoa. Se você já preperou algo de um livro de receitas, seguindo uma receita, você está executando um algoritmo passoa a passo.

Mas ao contrário de muitas receitas ou, ao contrário de muito tipos de intruções que nós humanos damos uns aos outros, não há espaço para ambiguidade nos computadores. 
Algoritmos dos computadores, quando implementados por máquinas, realmente têm que ser corretos não apenas ter os outputs(saídas / "resultados") com que você se importa de forma adequada,  mas eles também precisam ser precisos. 

Você precisa ser muito preciso, porque ao contrário de nós humanos, que podemos gostar de ler nas entrelinhas, e dizer sim eu entendo o que você quis dizer, os computadores vão entender tudo ao pé da letra. 
E assim, ao programar um computador, ou seja, traduzindo um algoritmo, instruções passoa a passo, em alguma linguagem que o computadot entenda, o cuidado é de assegurar que o computador não pode interpretar errado o que você qur.

Vamos considerar um desses algoritmos. Em todos os nossos telefones, independente se é android ou IOS ou similare, você tem alguns apps de contatos. Nesses apps, provavelmente estão armazenados os contatos de todos os seus amigos e familiares e colegas, provavelmente em ordem alfabética. Talvez pelo primeiro nome, talvez pelo sobrenome, ou no entanto você organizou esse dispositivo personalinazadamente. Bem a versão old school disso é em forma de papel, como uma agenda telefônica, e dentro de uma agenda telefônica old scholl a ideia é a mesma. Porém maior, impresso e pesado. Há um monte de nomes e números em uma lista telefônica típica, ordenada alfabeticamente, assimo como em seu telefone também faz.

Portanto, suponha que queiramos resolver um problema. E a contribuição para esse problema é não apenas esta lista telefônica, mas também o nome de alguém para procurar o número. Seu próprio nome por exemplo, se eu quiser pesquisar meu número de telefone, você pode abrir a agenda e começar a procurar pelo nome, por exemplo, David, partindo do princípio qe está ordenado pelo primeiro nome. E você procura em cada página da agenda pelo nome David.

##### Este algoritmo, girando as páginas, passo a passo, na procura por David está correto ?  verificando cada página  ?
Parece que o algoritmo está de fato correto, mas é terrivelmente lento, mais muito lento mesmo. Porque não buscar duas página por vez,ou mais, dez,  é mais rápido. 

#### Este algoritmo está correto ?
sim, mas pode acabar passando o nome. Um pequeno bug.

Não temos que sacrificar a ideia de agilizar este algoritmo, movendo-se duas vezes mais rápido. Basta acessar uma página e ver as iniciais dos nomes, ao abrir uma página e tiver o nome Alexandre por exmplo, pule a página pois esta página contêm apenas nomes que comecem com a letra A. Mas ainda assim seria lento. Imagine verificar as iniciais de cada página de uma uma agenda telefônica de 2000 páginas

* Bug: É apenas um erro em um programa, ou um engano, geralmente em um algoritmo.

* Para resolver esse bug: Você pode dividir o problema ao meio, literalmente, por exemplo, o nome David, começa com  aletra D, se você abrir a agenda telefônica no M, descarte tudo do M e diante, porque D vem antes de M, reduzindo as possibilidades. Jogando metade do problema fora. E refaça novamente reduzindo as possibilidades. Suponha que a agenda tenha 1000 páginas, Reduzindo as possiblidades, fica 500 páginas, novamente, 250 páginas, novamente, 145 páginas, e de novo, 72,5 (desconsidere esse ,5 se preferir para deixar mais simples) de novo, 36, e de novo, 18, 9, 4.5 , 2, e por fim resta uma página apenas.

##### Percebeu ? levou apenas 10 páginas totais para achar a resposta. 1000-500-250-145-72-36-18-9-4.5-2
Ao fazer um algoritmo, não pense apenas em como ele funcionara, mas também em sua eficiência. Considere os exemplos acima.
1. Verificaria cada página para achar o nome.
2. O segundo pularia de duas em duas páginas para achar o nome, mas, há a possibilidade dele pular a página que está o seu nome.
3. E o terceiro reduzria o problema diversas vezes até achar o nome, sendo necessário neste exemplo, apenas a verificação de 10 páginas.

##### Percebeu a economia de tempo ? Se ainda não, imagine relizar esses mesmos algoritmos, com uma agenda telefônica de um estado inteiro. Quantas semanas ou até messes, ou anos demoraria com o 1 e 2 algoritmos ? Considerando que você é somente uma pessoa para verificar milhões de telefones tentando achar um em específico. E se usar o 2 algoritmo corre o risco de pular o nome e o número de quem está procurando, e só perceber após verificar todos os milhões de números. Os três algoritmos são válidos, não estão errados, mas o terceiro é mais eficiente. Por exemplo, um estado com 2 milhões de pessoas, usando o terceiro algoritmos seria assim: 2.000.000 -> 1.000.000 -> 500.00 -> 250.000 -> 145.000 -> 72.500 -> 36.250 -> 18.125 -> 9.062,5 -> 4.531,25 -> 2.265,62 -> 1.132,81 -> 566.40 -> 283.20 -> 141.60 -> 70.80 -> 35.40 -> 17.70 -> 8.85 -> 4.42 -> 2.21 -> 1 
21 páginas no total até chegar na resposta. 

* Portanto, quando se trata de programação, agora precisamos traduzir estas coisas chamadas algoritmos, para codificar. Ou neste cada, vamos chamá-lo de pseudocódigo. 

* O que foi feito pode ser traduzido verbalmente em psudocódigo, que é como um algoritmo implementado em qualquer que seja a sua lingua falada ou escirita. Mas a chave é que tem que estar correto, e, idealmente, é melhor ser preciso para que não haja ambiguidade.

1. Passo um, **pegar** a lista telefônica.
2. Passo dois, **abrir até** o meio da lista telefônica.
3. Terceiro passo **ver a** página.
4. *Se* a pessoa está na página.
5. **Ligue** para a pessoa. Problema resolvido
6. *Senão se* a pessoa não está na página, se a pessoa está no início...
7. **Abrir o** meio da metade da esquerda.
8. volte a linha 3.
9. *Senão se* a pessoa estiver mais ao final da lista..
10. **Abrir o** meio da metade da direita.
11. volte a linha 3.
12. *Senão*... (se a pessoa não estiver na lista)
13. **Sair.**

Há 4 cenários possíveis neste pseudocódigo:
1. Achar a pessoa logo ao abrir.
2. Achar a pessoa na metade direita.
3. Achar a pessoa na metade esquerda.
4. Não achar a pessoa.

#### Você deve ter notado que algumas palavras estão destacadas, são verbos ou ações que fazemos com esta lista telefônica. Estes são, em programação, as funções.

* Uma função é uma ação ou verbo. É um declaração que o computador recebe para fazer algo.

* Em seguida, temos destacado ( se, senão se, senão) o que chamaremos de condições de brances. Estas são mais ou menos as bifurcações na estrada. Pode seguir por esse caminho ou por esse outro. São chamados de *estruturas condicionais.*

Mas como decidir qual caminha seguir  ?

*  Para isso, precisamos de algo chamado expressões booleanas. Uma expressão booleana é apenas uma pergunta cuja resposta seja sim ou não, ou verdadeiro (True) ou Falso (False), 1 ou 0. Por exemplo, Se está condição for verdadeira faça isso. 

*  Volte a linha 3. Isto vai induzir o que nós chamamos de loop ou ciclo, que é apenas uma construção de programa ou de um algoritmo que faz com que você faça algo repetidas vezes para que você não precise escrever um algoritmo com muitas linhas. Você pode escrever um pequeno algoritmo e reutilizar partes dele repetidas vezes.

       # include <stdio.h>
       int main(void)
       {
           prinf("Hello, world\n");
       }
Acima está um exemplo de uma língua chamada C. Esta é a linguagem mais antiga, baseada em texto, em teclado. Mas esta linguagem é um pouco críptica. À primeira vista, você pode se perguntar por que o símbolo hash ( # ) está ali, os parênteses angulares, os parênteses, as chaves, o ponto e vírgula, as aspas etc. Este programa imprime a mensagem Hello world. 

Por outro lado o scratch é menos complexo, amigável, muito mais gráfico, que nos permite explorar estas mesmas ideias e preparar o cenário para linguagens mais sofisticadas, mais tradicionais adiante; mas no contexto onde não temos que nos preocupar com parênteses, ponto e vírgula, chaves, etc. 

* https://scratch.mit.edu/

É baseado na web, mas há também uma versão offline. Á esquerda da tela ( ao acessar o Scratch) estaráo todos os blocos de construção que vêm com o scratch, semelhante a peças de quebra-cabeça.  

* Abstração é uma solução de problemas, uma técnica que é realmente apenas uma forma extravagante de dizer, vamos ter uma ideia muito complicada, ou uma ideia um pouco complicada e simplificá-lo de tal forma que nós todos concordemos que você pode implementá-la da maneira complicada, mas vamos agora apenas estipular que vamos pensar nela em um nível mais simples.

* Uma prática recomendada para ter em seus códigos, é fazer com que o código seja autodescritivo, sem precisar de comentários.
