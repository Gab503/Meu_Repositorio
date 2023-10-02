# Integridade dos dados

### Porque a integrridade dos dados é importante ?
Se os dados que você está usando forem comprometidos de alguma forma, sua análise não será tão forte quanto deveria. 
A integridade dos dados é a precisão, integridade, consistência e confiabilidade dos dados durante o ciclo de vida deles.

Quando a integridade dos dados é baixa, pode causar desde a perda de um único pixel em uma imagem, até uma decisão médica incorreta.
Em alguns casos, uma peça que falta pode tornar todos os seus dados inúteis.

A integridade dos dados pode ser comprometida de várias maneiras diferentes. Há chance dos dados serem comprometidos quando:

* São Replicados
* Transferidos
* Manipulados

  * A replicação de dados é o processo de armazenamento de dados em vários locais. Se você estiver replicando dados em momentos
  diferentes e em lugares diferentes há uma chance de seus dados ficarem fora de sincronia. Esses dados carecem de integridade,
  porque pessoas diferentes podem não estar usando os mesmo dados para suas descobertas, o que pode causar inconsistências.

  * A transferência de dados é o processo de copiar dados de um dispositivo de armazenamento para a memória, ou de um computador
    para o outro. Se a sua transferência de dados for interrompida, você pode acabar com um conjunto de dados incompletos.

  * O processo de manipulação de dados envolve a alteração de dados para torná-los mais organizados e fáceis de ler.
    A manipulação de dados visa tornar o processo de análise de dados mais eficiente, mas um erro durante o processo pode comprometer a eficiência.

 Os dados também podem ser comprometidos por:
 * Erro humano
 * Vírus.
 * Malware.
 * Hackers
 * Falhas no sistema.

Em muitas empresas o armazenamento de dados e a sua integridade é feita por uma equipe de engenharia de dados se encarrega destas questões.

<<<<<<< HEAD
=======
* Também é importante verificar se os dados que você está usando, estão alinhados com o objetivo de negócios.
  Isso adiciona outra camada à manutenção da integridade dos dados, porque os dados que você está usando podem ter limitações com as quais você precisará lidar.

* Cuidado para não haver Dados duplicados
* Verifique se há dados suficientes para análise.

Como uma analista de dados, o alinhamento é algo que você precisará julgar. Um bom alinhamento significa que os dados são relevantes e podem ajudá-lo a resolver um problema de negócios ou determinar um curso de ação para atingir um determinado objetivo de negócios. 

* Quando há dados limpos e um bom alinhamento, você pode obter insights precisos e tirar conclusões que os dados suportam.

* Se houver um bom alinhamento, mas os dados precisarem ser limpos, limpe os dados antes de realizar sua análise.

* Se os dados estiverem apenas parcialmente alinhados com um objetivo, pense em como você pode modificar o objetivo ou use restrições de dados para garantir que o subconjunto de dados se alinhe melhor ao objetivo de negócios.

# Como lidar com a insuficiência de dados
#### Diferentes tipos de dados insuficientes:

* Dados de apenas uma fonte.

* Dados que continuam atualizando.

* Dados desatualizados.

* Dados geograficamente limitados.

#### Maneiras de lidar com estes dados insuficiente:

* Identificar tendências com os dados disponíveis.

* Esperar por mais dados se o tempo permitir.

* Conversar com as partes interessadas e ajustar seu objetivo

* Procurar um novo conjunto de dados.

#### Falta de dados: 
* Colete os dados em pequena escala para realizar uma análise preliminar e, em seguida, solicite mais tempo para concluir a análise depois de coletar mais dados.

* Se não houver tempo para coletar dados, realize a análise usando dados de proxy de outros conjuntos de dados. Esta é a solução mais comum.

#### Muito poucos dados:
* Faça a análise usando dados de proxy junto com dados reais.

* Ajuste sua análise para alinhar com os dados que você já possui.

#### Dados errados, incluindo dados com erros:
* Se você tiver os dados errados porque os requisitos foram mal compreendidos, comunique os requesitos novamente.

* Identifique erros nos dados e, se possível, corrija-os na origem, procurando um padrão nos erros.

