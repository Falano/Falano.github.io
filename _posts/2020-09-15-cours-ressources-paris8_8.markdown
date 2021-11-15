---
layout: default
title:  "Cours Paris 8: Création et Gestion de ressources"
date:   2020-09-15 19:05:09 +0200
categories: classes, krita, 2D, fr
permalink: /cours/creation_gestion_ressources_8.html
---  

# O. [Menu](/cours/creation_gestion_ressources.html)
# I. [Introduction](/cours/creation_gestion_ressources_1.html)
# II. [Krita](/cours/creation_gestion_ressources_2.html)
# III. [Décors](/cours/creation_gestion_ressources_3.html)
# IV. [Son](/cours/creation_gestion_ressources_4.html)
# V. [Animation](/cours/creation_gestion_ressources_5.html)
# VI. [Finitions](/cours/creation_gestion_ressources_6.html)
# VII. [Exports](/cours/creation_gestion_ressources_7.html)
# VIII. [Game Design](/cours/creation_gestion_ressources_8.html)
## 1) notions de game design
- si jeu de plateforme/énigmes avec plusieurs niveaux: introduire une seule mécanique de jeu à la fois et laisser le temps d'expérimenter (cf III.x) (cf [une vidéo en anglais intéressante mais où il parle vite](https://www.youtube.com/watch?v=8FpigqfcvlM))
- lisibilité (cf II.2)
- vitesse de réaction du jeu: éviter les animations longues en début d'action (cf V.1)
- de l'importance du son (cf IV.1)
- de l'importance des retours visuels (feedback) (cf V.1)
- essayer d'avoir une unité graphique
    - et une unité entre le graphique, l'audio, l'histoire et le gameplay
    - ou au contraire qu'ils soient opposés, pour un effet de malaise bizarre
        - cf Happy Tree Friends (attention: gore), [Limbo](/assets/995_limbo.jpg) par Playdead: <https://playdead.com/games/limbo/>
- à propos de la musique: pour chaque musique différente, penser à son utilisation
    - une musique de fond doit avoir un cycle long (ne se répéter qu'au bout d'un certain temps)
        - mais on peut avoir plusieurs variations sur le même thème
        - tester de l'écouter en boucle pendant dix minutes (y compris en faisant autre chose) pour vérifier qu'elle ne devient pas irritante à la longue
    - une musique de fin de combat par exemple peut avoir un cycle beaucoup plus court
- à propos du son: penser aussi à son utilisation
    - si vous mettez des bruits de pas, envisager de prévoir plusieurs variations
        - pas trop différents non plus, qu'on sente que c'est la même personne qui marche sur le même matériau
            - juste pour éviter d'avoir exactement le même son plein de fois de suite
                - (on fait beaucoup de pas quand on marche)
    - même pour un son qui est censé être très fort, strident ou un peu désagréable, ne pas le rendre trop fort/strident/désagréable
        - penser aux tympans du joueur
    - plus on entend un bruit souvent plus il devrait être discret
        - un bruit de pas n'a pas besoin d'être très fort
        - la super attaque du boss final qu'il n'utilise qu'une fois toutes les cinq minutes peut avoir un son plus fort, et durer plus longtemps, et avoir un son plus remarquable
            - et avoir un screen-shake
            - et un flash sur le perso
            - et des particules!
- flow

