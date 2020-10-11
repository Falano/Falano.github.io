---
layout: default
title:  "Cours Paris 8: Création et Gestion de ressources"
date:   2020-09-15 19:05:09 +0200
categories: classes, krita, 2D, fr
permalink: /cours/creation_gestion_ressources_0.html
---

# O. [Menu](/cours/creation_gestion_ressources.html)
# I. [Introduction](/cours/creation_gestion_ressources_1.html)
# II. [Krita](/cours/creation_gestion_ressources_2.html)
# III. [Décors](/cours/creation_gestion_ressources_3.html)
# IV. [Son](/cours/creation_gestion_ressources_4.html)
# V. [Animation](/cours/creation_gestion_ressources_5.html)
# X. Annexes
## 1) schéma de l'interface de Krita
![Interface Krita](/assets/999_interfaceKrita.png)
- **0**:
    - nouveau document,
    - ouvrir un document,
    - sauvegarder (*ctrl S*),
    - annuler (*ctrl Z*),
    - refaire (*ctrl shift Z*)
- **1**:
    - brosse, pinceau (*B*). Pour dessiner (déposer de la couleur sur le canevas).
- **2**: couleurs:
    - couleur principale (haut gauche) et couleur secondaire (bas droite).
    - cliquer sur les carrés de couleur pour la changer,
    - cliquer sur les carrés noir et blanc en bas à gauche pour retourner aux valeurs par défaut.
    - *X* pour intervertir couleur principale et secondaire.
    - *Ctrl clic* pour définir comme couleur principale une couleur présente dans l'image
- **3**:
    - opacité
    - taille du pinceau (*shift clic*)
- **4**:
    - Eraser / gomme (*E*): effacer (remplacer des pixels de couleur par des pixels transparents); attention: la gomme est un mode du pinceau et non un outil à part.
    - *Suppr*: effacer tout le calque actif (ou la sélection).
- **5**:
    - Brush Presets / liste des brosses,
    - barre de recherche en bas,
    - liste des catégories en haut
- **6**: Layers/ Calques:
    - nouveau calque,
    - dupliquer calque,
    - déplacer le calque dans la pile vers le bas,
    - déplacer le calque dans la pile vers le haut;
    - tout à droite, supprimer le calque
    - *double clic* ou *F2* sur le nom du calque pour le renommer
        - bien nommer ses calques!
    - icone "oeil" à gauche de chaque calque: visibilité du calque
    - à droite de chaque calque:
        - icone "ampoule": dés/activer l'ionion skin (aussi appelé "table lumineuse")
        - icone "verrou": rendre le calque non sélectionnable et non modifiable (temporairement)
        - icone "alpha": option "inherit alpha"; ne seront visibles que les pixels à l'emplacement desquels il y a un pixel opaque sur un calque plus bas (en tenant compte des groupes de calques)
        - icone "quadrillage/transparence": option "lock alpha": quand on dessine sur ce calque, on ne change que la couleur des pixels, ils gardent leur transparence (du coup sur un pixel transparent on ne voit pas de changement)
    - *ctrl G*: faire un groupe de calques avec tous les calques sélectionnés
        - pratique pour l'organisation
    - tout en haut (là où il y a écrit "Normal" sur le screenshot), changer le mode du calque actif
    - juste en dessous, changer l'opacité du calque
- **7**:
    - Advanced Color Selector / sélecteur de couleurs: change la couleur de premier plan;
    - a un historique de couleurs sur la droite (cliquer sur une des couleurs pour la rendre couleur de premier plan)
- **8**:
    - Tool Options / Options des Outils: toujours vérifier s'il ne contient pas une option qui fait exactement ce dont on a besoin avec l'outil actuel.
