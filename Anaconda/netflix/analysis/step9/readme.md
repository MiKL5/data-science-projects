# **Top 10 des catégories de** <a href="#"><img align="center" src="https://images.ctfassets.net/y2ske730sjqp/821Wg4N9hJD8vs5FBcCGg/9eaf66123397cc61be14e40174123c40/Vector__3_.svg?w=460" alt="netflix" height="30"></a><a href="../"><picture><source media="(prefers-color-scheme: dark)" srcset="https://cdn.simpleicons.org/jupyter/white"><source media="(prefers-color-scheme: light)" srcset="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg?utm_source=commons.wikimedia.org&utm_campaign=index&utm_content=original"><img src="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg" alt="Jupyter Notebook" height="64" align="right"></picture></a>
## **🎯 Objectifs**
- Extraire et normaliser les informations pays et catégories.
- Identifier les pays et catégories les plus productifs.
- Comparer la distribution films vs émissions pour les principaux pays producteurs.
- Produire des visualisations lisibles et prêtes pour présentation ou portfolio.
---
## **📚 Jeux de données et prérequis**
- `data` : DataFrame pandas contenant au minimum les colonnes `title`, `country`, `type`, `listed_in`.
- Librairies : `pandas`, `matplotlib`, `seaborn`.
- Environnement recommandé : Python 3.8+
---
## 💻Étapes et code clés 
### 1. Top 25 des pays producteurs 🌎
Séparer les cellules `country` contenant plusieurs pays, passer en format long et compter les occurrences.
```python
# séparer puis empiler
pays = data.set_index('title').country.str.split(',', expand=True).stack().reset_index(level=1, drop=True)
# top 25
top_25_pays = pays.value_counts().head(25)
# visualisation
plt.figure(figsize=(12, 8))
ax = sns.barplot(x=top_25_pays.values, y=top_25_pays.index, palette='viridis')
plt.title('Top 25 des pays producteurs')
plt.xlabel("Nombre d'occurrences")
plt.ylabel("Pays")
for container in ax.containers:
    ax.bar_label(container, fmt='%d', padding=3)
plt.tight_layout()
plt.show()
```
### 2. Productions par pays selon le type (Top 10 producteurs) 🎬📺
Filtrer sur les 10 pays les plus producteurs et comparer `Movie` vs `TV Show`.
```python
data_producteurs = data[(data['country']=="United States")|(data['country']=="India")
                      |(data['country']=="United Kingdom")|(data['country']=="Canada")
                      |(data['country']=="France")|(data['country']=="Japan")
                      |(data['country']=="Spain")|(data['country']=="South Korea")
                      |(data['country']=="Germany")|(data['country']=="Mexico")]

plt.figure(figsize=(11,6))
sns.countplot(x='country', hue='type', data=data_producteurs)
```
> Observation : Royaume-Uni, Japon et Corée du Sud affichent une proportion supérieure d'émissions (TV Shows) comparée aux films.
### 3. Top 10 des catégories de productions 🏆
Séparer la colonne `listed_in` (jusqu'à 3 catégories), passer en format long, compter et visualiser le top 10.
```python
top_categorie = data.set_index('title').listed_in.str.split(', ', expand=True).stack().reset_index(level=1, drop=True)
top10 = top_categorie.value_counts().index[:10]

plt.figure(figsize=(12, 8))
sns.countplot(y=top_categorie, order=top10, palette='turbo')
plt.title('Top 10 des catégories', fontsize=16)
plt.xlabel("Nombre d'occurrences")
plt.ylabel("Catégorie")
plt.show()
```
## **📊 Résultats clés**
- Top 25 pays identifiés et visualisés.  
- 5 269 productions provenant des 10 principaux pays producteurs.  
- Différences pays/type : Royaume-Uni, Japon et Corée du Sud favorisent les émissions.  
- Top 10 catégories extraites et visualisées.  
## **🤝 Compétences démontrées**
- Manipulation avancée de `pandas` (split, stack, reset_index, value_counts).  
- Visualisation avec `seaborn` et `matplotlib`.  
- Préparation de données multi-valeurs et index multi-niveaux.  
- Communication des résultats pour pairs et recruteurs.
<!-- ## **🚀 Perspectives d'amélioration**
- Normalisation des libellés pays et détection des doublons (USA / United States).  
- Nettoyage sémantique des catégories (synonymes, pluriels).  
- Calculs de ratios films/TV par pays.  
- Ajout de colonnes temporelles et analyses de tendance.  
- Passage à des visualisations interactives pour exploration (plotly, dash, streamlit).  
- Transformer l'analyse en pipeline reproductible avec scripts et notebooks.
---
##  **🔄 Reproduire l'analyse**
1. Charger le CSV/JSON dans `data` (pandas).  
2. Exécuter les cellules dans l'ordre indiqué ci-dessus.  
3. Sauvegarder les figures avec `plt.savefig(...)` pour inclusion dans rapports ou README. -->