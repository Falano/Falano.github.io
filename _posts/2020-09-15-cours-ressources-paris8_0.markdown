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
[Image](/assets/999_interfaceKrita.png) (à ouvrir dans une nouvelle fenêtre pour la voir à côté de la légende ci-dessous)
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
    - !!!!!!! more layers stuff!!!!!!!!!!!!
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
à venir

## 3) Ressources externes
à venir

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
	- mini-metro
	- [*gophers*](/assets/105_gophers.png)
		- les palettes de couleurs limitées, utilisées à bon escient, marchent souvent bien
		- un travail sur l'atmosphère (accord graphisme-son-histoire-gameplay)
