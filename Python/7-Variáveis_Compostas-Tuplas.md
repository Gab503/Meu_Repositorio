# Tuplas

Geralmente, ao atribuir algo a uma variável, por exemplo, lanche recebe suco, e depois fazer lanche recebe macarrão, a variável lanche irá eliminar o item anterior (suco) 
e colocar o macarrão, isto é, uma variável aceita apenas um “atributo” por vez, por isso há as variáveis compostas.

Variáveis compostas podem armazenar vários valores.

Sintaxe da Tupla: Basta colocar em parênteses  e com aspas (ou somente aspas), por exemplo:

        lanche = (‘Suco’, ‘Macarrão’, ‘Arroz’) 
        print(lanche[0]) == suco
        print(lanche[2]) == arroz
        print(lanche) == Suco, macarrão, arroz
Vale ressaltar que tuplas são imutáveis, isto é, não há maneiras de modificá-las.

          lanche = 'Hambúrguer','suco','Pizza','Pudim','Batata frita'
          for comida in lanche:
              print(f"Eu vou comer {comida}")
              
          for cont in range(0, len(lanche)):
              print(f'Eu vou comer {comida} na posição {cont}')
              
          for posição, comida in enumerate(lanche):
              print(f'Eu vou comer {comida} na posição {posição}')

  # Comandos úteis:
.Sorted: vai ordenar a tupla.

.index( ): Em que posição está…
Obs: Caso apareça mais de uma vez o item procurado, irá retornar a primeira aparição.

del( ): Apagar a tupla inteira, não é possível apagar somente um item da tupla.

  
  