# **Création de vecteur**<a href="../"><img align="right" src="https://github.com/MiKL5/python/blob/main/assets/logo/NumPy_2020.svg" alt="Numpy" height="64px"></a>
Il y a plusieurs manières de créer des vecteurs.

1️⃣ Avec Python pur (listes et compréhension)
```py
# Liste initiale
lst = [1, 2, 3, 4, 5]

# 1.1 Conversion directe en "vecteur" (liste Python)
vecteur = list(lst)
print(vecteur)  # [1, 2, 3, 4, 5]

# 1.2 Avec compréhension de liste (utile si transformation)
vecteur2 = [x*2 for x in lst]
print(vecteur2)  # [2, 4, 6, 8, 10]
```
⚠️ Ici, un "vecteur" n’est qu’une liste Python. Pas de calcul vectoriel natif.

2️⃣ Avec NumPy (le plus courant pour le calcul scientifique)
```py
import numpy as np

lst = [1, 2, 3, 4, 5]

# 2.1 Créer un vecteur 1D
vecteur_np = np.array(lst)
print(vecteur_np)  # [1 2 3 4 5]
print(type(vecteur_np))  # <class 'numpy.ndarray'>

# 2.2 Créer un vecteur colonne (shape: (5,1))
vecteur_col = np.array(lst).reshape(-1, 1)
print(vecteur_col)

# 2.3 Créer un vecteur ligne (shape: (1,5))
vecteur_ligne = np.array(lst).reshape(1, -1)
print(vecteur_ligne)
```
✅ NumPy est optimal pour les calculs vectoriels et matrices.

3️⃣ Avec pandas (pour DataFrame ou Series)
```py
import pandas as pd

lst = [1, 2, 3, 4, 5]

# 3.1 Créer un vecteur Series (1D)
vecteur_series = pd.Series(lst)
print(vecteur_series)

# 3.2 Créer un vecteur DataFrame (1 colonne)
vecteur_df = pd.DataFrame(lst, columns=['Valeurs'])
print(vecteur_df)
```
✅ Utile si tu veux manipuler des données avec index et étiquettes.

4️⃣ Avec array.array (Python standard, type fixe)
```py
from array import array

lst = [1, 2, 3, 4, 5]

vecteur_array = array('i', lst)  # 'i' = int
print(vecteur_array)  # array('i', [1, 2, 3, 4, 5])
```
⚡ Plus efficace en mémoire qu’une liste si tu as beaucoup d’entiers ou floats.

5️⃣ Avec torch (PyTorch) pour Deep Learning
```py
import torch

lst = [1, 2, 3, 4, 5]

vecteur_torch = torch.tensor(lst)
print(vecteur_torch)
```
✅ Vecteur utilisable pour GPU et calculs tensoriels.

6️⃣ Avec JAX (calcul scientifique avancé)
```py
import jax.numpy as jnp

lst = [1, 2, 3, 4, 5]

vecteur_jax = jnp.array(lst)
print(vecteur_jax)
```
🔹 Comme NumPy mais optimisé pour GPU/TPU et différentiation automatique.

7️⃣ Avec SciPy sparse vector (si vecteur très creux)
```py
from scipy.sparse import csr_matrix

lst = [0, 0, 3, 0, 5]

vecteur_sparse = csr_matrix(lst)
print(vecteur_sparse)
```
⚠️ Utile si la liste contient beaucoup de zéros, gain mémoire important.

✅ Résumé rapide

Méthode | Type | Usage principal
---|:-:|---
list() | Liste Python | Simple, natif, pas de calcul vectoriel
numpy.array() | ndarray | Calcul scientifique, vectorisation
pandas.Series | Series | Données étiquetées, analyses statistiques
pandas.DataFrame | DataFrame | Tableaux 2D avec index
array.array | Array Python | Optimisation mémoire pour type fixe
torch.tensor | Tensor | Deep Learning, GPU
jax.numpy.array | jax.ndarray | Calcul scientifique avancé, GPU/TPU
scipy.sparse | sparse matrix | Vecteurs creux, économie mémoire

```mermaid
flowchart TD
    A[Liste Python] --> B[List()] 
    A --> C[Numpy Array] 
    A --> D[Pandas Series] 
    A --> E[Pandas DataFrame] 
    A --> F[Array.array]
    A --> G[Torch Tensor]
    A --> H[JAX Array]
    A --> I[SciPy Sparse]

    B --> B1[Type: list] 
    B --> B2[Usage: simple stockage, natif Python]

    C --> C1[Type: numpy.ndarray] 
    C --> C2[Usage: calcul scientifique, vectorisation]
    C --> C3[Formes: 1D (vecteur), 2D (ligne/colonne)]

    D --> D1[Type: pandas.Series] 
    D --> D2[Usage: données étiquetées, statistiques]

    E --> E1[Type: pandas.DataFrame] 
    E --> E2[Usage: tableau 2D avec index et colonnes]

    F --> F1[Type: array.array] 
    F --> F2[Usage: optimisation mémoire, type fixe]

    G --> G1[Type: torch.Tensor] 
    G --> G2[Usage: Deep Learning, GPU]

    H --> H1[Type: jax.numpy.ndarray] 
    H --> H2[Usage: calcul scientifique avancé, GPU/TPU]

    I --> I1[Type: scipy.sparse.csr_matrix] 
    I --> I2[Usage: vecteurs creux, économie mémoire]
```