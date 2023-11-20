# Loops: While and do while
O laço de repetição while, vai executar algo, enquanto for true, enquanto a condição for verdadeira.

## Do while
Enquanto o while faz a condição sempre em primeiro, o do while primeiro executa o do, e depois passa a condição. Então irá executar
algo dentro do "Do" enquanto a condição for True ( verdadeira) 
  
    fun eatACake() = println("Eat a Cake")
    fun bakeACake() = println("Baker a Caker")

    fun main()
    {
    var cakesEaten = 0
    var cakesBaked = 0
    
    while (cakesEaten < 5) 
    {
        eatACake()
        cakesEaten ++
    }
    
    do
    {
        bakeACake() 
        cakesBaked++
    }   while (cakesBaked < cakesEaten)

    }
