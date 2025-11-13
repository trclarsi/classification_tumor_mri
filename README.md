# Classification des Tumeurs Cérébrales par IRM avec CNN

![Python 3.9+](https://img.shields.io/badge/Python-3.9%2B-blue.svg)

Ce projet a pour but de développer un modèle de classification d'images basé sur un réseau de neurones convolutif (CNN) pour identifier et classer différents types de tumeurs cérébrales (gliome, méningiome, pituitaire) ainsi que des images saines à partir d'images par résonance magnétique (IRM). Ce projet est réalisé dans un cadre académique.

## Table des matières

-   [Structure du projet](#structure-du-projet)
-   [Jeu de données](#jeu-de-données)
-   [Architecture du modèle](#architecture-du-modèle)
-   [Technologies utilisées](#technologies-utilisées)
-   [Installation et exécution](#installation-et-exécution)
-   [Résultats attendus](#résultats-attendus)
-   [Utilisation du modèle](#utilisation-du-modèle)
-   [Auteur](#auteur)

## Structure du projet

Le répertoire `Classification image` contient les éléments suivants :

-   `CNN_TUMOR_MRI.ipynb` : Le notebook Jupyter principal contenant le code pour le chargement des données, la construction, l'entraînement et l'évaluation du modèle.
-   `matrice de confusion.png` : Image de la matrice de confusion illustrant les performances du modèle.
-   `output.png` : Une image de sortie, potentiellement des exemples de prédictions ou des visualisations.
-   `README.md` : Ce fichier.

## Jeu de données

Le jeu de données est situé dans le répertoire `DATA` (à la racine du projet `Computer vision`) et est structuré comme suit :

```
DATA/
├── Testing/
│   ├── glioma_tumor/
│   ├── meningioma_tumor/
│   ├── no_tumor/
│   └── pituitary_tumor/
└── Training/
    ├── glioma_tumor/
    ├── meningioma_tumor/
    ├── no_tumor/
    └── pituitary_tumor/
```

Chaque sous-dossier contient des images IRM correspondant à l'une des quatre catégories.

## Architecture du modèle

Le modèle est un réseau de neurones convolutif (CNN) construit avec TensorFlow/Keras. L'architecture typique comprend :

-   Plusieurs couches de convolution (`Conv2D`) pour l'extraction de caractéristiques.
-   Des couches de Max-Pooling (`MaxPooling2D`) pour réduire la dimensionnalité.
-   Des couches de `Dropout` pour prévenir le sur-apprentissage.
-   Une couche `Flatten` pour transformer les cartes de caractéristiques en un vecteur.
-   Des couches `Dense` pour la classification finale.

L'architecture détaillée est disponible dans le notebook `CNN_TUMOR_MRI.ipynb`.

## Technologies utilisées

-   Python 3.9+
-   TensorFlow / Keras
-   Jupyter Notebook
-   NumPy, Pandas
-   Matplotlib, Seaborn
-   Scikit-learn

## Installation et exécution

1.  **Cloner le dépôt** (si ce n'est pas déjà fait) :
    ```bash
    git clone <URL_DU_DEPOT>
    cd Classification image
    ```
2.  **Installer les dépendances** :
    Assurez-vous d'avoir Python installé. Ensuite, installez les bibliothèques nécessaires :
    ```bash
    pip install tensorflow keras numpy matplotlib scikit-learn jupyter pandas seaborn
    ```

3.  **Lancer Jupyter Notebook** :
    ```bash
    jupyter notebook
    ```
4.  **Ouvrir et exécuter le notebook** :
    Dans l'interface Jupyter, ouvrez `CNN_TUMOR_MRI.ipynb` et exécutez toutes les cellules pour entraîner le modèle et visualiser les résultats.

## Résultats attendus

L'exécution du notebook produira :

-   L'entraînement du modèle sur les données d'apprentissage.
-   L'évaluation du modèle sur les données de test.
-   Des métriques de performance telles que :
    -   La précision (accuracy)
    -   La perte (loss)
    -   La matrice de confusion
    -   Le rapport de classification (précision, rappel, F1-score par classe)
-   Des visualisations des courbes d'apprentissage et des exemples de prédictions.

## Utilisation du modèle

Une fois le modèle entraîné et sauvegardé (par exemple, au format `.h5` ou `.keras`), il peut être chargé pour faire des prédictions sur de nouvelles images IRM. Une fonction de prédiction peut être implémentée pour :

1.  Prétraiter l'image d'entrée (redimensionnement, normalisation).
2.  Charger le modèle pré-entraîné.
3.  Prédire la classe de l'image.
4.  Retourner la classe prédite (par exemple, "gliome", "pas de tumeur", etc.).

Des exemples de code pour cela peuvent être ajoutés à la fin du notebook.
