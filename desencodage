import json
fichier = 'data.json'
reponse, message = '', ''
liste, liste_nb, liste_code = [], [], []
key = 1

while True:
    reponse = input(' Tapez 1 pour modifier la clef, Tapez 2 pour desencoder des caratères')


    if reponse == '1':
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
        message = input('message a décodé : ')
        liste = list(message)
        for i in liste:
            a = int(ord(i))
            with open(fichier, 'r') as f:
                key = json.load(f)
            liste_nb.append(a - int(key))
        
        for b in liste_nb:
            liste_code.append(chr(b))
        print("".join(map(str, liste_code)))
        exit()
    else :
        print("Veuillez mettre une clef valide, merci !")
        exit()