- **9**: Overview:
    - permet de zoomer et se déplacer dans l'image sans utiliser les raccourcis claviers; qui sont:
    - *molette* ou *ctrl clic molette*: zoom;
    - *espace clic* ou *clic molette*: se déplacer;
    - *shift clic molette* ou *shift espace clic*: rotation;
    - *pav num 5*: remettre la rotation à 0° (droite);
    - *pav num 1*: échelle 100%;
    - *pav num 2*: adapter à la hauteur,
    - *pav num 3*: adapter à la largeur;
    - *Tab*: full paint mode
    - il y a aussi un outil zoom et un outil déplacement dans la sous-fenêtre des outils (ce sont les deux derniers de la liste)
- **10**: options d'animation:
    - Onion Skins / peau d'oignon: permet de voir en transparence les images précédentes et suivantes de l'animation (activable/désactivable par calque dans la timeline, ou pour tous les calques en cliquant sur le 0 dans le docker Peau d'Oignon);
    - Animation:
        - Lancer/Pauser l'animation,
        - Images de début et de fin (Start et End),
        - nombre d'images par seconde (Frame Rate) (24 pour les mouvements rapides (le nombre d'images de la télé TODO: ou du cinéma? en Europe), 12 c'est bien, 6 c'est possible mais limite);
        - Timeline / Timing: là où se passe le gros de l'animation, où on passe d'une image à l'autre, et peut déplacer des images