* Se você não puder corrigir os erros de dados sozinho, poderá ignorar os dados errados e prosseguir com a análise se o tamanho da amostra ainda for grande o suficiente e ignorar os dados não causará viés sistemático.

  ##### Observação: Às vezes, dados com erros podem ser um sinal de alerta de que os dados não são confiáveis.

  # A importância do tamnho da amostra:
* População em análise de dados: São todos os valores de dados possíveisem um determinado conjunto de dados.

 Se você poder usar 100 % de uma população em sua análise, será ótimo. Mas, nem sempre será possível coletar informações sobre uma população inteira. Demanda muito tempo e é caro.

 * Amostra: Ao usar uma amostra, você usar uma parcela de uma população, que é representativa da população.

O objetivo é obter informações suficientes de um pequeno grupo dentro de uma população para fazer previsões ou conclusões sobre toda a população.
Ao usar uma amostra de uma população para análisar, é mais econômico e leva menos tempo. 

Porém há uma desvantagem, quando você usa apenas uma pequena amostra de uma população, isso pode levar à incerteza. Você não pode ter 100 % de certezade que suas estatísticas são uma representação completa e precisa da população. Isso leva ao viés de amostragem, 

* O viés de amostragem ocorre quando uma amostra não é representativa da população como um todo. Isso significa que alguns membros da população estão sendo super-representados ou sub-representados. 

O uso de amostra aleatória pode ajudar a resolver alguns desses problemas com viés de amostragem

* Amostragem aleatória é uma maneira de selecionar uma amostra de uma população de modo que todos os tipos possíveis de amostra tenham a mesma chance de serem escolhidos.

As empresas geralmente criam tamanhos das amostras antes da análise de dados para que os analistas saibam que o conjunto de dados resultante é representativo de uma população.

### Termos e definições:

* População: Todo o grupo em que você está interessado para o seu estudo.

* Amostra: Um subconjunto de sua população. Uma pequena parte.

* Margem de erro: Como uma amostra é usada para representar uma população, é esperado que os resultados da amostra sejam diferentes do que teria sido se você tivesse pesquisado toda a população. Essa diferença é chamada de margem de erro. Quanto menor a margem de erro, mais próximos os resultados da amostra estarão do resultado se você tivesse pesquisado toda a população.

* Nível de confiança: Quão confiante você se sente nos resultados da pesquisa. Por exemplo, um nível de confiança de 95% significa que se você executar a mesma pesquisa 100 vezes, obterá resultados semelhantes 95 dessas 100 vezes. O nível de confiança é direcionado antes de você iniciar seu estudo, porque afetará o tamanho da sua margem de erro no final do seu estudo.

* Intervalo de confiança: O intervalo de valores possíveis que o resultado da população estaria no nível de confiança do estudo. Este intervalo é o resultado da amostra +/- a margem de erro.

* Significância estatística: A determinação de se o seu resultado pode ser devido ao acaso ou não. Quanto maior o significado, menos devido ao acaso.

## Para determinar o tamanho da sua amostra:
* Não use um tamanho da amostra menor que 30. Está estatisticamente comprovado que 30 é o menor tamanho da amostra onde um resultado médio de uma amostra passa a representar o resultado médio de uma população.

* O nível de confiança mais usado é 95%, mas 90% pode funvionar em alguns casos.

* Para um nível de confiança mais alto, use um tamanho da amostra maior.

* Para diminuir a margem de erro, use um tamanho da amostra maior.

* Para mior significância estatística, use um tamanho da amostra maior.

### Por que uma amostra mínima de 30 ?
 Esta recomendação é baseada no Teorema do limite Central (CLT) no campo da probabilidade e estatística. Conforme o tamanho da amostra aumenta, os resultados se assemelham mais à distribuição normal de um grande número de amostras. Uma amostra de 30 é o menor tamanho da amostra o qual o CLT ( não confundir com carteira assinada) ainda é válido.
Pesquisadores que confiam em anáise de regressão, métodos estatísticos para determinar as relações entre variáveis controladas e dependentes também preferem uma amostra mínima de 30.



>>>>>>> d6ae1d9c7ce197c364d5686f95c2a82e2808e424
