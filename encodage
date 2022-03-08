import json
fichier = "data.json"
liste_nb = []
liste_code = []
reponse = ''

while True:
    reponse = input(' Tapez 1 pour modifier la clef, Tapez 2 pour encoder des caratères')

    if reponse == '1':
        key = 0
        key = input("Clef ? (nombre uniquement)")
        if key.isdigit():
            print('ok')
            with open(fichier, 'w') as f:
                json.dump(key, f)
            continue
        else:
            print("Veuillez mettre une clef valide, merci !")
            continue

    elif reponse == '2':
        message = input("message a codé : ")
        liste = list(message)

        for i in liste:
            a = int(ord(i))
            with open(fichier, 'r') as f:
                key = json.load(f)
            liste_nb.append(int(key) + a)

        for b in liste_nb:
            liste_code.append(chr(b))
        print("".join(map(str, liste_code)))
        exit()

    else:
        print("Veuillez mettre une clef valide, merci !")
        exit()
