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

<!--
Commençons par le plus fondamental : comment organiser une séquence d'éléments ?

[ARRAYS]
Arrays = mémoire contiguë. Imaginez des maisons numérotées dans une rue : pour aller à la maison 10, vous calculez directement l'adresse. C'est O(1). Mais pour insérer une nouvelle maison au milieu ? Il faut décaler toutes les suivantes = O(n).

[LINKED LISTS]  
Linked Lists = comme un jeu de piste. Chaque nœud dit "le suivant est là-bas". Pour accéder au 10e élément ? Suivez la chaîne = O(n). Mais pour insérer ? Changez juste 2 pointeurs = O(1).

[DÉMO LIVE - si possible]
"Faisons un test rapide en Python :
- Array : accès arr[1000] vs insertion arr.insert(500, x)
- LinkedList : accès suivre 1000 liens vs insertion entre 2 nœuds"

Le message clé : LA STRUCTURE PHYSIQUE EN MÉMOIRE détermine les performances. Arrays = accès random rapide, Lists = modifications rapides. Votre choix dépend de votre usage dominant : vous accédez plus ou vous modifiez plus ?

Pour les seniors : c'est pourquoi Python utilise dynamic arrays (listes qui peuvent grandir) - compromis entre les deux !
-->

---

# Dictionnaires - La Révolution O(1)

## Comment le Hachage Change Tout
- **Principe:** Transformer une clé en adresse mémoire directe
- **Résultat:** Accès instantané, indépendant de la taille

<br>

## Cas d'Usage Transformateurs:
- **Comptage de fréquences:** Counter en O(n) au lieu de O(n²)
- **Recherche d'existence:** O(1) au lieu de O(n)
- **Index inversé:** Moteurs de recherche
- **Cache/Mémoïsation:** Éviter les recalculs

<br>

⚡ **Une structure qui transforme O(n) en O(1) = Révolution algorithmique**

<!--
Les dictionnaires/hash tables = LA révolution en informatique !

[PRINCIPE DE BASE]
Imaginez une bibliothèque où au lieu de chercher un livre rayon par rayon, vous avez une formule magique : "titre du livre" → adresse exacte de l'étagère. C'est le hachage : clé → adresse mémoire directe.

[IMPACT TRANSFORMATEUR - exemples concrets]
- Compter les mots dans un texte : sans dict = comparer chaque mot à tous les précédents O(n²), avec dict = un seul lookup O(1) par mot = O(n) total !
- "Est-ce que cet utilisateur existe ?" : sans dict = parcourir toute la liste, avec dict = lookup instantané
- Google : chercher "python" → hash("python") → liste instantanée des pages

[POUR LES JUNIORS]
Exemple pratique : vous avez une liste d'emails et vous voulez savoir si "john@email.com" est dedans. Sans dict : parcourir toute la liste. Avec dict : transformation en 0.0001 seconde !

[POUR LES SENIORS]  
C'est pourquoi Redis, les caches, les bases NoSQL sont si puissants. La structure hash table permet des algorithmes qui étaient impensables avant.

Message clé : une structure qui casse la barrière O(n) et donne O(1) = c'est RÉVOLUTIONNAIRE. Cela change complètement quels algorithmes sont possibles !
-->

---
layout: two-cols-header
---

# LIFO/FIFO - Quand l'Ordre Dicte l'Algorithme

::left::

## 🥞 Stacks (LIFO)
- **Structure:** Dernier entré, premier sorti
- **Opérations:** push(), pop()
- **Algorithmes naturels:**
  - Parcours DFS
  - Évaluation d'expressions
  - Undo/Redo

::right::

## 🚶‍♂️ Queues (FIFO)
- **Structure:** Premier entré, premier sorti
- **Opérations:** enqueue(), dequeue()
- **Algorithmes naturels:**
  - Parcours BFS
  - Files d'attente
  - Traitement par lots

