---
layout: post_cera_FR
title: "Personnes et Lieux - 5 : animation"
tags: FR illu
categories: 3D FR illu
last_updated: 26 juin 2026
description: tutoriel sur la série Personnes et Lieux
permalink: /illu/2026-06-26_PeopleInPlaces_5_FR.html
topnav: topnav_Portfolio_illu_FR
---
\
[< partie précédente: options du slicer <](/illu/2026-06-26_PeopleInPlaces_4_FR.html)

# Personnes et Lieux: Montagne

<iframe width="741" height="417" src="https://www.youtube.com/embed/rQhMd-MoOHM" frameborder="0" allow="gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Animation
- je les avais modélisés déjà en position, parce que je n'avais pas prévu, au départ, de les animer (aussi c'est plus intéressant à modéliser).
- je les ai ensuite riggés (ajouté une armature liée au mesh) et animés.
- je n'ai pas fait une armature complète quand je savais que je ne voulais qu'un mouvement très limité.\
Ne sont riggés / animés sur le photographe qu'un bras, deux mains, son objectif, et les papillons:
![photographer](/assets/art/2D/mountainPeeps_08_anim_photographer.jpg)

Le spéléologue était entièrement riggé, y compris la lampe frontale (c'est l'os de la tete), mais comme il pendait d'une corde il a été un peu plus compliqué de décider du rig (la racine du rig est sur la corde, là où le spéléologue s'y tient avec sa main):
![spelunker](/assets/art/2D/mountainPeeps_08b_anim_spelunker.jpg)

- les animations sont des turnarounds: le mode d'interpolation des keyframes de la caméra (dans le Graph Editor, Key > Interpolation Mode; la manière dont c'est animé entre deux keyframes) doit être Linear. Si on garde la valeur par défaut (Bézier), son mouvement commencera et finira très lentement et le début/fin de la boucle sera très visible.
- les keyframes des textures animées doivent aussi avoir comme mode d'interpolation Linear, pour les mêmes raisons. Dans le cas où on décide de ne pas choisir Linear, il est préférable de choisir le même mode pour le mouvement de caméra et le W des textures.
- les valeurs des keyframes des textures animées auront probablement besoin de changer très lentement. Pour mon animation, ça passe de 0 à 1 en 600 frames (24 secondes).
- pour que la texture boucle, elle ne va pas juste de W:0 à W:1, mais il y a en fait deux textures superposées (par une node Mix Color en mode Soft Light), l'un allant de 0 à 1 et l'autre de 1 à 0. Sans cela, il y aurait un à-coup visible entre la dernière et la première frame de la boucle.
- Etant donné que l'arrière-plan était sensiblement vide, et que je ne voulais pas montrer l'ombre des personnages sur un sol invisible (parfois une bonne solution, mais ici le photographe aurait dû avoir de l'herbe, et je n'avais pas envie de gérer ou modéliser ça), j'ai ajouté quelques éléments d'arrière-plan pour qu'il soit évident que c'est la caméra qui tourne et pas le personnage. Il est préférable d'avoir (au moins) deux éléments, un de chaque côté du personnage; autrement tant que les deux sont du même côté, le personnage a l'air de se déplacer au lieu de tourner.
- le turnaround dure environ 600 frames. Les animations des personnages durent 200 ou 300 frames (si la durée du turnaround est un multiple de la durée des animations de personnages, alors je peux n'exporter qu'un seul turnaround et il bouclera bien). Leur mode d'extrapolation (dans le Graph Editor, Channel > Extrapolation Mode; leur comportement après la dernière keyframe) doit être Make Cyclic (peut-être qu'il faut sélectionner toutes les nodes des courbes avant, je ne sais plus). Pour que ça boucle à l'infini.

## Conclusion
Parfait, j'espère que c'était utile! (et/ou intéressant)\
\
Il est peu probable que j'anime davantage de ces personnages sauf si un projet spécifique émerge.\
J'en imprimerai probablement assez pour en avoir un de chaque.\
Et j'ai une série Personnes et Lieux: Mer en cours, qui verra probablement la lumière du jour (en douze images fixes) d'ici les, disons, cinq prochaines années.
