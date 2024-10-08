---
layout: page
title:  "Cours Paris 8: Création et Gestion de ressources"
last_updated: July 27, 2023
permalink: /cours/creation_gestion_ressources/decors.html
topnav: topnav_P8_Ressources
---
# III. Décors
## 1) Tiles
- doivent s'emboîter sans que ça se voie
	- pour les décors naturels: avoir plusieurs variantes excentrées
- perspective au choix
    - vu de haut (jrpgs) (cf: chrono trigger, stardew valley, ff6)<details> - chrono trigger ![chrono trigger](/assets/cours/501_chronoTrigger.png) <br> - stardew valley ![stardew valley](/assets/cours/502_stardewValley.jpg) <br> - final fantasy 6 ![ff6](/assets/cours/103_ff6.jpg)
    - vu de côté (platformers) (cf SuperMeatBoy, braid, super metroid, celeste) <details> - braid ![braid](/assets/cours/503_braid.jpg) <br> - super meat boy ![super meat boy](/assets/cours/504_superMeatBoy.jpg) <br> - super metroid ![super metroid](/assets/cours/505_superMetroid.png) <br> - celeste ![celeste](/assets/cours/109_celeste.png)
    - vue isométrique (souvent stratégie ou rpg européen); supporté par Godot (cf transistor, freecol) <details> - transistor ![transistor](/assets/cours/506_transistor.jpg) <br> - freecol ![freecol](/assets/cours/507_freecol.jpg)
    - vue de haut non-carrée (type jeu de plateau); supporté par Godot (cf Battle for Wesnoth) <details> - battle for wesnoth ![wesnoth](/assets/cours/508_wesnoth.jpg)
- exemples de tileset vu du haut avec explications <details> - tileset minimal; en bas le tilest en haut un exemple d'utilisation <br> ![topdown tileset minimal](/assets/cours/mine/tiles-example-02_minimal_blank_4px.png) <br> - tileset minimal - avec légende <br> ![topdown tile minimal legend](/assets/cours/mine/tiles-example-02_minimal_legende_4px.png) <br> - tileset médian - base (pour être sûr que ça marche bien avant de mettre les détails); avec des variations pour plusieurs tiles et des diagonales <br> ![topdown tileset medium basis](/assets/cours/mine/tiles-example-02_median_A_basis_4px.png) <br> - tileset médian - détails <br> ![topdown tileset medium details](/assets/cours/mine/tiles-example-02_median_B_details_4px.png) <br> - tileset médian - légende <br> ![topdown tileset medium legend](/assets/cours/mine/tiles-example-02_median_C_legend_4px.png)

**références**  
Chrono Trigger, par Square  
Stardew Valley, par Concerned Ape: <https://www.stardewvalley.net/>  
Final Fantasy 6, par Square Enix  
Super Meat Boy, par Team Meat: <http://www.supermeatboy.com/>  
Braid, par Jonathan Blow: <https://www.gog.com/game/braid>  
Super Metroid, par Nintendo  
Celeste, par Matt Makes Games: <http://www.celestegame.com/>  
Transistor, par Supergiant Games: <https://www.supergiantgames.com/games/transistor/>  
Freecol, par Tout Un Tas De Gens C'est Open Source: <http://www.freecol.org>  
Battle for Wesnoth, par Tout Un Tas De Gens Aussi C'est Open Source: <https://www.wesnoth.org/>

