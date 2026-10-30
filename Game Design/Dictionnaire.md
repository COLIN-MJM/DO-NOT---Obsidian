_________________________
__________________________________________________________________________

### Définitions globales
______________
#### Token

> [!NOTE]
> - Un Token est la plus petite brique de construction d’une phrase logique.
> - Une suite valide de Token est une [règle](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21).
> - En fonction de son type, il peut servir à identifier une [Identity](https://app.notion.com/p/3f862d77a12d8028a85bc0703dc32b22?pvs=21), une [Ability](https://app.notion.com/p/3f862d77a12d8004b619f0b8f2939294?pvs=21) ou peut servir d’élément logique d’assignation via les [Verbs](https://app.notion.com/p/3f862d77a12d80acb64ad4c1a0034d0b?pvs=21).

#### Règle

> [!NOTE]
> - Une [règle](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) est une suite logique de [Token](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21)s, qui agit en temps réel sur le monde.
> - Dans le setting initial du monde, une série de [règles](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) est déjà mise en place.
> - Le joueur a accès en temps réel cette série de [règles](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21), et peut venir y déplacer les [Tokens](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) de façon à modifier le comportement du monde.
> - Chaque [règle](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) est contrainte par des [limites syntaxiques](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21).

#### Limites syntaxique

> [!NOTE]
> 
> - Les [règles](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) sont soumises à un arbre de construction syntaxique, qui permet d’assurer une certaine logique dans l’énoncé des [règles](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21).
> - L’éditeur de [règles](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) empêche ainsi le placement de certains [Tokens](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) en fonction de ces [règles](https://app.notion.com/p/Dictionnaire-3f862d77a12d80b99a46f3ddf4a51b51?pvs=21) de construction.
> ![[Schéma_Syntaxe.png]]

### Légende

- **Individu** = _membre d’une Identity_
- **Null si incomplète.** = _Si rien n’est attaché, alors la phrase est incomplète et aucun effet n’est appliqué._