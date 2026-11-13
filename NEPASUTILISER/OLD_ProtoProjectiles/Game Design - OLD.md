---
icon: 📚
tags:
  - old
---
Le système du jouet est composé de 4 éléments principaux :
- la [[Sphère]] ;
- l'[[OriginSpawner]] ;
- les [[Projectiles]] ;
- le [[Joueur - 3Cs]].

![[Pasted image 20261103115408.png]]


![[Pasted image 20261103131305.png]]


# Character

---

- Le [[Joueur - 3Cs]] n'a pas de réelle incarnation physique dans la scène : il est rattaché au départ à un POV global depuis l' [[OriginSpawner]], mais peut prendre le POV de n'importe quel [[Projectiles]] à son instanciation.
- Le [[Joueur - 3Cs]] peut instancier des [[Projectiles]], altérer la rotation d'un [[Projectiles]] dont il a pris le POV, ainsi que bouger la caméra autour de la [[Sphère]] s'il est sur le POV global.

# Controller

---

- Le [[Joueur - 3Cs]] instancie un projectile avec les inputs A-Z-E-R-T-Y
	- + Control : Prend le POV du projectile instancié
	- + Shift : Instancie 8 projectiles en même temps
	NB : Si le joueur utilise Control + Shift, il prendra le POV du projectile situé au Forward du [[OriginSpawner]].


Contextuel :
 - Si le joueur est dans le POV global :
	 - Manipuler la caméra : Souris
 - Si le joueur est dans le POV d'un projectile :
	 - Altérer la rotation du projectile : Souris (via un slider)

# Camera

---

En fonction du POV du joueur, le comportement de la caméra change :
- Dans le POV global, le joueur a un contrôle semi-libre de la caméra, qui cadre la sphère au centre de l'écran.
- Dans le POV d'un projectile, la caméra suit automatiquement le projectile, qui est cadré au centre de l'écran.