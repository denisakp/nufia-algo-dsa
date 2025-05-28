---
theme: frankfurt
infoLine: true
title: Algorithmique et Structures de Données Avancées
author: Denis AKPAGNONITE
transition: fade
mdc: true
presenter: true
colorSchema: auto
---

# Algorithmique et Structures de Données Avancées


🎯 Développer une mentalité **Structure-First**

<!-- -->

---
section: 'Intro'
layout: image-left
image: https://media.newyorker.com/photos/5ba177da9eb2f7420aadeb98/4:3/w_1229,h_921,c_limit/Cohen-Linus-Torvalds.jpg
---

# Linus Torvalds once says 

> "Bad programmers worry about the code. Good programmers worry about data structures and their relationships."
>

<!-- 
Avant de rentrer dans le vif du sujet, je voulais commencer avec cette citation de Linus Torvalds, le créateur de Git et du noyau Linux.

Elle peut paraître un peu dure, mais elle met le doigt sur quelque chose de très profond.

Quand on débute en programmation, ou même parfois après quelques années d’expérience, on a tendance à se concentrer uniquement sur le code. Est-ce qu’il compile ? Est-ce qu’il fonctionne ? Est-ce qu’il est propre, ou rapide ?

Mais en réalité, le code, ce n’est que la surface. Ce n’est que la manière dont on traduit une idée en instructions.

Ce que Linus veut dire ici, c’est que ce qui fait vraiment la différence entre un développeur correct et un très bon développeur, c’est sa capacité à penser en termes de structures de données. À comprendre comment organiser les informations, comment elles s’enchaînent, comment elles interagissent entre elles.

C’est ça qui permet de résoudre un problème de manière élégante, performante et maintenable.

Prenons un exemple simple :
Imaginons que vous devez gérer une file d’attente pour un système de support client.

Un développeur débutant va peut-être coder ça avec un tableau classique — un array. Ça peut marcher, mais au fur et à mesure, il va rencontrer des lenteurs, des bugs, des incohérences.

Un développeur expérimenté, lui, va se poser la question autrement :
	•	Quel est mon besoin en matière d’insertion et de suppression ?
	•	Est-ce que j’ai besoin d’accéder rapidement au premier élément ?
	•	Est-ce que l’ordre est important ?

Et là, il va peut-être choisir une file (queue) ou une deque, qui répond exactement au besoin avec une meilleure complexité algorithmique.

Donc tout ça pour dire que la manière dont on pense un problème — la modélisation algorithmique, les structures de données qu’on choisit — c’est ça le cœur du métier.

Et c’est exactement ce qu’on va voir aujourd’hui.

-->

---

# Objectifs de la Formation

- **Adopter** la mentalité du **bon programmeur** selon Torvalds
- **Maîtriser** les structures de données fondamentales et avancées
- **Comprendre** comment les structures dictent les algorithmes
- **Appliquer** le **Structure-First Thinking** en pratique
- **Optimiser** ses solutions pour les entretiens techniques

<!-- 
1. Adopter la mentalité du bon programmeur selon Torvalds

Quand on parle de “bon programmeur”, ce n’est pas une question d’élitisme, c’est une question de perspective.
Ce que Linus Torvalds met en avant, c’est que la qualité d’un développeur ne se mesure pas juste à la propreté de son code ou à sa capacité à écrire vite. Elle se mesure à sa capacité à comprendre la structure sous-jacente d’un problème.
Durant cette présentation, je vais insister sur cette approche : penser les données d’abord, le code ensuite.

2. Maîtriser les structures de données fondamentales et avancées

Ici, l’objectif est de passer en revue non seulement les classiques — listes, piles, files, tableaux, arbres, graphes — mais aussi quand et pourquoi les utiliser.
On abordera aussi des structures un peu plus avancées comme les heaps, les hash maps, les sets, les tries, etc.
Ce qui est important, ce n’est pas juste de connaître leur définition, mais de comprendre les implications pratiques en termes de performance et de logique algorithmique.

