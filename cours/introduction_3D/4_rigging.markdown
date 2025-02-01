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

## 2) Créer une armature simple

### a) Créer une forme de grue de chantier sommaire
- avec plusieurs cubes étirés, faire une grue rudimentaire
- rappel: *L* pour sélectionner tous les vertices liés à là où il y a la souris

### b) Créer une armature
- En Object Mode, ajouter une Armature (*Shift A*, ou Add > Armature)
- Passer en Edit Mode (*Tab*) 
- Sélectionner les bouts de l'os créé pour le déplacer pour qu'il corresponde au pied de la grue (avec *Shift* pour être plus précis)
- De son sommet duquel partira le bras de la grue, extruder (*E*) pour l'os du bras de la grue (on peut aussi *shift D* dupliquer un os mais quand on extrude il est lié au précédent par défaut)
- Extruder à nouveau pour l'os du chargement
- Dans la fenêtre Properties en bas à droite, onglet Os / Bones (icône d'un os), renommer chacun des os (en haut)
- pour info, pour dé-lier un os au précédent, c'est dans Bone > Relations > Connected. On peut aussi y changer qui est le parent de l'os actuel, et si l'enfant hérite la rotation du parent.
- D'ailleurs pour le chargement de la grue on ne veut pas que cet os hérite la rotation (parce que c'est juste une chaine souple, donc elle est toujours à la verticale).

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
- sélectionner le mesh en object mode puis passer en mode Weight Painting avec *ctrl Tab*
- dans la vue Properties, onglet Data, il y a un groupe par os. En choisir un.
- Peindre en cliquant sur le mesh. En rouge sont les vertices qui héritent de 100% des paramètres de l'os d'après lequel le groupe est nommé, en bleu foncé ceux sur lesquels cet os n'a aucune influence.
- Pour gommer, trouver le bouton "brush" parmi ceux dans le haut de la vue 3D, et changer Blend (qui par défaut est sur Mix) à Substract
- cacher des sommets si besoin (*H* en edit mode) (pour les rendre visibles à nouveau, *alt H*)
- (de manière générale: alt a tendance à annuler des choses. *alt H* ou dé-cacher, *alt P* pour dé-parenter, *alt G* pour remettre la position à zéro, etc.)
- tester les mouvements

### e) le transformer en bras de robot (en ajoutant un pied et acceptant qu'il s'incline mais pas qu'il se déplace)
- un mesh de cylindre
- une contrainte de position (vue Properties, onglet Bone Constraints, Limit Location)
- notre armature a donc maintenant quatre os: un pied fixe, une jambe verticale qui peut s'incliner, un bras horizontal qui peut s'incliner, et un os vertical qui ne s'incline pas.

### f) EXERCICE 1: un mouvement de la grue entre trois positions précises
- déterminer trois positions proches de la grue choisies au hasard, pour que la grue y récupère/dépose un objet (marquer chaque position avec un empty)
- faire une animation entre le bout de la grue touchant chacune des trois positions
- pour une animation, mettre dans la bonne position, sélectionner tous les os et appuyer sur *I*, puis dans la vue Timeline changer de frame (point dans le temps; avec clic gauche en haut ou flèche droite) et appliquer la position suivante.

