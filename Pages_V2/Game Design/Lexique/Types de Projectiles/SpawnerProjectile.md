---
tags:
  - projectile
---
## Informations 
___
- Comportement : Avance vers son forward + Instancie des projectiles toutes le X sec
	- Projectile instancié : Manipulable via l'éditeur + Dépend de l'Input
	- Orientation de l'instanciation : Perpendiculairement, de chaque côté
- Input : 
	- R : Fait spawner des [[StraightProjectile]]
	- T : Fait spawner des [[RotatingProjectile]]
	- Y : Fait spawner des [[BouncyProjectile]]
	NB : Une touche U, permettant de faire spawn des [[SpawnerProjectile]], a été pensée mais pas implémentée.
- Durée de vie : Infini
- <span style="color:#1c7ed6">Couleur : Bleu</span>
