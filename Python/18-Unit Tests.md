# Testes unitários
* Testar seu código usando seu próprio código.

File name: Calculator.py

      def main():
          x = int(input("What's x ? "))
          print("X squared is", square(x))

      def square(n):
          return n * n


      if __name__ =="__main__":
          main()

Crie outro arquivo. File name test_calculator.py

    from teste import square

    def main():
        test_square()


    def test_square():
        if square(2) != 4:
            print("2 square was not 4")
        if square(3) != 9:
            print("3 square was not 9")


    if __name__ == "__main__":
        main()

Se ao executar tes_calculator.py e não aparecer nada no terminal, isso é um bom sinal, significa que seu código funcionou como desejado.

* assert: assert é uma palavra chave em python e também em algumas outras linguagens,
 que permite que você faça exatamente isso, como em inglês, para afirmar que algo é verdadeiro.
 E se não for, nada vai acontecer. Ou melhor, aparecerá um assertonError.

      from teste import square

      def main():
          test_square()


      def test_square():
          assert square(2) == 4
          assert square(3) == 9


      if __name__ == "__main__":
          main()

* AssertionError, para tratar esse erro, podemos utilizar tratamento de erros, isto é, try and except.

      from teste import square

      def main():
          test_square()


      def test_square():
          try:
              assert square(2) == 4
          except AssertionError:
              print("2 square was not 4")
  
          try:
              assert square(3) == 9
          except AssertionError:
              print("3 square was not 9")
  
          try:
              assert square(0) == 0
          except AssertionError:
              print("0 square was not 0")

          try:
              assert square(-2) == 4
          except AssertionError:
              print("-2 square was not 4")
  
          try:
              assert square(-3) == 9
          except AssertionError:
              print("-3 square was not 9")

      if __name__ == "__main__":
          main()

  
* Pytest: Pytest é um programa de terceiros que você pode baixar e instalar e que automatizará o teste do seu código, desde que você escreva os testes. Esta biblioteca adota algumas convenções para que você não precise escrever tantas linhas de código manualmente. Eles fazem parte disso automaticamente para você. Existem outras bibliotecas para testes unitários, que testam unidades do seu código. Mas o pytest é um pouco mais simples.

* O teste unitário é apenas uma forma formal de escrever o teste de unidades indivíduais do seu programa. Essas unidades indivíduais são as funções. 

Portanto, os teste unitários são normalmente testes para funções que você escreveu. 

Documentação do Pytest: https://docs.pytest.org/en/7.4.x/ 

Para instalar, digite no terminal pip install pytest


