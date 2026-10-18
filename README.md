# Generative Models

## Rapport d'avancement

Dans le cadre de cette activité pratique, les premières étapes de mise en place et
d'expérimentation ont été réalisées dans le notebook
[`modeles_generatifs.ipynb`](./modeles_generatifs.ipynb).

### Travaux réalisés

- Installation et importation des bibliothèques nécessaires, notamment PyTorch,
  Torchvision, NumPy et Matplotlib.
- Vérification de l'environnement d'exécution : PyTorch `2.14.1` fonctionne
  actuellement sur le processeur (`CPU`).
- Téléchargement et chargement du jeu de données **MNIST** à l'aide de
  Torchvision.
- Prétraitement des images avec `ToTensor` et préparation des
  `DataLoader` d'entraînement et de test, avec une taille de lot de 128.
- Création d'un premier modèle **discriminatif** pour reconnaître les chiffres
  manuscrits. Le réseau est composé d'une transformation `Flatten`, d'une couche
  linéaire de 784 à 128 neurones, d'une activation ReLU et d'une couche de sortie
  de 10 classes.
- Entraînement du modèle pendant 3 époques avec la fonction de perte
  `CrossEntropyLoss` et l'optimiseur Adam.
- Évaluation sur le jeu de test, jamais utilisé pendant l'entraînement :
  le modèle atteint une précision de **96,14 %**.
- Visualisation de plusieurs prédictions afin de comparer les classes réelles et
  les classes prédites.

Cette première partie permet de valider l'environnement, la préparation des
données et le fonctionnement d'un modèle de classification de référence avant
de passer à la construction et à l'évaluation des modèles génératifs.
