# INF573_project

escalade difficulté:

## Objectif:
reconstruire la voie:
* en 2D: homographie entre les plans ou utilisation du travelling
* en 3D: stereo (maths cf cours 6 ?) / structure from motion (logiciel colmap) -> mesh de triangulation (voir Pyvista library ?)

pb reconstruction:
* peu de relief, MAIS info initiale: facettes planes
* identification des facettes : pointage à la main / détection des lignes (Canny, pas très efficace)

identification des prise: segmentation d’image  
à compléter

analyse mouvement:
* analyse squelette (biblio mediapipe)
* reconstruction squelette sur l'image 2D/3D

autre:
* suivie mouvement grimpeur
* score (prise tenue, bonus pour mouv supplémentaire)
* clippage dégaine -> efficacité clippage
* automatiser l'extraction plans


données:
vidéo: https://www.youtube.com/watch?v=F7YqluAHnfY
travel F: 9:33		travel face, plan côté, 2 gros plans
travel H: 1:18:43	travel côté, travel gros plan face (gros plan coté et 2 zoom gratons)
	1.18.43: vue d'ensemble
	1.18.46: plan coté 1
	1.18.51: plan coté 2
	1.18.53: plan face 1
