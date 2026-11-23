# **Analyse des Données de** <a href="#"><img align="center" src="https://images.ctfassets.net/y2ske730sjqp/821Wg4N9hJD8vs5FBcCGg/9eaf66123397cc61be14e40174123c40/Vector__3_.svg?w=460" alt="netflix" height="36px"></a><a href="../"><picture><source media="(prefers-color-scheme: dark)" srcset="https://cdn.simpleicons.org/jupyter/white"><source media="(prefers-color-scheme: light)" srcset="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg?utm_source=commons.wikimedia.org&utm_campaign=index&utm_content=original"><img src="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg" alt="Jupyter Notebook" height="64" align="right"></picture></a>
<!-- 
## Sommaire
- [Objectif](#objectif)
- [Étapes principales du traitement](#étapes-principales-du-traitement)  
  - [1. Extraction et transformation des données](#1-extraction-et-transformation-des-données)  
  - [2. Analyse des pays producteurs](#2-analyse-des-pays-producteurs)  
  - [3. Visualisation du Top 25](#3-visualisation-du-top-25)  
  - [4. Visualisation du Top 15 avec style personnalisé](#4-visualisation-du-top-15-avec-style-personnalisé)  
- [Compétences démontrées](#compétences-démontrées)   -->
<!-- - [Perspectives d’amélioration](#perspectives-damélioration)
--- -->

## Objectif
Extraire, transformer et visualiser les données liées aux pays producteurs présents dans la base, afin d’identifier les pays les plus représentés et de produire des visualisations exploitables pour l’analyse.
---
## Étapes principales du traitement
### 1. Extraction et transformation des données
- **Séparation des pays** contenus dans une même cellule en plusieurs colonnes avec `str.split(',', expand=True)`.  
- **Conversion en format long** avec `.stack()`, afin d’obtenir une ligne par pays et par titre.  
- **Nettoyage de l’index** avec `reset_index(level=1, drop=True)` pour simplifier la structure.  
```python
pays = data.set_index('title').country.str.split(',', expand=True).stack().reset_index(level=1, drop=True)
```
➡️ Résultat : chaque film/série est lié à un ou plusieurs pays, chacun apparaissant dans une ligne distincte.
### 2. Analyse des pays producteurs
- **Comptage des occurrences** par pays avec `value_counts()`.  
- Extraction des **25 pays les plus producteurs**.  
```python
top_25_pays = pays.value_counts().head(25)
```
### 3. Visualisation du Top 25
- **Graphique en barres horizontales** avec Seaborn (`sns.barplot`).  
- Affichage des **valeurs directement sur les barres** avec `ax.bar_label`.  
- Palette utilisée : `viridis` pour une meilleure lisibilité.  
### 4. Visualisation du Top 15 avec style personnalisé
- **Graphique en barres verticales** avec `sns.countplot`.  
- Mise en forme avancée :  
  - **Fond noir** pour l’esthétique.  
  - Titres et labels colorés en blanc.  
  - **Annotations** : affichage du nombre de productions directement sur les barres.  
  - Palette utilisée : `turbo` pour un rendu contrasté et dynamique.  
## Compétences démontrées
- Manipulation avancée de **pandas** (`split`, `stack`, `reset_index`, `value_counts`).  
- Visualisation avec **Seaborn** et personnalisation poussée des graphiques :  
  - ajout de labels dynamiques  
  - modification des couleurs de fond et des textes  
- Analyse descriptive appliquée à un dataset complexe.  
- Production de résultats **clairs, interprétables et présentables** pour des décideurs ou des chercheurs.  
<!-- ## Perspectives d’amélioration 🚀
- Normalisation des noms de pays (ex. : gérer les doublons comme "USA" vs "United States").  
- Analyse temporelle des productions par pays.  
- Visualisation interactive (ex. : `plotly`, `dash`, `streamlit`).  
- Comparaison des tendances pays par genres ou catégories.   -->
<!-- ---
👉 Ce travail illustre la capacité à **transformer des données brutes en insights visuels exploitables**, compétence clé pour un **Data Scientist / Data Analyst**.   -->