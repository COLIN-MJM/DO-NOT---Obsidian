### Définitions globales
______________
#### <span style="color:#f76707">Token</span>

> [!info]
> - Un Token est la plus petite brique de construction d’une phrase logique.
> - Une suite valide de Token est une règle.
> - En fonction de son type, il peut servir à identifier une [[Identity]], une [[Ability]] ou peut servir d’élément logique d’assignation via les [[Verbs]].

> Il existe 4 types de tokens :
> - [[Identity]]
> - [[Ability]]
> - [[Verbs]]
> - [[Autre]]
#### <span style="color:#1c7ed6">Règle</span>

> [!info]
> - Une règle est une suite logique de Tokens, qui agit en temps réel sur le monde.
> - Dans le setting initial du monde, une série de règles est déjà mise en place.
> - Le joueur a accès en temps réel cette série de règles, et peut venir y déplacer les Tokens de façon à modifier le comportement du monde.
> - Chaque règle est contrainte par des limites syntaxiques.

#### <span style="color:#ffa200">Limites syntaxique</span>

> [!info]
> 
> - Les règles sont soumises à un arbre de construction syntaxique, qui permet d’assurer une certaine logique dans l’énoncé des règles.
> - L’éditeur de règles empêche ainsi le placement de certains Tokens en fonction de ces règles de construction.

### Légende

- **Individu** = _membre d’une Identity_
- **Null si incomplète.** = _Si rien n’est attaché, alors la phrase est incomplète et aucun effet n’est appliqué._