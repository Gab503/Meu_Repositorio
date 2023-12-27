<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> Aprendendo HTML-CSS </title>
</head>
<body>
    <h1>A história da Internet</h1>
    <p>Surgiu durante a Guerra Fria para cumprir seus objetivos. <br>O presidente Dwight Eisenhower fundou uma agência de estudos de tecnologias para a guerra, a DARPA, existente até os dias atuais.</p>
      <p> Em 1969 para evitar perda de dados (ter um Backup) em caso de um ataque da URSS, eles inventaram a ARPANET, uma pequena rede com inicialmente 4 pontos, com 4 computadores ("primitivos") cujo o objetivo era de conectar essa rede e fazer se comunicarem entre si, porém, os computadores eram diferentes, na época computadores diferentes falavam linguagens diferentes, para resolver isso, foi criado um protocolo chamado NCP (que tinha que parar a rede para a comunicação de dois pontos), que falava uma linguagem única.</p>
    
  <p>Entretanto com o aumento da rede, o NCP não dava conta de tantos pontos existentes (1973). Assim surgiu dois protocolos que posteriormente foram unidos, o TCP, criado por Bob Kanh, que possui dificuldade de identificação dos pontos da rede, e o IP, criado por Vint Cerf, cujo objetivos era identificar esses pontos da rede, juntando ambos, foi criado o TCP/IP, usado atualmente na versão 6, cuja comunicação não era mais feito por cabos, como anteriormente, mas sim por satélites, permitindo a comunicação internacional.</p>

  <p>A ARPANET cresceu de forma muito rápida, e como deixou de ser somente uma rede militar, houve a necessidade de uma separação, a parte militar ficou com uma rede menor chamada MILNET, a parte de pesquisa científica ficou com a NSFNET, e várias outras redes comerciais surgiram. <br>Essas diferentes redes (com execeção da militar) queriam se comunicar, se conectar, uma Rede de Interconexão, ou melhor, uma Interconnect Networking, abreviada para Internetworking, mais ainda simplificada, surgiu o termo Interner.<br>Atualemente a internet cobre quase o mundo inteiro, se comunicando através de cabos submarinos intercontinentais, a Internet, em suma, não é uma rede, é um conjunto de várias redes.</p>

   <p>Hoje, como funciona a comunicação entre pontos ? Como transferir um dado de um conjunto de um ponto A para um ponto B ? </p>

  <p>O TCP/IP identifica os pontos/servidores, e quebra o dado em pacotes ("pedacinhos") e envia por rotas, caminhos e tempo diferetes (por isso "a bolinha de carregando" dos sites), o TCP/IP do ponto B recebe esses dados, e reuni os pedacinhos para ver a "mensagem" (não necessariamente um texto, pode ser uma imagem, um vídeo etc).</p>

  <p>A Internet antigamente era rudimentar, usava-se o Gopher para "navegar", não havia gráficos bonitos.<br> Em 1993 em Genebra, Tim Berners-Lee participou de um projeto semelhante ao Gopher, mas que podia ser acessado por "links", ele criou um protocolo que foi incluído no TCP/IP, o Http://, Hypertext Transfer Protocol.<br>Além disso, criou a linguagem (não de programação) HTML, uma linguagem de marcação para hipertextos, (clica e é redirecionado para outro lugar). O que chamamos de Internet, cujo nome na realidade é World Wide Web, ou WWW, uma rede de alcance mundial, também precisou-se criar um navegador, criado por Marc Andreessen o Mosaic, o primeiro navegador da Internet compátivel ao http.</p><hr>

