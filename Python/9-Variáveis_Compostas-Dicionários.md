# Dict - Dicionários
Enquanto as listas têm localizações que são numéricas 0, 1, 2; os dicionários permitem que você use palavras reais como seus índices, por assim dizer. Através de palavras-chaves, assim com um dicionários real.

    students = {"Hermione": "Gryffindor",
            "Harry": "Gryffindor",
            "Ron": "Gryffindor",}

    print(students["Hermione"])
    print(students["Harry"])
    print(students["Ron"])
    
# Listas de Dicionários

    students = [
    {"Name": "Hermione", "House": "Gryffindor", "Patronus": "Otter"},
    {"Name": "Harry", "House": "Gryffindor", "Patronus": "Stag"},
    {"Name": "Ron", "House": "Gryffindor", "Patronus": "Jack Russel Terrir"},
    {"Name": "Draco", "House": "Slytherin", "Patronus": None}
    ] # Uma lista de dicionários / Uma variável composta dentro de outra. Palavras chaves: Name House Patronus

    for aluno in students:
        print(aluno["Name"], aluno["House"], aluno["Patronus"], sep=", ")

Saída:

    Hermione, Gryffindor, Otter
    Harry, Gryffindor, Stag
    Ron, Gryffindor, Jack Russel Terrir
    Draco, Slytherin, None
    