## 2a) Libresprite: 4
- grilles (View > Grid > Grid Settings; éventuellement, Snap to Grid)
- mode infini (View > Tiled Mode)
- remplir une zone d'une tile (pour les tilemaps ou les motifs réguliers) répétée: dessiner sa tile, la sélectionner, Edit > New Brush (*Ctrl B*); marche avec le pinceau, le pot de peinture/remplissage/goutte, les formes géométriques, etc. 
    - pour les motifs irréguliers (feuilles, rochers, etc.), utiliser ça avec l'outil "Spray" (*Shift B*, sur la même ligne que l'outil pinceau), avec des valeurs basses de "spray width" et "spray speed": (tuto détaillé)[https://www.artstation.com/artwork/Nx2vz5]
- rappel: outils forme (*shift* pour conserver la proportion 1/1)
- (variations de tiles)[https://www.patreon.com/posts/making-tiles-12881715]
- placer les tiles côte-à-côte et de manière logique et continue

## 2b) Godot tilemaps
- importer la tilemap (en .png) dans godot
- créer un objet tilemap, lui ajouter un nouveau tileset
- new autotile
- mettre le bitmask, l'icône, les priorités et les collisions.
- attention à ne pas avoir de tiles qui se superposent, c'est compliqué à gérer
- Si on voit les contours des tiles, activer pixel snap (Set Project > Project Settings > Rendering > Quality > 2d > Use Pixel Snap (activé), ou bien utiliser la recherche pour trouver "Pixel Snap").


--  
**EXERCICE 5**  
- faire une tilemap  
- dessiner un polygone fermé d'au moins 7 sommets, dont chaque sommet est dans une case de quadrillage différente
- dans le logiciel de dessin, assembler une forme utilisant sa tilemap qui suit la forme du polygone.

--  

**EXERCICE 6**  
- importer sa tilemap dans Godot, la tester
- vérifier le type de formes qu'on peut faire avec et si les transitions marchent bien
- s'il manque des tiles, en rajouter
- si des tiles ne communiquent pas bien, les modifier
- continuer jusqu'à ce que la tilemap marche

--  

## 3a) lisibilité
- personnage/fond: que le perso se détache sur le fond
    - pensez à mettre votre personnage dans votre fond quand vous travaillez
        - pour tester sa taille
        - et sa lisibilité
- plateformes et éléments interactifs: qu'ils soient clairement identifiables comme tels
    - supertux (bonus)
        - plateformes invisibles
        - murs creux
        - difficulté artificielle créée par de faux signaux: le joueur n'est pas l'ennemi du game designer.
    - dead cells / celeste
        - plateformes qui se détachent bien
        - arrière-plan dé-contrasté <details> - dead cells ![Dead Cells](/assets/cours/111_Dead-Cells.jpg) <br> - Celeste ![Celeste](/assets/cours/109_celeste.png)
- personnages entre eux: qu'ils soient facilement différenciables
- personnages/ennemis: qu'ils soient différenciables en un coup d'oeil
- fond/fond: premier plan en illustration: ajoute de la profondeur; en level design: gaffe à la parallaxe qui peut cacher des éléments importants au gameplay) <details> - Horizon Zero Dawn ![horizon zero dawn](/assets/cours/300_horizonZeroDawn.jpg) <br> - fantasia ![fantasia](/assets/cours/301_fantasiaInfogrames_gd.png)

**références**  
Horizon Zero Dawn, par Guerilla Games: <https://www.guerrilla-games.com/play/horizon>  
Fantasia, par Infogrames: <https://fr.wikipedia.org/wiki/Fantasia_(jeu_vid%C3%A9o)>  
Supertux, par Tout Un Tas De Gens C'est Open Source: <https://www.supertux.org/>

## 3b) Décor plein
- rappel: lisibilité (perso/fond, plateformes, fond/fond)
- perspective atmosphérique: avec la distance...
    - tout prend la teinte de l'air (en général: bleuté)
    - moins de contrastes
        - noirs moins noirs
        - couleurs moins saturées <details> <br>![perspective atmospherique](/assets/cours/601_persAtmo.jpg)
- parallaxe
    - plus c'est proche, plus ça va vite <details> <br>![parallaxe](/assets/cours/602_Parallax_scroll.gif)
- lumière
	- comme unificateur (une seule source de lumière)
	- comme évidenciateur (les endroits importants et interactifs sont dans la lumière)
- règle des tiers (ne pas mettre de truc important tout contre le bord; il risque de ne pas être visible ou remarquable)

**références**  
Maxim Massalitin, [Désert des Agriates](https://commons.wikimedia.org/wiki/File:D%C3%A9sert_des_Agriates_(5739231175).jpg) sur wikimedia commons  
NuclearDuckie, [Parallax Scroll](https://commons.wikimedia.org/wiki/File:Parallax_scroll.gif) sur wikimedia commons  

## 3c) Parallaxe dans Godot
- nodes:
- ParallaxBackground
-- ParallaxLayer
--- Sprite2D (mettre comme texture son image de ce calque de la parallaxe)
-- ParallaxLayer
--- Sprite2D (un autre calque de la parallaxe)
-- ParallaxLayer
--- Sprite2D

- avoir des images au moins deux fois plus grandes (sur chaque dimension qui subit de la parallaxe) que le nombre de pixels affiché sur l'écran (taille de la fenetre / zoom de la caméra (sur la node camera) * scale du projet (dans les projets settings) )
- ParallaxLayer > Mirroring: mettre les dimensions de la texture de la Sprite2D (pour chaque dimension qui subit de la parallaxe)
- pour désactiver la parallaxe sur l'axe horizontal, mettre à 0 le Mirroring en Y.

## 99) plus de ressources (principalement en anglais)
- plein de tutoriels format gif, courts et efficaces: [https://saint11.org/blog/pixel-art-tutorials/](https://saint11.org/blog/pixel-art-tutorials/)
    - [arbres](https://www.patreon.com/posts/vegetation-part-7416630)
    - [variations de tiles](https://www.patreon.com/posts/making-tiles-12881715)
    - [perspective](https://www.patreon.com/posts/parallax-and-7863658)
- tutoriels en images, courts et efficaces:
    - [utiliser une forme simple pour construire des formes complexes facilement](https://www.artstation.com/artwork/68Rr8V)
    - [des variations de texture sur la même base pour ajouter de la diversité](https://www.artstation.com/artwork/PoErV4)
- un [tutoriel vidéo sur le système de tiles de godot](https://www.youtube.com/watch?v=F6VerW98gEc)
- un [tutoriel écrit sur les tiles dans godot](https://www.davidepesce.com/2019/10/18/godot-tutorial-7-using-tile-maps-to-create-game-map/)
- les [un tuto visuel sur les brosses non-régulières dans Libresprite](https://www.artstation.com/artwork/Nx2vz5)
