---
layout: default
title:  "Cours Paris 8: Création et Gestion de ressources"
date:   2020-09-15 19:05:09 +0200
categories: classes, krita, 2D, fr
permalink: /cours/creation_gestion_ressources_6.html
---  

# O. [Menu](/cours/creation_gestion_ressources.html)
# I. [Introduction](/cours/creation_gestion_ressources_1.html)
# II. [Krita](/cours/creation_gestion_ressources_2.html)
# III. [Décors](/cours/creation_gestion_ressources_3.html)
# IV. [Son](/cours/creation_gestion_ressources_4.html)
# V. [Animation](/cours/creation_gestion_ressources_5.html)
# VI. [Finitions](/cours/creation_gestion_ressources_6.html)
## 1) UI
- on a (sur ordinateur) quatre états états de boutons:
    - désactivé
        - le bouton n'est pas disponible, il est impossible de cliquer dessus
    - au repos
        - le bouton est disponible mais personne n'est en train d'interagir avec
    - sélectionné
        - le bouton est sélectionné, soit avec la souris qui est au-dessus ("hover"), soit avec le clavier ou la manette; il est prêt à être actionné
        - en général, n'existe pas pour les jeux mobiles où on passe directement de repos à cliqué
    - cliqué
        - le bouton est en train d'être activé (à l'instant où on clique avec la souris, ou appuie sur la touche du clavier ou de la manette)
- UI cohérent avec l'univers graphique
    - figuratif
        - moyen-âge: bois et parchemin (cf Age of Empires)
        - antiquité grecque: pierre taillée, motifs géométriques
        - nature: terre, arbres et feuilles
        - moderne-ish: posters, cahiers, etc. (cf Moonlighter, Night in the Wood)
        - futur: néons, hologrammes, effet écran (glitches, lignes cathodiques), semi-transparence (cf Transistor, cf Starcraft II)<details> - ![Age of Empires](/assets/702_aoe2.jpg) <br> - ![moonlighter](/assets/703_moonlighter.jpg) <br> - ![Night in the woods](/assets/704_nitw.jpg) <br> - ![Transistor](/assets/705_transistor.jpg) <br> - ![Starcraft II](/assets/706_sc2.jpg)
    - abstrait (cf sims)
        - minimaliste (cf overland, mini metro, a short hike)
        - cartoon
        - motifs
        - style graphique non-figuratif précis (cf persona 5) <details> - ![les sims 4](/assets/707_sims.jpg) <br> - ![overland](/assets/708_overland.jpg) <br> - ![minimetro](/assets/997_minimetro.jpg) <br> - ![a short hike](/assets/708b_aShortHike.jpg) <br> - ![persona 5](/assets/709_persona5.jpg)
    - ou un mélange des deux (cf crusader kings 2)
        - motifs abstraits sur un fond qui évoque du parchemin (cf pyre) <details> - ![crusader kings 2](/assets/710_crusaderKings2.jpg) <br> - ![pyre](/assets/711_pyre.jpg)
- strategie (cf wesnoth) <details> ![wesnoth](/assets/508_wesnoth.jpg)
    - grille?
    - couleurs des équipes?
    - déplacements disponibles?
    - cône de visibilité (jeux furtifs) et radius du son?
- astuce pour créer du volume rapidement sur un élément de UI (cf minecraft) <details> ![minecraft](/assets/712_minecraft.jpg)
- prendre en compte la taille de l'écran (le texte sera-t-il lisible? les boutons seront-ils cliquables?)
    - les jeux mobiles ont des boutons plus grands
    - des boutons trop grands sur un jeu pc ça fait cheap
- comparaison ff7 vieux/remake (plus petits écrans) <details> ![ff7](/assets/713_ff7.jpg)
- utiliser l'anticipation et le squash and stretch dans la UI pour un effet cartoon
- cohérence visuelle
    - limiter le nombre de polices de caractère différentes
    - ne pas avoir non plus quinze type de boutons différents
