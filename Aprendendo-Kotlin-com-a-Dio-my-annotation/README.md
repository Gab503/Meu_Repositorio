# Programação Orientada a Objetos em Kotlin
https://play.kotlinlang.org/ IDE online de Kotlin ( um lugar online para rodar os códigos)

Documentação oficial: https://kotlinlang.org/

Um paradigma de programação é definido pela maneira como um determinado programador resolve um certo problema, 
fornecendo visão e determinando como o programador estrutura e executa este programa. De certa forma, é uma receita de como 
uma pessoa pode resolver um problema.  

Os quatro principais paradigmas de programação são: paradigma imperativo, declarativo, funcional e orientado a objetos.
A diferenciação entre os paradigmas de programação é feita através das técnicas que estes mesmos paradigmas permitem ou proíbem.

    fun main()
    {
        printf("Hello World !")
        
    }

**Para que serve os Paradigmas:** Reutilização de código. Os paradigmas da programação iram ajudar a reutilizar um código já escrito, com um modelo de como fazer várias coisas com um mesmo código. 

* Programadores devem buscar não gerar bugs (erros no código), escrever seu código e o reutilizar, escrever códigos limpos,
isto é, lembrar que outra pessoa ( ou você futuramente) poderá ler seu código e também que o computador possa entender e saber o que fazer.



**Princípios da POO (Programação Orientada a Objetos):** 

**Classes:** Em programação Orientada a Objetos (POO), uma classe é uma estrutura fundamental que representa um tipo de objeto. Ela é um modelo ou plano para criar objetos.

**Objetos:**É uma instância de uma classe. Um objeto é uma entidade concreta que existe em tempo de execução e possui valores específicos para seus atributos. uma instância (ou objeto) está "conectada" à classe a partir da qual foi criada. Ela herda as características e comportamentos definidos pela classe, mas pode ter valores específicos para seus próprios atributos.

**Instância:** Um objeto concreto criado a partir do uso de uma classe é chamado de instância dessa classe. Por exemplo, se temos uma classe "Cachorro", uma instância seria um cachorro específico, com características e comportamentos específicos.

**Atributos:**Uma classe define atributos que são características ou propriedades dos objetos dessa classe. Por exemplo, se estivermos falando sobre uma classe "Carro", os atributos podem incluir cor, modelo, ano de fabricaçãom etc.

**Propriedades:** O termo "propriedades" é muitas vezes usado de forma intercambiável com "atributos". Em alguns contextos, "propriedades" pode ser usado para se referir especificamente aos atributos de uma classe que têm métodos associados, chamados de "métodos de propriedade". Esses métodos são usados para obter ou definir o valor de um atributo e podem incluir lógica adicional.

**Métodos:** Além dos atributos, uma classe também define métodos. Métodos são funções ou procedimentos que podem ser executados pelos objetos da classe. No contecto "Carro", métodos podem incluir "ligar", "deligar", "acelerar", etc. Em termos simples, os métodos são ações que um objeto da classe pode realizar.


* Encapsulamento.

Esse conceito refere-se à capacidade de uma classe de ocultar a implementação interna e expor apenas uma interface bem definida. Em outras palavras, os detalhes internos de como uma classe realiza suas operações são encapsulados, tornando mais fácilo para outros desenvolvedores utilizarem a classe sem precisar entender todos os detalhes internos.
  
* Herança

Uma classe pode herdar características (atributos e métodos) de outra classe. A classe que é herdada é chamada de classe pai ou classe base, e a classe que herda é chamada de classe filha ou subclasse. Isso promove a reutilização de código e facilita a organização hierárquica de classes.
  
* Abstração

A abstração é a capacidade de modelar objetos do mundo real de forma simplificada, destacando apenas os detalhes relevante para o contexto do problema. Em outras palavras, ela permite que você represente conceitos complexos de maneira mais simples, ignorando detalhes desncessários 
  
* Polimorfismo

O polimorfismo permite que objetos de diferentes classes sejam tratados de maneira uniforme. Isso significa que você pode usar um objeto de uma classe filha onde um objeto da classe pai é esperado. O polimorfismo é frequentemente alcançado através do uso de interfaces ou herança. 

**Construtores:** Os construtores são responsáveis por inicializar os atributos de uma classe quando um objeto dessa classe é criado. Eles definem como os atributos serão configurados quando uma instância da classe for instanciada. Em Kotlin, você pode ter um construtor primário diretamente na declaração da classe ou, se necessário, construtores secundários adicionais. São escritos entre parênteses após o nome da classe. 

**Parâmetros:** São basicamente os inputs de uma classe ou função. 
    
**Variáveis:**

       fun main()
       {
       val name: String = "Gab" // variável imutável do tipo String ("semelhante a uma tupla no Python")

       var idade: Int? // Variável mutável que pode ser nula

       idade = 19
       println("Olá $name, você tem $idade anos")
       // $name == pegar o que estiver na variável name, parecido com o format do Python ou % do C
       
       }
       
* Por padrão, após a palavra-chave **class** se coloca o nome da classe cujo primeira letra é maiúscula, e crie um arquivo com o mesmo nome da classe e o defina nele. Ex:

 file: Dog

     class Dog
     {
         var name: String? = null
         // variável mutável chamada name do tipo(Isso que significa :) string, o ponto de interrogação significa que pode ser nulo ("vazio"). 
     }

Arquivo em execução:

    fun main()
    {
        val dog = Dog( )
        dog.name = "Linux"
        println(" Ola ${dog.name}")
    }

 crio a classe Dog com um atributo name, dela instâncio dog ( crio um objeto chamado dog da classe Dog), e faço dog.name = "Linux" então o atributo name de dog recebe "Linux", e é imprimido Olá Linux.

 * Dentro da classe Dog há uma variável name, como está em uma classe chamamos ela de atributo / propriedade.




