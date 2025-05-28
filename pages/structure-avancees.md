# Programmation Dynamique - Ajouter une Structure Cache

## Principe Fondamental:
- **Problème:** Recalculs répétitifs coûteux
- **Solution:** Ajouter une structure de mémorisation
- **Résultat:** Complexité exponentielle → polynomiale

## Exemples Classiques:
- **Fibonacci:** Dict pour stocker les résultats calculés
- **Sac à dos:** Tableau 2D pour les sous-problèmes
- **Plus court chemin:** Matrice des distances

💡 **Pattern:** Structure de cache transforme la récursion naïve en solution efficace !

💾 **Ajouter une structure de stockage = transformer un problème difficile en facile**

<!-- Speaker Notes: (à compléter) -->

---

# Structures Probabilistes - Approximation Structurée

## Bloom Filters:
- **Principe:** Structure compacte pour réponses probabilistes
- **Garantie:** "Probablement présent" ou "Certainement absent"
- **Avantage:** Mémoire constante, vitesse O(1)

## Applications Réelles:
- **Navigateurs web:** URLs malveillantes
- **Bases de données:** Éviter les accès disque inutiles
- **CDN:** Cache distribué
- **Bitcoin:** Vérification rapide des transactions

🎲 **Parfois, une approximation structurée est plus utile qu'une certitude coûteuse**

<!-- Speaker Notes: (à compléter) -->

---

# Structures Persistantes - Immutabilité Structurée

## Concept:
- **Immutabilité:** Les données ne changent jamais
- **Nouvelles versions:** Création de nouvelles structures
- **Partage:** Réutilisation des parties communes

## Avantages Structurels:
- **Parallélisme:** Pas de verrous nécessaires
- **Historique:** Toutes les versions conservées
- **Debugging:** États précédents accessibles
- **Undo/Redo:** Naturellement implémenté

🔒 **Structure immuable = garanties de cohérence et parallélisme naturel**

<!-- Speaker Notes: (à compléter) -->

---

# Big Data - Structures Distribuées

## MapReduce - Un Pattern Structural:
- **Map:** Transformer les données localement
- **Shuffle:** Redistribuer par clé
- **Reduce:** Agréger les résultats

## Applications:
- **Google:** Indexation du web
- **Netflix:** Recommandations personnalisées
- **Banques:** Détection de fraudes
- **Sciences:** Analyse de génomes

💡 **Insight:** Structure de traitement adaptée à la structure des données massives !

🌍 **Données massives = structures et algorithmes distribués naturellement**

<!-- Speaker Notes: (à compléter) -->