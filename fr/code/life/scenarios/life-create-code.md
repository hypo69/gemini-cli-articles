Dans le répertoire `game`, créez le fichier life.py.
À l'intérieur, écrivez l'implémentation du "Jeu de la Vie" de Conway en Python, en utilisant une approche orientée objet.
Utilisez les bibliothèques : `numpy`, `pygame` (pour les graphiques).


Exigences :
1.  Créez une classe `Game`.
2.  Dans `__init__`, la classe doit prendre les dimensions de la grille (largeur, hauteur) et créer un champ initial aléatoire.
3.  Créez une méthode `step()` qui met à jour l'état du jeu d'un pas selon les règles :
    - Une cellule vivante avec < 2 voisins vivants meurt (sous-population).
    - Une cellule vivante avec 2 ou 3 voisins vivants survit.
    - Une cellule vivante avec > 3 voisins vivants meurt (surpopulation).
    - Une cellule morte avec exactement 3 voisins vivants devient vivante (reproduction).
4.  Créez une méthode `display()` ou remplacez `__str__` pour afficher le champ dans la console. Utilisez des symboles, par exemple '■' pour une cellule vivante et ' ' pour une cellule morte.
5.  Utilisez la bibliothèque `numpy` pour des opérations de grille efficaces.
6.  Dans le bloc `if __name__ == '__main__':`, ajoutez un exemple qui crée un jeu et exécute la simulation en boucle avec un petit délai entre les étapes.
7. Utilisez pygame ou une autre bibliothèque graphique pour la visualisation du jeu, si possible.