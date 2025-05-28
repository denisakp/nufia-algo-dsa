---
theme: frankfurt
infoLine: true
title: Algorithmique et Structures de Données Avancées
author: Denis AKPAGNONITE
transition: slide-left
mdc: true
presenter: true
colorSchema: auto
---

# Algorithmique et Structures de Données Avancées


🎯 Développer une mentalité **Structure-First**

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

# Objectifs de la Formation

- **Adopter** la mentalité du "bon programmeur" selon Torvalds
- **Maîtriser** les structures de données fondamentales et avancées
- **Comprendre** comment les structures dictent les algorithmes
- **Appliquer** le "Structure-First Thinking" en pratique
- **Optimiser** ses solutions pour les entretiens techniques


💡 **Les données dirigent le code, pas l'inverse !**

<!-- Speaker Notes: (à compléter) -->

---
layout: quote
---

# 

> "Bad programmers worry about the code. Good programmers worry about data structures and their relationships."
> 
**Linus Torvalds**

---

# Pourquoi "Structure First" ?

## ❌ Approche "Code First"
- Je veux chercher → j'écris une boucle  
- Complexité: O(n)  
- Performance dégradée  
<br>

## ✅ Approche "Structure First"

- J'analyse mes données → Hash Table  
- Complexité: O(1)  
- Performance optimale

<br>

## Résultat
<br>

> Un changement de structure = **1000x plus rapide** !  
> 🔑 La structure de données détermine naturellement l'algorithme optimal

<!-- Speaker Notes: (à compléter) -->

---

# Complexité - Conséquence des Structures

| Complexité | Structure Typique | Exemple |
|------------|------------------|---------|
| O(1) | Hash Table | dict[key] |
| O(log n) | Arbre équilibré | Binary Search |
| O(n) | Liste non structurée | Parcours linéaire |
| O(n log n) | Divide & Conquer | MergeSort |

<br/>

📊 **La complexité n'est pas choisie, elle découle de la structure !**

<!-- Speaker Notes: (à compléter) -->

---

# Séquences - Arrays vs Linked Lists

## Arrays/Lists
- **Structure:** Mémoire contiguë
- **Accès:** O(1) par index
- **Insertion:** O(n) au milieu
- **Usage:** Accès fréquent par position
  
<br/>

## Linked Lists
- **Structure:** Nœuds + pointeurs
- **Accès:** O(n) séquentiel
- **Insertion:** O(1) si position connue
- **Usage:** Insertions/suppressions fréquentes

💡 **Démo Live:** Mesure de performance avec timeit

🏗️ **La structure physique en mémoire dicte les performances**

<!-- Speaker Notes: (à compléter) -->

---

# Dictionnaires - La Révolution O(1)

## Comment le Hachage Change Tout
- **Principe:** Transformer une clé en adresse mémoire directe
- **Résultat:** Accès instantané, indépendant de la taille

## Cas d'Usage Transformateurs:
- **Comptage de fréquences:** Counter en O(n) au lieu de O(n²)
- **Recherche d'existence:** O(1) au lieu de O(n)
- **Index inversé:** Moteurs de recherche
- **Cache/Mémoïsation:** Éviter les recalculs

⚡ **Une structure qui transforme O(n) en O(1) = Révolution algorithmique**

<!-- Speaker Notes: (à compléter) -->

---

# LIFO/FIFO - Quand l'Ordre Dicte l'Algorithme

## 🥞 Stacks (LIFO)
- **Structure:** Dernier entré, premier sorti
- **Opérations:** push(), pop()
- **Algorithmes naturels:**
  - Parcours DFS
  - Évaluation d'expressions
  - Undo/Redo

## 🚶‍♂️ Queues (FIFO)
- **Structure:** Premier entré, premier sorti
- **Opérations:** enqueue(), dequeue()
- **Algorithmes naturels:**
  - Parcours BFS
  - Files d'attente
  - Traitement par lots

🔄 **La contrainte d'ordre de la structure génère naturellement l'algorithme**

<!-- Speaker Notes: (à compléter) -->

---

# Arbres - Penser en Hiérarchies

## Concepts Fondamentaux:
- **Nœuds:** Éléments de données
- **Relations:** Parent-enfant naturelles
- **Racine:** Point d'entrée unique
- **Feuilles:** Nœuds terminaux

## Applications Concrètes:
- **DOM HTML:** Structure hiérarchique des pages web
- **Système de fichiers:** Dossiers et sous-dossiers
- **Arbres de décision:** Intelligence artificielle
- **Taxonomies:** Classifications biologiques

