# Méthodes statistiques pour les données qualitatives - Analyse des champignons comestibles/toxiques

Ce projet vise à analyser un jeu de données qualitatives décrivant des caractéristiques morphologiques de champignons pour déterminer leur comestibilité. Il combine des techniques statistiques avancées (ACM, CAH, analyse discriminante) afin d'identifier des motifs discriminants entre espèces comestibles et toxiques.

##  Jeu de données

Le dataset **Mushroom** contient 8 124 échantillons décrits par **22 variables qualitatives** (forme, couleur, texture, etc.) avec une variable cible binaire : `edible` (comestible) ou `poisonous` (toxique).

**Variables clés** :
- `cap-shape`, `cap-color`, `odor`, `gill-color`, `spore-print-color`, etc.
- **Prétraitement** : Suppression/regroupement de modalités rares (ex: `grooves` dans `cap-surface`).

[Voir la description complète des variables](https://github.com/amenallah01/Methodes-statistiques-pour-les-donnees-qualitatives/blob/main/KRISSAAN_BACHA.pdf)

##  Méthodologie

1. **Statistique descriptive** : Analyse des distributions et déséquilibres.
2. **Analyse des Correspondances Multiples (ACM)** : Réduction de dimension pour visualiser les relations entre modalités.
3. **Classification non supervisée (CAH)** : Regroupement des individus en clusters homogènes.
4. **Analyse discriminante** : Validation des axes factoriels pour différencier les classes.
5. **k-NN (k plus proches voisins)** : Classification supervisée avec une précision de 100%.

##  Résultats clés

- **ACM** : Les axes 1 et 2 séparent clairement les champignons comestibles (associés à `habitat=leaves`, `gill-color=buff`) des toxiques (liés à `spore-print-color=chocolate`, `stalk-root=bulbous`).
- **CAH** : Trois clusters identifiés, correspondant aux classes comestible/toxique et une zone intermédiaire.
- **Modèle k-NN** : Aucune erreur de classification, confirmant la séparabilité des données.

## ⚙️ Installation

1. Clonez le dépôt :
   ```bash
   git clone https://github.com/Krissaan-amen/Methodes-statistiques-pour-les-donnees-qualitatives.git
   ```
2. Installez les dépendances :
   ```bash
   pip install -r requirements.txt
   ```
3. Exécutez les notebooks Jupyter :
   - `Descriptive_Analysis.ipynb` : Statistiques descriptives et prétraitement.
   - `ACM_Clustering.ipynb` : Analyse factorielle et classification.
   - `Discriminant_Analysis.ipynb` : Validation des modèles.

## Structure du projet

```
.
├── data/                   # Jeu de données Mushroom
├── notebooks/              # Analyses et visualisations
├── reports/                # Rapport détaillé (PDF)
├── requirements.txt        # Dépendances
└── README.md
```

## Contributeurs

- **Krissaan Amen Allah**
  [ amen.krissaan@gmail.com](mailto:amen.krissaan@gmail.com)

## License

This project is for educational and research purposes. Please cite appropriately if used in academic work.

---

*This project demonstrates the intersection of traditional database management with modern machine learning techniques, showcasing practical skills in both domains.*
