---
layout: post_cera_FR
title: "Personnes et Lieux - 1 : impression 2D"
tags: FR illu
categories: 3D FR illu
last_updated: 26 juin 2026
description: tutoriel sur la série Personnes et Lieux
permalink: /illu/2026-06-26_PeopleInPlaces_1_FR.html
topnav: topnav_Portfolio_illu_FR
---
\
[< partie précédente: introduction <](/illu/2026-06-19_PeopleInPlaces_0_FR.html) | [> partie suivante: textures procédurales >](/illu/2026-06-19_PeopleInPlaces_2_FR.html)

# Personnes et Lieux: Montagne

|![mountain peeps: 100](/assets/art/2D/mountainPeeps_0100_wm.jpg)|![mountain peeps: 160](/assets/art/2D/mountainPeeps_0160_wm.jpg)|
|![mountain peeps: 140](/assets/art/2D/mountainPeeps_0140_wm.jpg)|![mountain peeps: 200](/assets/art/2D/mountainPeeps_0200_wm.jpg)|

## Impression 2D
### modélisation
- D'abord, je modélise un personnage en low-poly. Je commence par un cube et j'extrude, loop cutte (ajouter des points en anneau), et Tourne/Déplace/Redimensionne des groupes de points, beaucoup de fois. Il y a d'autres manières de le faire mais c'est celle que je préfère.

|![mountain peeps: modeling](/assets/art/2D/mountainPeeps_01a_lopo.jpg)|![mountain peeps: modeling](/assets/art/2D/mountainPeeps_01b_lopo.jpg)|

### matériau
- Ensuite je dessine quelques dégradés; ici j'ai utilisé 256x256 mais ça pourrait marcher avec un canevas aussi petit que 10x10. Je commence en général avec deux ou trois dégradés et en ajoute quand nécessaire. Tous les personnages de la série partagent le même fichier de couleurs, et le même matériau.
- Ensuite, j'unwrappe (déplie? le mettre à plat pour assigner à chaque face une couleur/motif); pour ce style j'utilise beaucoup "unwrap from view" en ayant sélectionné toute la zone de la même couleur que je place ensuite sur le dégradé. Certaines faces se superposent, ce n'est pas un problème, ça veut juste dire qu'elles ont la même couleur. Je dois souvent aussi redimmensionner les faces sélectionnées sur l'axe X ou Y pour qu'elles ne dépassent pas du dégradé mais changent de couleur à la bonne vitesse.
- En général j'ajoute au matériau un peu d'émission, en utilisant exactement les mêmes couleurs/la même image que pour la couleur, pour éclaircir les ombres.

|![mountain peeps: material](/assets/art/2D/mountainPeeps_02a_tex.jpg)|![mountain peeps: material](/assets/art/2D/mountainPeeps_02b_tex.jpg)|

### organisation
- J'ai mis tous les personnages dans le même fichier, sur une ligne, un chaque 20 unités, et animé la position de la caméra (qui bouge d'une unité par frame) et la couleur de l'arrière-plan, ce qui me permet faire un rendu pour tous les personnages d'un coup en mettant l'animation frame step ("pas de l'animation"?) à 20 (pour qu'il fasse un rendu chaque 20 image). Je n'ai pas de certitude que ce soit la meilleure manière de faire (au lieu de les laisser chacun dans son propre fichier) mais ça marche pour moi.

### calque de texture
- ensuite, je vais dans la fenetre Compositor.
- La texture des impressions 2D est procédurale. Dans une première version j'utilisais des scans de papier taché de thé que j'ajoutais après coup dans un logiciel de dessin, mais pour cette version je voulais tout faire dans blender (plus simple) et avoir un nombre infini de textures possible (ou au moins douze, vu que j'ai douze personnages).
- Dans le Compositor j'utilise surtout des nodes Noise (Gabor et Voronoi donnent aussi des résultats intéressants; pour info, le Noise de blender est du bruit de Perlin), auxquelles j'applique des ColorRamp et que je mélange ensemble entre elles avec une node Mix Color. Je teste les différents modes de mélange de la node Mix Color et parfois j'utilise une texture (au lieu d'un nombre) comme entrée Factor.
- Pour faire une animation ou plusieurs textures différentes, il est important que la texture Noise soit de type "4D", et que toutes les entrées W des nodes Noise soient contrôlées par la même node Value, ce qui permet de toutes les changer d'un coup. Par exemple quand on teste à quelle vitesse on veut que la texture change. 
- - Pour zoomer sur la texture le principe est le même: une même node Value définissant toutes les entrées Scale (avec une node Add/Multiply si besoin pour qu'elle gardent les mêmes proportions relatives mais n'aient pas exactement la même valeur). 
- - Idéalement si on groupe ses nodes de bruit la variable (qui gère les W) devrait être hors du groupe, pour pouvoir utiliser la même pour différents groupes.
- J'ai aussi utilisé des nodes Glare, Gamma et Exposure pour contrôler la luminosité, comme elle est très affectée par les textures, et qu'il faut une version plus claire pour l'impression que pour le web.

Toute la hiérarchie des nodes (les nodes "unused output" ne servent qu'à créer des images intermédiaires pour la documentation, elles ne changent pas la texture elle-même):
![mountain peeps: texture overlay node structure](/assets/art/2D/mountainPeeps_03g_tex-structure.jpg)

Le groupe de nodes (qui s'appelait "Noise" sur l'image précédente) qui crée la texture:
![mountain peeps: texture overlay node structure](/assets/art/2D/mountainPeeps_03d_tex-structure.jpg)

Le groupe de nodes, en images intermédiaires:
![mountain peeps: texture overlay node structure](/assets/art/2D/mountainPeeps_03h_texs.jpg)

Toutes les étapes:
![mountain peeps: one picture for each step of the process, on two characters: Base, Glare, Texture, Picture + Texture, Exposure and Gamma](/assets/art/2D/mountainPeeps_all.jpg)


### test de texture sur la géométrie
- J'ai essayé de faire une texture procédurale de bois (qui modifierait la géométrie de l'objet) pour accentuer l'aspect non-plastique, mais ce n'était pas tout à fait convainquant. J'ai utilisé des Geometry Nodes (nodes de géométrie?) avec une texture de bois procédurale redimensionnée sur un axe pour l'allonger, et un modifier Subdivision Surface très haut (option: simple, pour que ça augmente la résolution sans arrondir la forme). Finalement j'ai estimé que ça attirait trop l'attention au détriment de mon esthétique low-poly, et parfois au lieu de creuser dans la forme (comme des veines de bois) ça en ressortait (comme des champignons) sans que je ne sache pourquoi. Je pense que je pourrais trouver une manière de le modifier pour atteindre un résultat satisfaisant, mais ça nécessiterait plus de tests que je n'avais le temps de faire.

Comparaison entre trois textures d'impressions 3D: à gauche, avec l'option fuzzy skin (les paramètres que j'ai utilisé pour toute la série), au milieu la texture bois des Geometry Nodes, à droite la texture par défaut.
![mountain peeps: comparison between three 3D prints with different textures](/assets/art/2D/mountainPeeps_04a_textures.jpg)

[> partie suivante: textures procédurales >](/illu/2026-06-19_PeopleInPlaces_2_FR.html)