🌳 **Les relations hiérarchiques naturelles des données suggèrent la structure arbre**

<!-- Speaker Notes: (à compléter) -->

---

# Binary Search Trees - Structure qui Garantit l'Efficacité

## Propriété Fondamentale:
- **Règle:** Gauche < Racine < Droite
- **Conséquence:** Recherche en O(log n) automatique

## Parcours Naturels:
- **In-order:** Gauche → Racine → Droite = **Tri automatique !**
- **Pre-order:** Racine → Gauche → Droite
- **Post-order:** Gauche → Droite → Racine

💡 **Insight clé:** La structure impose l'ordre, l'algorithme de tri devient trivial !

🎯 **Une contrainte structurelle simple = algorithmes complexes rendus évidents**

<!-- Speaker Notes: (à compléter) -->

---

# Heaps - Priorité Structurée

## Propriété de Tas:
- **Min-Heap:** Parent ≤ Enfants
- **Max-Heap:** Parent ≥ Enfants
- **Résultat:** Minimum/Maximum accessible en O(1)

## Applications Naturelles:
- **Files de priorité:** Urgences hospitalières
- **Algorithme de Dijkstra:** Plus court chemin
- **Tri par tas:** HeapSort en O(n log n)
- **Ordonnancement OS:** Gestion des processus

⚖️ **Une contrainte de priorité dans la structure = gestion automatique des priorités**

<!-- Speaker Notes: (à compléter) -->

---

# Tries - Structure Spécialisée pour Chaînes

## Principe:
- **Arbre de préfixes:** Chaque chemin = un mot
- **Partage:** Préfixes communs partagés
- **Efficacité:** Recherche en O(longueur du mot)

## Applications Évidentes:
- **Auto-complétion:** Suggestions de recherche Google
- **Correcteurs orthographiques:** Vérification de mots
- **Routage IP:** Tables de routage réseau
- **Compression:** Algorithmes de codage

💡 **Magie:** La structure reflète parfaitement le problème à résoudre !

🔤 **Structure spécialisée pour un type de données = algorithmes spécialisés optimaux**

<!-- Speaker Notes: (à compléter) -->

---

# Graphes - Modéliser les Relations Complexes

## Concepts Fondamentaux:
- **Nœuds (Vertices):** Entités
- **Arêtes (Edges):** Relations entre entités
- **Orienté/Non-orienté:** Relations symétriques ou non
- **Pondéré:** Relations avec coût/distance

## Abstraction Universelle:
- **Réseaux sociaux:** Personnes + Amitiés
- **GPS:** Intersections + Routes
- **Internet:** Pages + Liens hypertextes
- **Molécules:** Atomes + Liaisons chimiques

🌐 **Le graphe = structure universelle pour modéliser n'importe quelle relation**

<!-- Speaker Notes: (à compléter) -->

---

# Représentations - Structure → Algorithmes

## Matrice d'Adjacence
- **Structure:** Tableau 2D
- **Avantage:** Vérifier arête en O(1)
- **Inconvénient:** O(V²) mémoire
- **Usage:** Graphes denses

## Liste d'Adjacence
- **Structure:** Dict de listes
- **Avantage:** O(V+E) mémoire
- **Inconvénient:** Vérifier arête en O(V)
- **Usage:** Graphes épars

💡 **Insight:** Le choix de représentation détermine quels algorithmes seront efficaces !

📊 **Même concept, représentations différentes = algorithmes optimaux différents**

<!-- Speaker Notes: (à compléter) -->

---

# Parcours - La Structure Guide l'Exploration

## 🏃‍♂️ BFS (Breadth-First)
- **Structure utilisée:** Queue
- **Principe:** Explorer niveau par niveau
- **Applications:**
  - Plus court chemin non pondéré
  - Niveaux dans un réseau
  - Diffusion d'information

## 🕳️ DFS (Depth-First)
- **Structure utilisée:** Stack
- **Principe:** Explorer en profondeur
- **Applications:**
  - Détection de cycles
  - Composantes connexes
  - Tri topologique

🧭 **Queue vs Stack dans l'algorithme = exploration complètement différente du même graphe**

<!-- Speaker Notes: (à compléter) -->

---

# Dijkstra - Quand Structure + Priorité = Optimal

## Algorithme Génial:
- **Structure utilisée:** Graphe pondéré + Priority Queue (Heap)
- **Principe:** Toujours explorer le nœud le plus "proche"
- **Garantie:** Plus court chemin optimal

## Applications Concrètes:
- **Google Maps:** Itinéraire optimal
- **Réseaux informatiques:** Routage optimal
- **Jeux vidéo:** IA de navigation
- **Logistique:** Optimisation des livraisons

