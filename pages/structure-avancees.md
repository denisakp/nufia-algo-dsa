# Programmation Dynamique - Ajouter une Structure Cache

## Principe Fondamental:
- **Problème:** Recalculs répétitifs coûteux
- **Solution:** Ajouter une structure de mémorisation
- **Résultat:** Complexité exponentielle → polynomiale

<br>

## Exemples Classiques:
- **Fibonacci:** Dict pour stocker les résultats calculés
- **Sac à dos:** Tableau 2D pour les sous-problèmes
- **Plus court chemin:** Matrice des distances

<br>

💡 **Pattern:** Structure de cache transforme la récursion naïve en solution efficace !

💾 **Ajouter une structure de stockage = transformer un problème difficile en facile**

<!--
🎯 Objectif du slide : Montrer que la structure cachée permet de transformer un problème inefficace en solution optimisée.

La programmation dynamique est une technique très puissante… mais en réalité, c’est souvent juste de la récursion + un cache.
	
Le problème initial ? On recalcule les mêmes choses encore et encore.
	
    Exemple : dans Fibonacci (modélise une croissance cumulative, où le passé immédiat influence directement le présent, avec une structure récursive naturelle) naïf (ignore qu’il l’a déjà fait.), f(30) appelle f(29) et f(28), mais f(28) est recalculé plusieurs fois.
	
    La solution : mémoriser ce qu’on a déjà fait.
	
    On ajoute une structure (comme un tableau ou un dictionnaire), et dès qu’un sous-problème est résolu, on stocke la réponse.
	
    Résultat ? On passe de complexité exponentielle à polynomiale.
	
Cette idée s’applique partout :
	
    - Fibonacci → dict simple

    - Problème du sac à dos → tableau 2D

    - Plus court chemin (Floyd-Warshall) → matrice de distances
	
Conclusion à marteler : ajouter une structure mémoire transforme la complexité et rend les problèmes gérables !
-->

---

# Structures Probabilistes - Approximation Structurée

## Bloom Filters:
- **Principe:** Structure compacte pour réponses probabilistes
- **Garantie:** "Probablement présent" ou "Certainement absent"
- **Avantage:** Mémoire constante, vitesse O(1)

<br>

## Applications Réelles:
- **Navigateurs web:** URLs malveillantes
- **Bases de données:** Éviter les accès disque inutiles
- **CDN:** Cache distribué
- **Bitcoin:** Vérification rapide des transactions

<br>

🎲 **Parfois, une approximation structurée est plus utile qu'une certitude coûteuse**

<!--
🎯 Objectif du slide : Présenter des structures comme les Bloom filters et expliquer pourquoi les approximations sont parfois plus utiles que la précision.

Ici, on entre dans un monde intéressant : celui des structures “imprécises”… mais très utiles.

Le Bloom filter est une structure qui peut vous dire :
“Cet élément est probablement présent” ou “sûrement absent”

Ça paraît bizarre ? Mais c’est extrêmement utile quand :
- La mémoire est limitée
- La vitesse est critique

Exemple concret :
- Dans les navigateurs, les URLs malveillantes sont vérifiées avec des Bloom filters.
- En base de données, on évite des accès disque coûteux inutilement.

Attention : on peut avoir de faux positifs, mais jamais de faux négatifs.

Le trade-off est clair : vous gagnez énormément en performance, pour un risque minime d’erreur.

Message à transmettre : parfois, une bonne approximation vaut mieux qu’une certitude coûteuse.
-->

---

# Structures Persistantes - Immutabilité Structurée

## Concept:
- **Immutabilité:** Les données ne changent jamais
- **Nouvelles versions:** Création de nouvelles structures
- **Partage:** Réutilisation des parties communes

<br>

## Avantages Structurels:
- **Parallélisme:** Pas de verrous nécessaires
- **Historique:** Toutes les versions conservées
- **Debugging:** États précédents accessibles
- **Undo/Redo:** Naturellement implémenté

<br>

🔒 **Structure immuable = garanties de cohérence et parallélisme naturel**

<!--
🎯 Objectif du slide : Montrer les avantages structurels des structures de données immuables dans des contextes modernes (concurrence, historique, etc.).

Une structure persistante ne veut pas dire “qui reste longtemps”, mais plutôt : chaque version est conservée.

On ne modifie jamais la structure en place.
On crée une nouvelle version en réutilisant les parties communes (partage mémoire).

Pourquoi faire ça ?
- Parallélisme : plusieurs threads peuvent lire des structures sans se bloquer.
- Débogage : on peut revenir en arrière.
- Undo/Redo : naturel à implémenter.
- Très utilisé dans :
- Les éditeurs de texte (type VS Code)
- Les frameworks fonctionnels (comme en Clojure, Elm, etc.)
- Les blockchains (états immuables des blocs)

Message fort : immuabilité = cohérence + sécurité + simplicité du code concurrent.

-->

---

# Big Data - Structures Distribuées

## MapReduce - Un Pattern Structural:
- **Map:** Transformer les données localement
- **Shuffle:** Redistribuer par clé
- **Reduce:** Agréger les résultats

<br>

## Applications:
- **Google:** Indexation du web
- **Netflix:** Recommandations personnalisées
- **Banques:** Détection de fraudes
- **Sciences:** Analyse de génomes

<br>

💡 **Insight:** Structure de traitement adaptée à la structure des données massives !

🌍 **Données massives = structures et algorithmes distribués naturellement**

<!--
🎯 Objectif du slide : Expliquer que face à des volumes massifs de données, la structure doit aussi être répartie.

Quand on parle de Big Data, la structure ne tient plus sur une seule machine.

Il faut repenser la structure de manière distribuée.

Le schéma classique est celui de MapReduce :
- Map : chaque machine traite ses données localement.
- Shuffle : on redistribue les résultats (par clé).
- Reduce : on agrège les données.

Ce modèle est simple… mais structurellement puissant.

- Il a permis à Google d’indexer le web
- À Netflix d’entraîner ses modèles de recommandation
- Aux chercheurs d’analyser des génomes entiers

Le point clé : les algorithmes doivent s’adapter à la structure distribuée des données, sinon ça ne scale pas.

Message fort : avec les données massives, la structure logique et la structure physique doivent évoluer ensemble.

-->
