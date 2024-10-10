# Evaluation git

def calculer_moyenne():
    # Initialiser une liste pour stocker les nombres
    nombres = []

    print("Entrez les nombres pour calculer la moyenne (entrez 'q' pour quitter) :")

    while True:
        # Demander à l'utilisateur d'entrer un nombre ou 'q' pour quitter
        entree = input("Nombre : ")

        if entree.lower() == 'q':
            break  # Quitter la boucle si l'utilisateur entre 'q'

        try:
            # Convertir l'entrée en nombre flottant et l'ajouter à la liste
            nombre = float(entree)
            nombres.append(nombre)
        except ValueError:
            print("Veuillez entrer un nombre valide.")

    # Calculer la moyenne
    if nombres:
        moyenne = sum(nombres) / len(nombres)
        print(f"La moyenne des nombres saisis est : {moyenne:.2f}")
    else:
        print("Aucun nombre n'a été saisi.")

# Appeler la fonction pour exécuter le programme
calculer_moyenne()

