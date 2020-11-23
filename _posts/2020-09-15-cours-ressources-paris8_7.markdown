---
layout: default
title:  "Cours Paris 8: Création et Gestion de ressources"
date:   2020-09-15 19:05:09 +0200
categories: classes, krita, 2D, fr
permalink: /cours/creation_gestion_ressources_7.html
---  

# O. [Menu](/cours/creation_gestion_ressources.html)
# I. [Introduction](/cours/creation_gestion_ressources_1.html)
# II. [Krita](/cours/creation_gestion_ressources_2.html)
# III. [Décors](/cours/creation_gestion_ressources_3.html)
# IV. [Son](/cours/creation_gestion_ressources_4.html)
# V. [Animation](/cours/creation_gestion_ressources_5.html)
# VI. [Finitions](/cours/creation_gestion_ressources_6.html)
# VII. [Exports](/cours/creation_gestion_ressources_7.html)
## 1) importer une spritesheet dans krita
- on va mettre chaque frame dans un fichier différent puis les réimporter dans la timeline
    - pour pouvoir la modifier
        - ajouter un accessoire ou changer le timing, par exemple
    - du coup:
        - l'ouvrir comme une image normale
        - Image > Image Split (Image > Fractionner l'image)
            - en png
        - ouvrir une nouvelle image de la taille d'une frame
        - File > Import as Animation Frames (Fichier > Importer les images de l'animation)
        - tadaaa!
            - vous pouvez commencer à travailler

## 2) exporter du pixel art pour des réseaux sociaux
- export png
- éventuellement ajouter de la marge
- agrandir x4 (ou x3, x2 ou x5 selon ce qui rend le mieux)
- filtre nearest neighbour (voisin le plus proche)
    - pour que ce soit lisible, parce que globalement un perso en pixel art tout seul, échelle 1, c'est pas hyper lisible
        - et si on zoome dans le navigateur il ne sait pas qu'il faut utiliser nearest neighbour
        - donc autant prendre les devants et le faire pour lui
    - et pour limiter les pertes de qualité dues aux algorithmes de compression des réseaux sociaux
        - il y aura une perte de qualité
        - mais moindre
        - parce qu'elle sera diluée dans un nombre de pixels identiques plus important

## 3) exporter son jeu
- itch.io
    - les collections de itch.io pour trier ses projets
    - ou pour ajouter les projets collaboratifs qui sont hébergés chez quelqu'un d'autre
    - les pages de jeux sont hautement personnalisables, et mieux vaut une belle page, tant qu'à faire
    - gamejolt aussi fait ça
        - je ne l'ai pas vraiment essayé, mais il n'y a pas de raison qu'il soit moins bien
- faire une version web
    - si possible
    - dans les game jams, les versions web sont en général plus jouées
        - mais hors du contexte d'une game jam, la différence est probablement moins grande
    - mais plus il y a de versions différentes plus les gens qui ont des configurations inhabituelles pourront en trouver une qui marche chez eux
- press kit
    - télécharger ici <http://dopresskit.com/>
    - exemples:
        - [](TODO: add examples)

# VIII. [Game Design](/cours/creation_gestion_ressources_8.html)
# X. [Annexes](/cours/creation_gestion_ressources_0.html)
