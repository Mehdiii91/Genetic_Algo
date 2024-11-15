
# README - Optimisation des Ventes par Algorithme Génétique

## 📋 Description du Projet
Ce projet vise à optimiser le budget publicitaire pour maximiser les ventes dans un magasin à l'aide d'un **algorithme génétique**. Le modèle repose sur un ensemble de données représentant des produits avec leurs caractéristiques : **quantités vendues**, **prix unitaire**, **coût unitaire**, **avis clients** et **budget publicitaire**. L'objectif est de trouver la meilleure stratégie publicitaire qui maximise les ventes globales.

### ⚙️ Technologies Utilisées
- **Python 3.8+**
- **Bibliothèques :**
  - `pandas` : Manipulation des données
  - `numpy` : Calcul numérique
  - `matplotlib` et `seaborn` : Visualisation des données
  - `sklearn` : Modélisation de la régression
  - `random` : Pour les choix aléatoires dans l'algorithme génétique

## 📈 Analyse Quantitative des Résultats
Le modèle a été évalué en utilisant des métriques quantitatives pour mesurer sa performance :

- **Mean Squared Error (MSE)** : 772,810.43
  - Cette erreur quadratique moyenne montre une certaine dispersion des prédictions par rapport aux valeurs réelles. Une erreur élevée indique une marge d'amélioration possible.
- **Coefficient de détermination (R²)** : 0.87
  - Le R² de 0.87 indique que le modèle explique **87 % de la variance** des ventes observées. C'est un bon indicateur de performance, montrant que le modèle est capable de capturer la majorité des variations des données.

### Analyse de Convergence
L'algorithme génétique a été exécuté sur **200 générations** avec une taille de population de **50 individus**. Les résultats montrent une amélioration progressive de la fitness jusqu'à la génération 190, où la convergence est atteinte.

- **Meilleure Fitness Initiale (Génération 0)** : 574,764.01
- **Meilleure Fitness Finale (Génération 190)** : 578,084.55
- **Amélioration Totale** : Environ **0.58 %** d'augmentation de la fitness, montrant que l'algorithme continue de progresser même après 100 générations.

### Graphique d'Évolution
Un graphique d'évolution de la fitness montre une augmentation continue de la performance jusqu'à la convergence, illustrant l'efficacité de l'algorithme.

## 📊 Analyse Exploratoire des Données (EDA)
Une analyse exploratoire des données a été réalisée avant la modélisation pour comprendre les corrélations et la distribution des variables :

- **Corrélations importantes :**
  - **Avis Client ↔ Ventes** : Corrélation positive de **0.65**, montrant l'impact significatif des avis sur les ventes.
  - **Publicité ↔ Ventes** : Corrélation de **0.58**, indiquant une influence notable du budget publicitaire.
- **Données manquantes** : Aucun problème de données manquantes n'a été détecté.
- **Distribution des ventes** : L'analyse de la distribution montre une asymétrie positive, indiquant que la majorité des ventes sont concentrées sur des valeurs faibles à moyennes.

## 🧠 Modélisation
Deux approches ont été utilisées pour résoudre le problème :

1. **Régression Linéaire**
   - Le modèle de régression linéaire a servi de base pour évaluer l'impact de chaque variable sur les ventes.
   - **Métriques :**
     - MSE : 772,810.43
     - R² : 0.87

2. **Algorithme Génétique**
   - L'algorithme génétique a été implémenté pour optimiser le budget publicitaire et maximiser les ventes.
   - **Taille de la population** : 50
   - **Nombre de générations** : 200
   - **Mutation Rate** : 0.1
   - **Sélection par élitisme** : Les meilleurs chromosomes sont conservés pour garantir une amélioration continue.

### Stratégies de Sélection
- **Crossover** : Combine les gènes des parents pour créer un enfant, permettant une exploration efficace de l'espace de recherche.
- **Mutation** : Introduit des variations aléatoires pour éviter la stagnation dans des solutions locales.
- **Réinitialisation partielle** : Utilisée pour réintroduire de la diversité dans la population lorsque la convergence est détectée.

## 📂 Structure du Projet
```
├── data/
│   └── sales_data_simplified.csv
├── notebooks/
│   └── Genetic_Algorithm_Optimization.ipynb
├── scripts/
│   └── genetic_algorithm.py
├── README.md
├── requirements.txt
└── results/
    ├── fitness_evolution.png
    └── model_performance.png
```

## 🚀 Instructions d'Installation
1. **Cloner le projet :**
   ```bash
   git clone https://github.com/votre-repo/genetic-sales-optimization.git
   cd genetic-sales-optimization
   ```

2. **Installer les dépendances :**
   ```bash
   pip install -r requirements.txt
   ```

3. **Exécuter le Jupyter Notebook pour l'analyse :**
   ```bash
   jupyter notebook notebooks/Genetic_Algorithm_Optimization.ipynb
   ```

4. **Exécuter le script de l'algorithme génétique :**
   ```bash
   python scripts/genetic_algorithm.py
   ```

## 📋 Limitations et Améliorations Futures
- **Surapprentissage** : Possibilité de surapprentissage si le modèle est sur-ajusté aux données.
- **Évolution plus rapide** : Augmenter le taux de mutation ou introduire des mécanismes d'adaptation pour accélérer la convergence.
- **Données supplémentaires** : Ajouter des variables externes (saison, concurrence) pour améliorer la prédiction des ventes.

## 📈 Conclusion
Le projet montre comment un algorithme génétique peut être utilisé pour optimiser une stratégie publicitaire et maximiser les ventes. Les résultats indiquent une amélioration progressive des performances et démontrent la capacité de l'algorithme à converger vers une solution optimale.

---

Pour toute question, veuillez contacter : **votre-email@example.com**