🔄 **La contrainte d'ordre de la structure génère naturellement l'algorithme**

<!--
Ici, la CONTRAINTE d'ordre de la structure dicte complètement l'algorithme !

[STACKS - LIFO]
Stack = pile d'assiettes. La dernière posée est la première récupérée. Cette contrainte simple génère des algorithmes puissants :
- DFS : on "empile" les voisins, on "dépile" le plus récent → exploration en profondeur naturelle
- Expressions : (2 + 3) * 4 → on empile les opérateurs, on dépile dans l'ordre inverse
- Undo : chaque action empilée, undo dépile la plus récente

[QUEUES - FIFO]  
Queue = file d'attente au supermarché. Premier arrivé, premier servi. Cette contrainte génère d'autres algorithmes :
- BFS : on "enfile" les voisins, on "défile" le plus ancien → exploration niveau par niveau
- Traitement : les requêtes arrivent, elles sont traitées dans l'ordre d'arrivée

[INSIGHT CRUCIAL]
Regardez la magie : même données (un graphe), mais structure différente (Stack vs Queue) = algorithme complètement différent (DFS vs BFS) !

Pour les débutants : Stack = pile de livres, Queue = file d'attente
Pour les seniors : c'est pourquoi les architectures asynchrones utilisent des queues - l'ordre FIFO garantit la fairness du traitement

Message : la contrainte structurelle (LIFO vs FIFO) génère NATURELLEMENT l'algorithme optimal !
-->

---

# Arbres - Penser en Hiérarchies

## Concepts Fondamentaux:
- **Nœuds:** Éléments de données
- **Relations:** Parent-enfant naturelles
- **Racine:** Point d'entrée unique
- **Feuilles:** Nœuds terminaux

<br>

## Applications Concrètes:
- **DOM HTML:** Structure hiérarchique des pages web
- **Système de fichiers:** Dossiers et sous-dossiers
- **Arbres de décision:** Intelligence artificielle
- **Taxonomies:** Classifications biologiques

🌳 **Les relations hiérarchiques naturelles des données suggèrent la structure arbre**

<!--
Les arbres = quand vos données ont des relations hiérarchiques naturelles !

[POURQUOI DES ARBRES ?]
Certaines données sont NATURELLEMENT hiérarchiques. Forcer une hiérarchie dans une liste = complexité artificielle. Accepter la hiérarchie avec un arbre = simplicité naturelle.

[EXEMPLES CONCRETS]
- HTML DOM : <html> contient <body>, <body> contient <div>, etc. → structure arbre parfaite
- Fichiers : Dossier "Photos" contient "Vacances", "Vacances" contient "plage.jpg" → arbre naturel
- Entreprise : CEO → Directeurs → Managers → Employés → hiérarchie = arbre
- IA : "Animal ?" → "Mammifère ?" → "Carnivore ?" → "Chat !" → arbre de décision

[INSIGHT FONDAMENTAL]
Ne FORCEZ pas des données hiérarchiques dans des structures plates ! Si vous avez des relations parent-enfant, utilisez un arbre. L'algorithme de navigation devient trivial : récursion naturelle.

Pour les débutants : pensez arbre généalogique - relations parent-enfant évidentes
Pour les seniors : c'est pourquoi React utilise un Virtual DOM tree, les parsers créent des AST trees - la structure reflète parfaitement le problème

Message : quand vos données sont hiérarchiques, la structure arbre rend les algorithmes évidents !
-->

---

# Binary Search Trees - Structure qui Garantit l'Efficacité

## Propriété Fondamentale:
- **Règle:** Gauche < Racine < Droite
- **Conséquence:** Recherche en O(log n) automatique

<br>

## Parcours Naturels:
- **In-order:** Gauche → Racine → Droite = **Tri automatique !**
- **Pre-order:** Racine → Gauche → Droite
- **Post-order:** Gauche → Droite → Racine

