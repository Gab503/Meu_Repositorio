# Criando suas próprias bibliotecas

Uma boa prática seria agrupar de alguma forma aquele código que você continua reutilizando e criar seu próprio módulo ou pacote Python. Você pode mantê-lo localmente em seu próprio computador ou servidor em nuvem. Ou você pode seguir as etapas de agrupá-los, torná-lo gratuito e de open source e colocá-lo em algo como PyPi, para que outros possam usar também.

def main():
    hello("World")
    goodbye("World")


def hello(name):
    print(f"Hello {name}")
def goodbye(name):
    print(f"Goodbye {name}")

#__name__ esta variável é um símbolo especial em Python, cujo valor é automaticamente definido pelo Python como "main", quando você executa um arquivo na linha de comando como executando o Python de teste.py .O conteúdo dentro da estrutura if__name__=="main" só vai ser executado quando você executar o código diretamente, ou seja, se importar e executá-lo por um código secundário, ele não vai aparecer.
if __name__ =="__main__":
    main()


import sys


# vai ignorar a chamada main, pq está envolvida em uma condicional.
from teste import hello


if len(sys.argv) ==2:
    hello(sys.argv[1])