<h2>(WWW) World Wide Web != Internet</h2>
    <p>Internet é a rede das redes, a interconexão, dentro dela há conjuntos de servidores especializados em determinado tipo de serviço ou protocolo. Já o WWW é uma sub rede da Internet, uma parte da Internet especializada em http. Em suma, o www é uma rede dentro da rede.<br>Vale ressaltar que as diferentes redes se comunicam entre si.</p>

  <p>Como a Internet funciona ?<br>Como o computador vê os dados ?<br> 0101 sinais elétricos com sinal, é igual a 1, e sem sinal é 0. Esses 0101 são códigos binários, ou Bit (binary digit).<br>Para representar os dados, há uma porção mínima para que se represente algum dados, 8 bits ou 1 byte.<br>Exemplo: 01000001 = A. Para ver a tabela inteira, veja o código multibyte ou UTF-8. Vale ressaltar que o computador verá as ondas quadradas e não um monte de 0 e 1.</p>

  <p>8 bits =  1 byte<br>1024 bytes  = 1 KB (kilobyte)<br>1024 KB = 1 MB (megabyte)<br>1024 MB = 1 GB (gigabyte)<br>1024 GB = 1 TB (terabyte)<br>1024 TB = 1 PB (petabyte)<br>1024 PB = 1 EB (exabyte)<br> 1024 EB = 1 ZB (zettabyte)<br>1024 ZB = 1 YB (yottabyte)</p><hr>

   <h2>MB != Mb:</h2>
    <p>Mb, minúsculo é um megabits, milhões de bit, usado para se referir à velocidade de transmissão.<br>MB megabyte, usado para se referir a armazenamento.</p><hr>

   <p>Como nos conectamos à Internet ? <br>Ao acessar a Internet, chamamos o seu dispositivo de cliente, porque está fazendo o uso de um serviço. O serviço, vídeo, imagem etc, está na Internet. <br>Para conseguir o acesso geralmente precisa-se de um "modem" ou uma linha telefônica, esses dispositivos é fazem ter acesso a Internet. Porém esses sistemas (de TV, de celular, linha telefônica) não aceitam as ondas quadradas; esse aparelho chamado "modem" faz a transformação desses ondas, modulação -> e o opsto <- demolução, de uma onda para outra.</p>

   <p>Como acessamos os Servidores ?<br>Exemplo: Instagram.com, onde está o Instagram ?<br> O Instagram nada mais é do que um monte de arquivos que estão em um servidor, ou em um conjunto de servidores, como é o caso do Instagram. Esses servidores são identificados por números, exemplo o do Instagram, 3.224.112.47.<br>Até mesmo você ao navegar na Internet possui um identificado, o IP. Para saber o seu ou de um site basta acessar o <a href="https://www.iplocation.net/" target="_blank">www.iplocation.net</a>, porém o IP muda constantemente (por questão de segurança).<br>Para não ter que ficar constantemente verificando IP, usa-se um "nome", um servidor DNS (sistema de nome de domínio), exemplo: Instagram.com ( <-uma URL) que verifica o nome e envia o IP do Site ao Modem que possibilita você acessar o site.</p>

<hr>

 <h1>Domínio e Hospedagem</h1>
 <p>Para outras pessoas acessarem o seu site, você precisa de um domínio, e também precisa de um local para guardar os arquivos que você desenvolve, esse lugar para guardar chamamos de hospedagem. 
    </p>
    <p>Domínio: É o nome que identifica o seu site, um nome único (Exemplo, Instagram.com). Geralmente é pago anualmente para mantê-lo. Há vários TLDs (Top Levek Domain)</p>

   <p>Hospedagem: É o local onde o seu site vai estar armazenado. Geralmente a hospedagem é paga mensalmente (pense como se fosse um hotel).</p>

  <p>O que é uma URL ? <br>Ex:<a href="http://www.brasilescola.com.br" target="_blank">http://www.brasilescola.com.br</a>, isso é uma URL ( Localizador de Recurso Único), dentro de uma URL há partes, ex: <a href="http://www.github.com/gustavoguanabara" target="_blank">http://www.github.com/gustavoguanabara</a>.<br> O github é o domínio.<br>O .com é o TLD ( ou .net entre outros).<br>O www é o sub domínio principal do servidor web.<br>A barra / e o que estiver depois é o caminho.</p>
<hr>

<h1>Front-end Back-end e Full stack</h1>
<p>Front-end: Client-Side. Desenvolvedor do lado do cliente. Gera a parte visual e iterativa do site. Linguagens: JavaScript, HTML, CSS.</p>

 <p>Back-end: Servir-Sider. Desenvolvedor ao lado do servidor. Foca na iteração do código com o servidor. Envolve bancos de dados. Linguagens: PHP, JavaScript, C#, Python entre outras.</p>
   
<p>Full Stack: É ambas as áreas.</p>
<hr>

<h1>04 Hello world!</h1>
<hr>
<p>Esse é o meu primeiro documento HTML! estou muito feliz!</p>
<hr>


</body>
</html>   
