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
    - vu de haut (jrpgs) (cf: [chrono trigger](/assets/501_chronoTrigger.png), stardew valley)
    - vu de côté (platformers) (cf SuperMeatBoy, braid, super metroid)
    - vue isométrique (souvent stratégie ou rpg européen); supporté par Godot (cf transistor)
    - vue de haut non-carrée (type jeu de plateau) (cf [Battle for Wesnoth](/assets/504_wesnoth.png))

**références**  
Chrono Trigger, par Square
Stardew Valley, par Concerned Ape: https://www.stardewvalley.net/
Super Meat Boy, par Team Meat: http://www.supermeatboy.com/
Braid, par Jonathan Blow: https://www.gog.com/game/braid
Super Metroid, par Nintendo
Transistor, par Supergiant Games: https://www.supergiantgames.com/games/transistor/
Battle for Wesnoth, par Tout Un Tas De Gens C'est Open Source: https://www.wesnoth.org/

## 2) Krita: 4
- grilles
    - grilles isométriques
    - re-teste magnétisme quand même
- wrap around mode
- remplir une zone d'une tile répétée: select tile > pattern icon (entre les couleurs et le bouton d'annulation) > use as pattern > sélectionner la zone > fill tool > use pattern

--  
**EXERCICE 5**  
faire une tilemap, et la monter sur Krita ou Godot  
-> pour apprendre à faire des tilemaps  
--  

## 3) Décor plein
- rappel: lisibilité (perso/fond, plateformes, fond/fond)
- perspective atmosphérique (cf Maxim Massalitin https://commons.wikimedia.org/wiki/File:D%C3%A9sert_des_Agriates_(5739231175).jpg)
    - tout prend la teinte de l'air (en général: bleuté)
    - moins de contrastes
        - noirs moins noirs
        - couleurs moins saturées
- parallaxe (cf https://commons.wikimedia.org/wiki/File:Parallax_scroll.gif TODO: find a better one)
- lumière
	- comme unificateur (une seule source de lumière)
	- comme évidenciateur (les endroits importants et interactifs sont dans la lumière)
- règle des tiers (ne pas mettre de truc important tout contre le bord; il risque de ne pas être visible ou remarquable)

## 4) Krita: 5
- outils perspective
    - règle parallèle / parallel ruler
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

# IV. [Son](/cours/creation_gestion_ressources_4.html)
# V. [Animation](/cours/creation_gestion_ressources_5.html)
# X. [Annexes](/cours/creation_gestion_ressources_0.html)

