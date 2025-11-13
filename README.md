# Classification d'images de tumeurs cérébrales par IRM

Ce projet vise à développer un modèle de classification d'images pour détecter et classer différents types de tumeurs cérébrales (gliome, méningiome, hypophysaire) ainsi que les cas sans tumeur, à partir d'images IRM.

## Structure du projet

Le répertoire `Classification image` contient les éléments suivants :

-   `CNN_TUMOR_MRI.ipynb` : Le notebook Jupyter principal contenant le code pour le chargement des données, la construction, l'entraînement et l'évaluation du modèle de réseau neuronal convolutif (CNN).
-   `matrice de confusion.png` : Image de la matrice de confusion des résultats du modèle.
-   `output.png` : Une image de sortie, potentiellement des résultats de prédiction ou des visualisations.
-   `Screenshot 2025-11-13 111543.png`, `Screenshot 2025-11-13 111809.png`, `tumor.png` : Captures d'écran ou exemples d'images liées au projet.

Le jeu de données est organisé comme suit dans le répertoire `DATA` (situé à la racine du projet `Computer vision`):

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

Chaque sous-dossier contient des images IRM correspondant à la catégorie de tumeur ou à l'absence de tumeur.

## Technologies utilisées

-   Python
-   TensorFlow / Keras (pour la construction et l'entraînement du modèle CNN)
-   Jupyter Notebook (pour le développement interactif)
-   NumPy, Matplotlib, scikit-learn (pour le traitement des données et l'évaluation)

## Comment exécuter le projet

1.  **Cloner le dépôt** (si ce n'est pas déjà fait) :
    ```bash
    git clone <URL_DU_DEPOT>
    cd Classification image
    ```
2.  **Installer les dépendances** :
    Assurez-vous d'avoir Python installé. Ensuite, installez les bibliothèques nécessaires :
    ```bash
    pip install tensorflow keras numpy matplotlib scikit-learn jupyter
    ```
3.  **Lancer Jupyter Notebook** :
    ```bash
    jupyter notebook
    ```
4.  **Ouvrir et exécuter le notebook** :
    Dans l'interface Jupyter, ouvrez `CNN_TUMOR_MRI.ipynb` et exécutez toutes les cellules pour entraîner le modèle et visualiser les résultats.

## Résultats

Les résultats de la classification, y compris la matrice de confusion et d'autres métriques de performance, sont générés et peuvent être visualisés dans le notebook et via les fichiers `.png` fournis.

## Auteur

[Votre Nom/Pseudo]
[Votre Contact ou Lien GitHub]
