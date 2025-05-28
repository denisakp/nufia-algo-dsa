# Recherche - Choisir sa Structure

| Structure | Algorithme Naturel | Complexité | Usage |
|-----------|-------------------|------------|-------|
| Liste non triée | Recherche linéaire | O(n) | Données rares |
| Liste triée | Recherche binaire | O(log n) | Données statiques |
| Hash Table | Hachage direct | O(1) | Recherches fréquentes |


💡 **Pattern:** Structure organisée = recherche efficace !

🔍 **L'organisation des données dicte naturellement la stratégie de recherche optimale**

<!-- 
Avant même de parler d’algorithmes, posons-nous une question simple : comment sont organisées vos données ?
	
Regardez ce tableau : il ne parle pas de magie ou d’optimisation micro. Il parle d’un principe fondamental :
➕ Une structure bien choisie = une recherche plus rapide.

### Liste non triée.
C’est souvent notre défaut de départ. On ajoute des éléments, sans réfléchir. Du coup, pour chercher un élément, on est obligé de tout balayer — c’est du O(n).

### Liste triée.
Là, on peut déjà faire beaucoup mieux. Triée → on peut couper en deux à chaque étape → recherche binaire → O(log n)
Parfait si les données ne changent pas souvent.

### Hash Table.
Là c’est la star des recherches fréquentes. On transforme une clé (ex : un ID) → en adresse directe.
C’est du O(1) : peu importe si on a 10, 1 000 ou 1 million d’éléments !

🧠 Point pédagogique pour les juniors/étudiants :

“Ce n’est pas juste un choix de performance. C’est une question de bon sens : quelle est la forme naturelle de mes données ? Et qu’est-ce que je veux faire le plus souvent avec elles ?”

💡 En résumé: Si vous avez une structure désorganisée, il ne faut pas s’étonner que la recherche soit lente. C’est comme chercher un livre dans une bibliothèque sans étagère ni étiquette.

-->

---

# Tri - Structure → Stratégie

## Algorithmes Simples
- **Bubble Sort:** Comparaisons adjacentes
- **Insertion Sort:** Construction progressive
- **Complexité:** O(n²)
- **Usage:** Petites données

<br>

## Divide & Conquer
- **MergeSort:** Diviser → Trier → Fusionner
- **QuickSort:** Pivot → Partitionner → Récursion
- **Complexité:** O(n log n)
- **Usage:** Grandes données

<br>

💡 **Visualisation:** Voir comment l'algorithme transforme la structure !

🔄 **Diviser la structure du problème = solution plus efficace (Divide & Conquer)**

<!--
Maintenant qu’on a vu comment la structure influence la recherche, parlons du tri.

Quand on doit trier des données, on se demande souvent : “Quel algorithme choisir ?

Mais en réalité, la bonne question c’est :
“Quelle est la taille de mes données ? Et quelle est leur structure actuelle ?”

### Algorithmes simples
	- Bubble Sort : très connu, très pédagogique. On compare des paires adjacentes, on les échange. Simple mais lent → O(n²)
	- Insertion Sort : on construit la liste triée pas à pas, comme quand on trie des cartes à jouer.

Très efficace pour des petites listes (ou presque triées), mais pas pour des volumes massifs.

C’est comme ranger quelques papiers sur votre bureau — inutile de sortir tout un système d’archivage.

### Divide & Conquer
	- MergeSort : On divise la liste en deux, on trie chaque moitié, puis on les fusionne.
	- QuickSort : On choisit un pivot, on partitionne autour, et on trie récursivement.

Ces deux-là sont bien plus rapides pour de grosses données. Complexité : O(n log n)

Diviser pour mieux régner, ce n’est pas juste une stratégie militaire — c’est littéralement ce qu’on fait avec nos données.

Conseil pour tous les niveaux :
	- Débutants : Ce slide montre qu’on n’a pas besoin d’un algo parfait – juste d’un algo adapté.
	- Mid/Seniors : Pensez complexité + structure + volume réel. Ne pas “sur-optimiser”, mais choisir intelligemment.

### Conclusion pour la séquence

Le vrai pouvoir ne vient pas de connaître tous les algos par cœur… mais de savoir reconnaître les bons patterns structurels. Une fois que vous voyez ça, l’algorithme devient presque évident.
-->