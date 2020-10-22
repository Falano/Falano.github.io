---
layout: default
title:  "Cours Paris 8: Création et Gestion de ressources"
date:   2020-09-15 19:05:09 +0200
categories: classes, krita, 2D, fr
permalink: /cours/creation_gestion_ressources_3.html
---

# O. [Menu](/cours/creation_gestion_ressources.html)
# I. [Introduction](/cours/creation_gestion_ressources_1.html)
# II. [Krita](/cours/creation_gestion_ressources_2.html)

# III. Décors
## 1) Tiles
- doivent s'emboîter sans que ça se voie
	- pour les décors naturels: avoir plusieurs variantes excentrées
- perspective au choix
    - vu de haut (jrpgs) (cf: chrono trigger, stardew valley, ff6)<details> - chrono trigger ![chrono trigger](/assets/501_chronoTrigger.png) <br> - stardew valley ![stardew valley](/assets/502_stardewValley.jpg) <br> - final fantasy 6 ![ff6](/assets/103_ff6.jpg)
    - vu de côté (platformers) (cf SuperMeatBoy, braid, super metroid, celeste) <details> - braid ![braid](/assets/503_braid.jpg) <br> - super meat boy ![super meat boy](/assets/504_superMeatBoy.jpg) <br> - super metroid ![super metroid](/assets/505_superMetroid.png) <br> - celeste ![celeste](/assets/109_celeste.png)
    - vue isométrique (souvent stratégie ou rpg européen); supporté par Godot (cf transistor, freecol) <details> - transistor ![transistor](/assets/506_transistor.jpg) <br> - freecol ![freecol](/assets/507_freecol.jpg)
    - vue de haut non-carrée (type jeu de plateau); supporté par Godot (cf Battle for Wesnoth) <details> - battle for wesnoth ![wesnoth](/assets/508_wesnoth.jpg)
- exemples de tileset vu du haut avec explications <details> - tileset minimal; en bas le tilest en haut un exemple d'utilisation <br> ![topdown tileset minimal](/assets/mine/tiles-example-02_minimal_blank_4px.png) <br> - tileset minimal - avec légende <br> ![topdown tile minimal legend](/assets/mine/tiles-example-02_minimal_legende_4px.png) <br> - tileset médian - base (pour être sûr que ça marche bien avant de mettre les détails); avec des variations pour plusieurs tiles et des diagonales <br> ![topdown tileset medium basis](/assets/mine/tiles-example-02_median_A_basis_4px.png) <br> - tileset médian - détails <br> ![topdown tileset medium details](/assets/mine/tiles-example-02_median_B_details_4px.png) <br> - tileset médian - légende <br> ![topdown tileset medium legend](/assets/mine/tiles-example-02_median_C_legend_4px.png)

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

## 2) Krita: 4
- grilles (Dockers > Grid and Guides)
    - grilles isométriques (dans le docker Grid and Guides > Type: Isometric; Left angle: 28°; Right angle: 27°) (cf [un fichier .kra avec une grille isométrique](/assets/mine/isoGrid.kra)) <details>- grille isométrique ![grille isometrique](/assets/mine/isoGrid.png)
- wrap around mode (View > Wrap Around Mode, ou: Affichage > Mode Enveloppant)
- remplir une zone d'une tile répétée: select tile > pattern icon (entre les couleurs et le bouton d'annulation) > use as pattern > sélectionner la zone > fill tool > use pattern

[](2. fin lundi aprèm 1?)
[](2. fin merc 1?)
[](2-3. fin lundi matin 12)
[](2-3. fin lundi aprèm 12)

{% comment %}
## 3) Tiled
godot-tiled:  
importer: https://github.com/vnen/godot-tiled-importer -> buggy?  
exporter: https://github.com/MikeMnD/tiled-to-godot-export -> unfinished?  
{% endcomment %}
--  
**EXERCICE 5**  
faire une tilemap, et la monter sur Krita ou Godot  
-> pour apprendre à faire des tilemaps  
--  

## 3) Décor plein
- rappel: lisibilité (perso/fond, plateformes, fond/fond)
- perspective atmosphérique: avec la distance...
    - tout prend la teinte de l'air (en général: bleuté)
    - moins de contrastes
        - noirs moins noirs
        - couleurs moins saturées <details> <br>![perspective atmospherique](/assets/601_persAtmo.jpg)
- parallaxe
    - plus c'est proche, plus ça va vite <details> <br>![parallaxe](/assets/602_Parallax_scroll.gif)
- lumière
	- comme unificateur (une seule source de lumière)
	- comme évidenciateur (les endroits importants et interactifs sont dans la lumière)
- règle des tiers (ne pas mettre de truc important tout contre le bord; il risque de ne pas être visible ou remarquable)


**références**  
Maxim Massalitin, [Désert des Agriates](https://commons.wikimedia.org/wiki/File:D%C3%A9sert_des_Agriates_(5739231175).jpg) sur wikimedia commons  
NuclearDuckie, [Parallax Scroll](https://commons.wikimedia.org/wiki/File:Parallax_scroll.gif) sur wikimedia commons  

## 4) Krita: 5
- outils perspective (Assistant Tool (icône en équerre))
    - /!\ ne pas oublier de cocher "snap to assistant" sur la brosse une fois les assistants mis en place
    - règle parallèle / parallel ruler (dans les Tool Options de l'outil Assistant)
    - concentric ellipse
    - vanishing point et perspective (pas utile pour des tilemaps)
- outils forme (*shift* pour conserver la proportion 1/1)
- gomme lasso (utiliser l'outil "t)_Shapes_Fill" en mode "erase" est pratique pour effacer de grandes zones irrégulières peu précises)

--  
**EXERCICE 6**  
importer sa tilemap de Tiled à Godot  
--  

## 99) plus de ressources (principalement en anglais)
- plein de tutoriels format gif, courts et efficaces: [https://blog.studiominiboss.com/pixelart](https://blog.studiominiboss.com/pixelart)
    - [arbres](https://www.patreon.com/posts/vegetation-part-7416630)
    - [variations de tiles](https://www.patreon.com/posts/making-tiles-12881715)
    - [perspective](https://www.patreon.com/posts/parallax-and-7863658)
- un [tutoriel vidéo sur le système de tiles de godot](https://www.youtube.com/watch?v=F6VerW98gEc)
- un [tutoriel écrit sur les tiles dans godot](https://www.davidepesce.com/2019/10/18/godot-tutorial-7-using-tile-maps-to-create-game-map/)

## 100) ressources en français
- un [enregistrement du cours sur les tiles](https://youtu.be/RQ73GgjVDRU), incluant:
    - 00:00 récapitulatif des outils de krita
    - 07:13: mise à jour du site
    - 07:50: courbes
    - 08:45: fenêtre secondaire de visualisation
    - 09:55: couleurs
    - 13:34: hue shifting
    - 17:39: personnage
    - 18:14: organisation projet
    - 19:40: tiles
- un [mini-tuto pour tester ses tiles rapidement sur krita](https://youtu.be/fe0xhI8vmAQ)
    - en gros:
    - *ctrl R* sélectionner,
    - *ctrl C* copier,
    - *ctrl V* coller sur un autre calque,
    - *T* déplacer,
    - *ctrl E* fusionner le calque actif avec celui du dessous
    - répéter
- une [démo de dessin de tiles de platformer]( https://youtu.be/bdgpp8OPXDo)

[](2. fin L1C12)

# IV. [Son](/cours/creation_gestion_ressources_4.html)
# V. [Animation](/cours/creation_gestion_ressources_5.html)
# X. [Annexes](/cours/creation_gestion_ressources_0.html)

