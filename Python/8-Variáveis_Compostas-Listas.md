# Listas
Sintaxe: [ ] or list( )

As listas são mutáveis, isto é, dá de modificar, o oposto de tuplas.

# Manipulação de listas:
## Inserir dados:
.append( ) : Vai adicionar itens no final da lista

.insert( ): Vai adicionar algo em determinada posição, por exemplo,
lanche.insert(0, ‘suco’)

## Deletar Dados:
del( ): Vai apagar determinado item se especificar a posição, ou a lista inteira.

.pop( ): Normalmente o método pop é usado para deletar o último elemento, mas pode passar como parâmetro o índice que você quer deletar.

.remove( ): Não indique o índice que você quer remover, mas sim o valor que você quer remover, por exemplo, lanche.remove(‘pizza’). Isto é, remover pelo conteúdo.

## Ordenar Listas:
.sorted( ): Vai ordenar os valores de uma lista. Para criar uma ordem inversa, basta utilizar o parâmetro reverse, por exemplo, 
valores.sorted(reverse=True).

## Tamanho da lista:
len( ): Vai mostrar o tamanho da lista, vale ressaltar que 0 também será contado.

Para copiar duas listas, basta fazer: [:], por exemplo, a = b[:].

Comprensão de listas: 

        # List comprehension with conditional Statement
        print("List comprehension result: ",end=" ")
        
        # The following list comprehension compacts multiple lines of code into one line:
        print([x for x in range(1,101) if x % 10 == 0])
        
        # the long form version of the code:
        print("\nLong form code result: ",end=" ")
        my_list = [] # or list()
        for x in range(1, 101):
            if x % 10 == 0:
                my_list.append(x)
        print(my_list)