### g) ajouter de l'IK
- oh wow l'exo d'avant était super pas pratique ce serait tellement mieux avec de l'IK
- IK c'est Inverse Kinematics (Cinématique Inverse); un mode d'animation où au lieu de contrôler les positions/rotations de chaque os on contrôle une cible qu'ils essaient de toucher et l'ordinateur se charge de les positionner comme il faut.
- du coup s'il y a deux positions possibles ça peut poser problème, il peut se plier dans le mauvais sens
- mais on peut minimiser le risque d'erreur en positionnant bien les os quand on crée l'armature, ou en utilisant des contraintes (soit diminuer la liberté de rotation, soit avoir un os qui contraint l'orientation d'un autre)
- du coup pour notre grue appliquer une Bone Constraint: Inverse Kinematics
- voir comment ça réagit avec les paramètres par défaut
- puis changer la chain length à 2 (ce qui veut dire: l'IK contrôle l'os actif et son parent; avec 3 il contrôlerait l'os actif et deux parents) et voir ce que ça donne
- puis rajouter un os à l'armature, le rendre sans parent, et le mettre comme "Target" de l'IK (ne pas oublier de définir comme target l'armature, puis l'os dans l'armature; ça se fait en deux étapes) et voir ce que ça donne
- puis activer "rotation" dans l'IK, et voir ce que ça donne (s'il n'y a pas de target alors rotation ne fait rien)

### h) EXERCICE 2: un mouvement de la grue entre trois positions précises - avec de l'IK

## 3) Créer une armature de quadrupède simple

### a) EXERCICE 3: créer l'armature
(si vous n'avez pas de mesh de quadrupède simple, vous pouvez utiliser [ce dromadaire low-poly](https://drive.google.com/file/d/1EriBObu5o36lKhlBurb3BOEdSZXGNJNe))
- ne pas oublier de changer de point de vue de temps en temps pour vérifier que l'armature n'est pas toute plate
- *ctrl E* extruder des os, éventuellement changer leurs parents et s'ils sont connectés
- Renommer ses os aussi, dans l'onglet Bone des Properties à droite.
- pour pouvoir utiliser les outils de symmétrie, faire une jambe et un bras, les nommer en .L ou .R
- les sélectionner, *clic droit > symmetrize* (si ça ne marche pas tourner l'armature en edit mode de 90°, et éventuellement changer le point de rotation) pour avoir les deuxièmes bras / jambe
- *alt R* pour réintialiser la rotation des os avant de commencer à animer

### b) Contraintes d'animation (Bone Constraints)
- Inverse Kinematics
- Limit Rotation: pour définir l'ampliture de mouvement d'une articulation par exemple
- Limit Location
- Copy Rotation: par exemple pour que toutes les roues d'une voiture tournent en même temps, mais chacune autour de son propre centre de gravité
- Copy Location
- Damped Track: faire que l'os pointe toujours vers l'objet cible. Par exemple pour un objet qui fait toujours face à la caméra.
- Floor: définir une limite que l'os ne peut pas dépasser, pour empêcher par exemple qu'un pied s'enfonce dans le sol
- pour info Spline IK est à utiliser pour une longue chaine d'os souple, comme par exemple une corde ou le cou d'un héron

### c) tester

### d) Skinning / Weight Painting
- voir 1.d) pour instructions

### e) tester
- tester
- notamment faire attention au placement des articulations par rapport aux faces et aux sommets pour que le centre de rotation soit correct et que ça ne déforme pas trop
- et parfois il y a des sommets qui sont par erreur liés à un os avec lequel ils n'ont rien à faire, et on ne s'en rend compte que quand on teste des mouvements
- modifier quand ça ne va pas
- re-tester
- re-modifier quand ça ne va toujours pas mais d'une manière différente
- etc.

### f) os non déformants
- on peut faire des os qui n'ont pas d'influence directe sur le mesh
- ils servent juste à bouger les autres os (par exemple les cibles de l'IK; d'ailleurs les os directement influencés par l'IK en général n'ont pas besoin d'être bougés; je conseille de nommer vos os cibles d'IK quelque chose comme "IK_bras.R" comme ça ils sont tous à côté les uns des autres dans la liste et facilement trouvables)
- quand on parente un mesh à une armature avec création de groupes automatiques, les os non déformants ne créeront pas de groupe (ce qui est pratique)
- quand je fais des mesh avec de l'IK, j'en ai un (que j'appelle ROOT, mais vous pouvez l'appeler autrement) qui est parent de l'os au sommet de la hiérarchie (le bassin, en général, chez un animal; on pourrait contrôler directement le bassin mais avoir un os qui dépasse et est très visible est pratique), et un autre (que j'appelle UBERROOT, mais pareil appelez-le comme vous voulez; ils sont tout en majuscules pour pouvoir les retrouver facilement), qui est parent de ROOT et des os cibles de l'IK (parce que les os cibles de l'IK ne peuvent pas être enfants de la chaîne d'os qu'ils dirigent). Ça permet d'avoir un perso humain qui se lève, les mains posées sur le bureau (on bouge ROOT), ou d'avoir un perso qui saute, et dont les bras et les jambes avancent plus ou moins au même rythme que leur corps (on bouge UBERROOT).
