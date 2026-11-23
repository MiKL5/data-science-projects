# **Analyse de données de** <a href="#"><img align="center" src="https://images.ctfassets.net/y2ske730sjqp/821Wg4N9hJD8vs5FBcCGg/9eaf66123397cc61be14e40174123c40/Vector__3_.svg?w=460" alt="netflix" height="36px"></a><a href="../"><picture><source media="(prefers-color-scheme: dark)" srcset="https://cdn.simpleicons.org/jupyter/white"><source media="(prefers-color-scheme: light)" srcset="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg?utm_source=commons.wikimedia.org&utm_campaign=index&utm_content=original"><img src="https://upload.wikimedia.org/wikipedia/commons/3/38/Jupyter_logo.svg" alt="Jupyter Notebook" height="64" align="right"></picture></a>

> Ce projet explore les données des films et séries disponibles sur Netflix, en utilisant des techniques d'analyse de données et de visualisation pour identifier des tendances, des préférences par pays, et des évolutions au fil du temps.

---

## 📌 Contexte
Ce projet vise à :
- Analyser la répartition des films et séries par pays.
- Identifier les tendances de production au fil des années.
- Explorer les genres les plus populaires.

---

## 📦 Dépendances
Pour exécuter ce projet, installez les librairies :
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

---

## 🔧 Étapes Clés

### 1. **Chargement et Prétraitement des Données**
- Lecture du fichier CSV contenant les données Netflix.
- Nettoyage des valeurs manquantes et des doublons.
- Conversion des colonnes de dates en format exploitable.

```python
import pandas as pd
data = pd.read_csv("netflix_data.csv")
data['date_added'] = pd.to_datetime(data['date_added'], errors='coerce')
```

### 2. **Analyse Exploratoire**
- Statistiques descriptives (nombre de films vs séries, répartition par pays).
- Visualisation des tendances de production par année.

```python
import matplotlib.pyplot as plt
data['year_added'] = data['date_added'].dt.year
data['year_added'].value_counts().sort_index().plot(kind='bar')
plt.title("Nombre de contenus ajoutés par année")
plt.show()
```

### 3. **Visualisation des Résultats**
- Cartes et graphiques pour illustrer les résultats :
  - Répartition des contenus par pays.
  - Évolution des genres au fil du temps.

---

## 📈 Résultats
- **Top 5 des pays producteurs** : États-Unis, Inde, Royaume-Uni, Japon, Corée du Sud.
- **Année avec le plus de contenus ajoutés** : 2020.
- **Genres dominants** : Documentaires, Comédies, Dramas.
<!-- 
---

## 👤 Auteur
- **Mickael Gaillard**
- Date : 29/08/2025 -->