<br>

💡 **Insight clé:** La structure impose l'ordre, l'algorithme de tri devient trivial !

🎯 **Une contrainte structurelle simple = algorithmes complexes rendus évidents**

<!--
BST = l'exemple PARFAIT de "structure first" ! Une règle simple génère des algorithmes puissants.

[LA RÈGLE MAGIQUE]
Une seule contrainte : "Gauche < Racine < Droite". C'est tout ! Mais cette règle simple génère automatiquement :
- Recherche O(log n) : comparez avec racine, allez à gauche ou droite, éliminez la moitié à chaque étape
- Insertion O(log n) : suivez la règle, trouvez la position, insérez
- Suppression : un peu plus complexe mais algorithme standard

[LE MIRACLE DU PARCOURS IN-ORDER]
Parcours in-order = Gauche → Racine → Droite. Résultat ? Les éléments sortent AUTOMATIQUEMENT triés ! Vous avez construit votre BST en insérant des éléments dans le désordre, mais un simple parcours les ressort triés !

[DÉMONSTRATION MENTALE]
Insérons : 15, 10, 20, 8, 12, 25, 6
    15
   /  \
  10   20
 / \    \
8   12   25
/
6

Parcours in-order : 6, 8, 10, 12, 15, 20, 25 → TRI AUTOMATIQUE !

Pour les seniors : c'est la base des bases de données indexées. L'index = BST, les requêtes utilisent la propriété BST.

Message puissant : UNE contrainte structurelle simple peut rendre des algorithmes complexes (tri, recherche) complètement triviaux !
-->

---

# Heaps - Priorité Structurée

## Propriété de Tas:
- **Min-Heap:** Parent ≤ Enfants
- **Max-Heap:** Parent ≥ Enfants
- **Résultat:** Minimum/Maximum accessible en O(1)

<br>

## Applications Naturelles:
- **Files de priorité:** Urgences hospitalières
- **Algorithme de Dijkstra:** Plus court chemin
- **Tri par tas:** HeapSort en O(n log n)
- **Ordonnancement OS:** Gestion des processus

<br>

⚖️ **Une contrainte de priorité dans la structure = gestion automatique des priorités**

<!--
Heaps = quand vous avez besoin de gérer des priorités efficacement !

[LA PROPRIÉTÉ HEAP]
Règle simple : dans un min-heap, parent ≤ enfants. Conséquence magique : le minimum est TOUJOURS à la racine ! Pas besoin de chercher, pas besoin de comparer - c'est structurellement garanti.

[APPLICATIONS RÉELLES - très concrètes]
- Hôpital : patients arrivent avec différentes urgences. Min-heap par gravité → le plus urgent sort automatiquement en premier
- Dijkstra : nœuds avec différentes distances. Min-heap par distance → le plus proche sort automatiquement
- OS : processus avec différentes priorités. Heap par priorité → le plus prioritaire s'exécute

[ALGORITHME NATUREL]
Insertion : ajoutez à la fin, "remontez" jusqu'à respecter la propriété → O(log n)
Extraction : prenez la racine (min garanti), "redescendez" le dernier élément → O(log n)

[COMPARAISON AVEC ALTERNATIVES]
Sans heap : "Quel est le minimum ?" = parcourir tout O(n)
Avec heap : "Quel est le minimum ?" = regarder la racine O(1)

Pour les débutants : heap = tas organisé où le plus petit/grand est toujours au sommet
Pour les seniors : c'est pourquoi les priority queues utilisent des heaps - structure optimale pour ce besoin

Message : quand vous gérez des priorités, la structure heap rend la gestion automatique et efficace !
-->

---

# Tries - Structure Spécialisée pour Chaînes

## Principe:
- **Arbre de préfixes:** Chaque chemin = un mot
- **Partage:** Préfixes communs partagés
- **Efficacité:** Recherche en O(longueur du mot)

