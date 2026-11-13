---
tags:
  - old
---
Les [[Projectiles]] sont des objets gravitant autour de la [[Sphère]] instanciés depuis l'[[OriginSpawner]] via l'input du [[Joueur - 3Cs]].

Il existe différents types de [[Projectiles]], caractérisés par leur comportement et leur trajectoire : 

- [[StraightProjectile]]
- [[RotatingProjectile]]
- [[BouncyProjectile]]
- [[SpawnerProjectile]]

Chaque type de [[Projectiles]] est associé à une couleur, permettant de l'identifier après instanciation sur la scène.

## Projectile et joueur
___
Lors de son instanciation, le [[Joueur - 3Cs]] peut choisir d'"incarner" le projectile instancié, résultant en un changement de point de vue.
Une fois incarné, le [[Joueur - 3Cs]] peut altérer la rotation du projectile en plein vol.
