# INF573_project: lead climbing

## Jupyter notebook
The core of the project is contained in project_INF573.ipynb. It should be directly runable, after installation of the needed dependencies.

## Colmap
This folder is the workspace used with colmap. It contains the results of the SfM, especially the file project.ini corresponding to the project initialisation. Use the script contained in extract_video.ipynb to extract images from the adequate video (by default, /data/video/travel.mp4, see below)

## Data
The original video is available on youtube at: https://www.youtube.com/watch?v=F7YqluAHnfY
The folder data/ contains:
* video/ : three extracts of the original video: one travelling along the route and two climbing performances
* other/ : a folder with two photos from the wall and corresponding text files of extracted key-points (by hand generated)

## Objectif:
reconstruire la voie:
* en 2D: homographie entre les plans ou utilisation du travelling
* en 3D: stereo (maths cf cours 6 ?) / structure from motion (logiciel colmap) -> mesh de triangulation (voir Pyvista library ?)

problème de reconstruction:
* peu de relief, MAIS info initiale: facettes planes
* identification des facettes : pointage à la main / détection des lignes (Canny pas très efficace)

identification des prise: segmentation d’image  

analyse du mouvement:
* analyse squelette (biblio mediapipe)
* reconstruction squelette sur l'image 2D/3D

pistes:
* suivie mouvement grimpeur
* score (prise tenue, bonus pour mouv supplémentaire)
* clippage dégaine -> efficacité clippage
* automatiser l'extraction plans. idée: détecter l'apparition et la disparition du chrono en bas à droite qui corrpond à la performance d'un grimpeur
