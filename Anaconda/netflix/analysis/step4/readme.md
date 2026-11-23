# Analyse exploratoir du catalogue de <a href="#"><img align="center" src="https://images.ctfassets.net/y2ske730sjqp/821Wg4N9hJD8vs5FBcCGg/9eaf66123397cc61be14e40174123c40/Vector__3_.svg?w=460" alt="netflix" height="24"></a><a href="../"><picture><source media="(prefers-color-scheme: dark)" srcset="https://cdn.simpleicons.org/jupyter/white"><source media="(prefers-color-scheme: light)" srcset="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg?utm_source=commons.wikimedia.org&utm_campaign=index&utm_content=original"><img src="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg" alt="Jupyter Notebook" height="64" align="right"></picture></a>
## 🎯 Objectif
> L’objectif de ce projet est d’explorer et de visualiser les données du catalogue Netflix afin de :
> - Comprendre la répartition des programmes par type (Films vs Séries).
> - Analyser l’évolution des acquisitions au fil des années.
> - Identifier les tendances de classification (`rating`) et leur impact sur la production.
---
## 🛠️ Outils et technologies
- **Python 3**
- **Bibliothèques principales** :
  - `pandas` → manipulation et préparation des données.
  - `numpy` → calculs numériques.
  - `matplotlib` & `seaborn` → visualisations descriptives et analytiques.
---
## 🔄 Étapes d’analyse (extrait)
### 1. Répartition des catégories de classification
- Analyse de la variable **`rating`** pour comprendre les restrictions d’âge et les usages.
- Visualisations :
  - Histogrammes (`matplotlib`).
  - Catplots (`seaborn`).
  - Diagrammes circulaires.
### 2. Analyse par type de programme
- Comparaison entre **Films** et **Séries** :
  - Distribution en volume.
  - Répartition en pourcentage.
- Visualisations :
  - Graphiques en barres (`seaborn`).
  - Diagrammes circulaires avec mise en évidence (`explode`).
### 3. Productions ajoutées par année
- Histogramme simple des ajouts annuels.
- Identification des périodes de forte croissance.
### 4. Répartition temporelle par type
- Étude de la proportion **Films vs Séries** par année.
- Calculs normalisés (%).
- Visualisation via :
  - Countplots segmentés par type.
  - Graphiques en barres empilées annotées (%).
## 📈 Résultats principaux
- Les **Films** constituent la majorité du catalogue.
- Les **Séries** occupent une place plus forte dans les contenus destinés à la jeunesse.
- Forte croissance des acquisitions après **2011**, avec un pic entre **2018 et 2020**.
- Diversification progressive et montée en puissance des séries au cours de la décennie.
## 🤝 Compétences démontrées
- Nettoyage et préparation de données réelles.
- Analyse descriptive et agrégation par catégories et périodes.
- Visualisations claires et adaptées (comparatif, temporel, proportionnel).
- **Data storytelling** : transformer des données brutes en insights lisibles pour décideurs et non-techniciens.
<!-- ## 🚀 Perspectives
- Étendre l’analyse aux **genres** et aux **pays de production**.
- Ajouter des visualisations interactives (`plotly`, `dash`).
- Développer un modèle prédictif pour anticiper les tendances futures de production. -->