## 2) notions de game design
- si jeu de plateforme/énigmes avec plusieurs niveaux: introduire une seule mécanique de jeu à la fois (cf III.x)
- lisibilité (cf II.2)
- vitesse de réaction du jeu: éviter les animations longues en début d'action (cf V.1)
- de l'importance du son (cf IV.1)
- de l'importance des retours visuels (feedback) (cf V.1)
- essayer d'avoir une unité graphique
    - et une unité entre le graphique, l'audio, l'histoire et le gameplay
    - ou au contraire qu'ils soient opposés, pour un effet de malaise bizarre
        - cf Happy Tree Friends, [Limbo](/assets/995_limbo.jpg) par Playdead: [https://playdead.com/games/limbo/](https://playdead.com/games/limbo/)

## 3a) Licences
- /!\ Toujours vérifier la licence des assets qu'on utilise.
    - [licences Creative Commons](https://creativecommons.fr/licences/#toc-les-licences-) (en 3ème année 2nd semestre vous avez un cours de "droit, éthique, informatique")
        - **CC-0**: on cède tous les droits cédables: permet de faire à peu près tout (sauf prétendre qu'on l'a fait soi-même: c'est le droit moral, qui est inaliénable en loi française; et sauf dire que l'auteur soutient l'utilisation qu'on en fait)
        - **CC-BY**: il faut [citer le nom de l'auteur, le titre de l'oeuvre, sa licence originale, et des liens vers chaque (par exemple dans l'écran de crédits du jeu vidéo, et un fichier texte avec les crédits et des hyperlinks)](https://creativecommons.org/use-remix/attribution/)
        - **CC-BY-SA-NC**: il faut citer l'auteur, l'oeuvre, la licence (BY: by), l'oeuvre dérivée doit avoir la même licence (SA: share alike), et on ne peut pas l'utiliser commercialement (NC: non commercial)
        - **CC-BY-ND**: a priori, ne pas l'utiliser pour un jeu: il faut citer l'auteur, l'oeuvre, la licence (BY: by), et on ne peut pas en diffuser d'adaptation (ND: non derivative; l'utilisation de sprites ou le montage d'audio pour un jeu compte très probablement comme "derivative")
        - si vous n'êtes pas sûr de la licence ou de si vous pouvez l'utiliser, et que vous pouvez contacter l'auteur, faites-le, très souvent il vous donnera la permission d'utiliser ses assets

## 4) game jams
- une game jam c'est, en gros, faire un jeu en (souvent) 48h, seul ou en groupe, avec d'autres gens qui font la même chose en même temps (proche des jams d'improvisation musicale et des hackatons)
    - ludum dare: deux fois par an (avril et octobre), probablement la jam la plus connue: ldjam.com
    - global game jam: une fois par an (en janvier), probablement la jam physique la plus connue: ggj.com
	- un agenda des jams en cours et à venir, sur un site où on peut publier ses jeux: https://itch.io/jams

## 5) jeux cool
J'ai noté en italique les jeux de jam, donc faits dans un temps très limité et nécessairement plus simples et courts que les autres.  
Les catégories sont assez floues, la plupart des jeux entrent dans plusieurs à la fois.  
- en pixel art
	- [fez](/assets/110_fez.png) (puzzle)
	- *bonsai* (un jeu de création de bonsais) : [https://ldjam.com/events/ludum-dare/46/bonsai](https://ldjam.com/events/ludum-dare/46/bonsai)
- style graphique simple mais qui marche
	- thomas was alone (platformer)
		- graphisme simple mais:
		- textures et lumières
		- voix des personnages
	- [*you must gather your party before venturing forth*](/assets/998_ymgypbvf.png)  (puzzle) : [https://ldjam.com/events/ludum-dare/46/ymgypbvf-you-must-gather-your-party-before-venturing-forth](https://ldjam.com/events/ludum-dare/46/ymgypbvf-you-must-gather-your-party-before-venturing-forth)
		- très stylisé
		- mais les informations importantes sont facilement lisibles (la race des persos, qui influence le gameplay)
	- [selfless heroes](/assets/003_selflessHeroes.png)
		- très stylisé
		- mais les informations importantes sont facilement lisibles
			- les persos sont des chevaliers
			- chacun est un personnage différent
			- la différence entre chaque type de tile est claire
		- et pour éviter la monotonie visuelle, il y a plusieurs types de chaque tile
	- [mini-metro](/assets/997_minimetro.jpg), par Dino Polo Club: [https://dinopoloclub.com/games/mini-metro/](https://dinopoloclub.com/games/mini-metro/)
	    - utilise des symboles plutôt que des illustrations
	- [*gophers*](/assets/105_gophers.png)
		- les palettes de couleurs limitées, utilisées à bon escient, marchent souvent bien
		- un travail sur l'atmosphère (accord graphisme-son-histoire-gameplay)
	- [night in the woods](/assets/996_nightInTheWoods.png) par Infinite Fall: [http://www.nightinthewoods.com/](http://www.nightinthewoods.com/)
	    - très chouette style graphique
	        - soutenu/contrasté par la musique et l'histoire
	    - mais composé quasi exclusivement de formes simples
	    - simplification et stylisation des textures

## 6) Vocabulaire
- **tile**: une image (en général un fragment de décor) utilisée pour composer une image plus grande (un niveau entier) avec d'autres tiles, espacées régulièrement; elle sera typiquement réutilisée de nombreuses fois dans le même niveau.
    - un ensemble de tiles est un **tileset**
    - un niveau composé de tiles est une **tilemap**; on utilise parfois "tilemap" pour dire "ensemble de tiles"
- **asset**: un élément composant le jeu. Dans sa définition la plus étroite, se réfère uniquement aux assets graphiques (les tiles, les personnages, etc.), mais souvent aussi aux assets sonores, et parfois inclue des scripts.
- **palette**: un ensemble de couleurs qu'on utilise dans l'image (et on n'en utilise aucune autre). Les palettes de pixel art sont souvent assez réduites.
- **prop**: littéralement, "accessoire"; un objet composant de décor, souvent avec lequel le personnage peut interagir
- termes spécifiques au pixel art, en anglais:
    - **jaggies**: des sortes d'accrocs créés par une courbe irrégulière ou une ligne à la largeur illogiquement irrégulière
    - **hue shifting**: le fait de changer la teinte d'une couleur en fonction de sa clarté au lieu de la rendre uniquement plus claire ou plus sombre
    - **orphan pixel**: un pixel tout seul, non relié à d'autres de la même couleur.
