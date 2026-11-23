# **Analyse des productions de <a href="#"><img align="center" src="https://images.ctfassets.net/y2ske730sjqp/821Wg4N9hJD8vs5FBcCGg/9eaf66123397cc61be14e40174123c40/Vector__3_.svg?w=460" alt="netflix" height="24"></a><br>par type et catégorie d’évaluation**<a href="../"><picture><source media="(prefers-color-scheme: dark)" srcset="https://cdn.simpleicons.org/jupyter/white"><source media="(prefers-color-scheme: light)" srcset="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg?utm_source=commons.wikimedia.org&utm_campaign=index&utm_content=original"><img src="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg" alt="Jupyter Notebook" height="64" align="right"></picture></a>
## 🎯 Objectif
> Ce projet explore et visualise le catalogue Netflix afin d’identifier des tendances de production, de distribution par catégories et d’évolution temporelle.  
L’approche combine **nettoyage de données, analyses statistiques et visualisations interactives**.
---
## 🛠️ Stack technique
- **Python 3**
- **Bibliothèques principales** :
  - `pandas` : manipulation et nettoyage des données
  - `numpy` : calculs numériques
  - `matplotlib` et `seaborn` : visualisations statistiques
  - `plotly` : graphiques interactifs
## 🔄 Étapes principales
### 1. Nettoyage
- Suppression des colonnes inutiles (`show_id`).
- Gestion des valeurs manquantes :
  - Suppression ou imputation selon le contexte.
  - Exemple : remplacement des `NaN` de `rating` par la modalité la plus fréquente.
- Conversion des dates (`date_added`) en format exploitable.
- Création d’une nouvelle variable `year_added`.
### 2. Analyse descriptive
- Étude de la variable **`rating`** (catégories de censure et classification par public).
- Analyse des **types de productions** (films vs séries).
- Identification des **doublons** et nettoyage complémentaire.
### 3. Visualisations clés
- **Distribution des catégories (`rating`)**
  - Histogrammes, barres et diagrammes circulaires.
- **Types de production (Film vs TV Show)**
  - Comparaison en fréquence et en pourcentage.
- **Évolution temporelle**
  - Nombre de productions ajoutées par année.
  - Répartition par type (stacked bar charts avec pourcentages).
- **Analyse 2011–2021**
  - Tendance des acquisitions via `Plotly` (graphique interactif).
- **Production par catégorie et type**
  - Comparaison Film/Série selon les classifications d’âge.
## 📈 Résultats principaux
- Les **films** dominent largement dans la majorité des catégories.
- Les **séries** sont plus présentes dans les contenus destinés aux enfants.
- Forte **croissance des acquisitions à partir de 2011**, avec un pic notable entre 2018 et 2020.
- La stratégie Netflix montre une diversification croissante des contenus et une internationalisation des pays de production.
---
## 🤝 Compétences démontrées
- Nettoyage avancé de données (gestion des valeurs manquantes, normalisation).
- Analyse descriptive et exploratoire.
- Visualisations statiques et interactives.
- Storytelling data : transformer des données brutes en **insights stratégiques**.
---
<!-- ## 🚀 Perspectives
- Étendre l’analyse par **pays de production**.
- Intégrer des **modèles prédictifs** pour anticiper les tendances futures.
- Croiser avec d’autres datasets (IMDB, Rotten Tomatoes) pour enrichir les insights. -->