# Tendance des acquisitions de <a href="#"><img align="center" src="https://images.ctfassets.net/y2ske730sjqp/821Wg4N9hJD8vs5FBcCGg/9eaf66123397cc61be14e40174123c40/Vector__3_.svg?w=460" alt="netflix" height="24"></a><a href="../"><picture><source media="(prefers-color-scheme: dark)" srcset="https://cdn.simpleicons.org/jupyter/white"><source media="(prefers-color-scheme: light)" srcset="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg?utm_source=commons.wikimedia.org&utm_campaign=index&utm_content=original"><img src="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg" alt="Jupyter Notebook" height="64" align="right"></picture></a>
## 🎯 Objectif
> Étudier l’évolution du catalogue Netflix entre 2011 et 2021 en mettant en évidence :
> - Les tendances de production (films vs séries).
> - La répartition par catégories de contenu (`rating`).
> - Les dynamiques temporelles d’acquisition de contenu.
## 🛠️ Outils et technologies
- **Python 3**
- **Bibliothèques utilisées** :
  - `pandas` → manipulation et agrégation des données.
  - `numpy` → opérations numériques.
  - `matplotlib` et `seaborn` → visualisations descriptives.
  - `plotly.express` → graphiques interactifs.
___
## 🔄 Étapes d’analyse (extrait du projet)
### 1. Analyse des classifications (`rating`)
- Étude de la distribution des catégories de censure et d’âge.
- Visualisation via :
  - Histogrammes (`matplotlib`).
  - Diagrammes circulaires (`pandas.plot.pie`).
  - Catplots (`seaborn`).
### 2. Répartition par type de production
- Films vs Séries TV.
- Comparaison en fréquence et en pourcentage.
- Visualisations :
  - Graphiques en barres.
  - Diagrammes circulaires avec surlignage (`explode`).
### 3. Dynamique temporelle
- Nombre de contenus ajoutés par année.
- Croissance significative à partir de 2011.
- Visualisation :
  - Histogrammes par année.
  - Countplots segmentés par type (`seaborn`).
### 4. Répartition annuelle par type (%)
- Transformation en **tableau croisé dynamique** (`pivot`).
- Graphiques en barres empilées avec annotations de pourcentages.
- Mise en avant de l’évolution des parts de marché Films vs Séries.
### 5. Tendance des acquisitions 2011–2021
- Agrégation des données par année et par type.
- Visualisation avec **`plotly.express.line`** pour un rendu interactif.
___
## 📈 Résultats clés
- **Films** dominent largement le catalogue global.
- **Séries** sont plus présentes dans les contenus jeunesse.
- Forte **croissance des acquisitions à partir de 2011**, avec un pic 2018–2020.
- Diversification progressive des types de productions et montée en puissance des séries.
---
## 🤝 Compétences démontrées
- Préparation et nettoyage des données.
- Analyses descriptives avancées.
- Visualisations statistiques et interactives.
- Storytelling orienté données (transformer des données brutes en insights exploitables).
---
## 🚀 Perspectives
- Étendre l’analyse par **pays de production**.
- Croiser avec d’autres sources (IMDB, Rotten Tomatoes).
- Construire un **modèle prédictif** sur les acquisitions futures.
- Explorer les **corrélations entre genres, ratings et tendances temporelles**.