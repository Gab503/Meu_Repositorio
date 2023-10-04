# Style
###  PEP 8:
Proposta de Aprimoramento do Python, é um conjunto de propostas que a comunidade dentro do mundo do Python normalmente gera não apenas para propor novas ideias, mas também para codificar certos padrões. 
E o PEP 8 é uma proposta que padronizou, ou melhor tentou padronizar, a aparência do nosso código, ou seja, é bem possível escrever um código que não seja apenas correto, mas que possa até ser bem projetado, mas é realmente uma bagunça, e simplesmente não parece bom, não é bonito, portanto é mais difícil de ler. Portanto, não é sustentável. 

Algo difícil de ler + Menos sustentável = Aumentando a probabilidade de introduzir bugs.

##### O que significa ter um boa aparência no mundo da programação de códigos ?

 https://peps.python.org/pep-0008/ tenta padronizar uma série de detalhes que seriam manifestados em seu próprio código uma vez que você escrevesse uma série de linhas.
Tenta padronizar a aparência dos códigos de todos.

Indentation - 4 espaços
Tabs or Spaces ? - Spaces
Maximum Line Length. 
Blank Lines
Imports
…

 ### Pylint
É um exemplo do que é geralmente conhecido como linter, que é um programa que analisa estaticamente, isto é, lê seu código de cima para baixo, da esquerda para a direita e tenta descobrir se há erros potenciais nele, ou pelo menos inconsistências com algo como um guia de estilo prescrito.

para instalar: pip install pylint
pycodestyle anteriormente conhecido como PEP 8, é um programa que você não só pode executar em seu computador, documentado em http://pycodestyle.pycqa.org, mas  também cuidará do processo de reformatação de seu código para você, se for um pouco bagunçado. Ou seja, se o estilo do seu código, seu recuo e linhas em branco e outros detalhes também não estiverem de acordo com o guia de estilo, algo como pycodestyle irá consertar isso para você. 

### black:
 Uma outra alternativa, black é um programa que você também pode instalar com pip install black, e está documentado nesta URL http://black.readthedocs.io  A etimologia do nome black é na verdade uma alusão a Henry Ford, que inventou os carros,  e só vendeu modelos pretos dos mesmos, ele é conhecido por dizer uma citação nesse sentido: “Qualquer cliente pode ter um carro pintado na cor que quiser, desde que seja preto.” É muito comum, que as empresas tenham sua própria preferência de estilo, de recuo, de linhas em branco etc, pior ainda, cada equipe ter sua própria preferência, seria uma bagunça. 
Esse formato específico, chamado de black, é teimoso no sentido de que toma muitas dessas decisões por você. E se você não gosta da maneira como o black está formatando seu código, é assim que vai ser feito sem margens para negociação. 
