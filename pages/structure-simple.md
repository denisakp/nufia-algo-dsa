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
