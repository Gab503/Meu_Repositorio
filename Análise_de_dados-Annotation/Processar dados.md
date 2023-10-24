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

  # A importância do tamanho da amostra:
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


## O poder estatístico:
O poder estatístico é a probabilidade de obter resultados significativos de um teste. 

* O teste de hipóteses é uma meneira de ver se uma pesquisa ou experimento tem resultados significativos. Normalmente, quanto maior o tamanho da amostra, maior a chance de você obter resultados estatisticamente significativos com seu teste.

Se seu poder estatístico for 0,6 é a mesma coisa que dizer 60%. 

O termo "estatisticamente significativo" é usado em estatísticas. Em termos básicos, se um teste é estatisticamente significativo, significa que os resultados do teste são reais e não um  erro causado por acaso.  

* Normalmente, você precisa de um poder estatísco de pelo menos 0,8 ou 80% para considerar seus resultados estatiscamente significativos.

* O poder estatísco pode ser calculado e relatado para um experimento completo para comentar sobre a confiança que se pode ter nas concçusões extraídas dos resultados do estudo, Também pode ser usado como uma ferramenta para estimar o número de observações ou o tamanho da amostra necessãria para detectar um efeito em um experimento.

  
## Como determinar o melhor tamanho da amostra.
Relembrando, uma amostra é uma parte de uma população que é representativa da população.
Pode ser tanto caro como levar muito tempo para analisar uma população inteira de dados. Usar o tamamho da amostra geralmente faz mais sentido e ainda pode levar a descobertas úteis. Existem calculadoras úteis online que podem ajudá-lo a encontrar o tamanho da amostra. 

Você precisa inserir o nível de confiança, o tamanho da população e a margem de erro. 

* O nível de confiança é a probabilidade de que sua amostra reflita com precisão a população maior. Você pode pensar nisso da mesma forma que a confiança em qualquer outra coisa. É o quão forte você sente que pode confiar em algo ou alguêm. Ter um nível de confiança de 99% é o ideal. Mas a maioria das indústrias espera um nível de confiança de pelo menos de 90% ou 95%.

Em outros estudos, as organizações podem precisar apenas saber que os resultados do teste ou da pesquisa os levam na direção certa. Por exemplo, se uma empresa de tintas estiver testando novas cores, um nível de confiança mais baixo é suficiente. 

* Você também deve considerar a margem de erro para seu estudo. Basicamente informa o quão próximos os resultados do tamanho da amostra estão do que seus resultados seriam se você usasse toda a população que o tamanho da amostra representa.
  
Por exemplo, digamos que o diretor de uma escola de ensino médio se aproxime de você com um estudo sobre as preferências de doces dos alunos. Eles precisam saber um tamanho da amostra adequado e precisam disso agora. A escola tem uma população de 500 alunos, e eles estão pedindo um nível de confiança de 95% e uma margem de erro de 5%. Configuramos uma calculadora em uma planilha, mas você também pode encontrar facilmente esse tipo de calculadora pesquisando "Calculadora de tamanho da amostra" na internet. Assim como essas calculadoras, a calculadora da planilha não mostra nenhum dos cálculos mais complexos para descobrir o tamanho da amostra, tudo o que precisa fazer é inserir os números para a população, nível de confiança e margem de erro. 
E quando digitamos 500 para o tamanho da população, 95 para a porcentagem de nível de confiança, 5 porcento para margem de erro, o resultado é cerca de 218. Isso significa que para este estudo, um tamanho da amostra apropriada seira 218. 

Se fizermos uma pesquisa com 218 alunos e descobrirmos que 55% deles prederem chocolate, poderíamos estar bastante confiante de que isso seria verdade para todos os 500 alunos. 218 é o número mínimo de pessoas que precisamos pesquisar com base em nossos critérios de nível de confiança de 95% e margem de erro de 5%.

* O nível de confiança e a margem de erro não precisam corresponder a 100%. Eles são independentes um do outro. Então digamos que mudamos nossa margem de erro de 5% para 3%.
Então descrobimos que nosso tamanho da amostra precisaria ser maior, cerca de 341 em vez de 218, para tornar os resultados do estudo mais representativos da população.

* Taxa de resposta estimada: Se você estiver realizando uma pesquisa com indivíduos, essa é a porcentagem de pessoas que você espera que preencham sua pesquisa entre aquelas que receberam a pesquisa.


