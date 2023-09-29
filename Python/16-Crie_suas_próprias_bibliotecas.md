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
.

    import sys


    # vai ignorar a chamada main, pq está envolvida em uma condicional.
    from teste import hello

    if len(sys.argv) ==2:
        hello(sys.argv[1])


Para criar sua própria biblioteca em Python e colocá-la open source, siga estas etapas:

1. Crie um projeto Python. Você pode fazer isso usando o interpretador Python ou um editor de texto. Se você estiver usando o interpretador Python, digite o seguinte comando:
```
python3 -m venv venv
```
Este comando criará um ambiente virtual chamado `venv`. Em seguida, você pode ativar o ambiente virtual com o seguinte comando:

```
source venv/bin/activate
```

Agora, você pode criar um novo arquivo Python chamado `my_library.py`. Este arquivo conterá o código da sua biblioteca.

2. Adicione o código da sua biblioteca. O código da sua biblioteca pode ser qualquer coisa que você quiser. Por exemplo, você pode criar uma biblioteca que fornece funções para trabalhar com arquivos, trabalhar com datas ou trabalhar com redes.

3. Crie um arquivo `setup.py`. Este arquivo é usado para configurar o seu projeto Python para ser distribuído como uma biblioteca. O arquivo `setup.py` deve conter o seguinte código:

```python
import setuptools

setuptools.setup(
    name='my_library',
    version='0.1.0',
    description='My Python library',
    author='Your name',
    author_email='your@email.com',
    packages=['my_library'],
    license='MIT',
    install_requires=[],
)
```

4. Instale a sua biblioteca. Para instalar a sua biblioteca, execute o seguinte comando no diretório do seu projeto:

```
pip install -e .
```

Este comando instalará a sua biblioteca no ambiente virtual atual.

5. Adicione a sua biblioteca ao GitHub. Você pode fazer isso criando um novo repositório no GitHub e enviando o código da sua biblioteca.

6. Escolha uma licença open source. Existem muitos tipos diferentes de licenças open source. Você pode escolher a licença que melhor atende às suas necessidades.

7. Adicione um arquivo `README.md`. Este arquivo é usado para descrever a sua biblioteca.

8. Adicione testes. Testes são importantes para garantir que a sua biblioteca funcione corretamente. Você pode usar o framework de testes unittest para escrever testes para a sua biblioteca.

9. **Documente a sua biblioteca.** Documentação é importante para ajudar os usuários a usar a sua biblioteca. Você pode escrever documentação em Markdown ou reStructuredText.

10. Promova a sua biblioteca. Você pode promover a sua biblioteca compartilhando-a em fóruns online, comunidades open source e redes sociais.

Aqui estão alguns recursos adicionais que podem ajudá-lo a criar sua própria biblioteca em Python:

* O tutorial do Python Packaging Authority: https://packaging.python.org/tutorials/packaging-projects/
* O guia de estilo do Python: https://www.python.org/dev/peps/pep-0008/
* O guia de documentação do Python: https://www.python.org/dev/peps/pep-0257/



Aqui estão os comandos que você precisará executar para criar uma biblioteca Python:

Criar um ambiente virtual
``python3 -m venv venv``

 Ativar o ambiente virtual
``source venv/bin/activate``

Criar um projeto Python
``mkdir my_library``
``touch my_library/my_library.py``

Adicionar o código da biblioteca
 ...
 
 Criar um arquivo setup.py
``echo "import setuptools" >> setup.py``
``echo "setuptools.setup(..." >> setup.py``
``echo ")" >> setup.py``

Instalar a biblioteca
``pip install -e .``

Adicionar a biblioteca ao GitHub

``git init``
``git add .``
``git commit -m "Initial commit"``
``git remote add origin https://github.com/your_username/my_library.git``
``git push origin master``