- flot intuitif
    - que "commencer à jouer" soit le premier bouton (ou celui qui ressort le plus), et qu'il soit au premier plan du menu
    - que tous les "back" soient alignés et ne mènent pas au "quit"; supposer que le joueur va bouriner et cliquer quinze fois sur le bouton
    - que les menus et sous-menus soient logiques et aient des noms clairs
    - préférer une organisation en grille, pour pouvoir naviguer facilement avec les flèches clavier
    - hiérarchiser les informations
- le HUD ne devrait pas déconcentrer par rapport à ce qu'il se passe dans l'écran principal
    - sauf si c'est des infos urgentes, importantes, et qui arrivent rarement
- si fonds de texte semi-transparents, attention à ce qu'il y a derrière, que ça reste lisible
- diégétique / extradiégétique (cf metroid prime, spelunky, dead space) <details> - ![Metroid Prime](/assets/714_metroidPrime.jpg) <br> - ![Spelunky](/assets/715_spelunky.jpg) <br> - ![Dead Space](/assets/716_deadSpace.jpg)
- pas de UI (cf alto's adventure, journey) <details> - ![alto's adventure](/assets/718_altosAdventure.jpg) <br> - ![journey](/assets/717_journey.jpg)
- nine patch rect ([documentation officielle godot](https://docs.godotengine.org/en/3.0/classes/class_ninepatchrect.html), [tuto vidéo (en)](https://www.youtube.com/watch?v=OrTMWb1bN24))

## 2) "Juice"
- Jan (Vlambeer), conférence "the art of screenshake" (vidéo): <https://www.youtube.com/watch?v=AJdEqssNZ-U>
    - "the main way you interact with the world"
    - "give the player a reason not to hold the button"
    - flux d'informations <details> ![flux d'informations](/assets/791_jansTalk.jpg)
    - permanence, si pertinent; effets spéciaux; fumée d'une explosion, corps, objets cassés, etc.
    - des ralentis!
- vidéo "juice it or lose it": <https://www.youtube.com/watch?v=Fy0aCDmgnxg>
    - son.
    - particules!!!
- Night In The Woods sauter sur les poubelles
- est-ce marrant? En ajouter? Pas marrant? L'enlever.

## 97) exemples
- UI
    - dead space: no UI <https://www.youtube.com/watch?v=nqvYW0xsyCU>
    - a short hike: no UI-ish: <https://www.youtube.com/watch?v=p6UDqtlmJpk> (mostly because indie probs)
    - tutoriel de spelunky: UI intradiégétique: <https://www.youtube.com/watch?v=_2lHMMF4XIM>
    - danganronpa 3, cuphead


## 99) plus de ressources (principalement en anglais)
- un tutoriel sur la [UI](https://www.patreon.com/posts/ui-9-slice-14798512) sur le site de studiominiboss (les tutos en .gif)  
- vidéo ["juice it or lose it"](https://www.youtube.com/watch?v=Fy0aCDmgnxg)  
- un tutoriel écrit sur le ["juice"](https://gameanalytics.com/blog/squeezing-more-juice-out-of-your-game-design.html)  
- un article sur les différents états des boutons et la navigation <https://material.io/design/interaction/states.html#usage>
- playlist [Good Design/Bad Design](https://www.youtube.com/watch?v=bE_ZuNp1CTI&list=PL8K0_g1wdQeoxta9RyvTK-DnhU4jI2QJN) d'analyse de jeux

## 100) ressources en français
- un [tutoriel écrit sur le feedback](https://www.forum-dessine.fr/tutoriels/les-signes-et-feedbacks)

[](6. fin L1C12)

# VII. [Exports](/cours/creation_gestion_ressources_7.html)
# VIII. [Game Design](/cours/creation_gestion_ressources_8.html)
# X. [Annexes](/cours/creation_gestion_ressources_0.html)
