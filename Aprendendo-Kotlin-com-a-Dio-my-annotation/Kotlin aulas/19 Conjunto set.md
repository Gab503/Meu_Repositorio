# Conjuntos Set
Enquanto as listas são ordenadas e permitem itens duplicados, os conjuntos não são ordenados (a ordem não importa) e
armazenam apenas itens únicos.

Para criar conjuntos imutáveis, utlize setOf().E para criar conjuntos mutáveis, use mutableSetOf()
Semelhante as lista, para criar uma variável somente para leitura, utlize apenas set (no caso das listas é List)

Ao criar conjuntos, o Kotlin pode inferir o tipo de itens armazenados. Para declarar o tipo explicitamente, adicione o tipo 
entre colchetes angulares, <>, após a declaração set.


        val openIssues: MutableSet<String> = mutableSetOf("uniqueDescr1", "uniqueDescr2", "uniqueDescr3")

            fun addIssue(uniqueDesc: String): Boolean
            {
                return openIssues.add(uniqueDesc)
            }
            
            fun getStatusLog(isAdded: Boolean): String
            {
                return if (isAdded) "registered correctly." else "marked as duplicate and rejected."
            }
            
            fun main()
            {
                val aNewIssue: String = "uniqueDescr4"
                val anIssueALreadyIn: String = "uniqueDescr2"
                
                println("Issue $aNewIssue ${getStatusLog(addIssue(aNewIssue))}")
                println("Issue $anIssueALreadyIn ${getStatusLog(addIssue(anIssueALreadyIn))}")
            }