### Como avaliar a confiabilidade dos dados
Como analista de dados, é importante descobrir o tamanho da amostra e variáveis como nível de confiança e margem de erro antes de executar qualquer tipo de teste ou pesquisa. É a melhor maneira de garantir que seus resultados sejam objetivos e oferece uma chance melhor de obter resultados estatisticamente significativos.

Mas se você já conhece o tamanho da amostra, como quando recebe os resultados da pesquisa para analisar, pode calcular a margem de erro por conta própria. Assim, terá uma ideia melhor de quanta diferença existe entre sua amostra e su população.

A margem de erro é o máximo que se espera que os resultados da amostra sejam diferentes daqueles da população real.
Seria ótimo pesquisar ou testar uma população inteira, mas geralmente é impossível fazer isso. Em vez disso, pegamos uma amostra da população maior. Com base no tamanho da amostra, a margem de erro resultante podem ser comparados aos resultados se tivéssemos pesquisado toda a população. A margem de erro ajuda você a entender o quão confiáveis são os dados do seu teste de hipóteses. 

Quanto mais próximo de zero a margem erro for, mais próximos os resultados de sua amostra corresponderiam aos resultados da população geral. 

Por exemplo: Digamos que você tenha completado uma pesquisa nacional usando uma amostra da população. Você perguntou às pessoas que trabalham cinco dias por semana se ela gostam da ideia de uma semana de trabalho de quatro dias. Portanto, sua pesquisa informa que 60% preferem uma semana de trabalho de quatro dias. A margem de erro foi de 10% o que nos diz que entre 50 e 70% gostaram da ideia.

Então, se fizéssemos uma pesquisa com todos os trabalhadores de cinco dias em todo o país, entre 50 e 70% concordaria com nossos resultados. Lembre-se que nosso alcance está entre 50 e 70%. Isso porque a margem de erro é contada nos dois sentidos a partir dos resultados da pesquisa de 60%.

Se você configurar um nível de confiança de 95% para sua pesquisa, haverá uma chance de 95% de que as respostas de toda a população caiam entre 50 e 70% dizendo sim, eles querem uma semana de trabalho de quatro dias. 
Como a margem de erro se sobrepões a essa marca de 50%, você não pode dizer com certeza que o público gosta da ideia de uma semana de trabalho de quatro dias. Nesse caso, você teria que dizer que sua pesquisa foi inconclusiva.

Agora, se você quisesse uma amostra de erro menor, digamos de 5%, com um intervalo entre 55 e 65%, você poderia aumentar o tamanho da amostra. Mas se você já recebeu o tamanho da amostra, você mesmo pode calcular a margem de erro. Assim, você pode decidir por si mesmo qual a chance de seus resultados serem estatiscamente significativos com base em sua margem de erro. Em geral, quanto mais pessoas você incluir em sua pesquisa, maior a probabilidade de sua amostra ser representativa de toda a população. 

Diminuir o nível de confiança também teria o mesmo efeito, mas também tornaria menos provável que sua pesquisa seja precisa. Portanto, para calcular a margem de erro, você precisa de três coisas:
1. Tamanho da população.
2. Tamanho da amostra.
3. Nível de confiança.

* E assim como no tamanho da amostra, você pode encontrar muitas calculadoras online pesquisando "calculadora de margem de erro".

  
Margem de erro é a quantidade máxima que se espera que os resultados da amostra sejam diferentes dos da população real. Mais tecnicamente, a margem de erro define um intervalo de valores abaixo e acima do resultado médio da amostra. Espera-se que o resultado médio para toda a população esteja dentro desse intervalo. 

* Dados sujos podem ser o resultado de alguém digitando um pedaço de dado incorretamente; formatação inconsistente; campos em branco ou mesmo pedaços de dados sendo inseridos mais de uma vez, o que cria duplicatas.
Dados sujos são dados incompletos, incorretos ou irrelevante para o problema que você está tentando resolver.

* Dados limpos são dados que estão completos, corretos e são relevantes para o problema que você está tentando resolver. Quando você trabalha com dados limpos você vai perceber que seus projetos acontecem muito mais tranquilamente. 

* Dados sujos, são incompletos, incorretos, ou irrelevantes para o problema que você está tentando resolver.

* Engenheiros de dados transformam dados em um formato útil para ánalise e dão uma infra-estrutura confiável. Isto significa que eles desenvolvem, mantêm e testam os bancos de dados e sistemas relacionados. Especialistas em armazenamento de dados desenvolvem processos e procedimentos para efetivamente armazenar e organizar os dados. Eles garatem que os dados estejam disponíveis, seguros e redundantes para evitar perdas.

