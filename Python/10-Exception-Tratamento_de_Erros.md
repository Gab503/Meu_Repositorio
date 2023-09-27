# Exceptions / Tratamento de erros
Erro de sintaxe é um problema com o código que você criou, sua sintaxe. (geralmente falta de aspas ou algo do tipo) 

Try: verificar se há algum erro.

Except: Posso tentar fazer algo, exceto se algo dar errado ( parece com o if elif e else) 

    try:
        x = int(input("What's x ? "))
        print(f"x is {x}")
    except ValueError:
        print("x is not an integer")
Basicamente o código acima diz, se ocorrer o erro de ValueError faça isso.

Name error: O valor de uma variável está incorreto, tende a se referir ao seu código.

Para saber mais sobre possíveis erros acesse a documentação oficial do Pytho.

    try:
        x = int(input("What's x ? "))
        
    except ValueError:
        print("x is not an integer")
    else:
        print(f"x is {x}")

Outro exemplo: 

    while True:
        try:
            x = int(input("What's x ? "))
        except ValueError:
            print("x is not an integer")
        else:
            break
    print(f" x is {x}")


    
