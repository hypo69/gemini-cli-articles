# Projet "Jeu de la Vie"

## Brève description

Ce projet est une implémentation de l'automate cellulaire "Jeu de la Vie" de Conway en Python. Le jeu simule l'évolution d'une population de cellules sur une grille bidimensionnelle, où l'état de chaque cellule (vivante ou morte) change en fonction de l'état de ses voisins.

## Structure des fichiers

-   `life.py`: Le fichier principal contenant l'implémentation de la classe `Game`, qui gère la logique de simulation du "Jeu de la Vie" et sa visualisation graphique à l'aide de la bibliothèque `pygame`.
-   `test_life.py`: Un fichier avec des tests unitaires pour la classe `Game`, utilisant le framework `pytest`. Comprend un test pour vérifier l'évolution de l'oscillateur "Blinker".

## Comment lancer la simulation

Pour lancer la simulation du "Jeu de la Vie", assurez-vous d'avoir installé les bibliothèques nécessaires (`numpy` et `pygame`). Si ce n'est pas le cas, installez-les:

```bash
pip install numpy pygame
```

Ensuite, lancez le fichier principal:

```bash
python game/life.py
```

## Comment lancer les tests

Pour lancer les tests, vous devez installer `pytest` et `numpy`:

```bash
pip install pytest numpy
```

Ensuite, lancez les tests, en spécifiant le chemin du fichier de test:

```bash
pytest game/test_life.py
```