<br>

## Applications Évidentes:
- **Auto-complétion:** Suggestions de recherche Google (O(longueur préfixe))
- **Correcteurs orthographiques:** Vérification de mots
- **Routage IP:** Tables de routage réseau
- **Compression:** Algorithmes de codage

<br>

💡 **Magie:** La structure reflète parfaitement le problème à résoudre !

🔤 **Structure spécialisée pour un type de données = algorithmes spécialisés optimaux**

<!--
Tries = exemple parfait de structure SPÉCIALISÉE pour un problème spécifique !

[PRINCIPE DE BASE]
Trie = arbre où chaque chemin de la racine à une feuille forme un mot. Mots avec préfixes communs partagent le début de chemin. "CAR", "CARD", "CARE" partagent "CAR".

[POURQUOI C'EST GÉNIAL]
Recherche de mot : suivez le chemin lettre par lettre. Temps = longueur du mot, PAS le nombre de mots dans le dictionnaire ! Avec 1 million de mots, chercher "HELLO" = 5 étapes seulement !

[APPLICATIONS CONCRÈTES]
- Google auto-complete : vous tapez "alg", le trie suit A→L→G et propose tous les mots qui continuent
- Correcteur : mot mal orthographié ? Parcourez le trie, trouvez les mots à distance 1-2
- Routage IP : 192.168.1.0 → suivez 1→9→2→1→6→8... dans le trie des routes

[COMPARAISON]
Sans trie : auto-complétion = comparer votre préfixe à TOUS les mots O(n×m)
Avec trie : auto-complétion = suivre UN chemin O(longueur préfixe)

[INSIGHT CRUCIAL]
Tries = structure qui REFLÈTE parfaitement la nature des chaînes de caractères (séquences de symboles avec préfixes communs).

Pour les débutants : imaginez un dictionnaire organisé par première lettre, puis deuxième, puis troisième...
Pour les seniors : c'est la base des algorithmes de compression (codes de Huffman), des DNS lookup tables

Message : pour les chaînes de caractères, une structure spécialisée (trie) donne des algorithmes beaucoup plus efficaces que les structures génériques !
-->

---

# Graphes - Modéliser les Relations Complexes

## Concepts Fondamentaux:
- **Nœuds (Vertices):** Entités
- **Arêtes (Edges):** Relations entre entités
- **Orienté/Non-orienté:** Relations symétriques ou non
- **Pondéré:** Relations avec coût/distance

<br>

## Abstraction Universelle:
- **Réseaux sociaux:** Personnes + Amitiés
- **GPS:** Intersections + Routes
- **Internet:** Pages + Liens hypertextes
- **Molécules:** Atomes + Liaisons chimiques

<br>

🌐 **Le graphe = structure universelle pour modéliser n'importe quelle relation**

<!--
Graphes = LA structure la plus puissante et universelle en informatique !

[CONCEPTS DE BASE]
Nœuds = entités (choses), 
Arêtes = relations entre ces choses. C'est tout ! Mais cette simplicité peut modéliser TOUT ce qui a des relations.

[EXEMPLES UNIVERSELS - montrer la flexibilité]
- Facebook : nœuds = personnes, arêtes = amitiés → graphe non-orienté
- Twitter : nœuds = personnes, arêtes = "suit" → graphe orienté (A suit B ≠ B suit A)
- GPS : nœuds = intersections, arêtes = routes avec distances → graphe pondéré
- Molécule : nœuds = atomes, arêtes = liaisons chimiques → graphe non-orienté

[PUISSANCE D'ABSTRACTION]
Une fois vos données modélisées en graphe, vous débloquez TOUS les algorithmes de graphes :
- Plus court chemin (Dijkstra, Floyd-Warshall)
- Détection de communautés
- Analyse de centralité
- Détection de cycles

[IMPACT CONCRET]
Google PageRank = algorithme sur le graphe du web (pages + liens)
GPS = algorithme de plus court chemin sur graphe routier
Recommandations Netflix = algorithmes sur graphe utilisateurs-films

Pour les débutants : graphe = réseau de relations, comme un plan de métro
Pour les seniors : c'est pourquoi les bases de données graphes (Neo4j) explosent - pour les données relationnelles complexes

Message : si vos données ont des RELATIONS, modélisez-les en graphe. Vous débloquez immédiatement des dizaines d'algorithmes puissants !

En résumé: 
Ce qu’il faut retenir : graphe = réseau de relations.
Si vos données sont connectées entre elles, pensez graphe.
Et surtout : il existe plein d’algorithmes puissants pour exploiter ces relations !

-->

---

# Représentations - Structure → Algorithmes

## Matrice d'Adjacence
- **Structure:** Tableau 2D (`matrice[i][j]` )
- **Avantage:** Vérifier arête en O(1)
- **Inconvénient:** O(V²) mémoire
- **Usage:** Graphes denses

<br>

## Liste d'Adjacence
- **Structure:** Dict de listes
- **Avantage:** O(V+E) mémoire
- **Inconvénient:** Vérifier arête en O(V)
- **Usage:** Graphes épars

<br>

💡 **Insight:** Le choix de représentation détermine quels algorithmes seront efficaces !

📊 **Même concept, représentations différentes = algorithmes optimaux différents**

<!--
MÊME données (un graphe), mais représentations différentes = algorithmes optimaux différents !

[MATRICE D'ADJACENCE]
Tableau 2D : matrice[i][j] = 1 si arête entre nœud i et j, 0 sinon.
Avantages : "Y a-t-il une arête entre A et B ?" → matrice[A][B] = réponse instantanée O(1)
Inconvénients : pour 1000 nœuds = 1 million de cases, même si seulement 10 arêtes !

[LISTE D'ADJACENCE] 
Dictionnaire : pour chaque nœud, liste de ses voisins.
Avantages : seulement les arêtes qui existent sont stockées → économie mémoire énorme
Inconvénients : "Y a-t-il une arête entre A et B ?" → parcourir la liste de A jusqu'à trouver B

[ALGORITHMES IMPACTÉS]
- Algorithme dense (beaucoup d'arêtes) : matrice plus efficace
- Algorithme épars (peu d'arêtes) : listes plus efficaces
- Parcours de tous les voisins : listes plus efficaces
- Vérifications d'existence fréquentes : matrice plus efficace

[EXEMPLE CONCRET]
Facebook (graphe dense, beaucoup d'amitiés) → tendance matrice
Internet (graphe épars, chaque page n'a que quelques liens) → tendance listes

Pour les débutants : matrice = tableau Excel, listes = carnets d'adresses
Pour les seniors : c'est pourquoi les bases de données ont différents index - même données, structures différentes pour différents patterns d'accès

Message crucial : le choix de représentation n'est PAS un détail d'implémentation - il détermine quels algorithmes seront efficaces !
-->

---
layout: two-cols-header
---

# Parcours - La Structure Guide l'Exploration

::left::

## 🏃‍♂️ BFS (Breadth-First)
- **Structure utilisée:** Queue
- **Principe:** Explorer niveau par niveau
- **Applications:**
  - Plus court chemin non pondéré
  - Niveaux dans un réseau
  - Diffusion d'information

::right::

## 🕳️ DFS (Depth-First)
- **Structure utilisée:** Stack
- **Principe:** Explorer en profondeur
- **Applications:**
  - Détection de cycles
  - Composantes connexes
  - Tri topologique

🧭 **Queue vs Stack dans l'algorithme = exploration complètement différente du même graphe**

<!--
Même graphe, même données, mais structure auxiliaire différente (Queue vs Stack) = exploration complètement différente !

[BFS - BREADTH FIRST]
Structure : Queue (FIFO)
Comportement : explorez tous les voisins du niveau actuel avant de passer au niveau suivant
Résultat : exploration "en largeur", niveau par niveau

Applications naturelles :
- Plus court chemin NON pondéré : BFS garantit qu'on trouve le chemin avec le moins d'arêtes
- "À quelle distance sommes-nous ?" : niveaux BFS = distance en nombre de sauts
- Diffusion virale : comment une info se propage niveau par niveau dans un réseau

[DFS - DEPTH FIRST]
Structure : Stack (LIFO - souvent récursion)
Comportement : explorez aussi loin que possible sur une branche avant de revenir
Résultat : exploration "en profondeur"

Applications naturelles :
- Détection de cycles : DFS peut détecter si on "revient" à un nœud déjà visité
- Composantes connexes : DFS explore complètement une composante avant de passer à la suivante
- Tri topologique : ordre de dépendances (cours prérequis, compilation)

[LA MAGIE]
Regardez : MÊME graphe, mais juste changer Queue→Stack change complètement l'ordre d'exploration !

Démo mentale sur un graphe simple :
    A
   / \
  B   C
 /   / \
D   E   F

BFS : A → B,C → D,E,F (niveau par niveau)
DFS : A → B → D, retour B, retour A → C → E, retour C → F (profondeur d'abord)

Message : la structure auxiliaire (Queue vs Stack) détermine complètement l'algorithme d'exploration !
-->

---

# Dijkstra - Quand Structure + Priorité = Optimal

## Algorithme Génial:
- **Structure utilisée:** Graphe pondéré + Priority Queue (Heap)
- **Principe:** Toujours explorer le nœud le plus "proche"
- **Garantie:** Plus court chemin optimal
  
<br>

## Applications Concrètes:
- **Google Maps:** Itinéraire optimal
- **Réseaux informatiques:** Routage optimal
- **Jeux vidéo:** IA de navigation
- **Logistique:** Optimisation des livraisons

<br>

🎯 **Combinaison de structures (Graphe + Heap) = algorithme puissant et élégant**

<!-- 
Dijkstra = exemple PARFAIT de combinaison de structures pour créer un algorithme génial !

[STRUCTURES COMBINÉES]
1. Graphe pondéré : modélise le problème (nœuds + arêtes avec coûts)
2. Priority Queue (Heap) : gère l'efficacité (toujours traiter le nœud le plus proche)

[PRINCIPE GÉNIAL]

"Glouton éclairé" : à chaque étape, explorer le nœud non-visité le plus PROCHE de la source. Pourquoi ça marche ? Si j'ai trouvé le chemin le plus court vers A, tout chemin vers B passant par A ne peut que s'allonger !

[ALGORITHME STEP-BY-STEP]
1. Mettez source dans priority queue avec distance 0
2. Extrayez le nœud le plus proche (heap.pop())
3. Explorez ses voisins, mettez à jour leurs distances
4. Ajoutez les voisins modifiés dans la priority queue
5. Répétez jusqu'à vider la queue

[APPLICATIONS CONCRÈTES]

- Google Maps : nœuds = intersections, arêtes = routes avec temps de trajet
- Internet : nœuds = routeurs, arêtes = liens avec latence
- Jeux : nœuds = positions, arêtes = mouvements avec coût d'énergie

[POURQUOI C'EST BEAU]

Sans priority queue : "quel est le nœud le plus proche ?" = parcourir tout O(V²)

Avec heap : "quel est le nœud le plus proche ?" = heap.pop() O(log V)
Complexité totale : O((V + E) log V) au lieu de O(V²)

Pour les débutants : Dijkstra = GPS qui trouve toujours le chemin le plus rapide
Pour les seniors : base de OSPF, BGP, et tous les protocoles de routage modernes

Message final : COMBINEZ les bonnes structures (graphe pour modéliser + heap pour optimiser) = algorithmes puissants et élégants !
-->