# Analyse des Données <a href="#"><img align="center" src="https://images.ctfassets.net/y2ske730sjqp/821Wg4N9hJD8vs5FBcCGg/9eaf66123397cc61be14e40174123c40/Vector__3_.svg?w=460" alt="netflix" height="36px"></a><a href="../"><picture><source media="(prefers-color-scheme: dark)" srcset="https://cdn.simpleicons.org/jupyter/white"><source media="(prefers-color-scheme: light)" srcset="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg?utm_source=commons.wikimedia.org&utm_campaign=index&utm_content=original"><img src="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg" alt="Jupyter Notebook" height="64" align="right"></picture></a>
Analyse d'un jeu de données de Netflix pour visualiser la répartition des types de programmes (films et séries).
## Description
Les bibliothèques `pandas`, `seaborn`, et `matplotlib` servent à l'analyse et la visualisation des données.
### Visualisations
1. **Graphique en barres** :
   - Utilise `sns.catplot` pour montrer le nombre de films et de séries.
   - Une palette de couleurs personnalisée (bleu et orange) est utilisée.
2. **Diagramme circulaire** :
   - Montre la répartition en pourcentage des types de programmes.
   - Utilise `plot.pie` pour afficher les pourcentages, avec des options pour les ombres, les couleurs, et un titre.
### Calculs
- **Fréquences relatives** :
  - Calcule les fréquences relatives des types de programmes avec `value_counts(normalize=True)`. 
  - Convertit ces fréquences en pourcentages.