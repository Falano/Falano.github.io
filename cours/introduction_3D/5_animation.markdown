---
layout: page
title:  "Cours Paris 8: introduction à la 3D avec blender"
last_updated: October 27, 2024
permalink: /cours/introduction_3D/animation.html
topnav: topnav_P8_3D
---

# V. Animation

## 1) Base
### a) Vocabulaire
- une Frame c'est un moment dans le temps. En animation 2D ça correspondait à un dessin. En 3D il y a l'interpolation donc les contraintes temporelles sont un peu différentes. Le framerate (ou fps, nombre de frames par seconde) par défaut de Blender est de 24 (on peut le changer dans Properties > Output > Format > Frame Rate)
- une Clé d'Animation, ou Keyframe, ou Key, est une position définie par l'animateur à un moment précis de l'animation, et l'ordinateur interpole (crée les positions intermédiaires entre les keyframes pour les frames pour lesquelles on n'a pas défini de keyframe)

### b) Principes généraux
- L'animation en gros c'est une suite de positions
- aller dans la vue Timeline, changer de place (*clic gauche* sur le numéro des frames ou *flèches droite et gauche*), déterminer une nouvelle position, sauvegarder avec *I* les os qui ont bougé, et recommencer
- **ATTENTION!** Si on pose notre armature puis change de frame sans la sauvegarder dans une keyframe avec *I*, alors la pose sera perdue. Si au contraire on pose notre armature et on la sauvegarde, mais on avait oublié de changer de frame au début, on écrase la pose précédente. Donc bien penser à changer de frame, poser, sauver, changer de frame.
- Si tous les bouts de notre action commencent et s'arrêtent en même temps, ça ne fait pas très naturel (cool pour un robot! Pas pour un chat): décaler légèrement chaque membre. Aussi, la position et la rotation d'un même os peuvent être sauvegardées indépendemment, donc peuvent ne pas être sur la même frame.
- dans la vue 3D, le menu de droite permet d'insérer/supprimer/remplacer une keyframe pour rotation/location (position)/scale (échelle), soit tout à la fois (le comportement par défaut de *I*), soit juste pour par exemple l'axe X de la position.
- pour lancer l'anim c'est *Barre Espace* (ou parfois *ctrl barre espace*, en fonction de vos paramètres; sinon au milieu haut dans la timeline il y a les boutons: jouer l'anim, la jouer à l'envers, aller à la keyframe suivante/précédente, aller à la fin/début de l'anim)
- si on n'aime pas le rythme d'une anim on peut sélectionner des keyframes dans la timeline et utiliser G pour les déplacer dans le temps ou S pour faire durer l'ensemble de la sélection plus ou moins longtemps (en gardant les rapports entre les clés)
- on utilise principalement les keyframes pour sauvegarder les positions et rotations des os d'une armature, mais beaucoup de paramètres de blender peuvent être animés avec des keyframes, comme par exemple les paramètres des matériaux ou des contraintes (faites un *clic droit* et voyez s'il vous propose d'insérer une keyframe)

### c) EXERCICE 1: animation simple
- faites une animation simple avec un des meshs que vous avez riggé jusque-là.
- vous pouvez changer la longueur de l'anim (à quelle frame Blender considère que l'anim est finie et retourne au début) dans la Timeline, ce sont les valeurs (haut droite) Start et End.

## 2) Méthodes d'animation additionnelles
### a) anim symmétrique
TODO

### b) EXERCICE 2: Cycle de marche
- faire un cycle de marche en utilisant les options de symmétrie

### c) courbes
- notamment utile pour lisser les débuts/fins de boucle d'animation
TODO

### d) EXERCICE 3: Courbes
- tester comment fonctionnent les courbes

### e) les Shape Keys
- vue Properties > onglet Data > Shape keys
- pas mal utilisé pour les expressions faciales et les mouvements de muscles
- le principe c'est qu'on a deux (ou plus) états de modélisation (donc on modèle le premier, qui compte comme état de base, on le sauvegarde comme shape key, puis on le modifie en bougeant les vertices comme pour de la modélisation normale pour atteindre le second état, qu'on sauvegarde comme notre première shape key), et on peut décider si la position des vertices est 100% la base, 100% la shape key, ou un mélange (voire -100% la shape key, ou 200%, si on veut).
- par contre on peut modifier la position des vertices mais on n'a pas le droit d'en ajouter ou d'en supprimer (mais on peut en mettre plusieurs à la même position, pour qu'il semble à l'oeil nu qu'il y en a moins)
- et du coup c'est compatible avec l'animation d'armatures. La position d'un vertice peut tout à fait être influencé à la fois par une shape key et par une armature (parce que l'animation d'armature c'est une modification par rapport à la position de repos du vertex; avec une shape key on déclare juste "non en fait la position de repos c'est celle-ci (la shape key) et pas celle-là (la base des shape keys)")

### f) EXERCICE 4: tester les shape keys
- faire une animation utilisant des shape keys.