## 2) notions d'organisation pour la fabrication de jeu
(ce sont principalement des conseils de game jam, mais ils s'appliquent à votre cas aussi)
- vous serez en retard sur le planning
    - prévoyez un temps conséquent pour résoudre les bugs <details> - ![le planning de A Short Hike](/assets/801_aShortHikesPlanning.jpg)
        - pour trouver les bugs, **faites tester votre jeu** par des amis qui n'ont pas participé à sa création. On ne voit pas facilement ses propres bugs parce qu'on sait comment le jeu doit marcher alors on ne fait rien d'inattendu.
            - demandez aussi à vos testeurs si les tutos et le but du jeu sont clairs.
    - faites un jeu modulaire
        - globalement identifiez ce qui est essentiel et commencez par là, et faites le cool mais optionel en dernier.
            - beaucoup plus de choses sont optionnelles qu'on ne croit.
        - pour les jeux où les mécaniques de jeu sont importantes: isolez le centre, la partie la plus importante du jeu, et commencez par là. Une fois que ça marche bien, vous pouvez en ajouter une autre. Une fois qu'elle marche bien et se mèle bien à l'autre, ajoutez-en une troisième.
        - pour les jeux où il y a de la narration: faites le début. Faites la fin. Puis faites le milieu. Comme ça si vous n'avez pas eu le temps de faire le milieu on ne s'en rendra pas compte.
        - pour les jeux où les graphismes sont importants: faites des placeholders qui vous satisfont mais ne sont pas parfaits, et sachez que vous pourrez les retravailler après.
    - d'expérience: si vous vous dites: après le rendu je finirai / polirai / ajouterai ce truc cool, il y a 96,8% de chances que vous ne le fassiez pas.
- FAITES TESTER VOTRE JEU
    - c'est important
- la présence de son a une importance disproportionnée: si vous passez une heure à faire un son basique, ça aura à peu près autant d'impact que si vous passiez vingt heures à fignoler les assets graphiques.
- éventuellement: faites un niveau de test, juste pour vous, avec les différentes parties du jeu toutes ensembles, histoire si vous devez tester un boss de ne pas avoir à rejouer tout le jeu.
    - alternativement ou en plus: des cheat keys.
        - Par exemple, pour un rpg, appuyer sur 'A' change le booléen "a fini la mission 1" à vrai.
        - ou des raccourcis vers de niveaux.

## 3) accessibilité
En gras les propositions qui ne demandent quasiment aucun effort.  
Tous ces paramètres doivent être accessibles avant le début du jeu (y compris avant la cinématique de début s'il y en a une).  
- possibilité de changer tous les contrôles
    - y compris celui d'accès au menu
    - y compris les boutons de la souris
    - idéalement, un jeu devrait pouvoir n'être joué qu'avec un seul dispositif (s'il se joue au clavier, que le menu puisse être navigué aussi avec uniquement le clavier)
    - idéalement, on devrait pouvoir y jouer avec une seule main
- si vous avez des dialogues audio: sous-titres, et possibilité de les activer ou non
    - je sais que ce n'est pas hyper important vu qu'a priori vous n'aurez pas le temps d'enregistrer de l'audio pour tous vos dialogues, et encore moins de les sous-titrer
        - mais sachez que c'est important si vous faites un jeu qui a des dialogues enregistrés et qui n'est pas une démo de moins d'une demi-heure
- daltonisme
    - envisager de mettre des motifs, en plus des couleurs, pour différencier deux types, ou ajouter des formes pour l'identification.
    - **ou changer la luminosité de manière à ce que ce soit reconnaissable aussi en niveaux de gris**
        - un [site qui transforme une image en "vue daltonienne", pour tester si elle reste lisible](https://www.color-blindness.com/coblis-color-blindness-simulator/)
    - **choisir orange/bleu au lieu de rouge/vert comme couleurs opposées est plus souvent lisible par les daltoniens**
        - idéalement laisser le choix
    - éventuellement leur mettre un son différent
    - ou laisser les gens choisir les couleurs eux-même
- épilepsie
    - si vous avez des flashs de couleurs très contrastées (blanc, ou rouge vif) qui prennent une grosse partie de l'écran (plus d'un quart)
        - ou des mouvements aléatoires de motifs de couleurs très contrastées, qui prennent une grosse partie de l'écran
    - **alors mettre un écran d'avertissement au début du jeu**
        - et éventuellement la possibilité de les désactiver
        - et éviter le rouge très vif pour les flashs
        - et éviter d'avoir trois ou plus flashs par seconde
- **contrastes du texte**
    - augmenter la taille du texte aide aussi à la lisibilité
    - le fond derrière le texte peut avoir une légère texture, mais pas trop forte ou elle peut nuire à la lisibilité
    - cf <https://webaim.org/resources/contrastchecker/>
- dyslexie et problèmes de vue
    - ne pas utiliser de polices serif
    - ni l'italique
    - ne pas rogner sur l'interligne (un interligne de 1.5 est plus lisible)
    - **utiliser des majuscules et des minuscules, pas tout majuscule ou tout minuscule**
    - préférer du texte non justifié
    - utiliser des lignes courtes: pas plus de 70-80 caractères par ligne
    - helvetica, arial et verdana sont, selon [une étude](http://dyslexiahelp.umich.edu/sites/default/files/good_fonts_for_dyslexia_study.pdf), facilement lisibles
- possibilité de passer les cinématiques

## 99) Ressources externes (en anglais)
- accessibilité:
    - un site extrêmement bien fait qui regroupe plein de conseils pour l'accessibilité, avec des exemples et des explications: <http://gameaccessibilityguidelines.com/full-list/>
    - à propos de l'épilepsie: <https://videogameseizures.wordpress.com/2018/02/15/seizures-from-2017s-best-video-games/> et <https://www.w3.org/TR/UNDERSTANDING-WCAG20/seizure-does-not-violate.html>
    - à propos du daltonisme: <https://www.color-blindness.com/coblis-color-blindness-simulator/>
    - à propos du texte: <https://webaim.org/resources/contrastchecker/>
    - à propos de la dyslexie: <https://bigelowandholmes.typepad.com/bigelow-holmes/2014/11/typography-dyslexia.html> et <http://dyslexiahelp.umich.edu/sites/default/files/good_fonts_for_dyslexia_study.pdf>
- général:
    - une [explication amusante et claire des différents métiers du jeu vidéo](https://www.gamasutra.com/blogs/LizEngland/20140423/216092/quotThe_Door_Problemquot_of_Game_Design.php)
    - plein de [conférences libres d'accès sur le jeu vidéo](https://www.gdcvault.com/free/)
    - [article "prototyper un jeu en moins de 7 jours" sur le game design et l'organisation](https://www.gamasutra.com/view/feature/130848/how_to_prototype_a_game_in_under_7_.php)

## 100) Plus de ressources (en français)
- game design:
    - L'art du game design (The Art of Game Design), de Jesse Schell


# X. [Annexes](/cours/creation_gestion_ressources_0.html)
