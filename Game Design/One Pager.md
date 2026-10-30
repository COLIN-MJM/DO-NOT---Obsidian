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

Ability : Une Ability est un Token définissant un comportement autonome. Certaines Ability correspondent à un comportement dépendant de l’assignation à une Identity.
- L’Ability “[Advance]” correspond au comportement autonome d’avancer vers l’avant.
- L’Ability “[Look At]” correspond au comportement autonome de s’orienter en direction de l’Identity assignée dans la règle.  

<aside>

[Verbs](https://app.notion.com/p/3f862d77a12d80acb64ad4c1a0034d0b?pvs=21) : Un Verb est un Token permettant de construire une règle en associant deux Tokens entre eux.

- Le Verb “[Is](https://app.notion.com/p/Is-3f862d77a12d80bf81d6c214022d5b71?pvs=21) ” permet d’assigner à une Identity A à une Identity B.
- Le Verb “[Will](https://app.notion.com/p/Will-3f862d77a12d80e3a7d9efa7c38add62?pvs=21) ” permet d’assigner une Ability à une Identity.  
    </aside>

<aside>

[Autre](https://app.notion.com/p/3f862d77a12d80409189e3073b6a39dd?pvs=21) : Certains Tokens comme “Player” ne rentrent dans aucun des précédents types, et sont définis individuellement par une fonction particulière dans une règle.

- Le token “[Player](https://app.notion.com/p/Player-3f862d77a12d80e6b7c1f4f08b355d3e?pvs=21) ” est un token unique représentant le joueur physique derrière son écran, à travers la manipulation du controller.  
    </aside>

# Comment construire une règle ?

---

![{55446660-454E-48C8-A08B-C8A15EC89E70}.png](attachment:64a95809-6048-4c83-8ece-9a7db38254cd:55446660-454E-48C8-A08B-C8A15EC89E70.png)

Une régle se présente par 4 slot vide (en bleu) ,dedans on peux y glisser des token .

![{0F85098E-B7F4-480F-99EB-03277E8579D4}.png](attachment:9fbeb145-cf06-4fa3-bdac-cdeaba450611:0F85098E-B7F4-480F-99EB-03277E8579D4.png)

_ci dessus “l’inventaire” qui stocke exactement 1 copie de tout les token de notre présentation ._

![{55F64857-6B52-4913-9869-1AD285DDF434}.png](attachment:ecb21557-ed69-4055-a86e-5bb8af20c7c9:55F64857-6B52-4913-9869-1AD285DDF434.png)

_ci dessus du drag and drop , drop sur un token déjà placer les 2 swap de place_

- Une [règle](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) est une suite logique de [Token](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21)s, qui agit en temps réel sur le monde.
- Dans le setting initial du monde, une série de [règles](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) est déjà mise en place.
- Le joueur a accès en temps réel cette série de [règles](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21), et peut venir y déplacer les [Tokens](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) de façon à modifier le comportement du monde.
- Chaque [règle](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) est contrainte par des [limites syntaxiques](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21).

## Limites syntaxique

<aside>  
💬

- Les [règles](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) sont soumises à un arbre de construction syntaxique, qui permet d’assurer une certaine logique dans l’énoncé des [règles](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21).
- L’éditeur de [règles](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) empêche ainsi le placement de certains [Tokens](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) en fonction de ces [règles](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) de construction(bien qu’il n’en donne pas de sign/feedback visuel dans l’état actuel).

![image.png](attachment:c2fad99d-e032-428c-8c74-bd32323d8105:image.png)

</aside>

# Les règles donnent vie à un système

---

La capacité à modifier les éléments ainsi que les comportements présents dans l’espace de jeu change la dynamique de jeu traditionnel des toys : on se rapproche plus du moteur de jeu (comme Scratch) que d’un bac à sable mécanique.

Le fun vient alors de la manipulation et la découverte du champ des possibles, qui laisse au joueur la liberté de créer ses propres situations.

Exemple :

- Le jeu du chat : cette situation est atteignable en associant “Player” à une Identity X qui possède qu’une seule entité et en donnant le “Will Advance” , “Will Look at X” et “Will Kill X” à une identité nombreuse.

![image.png](attachment:22a4d9be-4a1b-4ddd-8657-cd70416c29cc:image.png)

![image.png](attachment:e2a2e0ff-8d37-4c70-bd13-ea54c48e1d1d:image.png)

- Une tourelle automatique : “will Look at X” ,”will spawn Y” et “Y will Advance”, “Will Kill X”

Le joueur à donc la capacité à crée des mini-jouet .