🎯 **Combinaison de structures (Graphe + Heap) = algorithme puissant et élégant**

<!-- Speaker Notes: (à compléter) -->

---

# Recherche - Choisir sa Structure

| Structure | Algorithme Naturel | Complexité | Usage |
|-----------|-------------------|------------|-------|
| Liste non triée | Recherche linéaire | O(n) | Données rares |
| Liste triée | Recherche binaire | O(log n) | Données statiques |
| Hash Table | Hachage direct | O(1) | Recherches fréquentes |


💡 **Pattern:** Structure organisée = recherche efficace !

🔍 **L'organisation des données dicte naturellement la stratégie de recherche optimale**

<!-- Speaker Notes: (à compléter) -->

---

# Tri - Structure → Stratégie

## Algorithmes Simples
- **Bubble Sort:** Comparaisons adjacentes
- **Insertion Sort:** Construction progressive
- **Complexité:** O(n²)
- **Usage:** Petites données

## Divide & Conquer (Diviser pour mieux reigner)
- **MergeSort:** Diviser → Trier → Fusionner
- **QuickSort:** Pivot → Partitionner → Récursion
- **Complexité:** O(n log n)
- **Usage:** Grandes données

💡 **Visualisation:** Voir comment l'algorithme transforme la structure !

🔄 **Diviser la structure du problème = solution plus efficace (Divide & Conquer)**

<!-- Speaker Notes: (à compléter) -->

---

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

---

# 🛠️ Atelier - Auto-complétion Structure-First

## Démarche Structure-First:
1. **Analyser:** Quelles sont mes données ? (Mots avec préfixes communs)
2. **Identifier:** Quelle structure naturelle ? (Arbre de préfixes)
3. **Choisir:** Trie comme évidence structurelle
4. **Implémenter:** L'algorithme découle naturellement

## Résultat:
- ✅ Insertion rapide: O(longueur mot)
- ✅ Recherche efficace: O(longueur préfixe)
- ✅ Suggestions naturelles: parcours de sous-arbre
- ✅ Mémoire optimisée: préfixes partagés

🎯 **Structure parfaitement adaptée au problème = implémentation évidente et optimale**

<!-- Speaker Notes: (à compléter) -->

---

# 🧩 Mini-Défis Structure-First

## Défi 1: Réseau Social
- **Problème:** Trouver les amis communs
- **Question:** Quelle structure choisir ?
- **Réponse:** Graphe + Sets pour intersection

## Défi 2: Historique Navigation
- **Problème:** Back/Forward dans navigateur
- **Question:** Quelle structure naturelle ?
- **Réponse:** Deux stacks ou liste + index

## Défi 3: Top K Éléments
- **Problème:** Maintenir les K plus grands éléments d'un stream
- **Structure-First Thinking:** Min-Heap de taille K
- **Pourquoi génial:** O(log K) par insertion, O(1) pour le minimum

🎲 **Participation audience: Problème → Structure → Validation collective**

<!-- Speaker Notes: (à compléter) -->

---

# 🧠 Mentalité du Bon Programmeur

## ❌ Mauvaise Approche
- Je code d'abord
- J'optimise après
- Je subis la complexité
- Je patche les problèmes

## ✅ Bonne Approche
- J'analyse les données d'abord
- Je choisis la structure adaptée
- L'algorithme devient évident
- Performance optimale by design

> "Give me six hours to chop down a tree and I will spend the first four sharpening the axe."
> 
> **— Abraham Lincoln**

**Application:** 80% du temps sur la structure, 20% sur le code !

🏆 **Structure-First = Différence entre développeur junior et senior**

<!-- Speaker Notes: (à compléter) -->

---

# 🎯 Récapitulatif & Prochaines Étapes

## Ce que vous avez appris:
- ✅ **Mentalité Structure-First** selon Torvalds
- ✅ **Structures fondamentales** et leurs algorithmes naturels
- ✅ **Structures avancées** pour problèmes complexes
- ✅ **Pattern recognition** : Problème → Structure → Solution

🚀 Challenge Final:
Repensez un projet existant avec cette mentalité Structure-First

**Question:** Quelle structure de données aurait simplifié votre code ?

---

#### 📚 Ressources pour Approfondir:
- LeetCode/HackerRank avec approche Structure-First
- "Introduction to Algorithms" - Cormen
- "System Design Interview" - Alex Xu

💡 **Vous êtes maintenant des "Good Programmers" selon Linus Torvalds !**

<!-- Speaker Notes: (à compléter) -->