* É importante ter em mente: Nenhum conjunto de dados é perfeito ! É sempre uma boa ideia examinar e limpar os dados antes de iniciar a análise.

### Como reconhecer e limpar dados sujos
* Ortografia incorreta, variações ortográficas, letras misturadas, pontuação inconsistente e erros de digitação em geral, acontecem quando alguém digita um pedaço de dado incorretamente.

* Como analista de dados, você também lida com diferentes moedas. 

* Formatação inconsistente, algo que devia ser formatado de um geito, mas está de outro. 

* Duplicatas

* Valores nulos (em branco)

* Etiquetagem:

Para entender a etiquetagem, imagine-se tentando conseguir um computador oara identificar corretamente os ursos panda entre imagens de todos os diferentes tipos de animais. Você precisa mostrar ao computador milhares de imagens de ursos panda, todos eles são rotulados como ursos panda. Qualquer imagem rotulada incorretamente, como um que é apenas um urso, causará um problema.

* Comprimento de campo incosistente:

Lembre-se que um campo é um único pedaço de informação de uma linha ou coluna de uma planilha. O comprimento do campo é uma ferramenta para determinar muitos como caracteres podem ser inseridos em um campo, atribuindo um certo comprimento a estes campos em sua planilha é uma ótima maneira de evitar erros. Por exemplo, se você tiver uma coluna para o ano de nascimento de alguém, você sabe que o comprimento do campo é quatro, porque todos os anos têm quatro dígitos.

#### A validação de dados é uma ferramenta para verificação da exatidão e qualidade dos dados antes de adiciona-los ou importa-los.

#### Princípios de integridade dos dados

* Validade: O conceito de usar princípios de integridade dos dados para garantir que as medidas estejam  em conformidade com as regras ou restrições de negócios definidas.

* Integridade: O grau em que todas as medidas necessárias são conhecidas.

* Consistência: O grau em que um conjunto de medidas é equivalente em todos os sistemas.

* Precisão: O grau de conformidade de uma medida com um padrão ou um valor verdadeiro.


### Ferramentas e técnicas para limpar dados - Uma visão geral básica

Antes de remover dados indesejados, é sempre uma boa prática fazer uma cópia do conjunto de dados.
Dessa forma, se você remover algo que acaba precisando no futuro, você pode acessá-los facilmente e colocá-lo de volta no conjunto de dados.

* Tipicamente, as duplicatas aparecem quando você está combinando conjuntos de dados de mais de uma fonte ou usando dados de múltiplos setores dentro da mesma empresa. As duplicatas podem ser um grande problema para analistas de dados.

Portanto, é realmente importante que você rpossa encontrá-los, removê-los antes do inpicio de qualquer análise. 
A maioria das planilhas oferecem ferramentas para ajudar a encontrar e remover duplitas. 

* Dados irrelevante, que são dados que não se ecaixam no problema específico que você está tentando resolver, também precisam ser removidos.

A remoção de dados irrelevantes requer um pouco mais de tempo e esforço porque você precisa descobrir a diferença entre os dados que você precisa e os dados que você não precisa. 

* Remover os espaços em brancos.

Espaços extras podem causar inesperados resultados quando você organiza, filtra, ou pesquisa atráves de seus dados. E porque esses caracteres são fáceis de errar, eles podem levar a resultados inesperados e confusos. 

Para remover esses espaços em indesejados ou células em branco, você mesmo pode apagá-los. Ou novamente, você pode confiar em suas planilhas, que oferecem muitas funções para remover espaços automaticamente. 

* Correção de erros ortográficos.

Uso inconsistente de maiúsculas e minúsculas, pontuação incorreta, e outros erros de digitação. Estes tipos de erros podem levar a alguns grandes problemas.

Como os outros problemas, você também pode resolver esses problemas manualmente. Ou você pode usar ferramentas de planilhas, como a verificação ortográfica, autocorreção e formatação condicional para facilitar a sua vida.

* Remover a formatação diferente.

Isto é importante quando você obtém dados de muitas fontes diferentes. Cada banco de dados tem sua própria formatação, o que pode fazer com que os dados pareçam incosistentes. Criar um visual limpo e uma aparência consistente para sias planilhas facilitará uma ferramenta valiosa para que você e sua equipe tomem decições importantes. 

A maioria das planilhas, também têm uma ferramenta de "formatos claros"
