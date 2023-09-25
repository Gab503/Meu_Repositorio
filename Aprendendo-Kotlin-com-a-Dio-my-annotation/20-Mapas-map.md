<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Mapas (Map):</h1><br>
    <p>Os mapas armazenam itens como pares de valores-chaves. Você acessa o valor referenciando a chave. <br>Os mapas são úteis se você quiser um valor sem usar um índice numerado, como uma lista. Semelhantes as bibliotecas do Python.</p>
    
  <p>Para criar um mapa imutável use: mapOf()<br>Para criar um mapa mutável use: mutableMapOf()</p>

    <p>
        
        // Uma constante imutável com valor 15
        const val POINTS_X_PASS: Int = 15
        
        // contas com um mapa mutável, o 1 tem 100, o 2 100, e o terceiro 100.
        val EZPassAccounts: MutableMap<Int, Int> = mutableMapOf(1 to 100, 2 to 100, 3 to 100)
        
        // Uma cópia somente para leitura.
        val EZPassReport: Map<Int, Int> = EZPassAccounts
        
        // update doss pontos,vai receber um Id da conta
        fun updatePointsCredit(accountId: Int) {
            
            //Vai ver se tem o accountId
            if (EZPassAccounts.containskey(accountId)){
              
                // se true, faz o update, adicionando os pontos ao que ele já tem
                println("updating $accountId...")
                EZPassAccounts[accountId] = EZPassAccounts.getValue(accountId) + POINTS_X_PASS
            } else
            {
                println("Error: Trying to update a non-existing account (id: $accountId)")
            }
        }
        
        fun accountsReport() {
            println("EZ-Pass report: ")
            EZPassReport.forEach{
                k, v -> println("ID $k: credit $v")
            }
        }
        
        fun main() {
            accountsReport()
            updatePointsCredit(1)
            updatePointsCredit(1)
            updatePointsCredit(5)
            accountsReport()
        }</p>
</body>
</html>