---
layout: page
title:  "Cours Paris 8: introduction à la 3D avec blender"
last_updated: October 27, 2024
permalink: /cours/introduction_3D/rigging.html
topnav: topnav_P8_3D
---

# IV. Rigging

## 1) Vocabulaire
- Squelette / Armature
- Os / Bone

## 1) Créer une armature simple

### a) Créer une forme de grue de chantier sommaire
- avec plusieurs cubes étirés, faire une grue rudimentaire
- rappel: *L* pour sélectionner tous les vertices liés à là où il y a la souris

### b) Créer une armature
ne pas hériter la rotation pour le chargement
- En Object Mode, ajouter une Armature (*Shift A*, ou Add > Armature)
- Passer en Edit Mode (*Tab*) 
- Sélectionner les bouts de l'os créé pour le déplacer pour qu'il corresponde au pied de la grue (avec *Shift* pour être plus précis)
- De son sommet duquel partira le bras de la grue, extruder (*E*) pour l'os du bras de la grue
- Extruder à nouveau pour l'os du chargement
- Dans la fenêtre Properties en bas à droite, onglet Os / Bones (icône d'un os), renommer chacun des os (en haut)

### c) Tester son mouvement
- quitter l'Edit Mode pour passer en Pose Mode (*ctrl Tab*; image: 3, haut gauche)
- (la sélection est maintenant en bleu clair au lieu de orange)
- essayer de déplacer (*G*), redimensionner (*S*) et tourner (*R*) les différents os.
- observer quels mouvements sont possibles et comment ils modifient les autres os
- (par défaut, les modifications des os parents sont héritées par les os enfants, ceux qui sont plus loin dans la chaine d'extrusion)
- retourner en Edit Mode, et dans la fenêtre Properties (en bas à droite), aller dans Relations, sélectionner le dernier os, changer Inherit Rotation
- tester les mouvements en Pose Mode

### d) Attacher l'armature à un mesh / Skinner / Weight Painting
- En Object Mode, sélectionner (*clic gauche*) le mesh, puis (*shift clic gauche*) l'armature
- les lier (*ctrl P*, ou Object > Parent). On va utiliser Armature Deform > With Empty Groups
- Sélectionner
- cacher des sommets si besoin (*H*) (pour les rendre visibles à nouveau, *alt H*)
- (de manière générale: alt a tendance à annuler des choses. *alt H* ou dé-cacher, *alt P* pour dé-parenter, *alt G* pour remettre la position à zéro, etc.)

### e) le transformer en bras de robot (en ajoutant un pied et acceptant qu'il s'incline mais pas qu'il se déplace)
- un mesh de cylindre
- une contrainte de position (lock position)

### f) EXO: essayer de toucher des positions précises deux/trois fois (voire: un mouvement entre deux/trois positions: leur montrer une base d'anim): oh wow c'est super pas pratique ce serait tellement mieux avec de l'IK

### g) ajouter de l'IK
- IK c'est Inverse Kinematics (Cinématique Inverse); un mode d'animation où au lieu de contrôler les positions/rotations de chaque os on contrôle une cible qu'ils essaient de toucher et l'ordinateur se charge de les positionner comme il faut.
- du coup s'il y a deux positions possibles ça peut poser problème, il peut se plier dans le mauvais sens
- mais on peut minimiser le risque d'erreur en positionnant bien les os quand on crée l'armature, ou en utilisant des contraintes (soit diminuer la liberté de rotation, soit avoir un os qui contraint l'orientation d'un autre)

## 2) Créer une armature de quadrupède simple

### a) EXO: créer l'armature
(choper le mesh du drom)
### a) Contraintes d'animation (Constraints)
### b) tester
### c) Skinning / Weight Painting
- hide
### d) tester
- tester
- notamment faire attention au placement des articulations par rapport aux faces et aux sommets pour que le centre de rotation soit correct et que ça ne déforme pas trop
- et parfois il y a des sommets qui sont par erreur liés à un os avec lequel ils n'ont rien à faire, et on ne s'en rend compte que quand on teste des mouvements
- modifier quand ça ne va pas
- re-tester
- re-modifier quand ça ne va toujours pas, mais d'une manière différente
- etc.
