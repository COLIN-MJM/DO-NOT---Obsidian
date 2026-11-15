*Note : S'il est possible -> Faire un ScriptableObject de type CameraParameters qui permettrait de faire des presets d'options de caméra (avec tous les paramètres cités plus bas).*

<u><b>Type</b></u> : TPS ;
<u><b>Input</u></b> : Mouvement de la souris / Stick droit permet de tourner la caméra;


La caméra possèdes deux modes distincts qu'elle est capable de naviguer.

<u><b>Mais premièrement, voici les propriétés partagées entre les deux modes :</u></b>
- Au contact de géométrie la caméra se déplace (se rapproche du joueur) pour éviter de passer au travers des murs ;
- Léger retard du mouvement de la caméra, la vitesse est progressive (pas instantanément la même que celle de l'avatar) pour éviter les à-coups
	- Être capable de paramétrer dans l'inspecteur :
		- la distance maximale de la caméra (par rapport au retard qu'elle peut prendre) ;
		- la vitesse à laquelle elle accélère à la vitesse de l'avatar ;
	- La caméra peut aller trop loin -> par exemple : le joueur s'arrête d'un coup sur un corps, la caméra ne s'arrête pas instantanément, elle ralentit très rapidement (donc elle va trop loin vers l'avant) avant de retourner à sa position cible ;
- Avoir une option paramétrable d'offset de la caméra avec un Vecteur 3, permettrait par exemple de paramétrer une vue épaule ;

<u><b>Avatar en apesanteur</u></b>
- La rotation de la caméra est lock en Z ;
- Rotation libre en X et Y ;

<u><b>Avatar sur un sol</u></b>
- La rotation de la caméra s'aligne à l'avatar pour avoir le sol au bas de l'écran : sol = bas ;
- La caméra à deux extrêmes qu'elle navigue de manière fluide (Lerp) en fonction de son état :
	- Caméra face l'avant = TPS
	- Caméra face le ciel (inverse du sol) = FPS
	(le lerp ne s'active pas avant de commencer à regarder vers le ciel à au moins 30 degrés par rapport à la caméra façant l'avant)
- Les inputs de mouvement de l'avatar s'adaptent à la caméra - Z = vers le forward de la caméra par rapport à l'avatar sans prendre en compte la rotation X de la caméra, sans input de mouvement, tourner la caméra autours de l'avatar ne change pas rotation ;
- Rotation libre en Y mais pas en X (il y a un maximum de 90° au au fait de regarder vers le haut ou le bas (dans les deux sens) ;