3. Comprendre comment les structures dictent les algorithmes

C’est un point souvent négligé. Un algorithme n’est jamais “magique” en soi : il est profondément lié à la structure de données qu’il utilise.
Prenez le tri rapide (QuickSort) : il tire sa force de la récursivité, des partitions efficaces sur des tableaux.
Ou les algorithmes de parcours : profondeur d’abord, largeur d’abord — tout dépend si vous êtes sur un arbre, un graphe, une structure orientée.
Donc comprendre une structure, c’est ouvrir la porte à une famille d’algorithmes efficaces.

4. Appliquer le Structure-First Thinking en pratique

Là, on va vraiment faire un switch de mindset.
Avant d’écrire du code, on va apprendre à se poser les bonnes questions :
	•	Quel est le vrai problème ?
	•	Quels sont les éléments que je manipule ?
	•	Quelle est la structure naturelle de ces données ?
Ce “structure-first thinking” permet d’éviter des mois de refactoring ou des performances catastrophiques plus tard.
On verra des cas concrets où cette manière de penser change tout.

5. Optimiser ses solutions pour les entretiens techniques

Enfin, je sais que beaucoup ici visent des entretiens techniques, des postes exigeants, des challenges en entreprise.
Et dans ces contextes-là, la connaissance algorithmique est toujours testée : pas seulement pour vous piéger, mais pour voir comment vous réfléchissez, structurez et optimisez une solution.
On verra ensemble comment aborder un problème posément, structurer sa réponse, et donner une solution propre avec une complexité maîtrisée.
-->

---
layout: full
---

# Qui je suis

<div class="flex items-center justify-between gap-8">

<!-- Partie gauche : texte -->
<div class="flex-1">
  <h2 class="text-2xl font-semibold text-gray-700">Denis AKPAGNONITE</h2>
  <p class="text-md text-gray-500 mb-4">Software Engineer 👨🏽‍💻 | Cloud Native Enthusiast ⎈</p>

  <ul class="list-disc pl-5 space-y-2 text-sm text-gray-600">
    <li>Passionné par les systèmes distribués / architectures orientées événements</li>
    <li>Spécialisé Cloud Native avec une approche DevSecOps</li>
    <li>Focus sur les l’automatisation, l’observabilité, la sécurité (IAM) et les tests </li>
    <li>Conception de systèmes simples, fiables et maintenables</li>
    <li>Curieux, intéressé par l’open source et le droit de la Propriété Intellectuelle</li>
    <li>Rédaction technique & formation (Cloud, DevOps, QA)</li>
  </ul>
</div>

<!-- Partie droite : photo -->
<div class="flex-1 flex justify-end">
  <img src="./assets/me.jpeg" alt="Photo de Denis" class="h-[350px] w-auto  rounded-xl shadow-md" />
</div>

</div>

---
section: 'Philosiphie'
src: ./pages/philosophie.md
---

---
section: 'Algorithme de base'
src: ./pages/algo-fondamentaux.md
---

---
section: Structures Simples
src: ./pages/structure-simple.md
---

---
section: 'Structures Avancées'
src: ./pages/structure-avancees.md
---

---
section: 'Quoi retenir'
src: ./pages/ateliers.md
---

---
section: 'Conclusion'
src: ./pages/conclusion.md
---

---
layout: end
---

✨ Une dernière pensée…

> "Bad programmers worry about the code. Good programmers worry about data structures and their relationships."
>

<!--
🧠 Cette citation résume toute la conférence.
Les bons programmeurs ne pensent pas d’abord à la syntaxe, au langage, au framework, au type de BD, micro-service/monolithique....

Ils pensent à la structure des données.
Et le code découle naturellement de cette structure.

Si vous repartez avec une seule idée aujourd’hui, c’est celle-là.
-->