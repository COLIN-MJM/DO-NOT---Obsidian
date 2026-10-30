---
banner: "#fe9d169e"
icon: 🎯
tags:
  - gamedesign
---
# Le jeu et la règle

---
Notre proposition de jouet actuelle repose sur le concept de règle dans le jeu vidéo.
- L’expression “Don’t” ramène de façon générale à l’interdiction, une forme de règle. Nous avons voulu nous concentrer sur la règle de façon générale, mais plutôt sous la forme d’affirmation (Don’t don’t = Do).

Dans un jeu, les règles permettent d’énoncer :
- Un objectif à atteindre (condition de victoire/défaite) ;
- Un comportement inhérent au fonctionnement du jeu.

Au stade de toy, nous avons choisi de nous concentrer sur cette deuxième utilisation de la règle, comme formulation du système dans un jeu.

Notre toy repose donc sur la possibilité pour le joueur de manipuler les règles du jeu :
- À partir d’une interface d’édition, le joueur modifie le système à l’échelle des entitées.
- L’interface d’édition est construite autour d’un outil d’assemblage de règles par tokens.

![[Pasted image 20261030143614.png]]

# Qu’est-ce qu’un Token ?
---
En partant d’une analyse grammaticale de la formulation des règles en anglais, nous avons définit un système d’assemblage de règle basé sur l’utilisation de Tokens.

- Un Token est la plus petite brique de constriction d’une règle dans le jeu, et s’apparente dans son utilisation à un mot.

Ces Tokens sont divisés en 4 types :

- Identity : Une Identity est un Token représentant un groupe d’acteurs in-game, identifiables par leur apparence visuelle.
	- L’Identity “Hero” réfère à l’avatar du héros du jeu, à travers sa représentation visuelle et son emplacement dans le monde  

- Ability : Une Ability est un Token définissant un comportement autonome. Certaines Ability correspondent à un comportement dépendant de l’assignation à une Identity.
	- L’Ability “Advance” correspond au comportement autonome d’avancer vers l’avant.
	- L’Ability “Look At” correspond au comportement autonome de s’orienter en direction de l’Identity assignée dans la règle.  

- Verbs : Un Verb est un Token permettant de construire une règle en associant deux Tokens entre eux.
	- Le Verb “Is” permet d’assigner à une Identity A à une Identity B.
	- Le Verb “Will” permet d’assigner une Ability à une Identity.  

- Autre : Certains Tokens comme “Player” ne rentrent dans aucun des précédents types, et sont définis individuellement par une fonction particulière dans une règle.
	- Le Token “Player” est un token unique représentant le joueur physique derrière son écran, à travers la manipulation du controller.  

# Comment construire une règle ?

---

![[Pasted image 20261030144008.png]]

Une règle, dans le Prototype v1, correspond à une ligne de 4 slots vides (en bleu), dans lesquels on peut insérer un Token.

![[Pasted image 20261030144058.png]]

Un inventaire situé en bas de l'écran permet de stocker une copie de chaque token présent dans le Prototype v1.

![[Pasted image 20261030144155.png]]

Le drag'n drop permet également d'intervertir deux tokens de place.

## Règles

- Une règle est une suite logique de Tokens, qui agit en temps réel sur le monde.
- Dans le setting initial du monde, une série de règles est déjà mise en place.
- Le joueur a accès en temps réel cette série de règles, et peut venir y déplacer les Tokens de façon à modifier le comportement du monde.
- Chaque règle est contrainte par des limites syntaxiques.

## Limites syntaxique

- Les règles sont soumises à un arbre de construction syntaxique, qui permet d’assurer une certaine logique dans l’énoncé des règles.
- L’éditeur de règles empêche ainsi le placement de certains Tokens en fonction de ces règles de construction (bien qu’il n’en donne pas de signe/feedback visuel dans l’état actuel).

# Les règles donnent vie à un système
---
La capacité à modifier les éléments ainsi que les comportements présents dans l’espace de jeu change la dynamique de jeu traditionnel des toys : on se rapproche plus du moteur de jeu (comme Scratch) que d’un bac à sable mécanique.

Le fun vient alors de la manipulation et la découverte du champ des possibles, qui laisse au joueur la liberté de créer ses propres situations.

