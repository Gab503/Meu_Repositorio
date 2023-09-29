# APIs


APIs são “tradutores” com a função de conectar sistemas, softwares e aplicativos.

Não é algo específico do python, todas as linguagens de programação possuem. De forma geral, uma API é uma interface de programação de aplicativos.

 E pode se referir a arquivos e funções em Python. Mas muitas vezes, as APIs realmente se referem a serviços de terceiros com os quais você e eu podemos escrever códigos que se comunicam.
Muitas APIs, mas não todas, vivem na Internet hoje em dia, de modo que, desde que você tenha um navegador ou alguma experiência com programação Python ou  programação em qualquer linguagem, você possa escrever códigos que, na verdade, finge ser um navegador, para conecta-se a essa API de terceiros em um servidor em seu próprio programa.

## Requests
A biblioteca de solicitações permite que você faça solicitação da web e da Internet usando código Python essencialmente como se você fosse um navegador.
Você pode automatizar, portanto a recuperação de URLs que começam com HTTP ou HTTPS. https://pypi.org/project/requests/
     
 A Apple tem sua própria API para o serviço iTunes.  O software que oferece a capacidade de baixar e pesquisar músicas, além de outras informações. 

## JSON JavaScript Object Notation:
É usado como um formato independente de linguagem para troca de dados entre computadores. Por linguagem independente, quer dizer que não precisa usar JavaScript, você pode usar qualquer outra linguagem para ler JSON ou escrevê-lo também. É um formato totalmente baseado em texto.

        
     import requests
     import sys

     if len(sys.argv) != 2:
         sys.exit()

    response = requests.get("https://itunes.apple.com/search? 
    entity=song&limit=1&term=" + sys.argv[1])
    print(response.json())

Saída:

    Python/itunes.py weezer (banda que eu quero pesquisar)
    {'resultCount': 1, 'results': [{'wrapperType': 'track', 'kind': 'song', 'artistId': 115234, 'collectionId': 1440878798, 'trackId': 1440879325, 'artistName': 'Weezer', 'collectionName': 'Weezer', 'trackName': 'Buddy Holly', 'collectionCensoredName': 'Weezer', 'trackCensoredName': 'Buddy Holly', 'artistViewUrl': 'https://music.apple.com/us/artist/weezer/115234?uo=4', 'collectionViewUrl': 'https://music.apple.com/us/album/buddy-holly/1440878798?i=1440879325&uo=4', 'trackViewUrl': 'https://music.apple.com/us/album/buddy-holly/1440878798?i=1440879325&uo=4', 'previewUrl': 'https://audio-ssl.itunes.apple.com/itunes-assets/AudioPreview112/v4/f0/ba/a8/f0baa81a-7449-c490-f43a-b5c6e3609e3f/mzaf_3988310882581261442.plus.aac.p.m4a', 'artworkUrl30': 'https://is1-ssl.mzstatic.com/image/thumb/Music125/v4/fc/74/67/fc74674a-1eb0-d50d-33fe-215caee529d1/16UMGIM52971.rgb.jpg/30x30bb.jpg', 'artworkUrl60': 'https://is1-ssl.mzstatic.com/image/thumb/Music125/v4/fc/74/67/fc74674a-1eb0-d50d-33fe-215caee529d1/16UMGIM52971.rgb.jpg/60x60bb.jpg', 'artworkUrl100': 'https://is1-ssl.mzstatic.com/image/thumb/Music125/v4/fc/74/67/fc74674a-1eb0-d50d-33fe-215caee529d1/16UMGIM52971.rgb.jpg/100x100bb.jpg', 'collectionPrice': 10.99, 'trackPrice': 1.29, 'releaseDate': '1994-01-01T12:00:00Z', 'collectionExplicitness': 'notExplicit', 'trackExplicitness': 'notExplicit', 'discCount': 1, 'discNumber': 1, 'trackCount': 10, 'trackNumber': 4, 'trackTimeMillis': 159587, 'country': 'USA', 'currency': 'USD', 'primaryGenreName': 'Pop', 'isStreamable': True}]}


<a href="https://docs.python.org/3/library/json.html" target="_blank">https://docs.python.org/3/library/json.html</a> Uma biblioteca especial no Python, chamada json, que permite manipular dados JSON e até mesmo imprimi-los formatados de uma maneira que será muito mais fácil para você e eu entendemos.  

      
    import json
    import requests
    import sys

    if len(sys.argv) != 2:
        sys.exit()

    response = requests.get("https://itunes.apple.com/search? 
    entity=song&limit=1&term=" + sys.argv[1])
    print(json.dumps(response.json(), indent=2))

 Saída:

         Python/itunes.py weezer
         {
      "resultCount": 1,
        "results": [
    {
      "wrapperType": "track",
      "kind": "song",
      "artistId": 115234,
      "collectionId": 1440878798,
      "trackId": 1440879325,
      "artistName": "Weezer",
      "collectionName": "Weezer",
      "trackName": "Buddy Holly",
      "collectionCensoredName": "Weezer",
      "trackCensoredName": "Buddy Holly",
      "artistViewUrl": "https://music.apple.com/us/artist/weezer/115234?uo=4",
      "collectionViewUrl": "https://music.apple.com/us/album/buddy-holly/1440878798?i=1440879325&uo=4",
      "trackViewUrl": "https://music.apple.com/us/album/buddy-holly/1440878798?i=1440879325&uo=4",     
      "previewUrl": "https://audio-ssl.itunes.apple.com/itunes-assets/AudioPreview112/v4/f0/ba/a8/f0baa81a-7449-c490-f43a-b5c6e3609e3f/mzaf_3988310882581261442.plus.aac.p.m4a",
      "artworkUrl30": "https://is1-ssl.mzstatic.com/image/thumb/Music125/v4/fc/74/67/fc74674a-1eb0-d50d-33fe-215caee529d1/16UMGIM52971.rgb.jpg/30x30bb.jpg",   
      "artworkUrl60": "https://is1-ssl.mzstatic.com/image/thumb/Music125/v4/fc/74/67/fc74674a-1eb0-d50d-33fe-215caee529d1/16UMGIM52971.rgb.jpg/60x60bb.jpg",   
      "artworkUrl100": "https://is1-ssl.mzstatic.com/image/thumb/Music125/v4/fc/74/67/fc74674a-1eb0-d50d-33fe-215caee529d1/16UMGIM52971.rgb.jpg/100x100bb.jpg",      "collectionPrice": 10.99,
      "trackPrice": 1.29,
      "releaseDate": "1994-01-01T12:00:00Z",
      "collectionExplicitness": "notExplicit",
      "trackExplicitness": "notExplicit",
      "discCount": 1,
      "discNumber": 1,
      "trackCount": 10,
      "trackNumber": 4,
      "trackTimeMillis": 159587,
      "country": "USA",
      "currency": "USD",
      "primaryGenreName": "Pop",
      "isStreamable": true
    }
     ]
    }
 .


    import json
    import requests
    import sys

    if len(sys.argv) != 2:
        sys.exit()

    #Fazendo uma solicitação HTTP usando Python, assim como fazemos em um navegador, digitando uma URL e pressionando Enter.
    response =requests.get("https://itunes.apple.com/search? 
    entity=song&limit=50&term=" + sys.argv[1])


    # Pegando daquela variável que contém a resposta do servidor, o JSON objeto que eu quero.
    # esse objeto tem uma chave chamada results, e essa chave de results é uma lista, e no momento, essa lista contém apenas uma musica, porque limitei a uma. Vou alterar de 1 para 50 nomes de faixas musicais, em limit=50&term
    o = response.json()
    for result in o["results"]:
        print(result["trackName"])

Saída:

     Python/itunes.py weezer
    Buddy Holly
    Say It Ain't So
    Undone - The Sweater Song
    My Name Is Jonas
    Weezer
    Holiday
    Only in Dreams
    Surf  Wax America
    The World Has Turned and Left Me Here
    In the Garage
    No One Else
    Lost in the Woods
    Buddy Holly
    Sundown
    Africa
    Say It Ain't So
    Say It Ain't So
    Take on Me
    Susanne
    Everybody Wants to Rule the World    
    The World Has Turned and Left Me Here
    Paranoid
    In the Garage
    My Name Is Jonas
    Mr. Blue Sky
    Happy Together
    Sweet Dreams (Are Made of This)      
    Stand by Me
    Billie Jean
    No Scrubs
    Jamie
    Surf Wax America
    Paperface
    My Evaline
    Undone - The Sweater Song
    Only In Dreams
    No One Else
    Lullabye For Wayne
    Undone -- The Sweater Song
    Island In the Sun
    Lost in the Woods
    My Name Is Jonas
    Surf Wax America
    Lost in the Woods
    Holiday
    Mykel and Carli
    I Swear It's True
    Jamie
    Only In Dreams
    No One Else
 



