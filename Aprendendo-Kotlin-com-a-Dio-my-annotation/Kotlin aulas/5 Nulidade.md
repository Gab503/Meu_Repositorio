# Null Safety Nulidade
Segurança nula, ou nulidade, é a característica do Kotlin que faz com que os desenvolvedores deixem de forma explícita,
se uma determinada variável vai receber ou não um valor nulo.
    
     fun main()
     {
            // Não pode ser nula, e sim uma string.
            // ao atribuir null, vai dar erro pois é uma string, não nula
            
            var neverNull: String = "This can't be null"
            
            neverNull = null
            
            // Strin? vai aceitar string ou nulo.
            var nullable: String? = "You can keep a null here"
            var nullable = null
            
            // Não foi específicada, vai automaticamente ser não nula
            var inferredNonNull = "The compiler assumes non-null"
            inferredNonNull = null
            
            fun strLength(notNull: String): Int
            {
                return notNull.length
            }
            strLength(neverNull)
            strLength(nullable)
        }

    
        // str?.lenght ? : 0 ->Se não for nula acesse isso
    fun strLength(str: String?): Int 
    {
       return str?.length ? : 0
    }
  Outro exemplo:
        
        fun describeString(maybeString: String?):String
        {
            if (maybeString != null && maybeString.length > 0)
            {
                return "String of length ${maybeString.length}"
            }
            else
            {
                return "empty or null string"
            }
        }
        
        fun main()
        {
            println(describeString(null))
            println(describeString(""))
            println(describeString("Dio.me"))
        
        }
    
