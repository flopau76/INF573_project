# INF573_project

escalade difficulté:

Objectif:
reconstruire la voie:
-homographie entre les plans ou utilisation travelling
-identification des prise: segmentation d’image

pb:
-3d/ profondeur	-> relativement plan, dur de trouver le relief
-quel donnée: travelling/gros plan grimpeur

suivie mouvement grimpeur
-mappage gros plan grimpeur et reconstruction de la voie
-score (prise tenue, bonus pour mouv supplémentaire)
-clippage dégaine -> efficacité clippage

analyse mouvement
-analyse squelette
-reconstruction sur image 3D

automatiser extraction plans
-détecter automatiquement les plans intéressants à partir de la vidéo


logiciel : colmap
pointage facettes à la main + équations position caméra/points

données:
vidéo: https://www.youtube.com/watch?v=F7YqluAHnfY
travel F: 9:33		travel face, plan côté, 2 gros plans
travel H: 1:18:43	travel côté, travel gros plan face (gros plan coté et 2 zoom gratons)
	1.18.43: vue d'ensemble
	1.18.46: plan coté 1
	1.18.51: plan coté 2
	1.18.53: plan face 1
	


	
J’ai pas accès à tout dans le Drive, notamment les data
pour l’identification des prises : 
odg 20-50 prises à trouver ??
est ce que chercher les outliers de la couleur des prises permet de les retrouver ?
cas des prises bitexture: un moyen de contourner ça est de retrouver la géométire de la prise (que ca soit dans le rendu final une tâche et pas un point) Est ce qu(on peut retrouver la tâche à partir de la couleur de la prise ? 
en dehors des prises, le plan est assez gris, on peut inclure la couleur dans les outliers pour avoir un truc + spécifique : surtout que les prises respectent un code couleur (noir joune et rouge pour la voie 1)) ?
pb des prises sur la voie d’à côté (est ce que c’est vraiment un pb ?)
pb du sol, plafond,(on peut tricher et les cacher dans les images inputs)  panneaux start & top (vu qu’on sait à quoi ils ressemblent on peut ptet les blacklister ??)


pour la géométrie du plan : 
extraire les faces (ou les 3-4 points qui la définissent) à partir des différents plans. Ca existe un logiciel python qui divise une image en triangles ??
à partir des 2 images stereo , on peut avoir une idée de la profondeur (rectification -> calcul disparity et f -> déduire profondeur) cours 6 slide 7
idée pour retrouver les faces : quand on a construit les outliers on les a fait pour qu’ils ne detectent pas les lignes (pris la plus petite valeur propre). On peut faire la démarche inverse pour qu’il détecte spécifiquement les lignes ?? (grande -  petite / C + petite )par exemple
avant de reconstruire en 3D, colorier la profondeur pour voir si c’est cohérent.
pour reconstruire en 3D, visual studio ?? ou bibliothèque python


 



mesh technology from the Pyvista library
