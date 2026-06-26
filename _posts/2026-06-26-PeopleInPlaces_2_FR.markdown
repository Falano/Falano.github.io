---
layout: post_cera_FR
title: "Personnes et Lieux - 2 : textures procédurales"
tags: FR illu
categories: 3D FR illu
last_updated: 26 juin 2026
description: tutoriel sur la série Personnes et Lieux
permalink: /illu/2026-06-26_PeopleInPlaces_2_FR.html
topnav: topnav_Portfolio_illu_FR
---
\
[< partie précédente: impressions 2D <](/illu/2026-06-19_PeopleInPlaces_1_FR.html) | [> partie suivante: impressions 3D >](/illu/2026-06-19_PeopleInPlaces_3_FR.html)

# Personnes et Lieux: Montagnes

|![mountain peeps: 100](/assets/art/2D/mountainPeeps_0100_wm.jpg)|![mountain peeps: 160](/assets/art/2D/mountainPeeps_0160_wm.jpg)|
|![mountain peeps: 140](/assets/art/2D/mountainPeeps_0140_wm.jpg)|![mountain peeps: 200](/assets/art/2D/mountainPeeps_0200_wm.jpg)|

## Un aparté sur les textures procédurales
Je voulais faire plusieurs textures différentes, en utilisant le même principe de Noise superposé que pour la série Personnes et Lieux, mais que j'exporterais en tant que seule texture (sans personnage 3D derrière) pour pouvoir ensuite l'appliquer dans mon logiciel de dessin sur mes dessins 2D.
- La version précédente du projet n'était pas procédurale: l'exemple ci-dessous montre un scan d'une feuille sur laquelle a été renversé du thé:
![pictures with and without overlay scanned texture](/assets/art/2D/mountainPeeps_05_texs_nat.jpg)

- les nouvelles versions sont procédurales: certaines ont pour but de copier la texture scannée, d'autres ont été faites sans modèle ni direction précise.
- Les plus simples fonctionnent comme ceci: un mélange entre une petite et une grande texture, puis on y ajoute du bruit (White Noise ou un texture de n'importe quel type mais minuscule) si c'est trop lisse.\
\
Celle que j'ai utilisée pour la série des personnages de la montagne:
![mountain peeps: texture overlay node structure](/assets/art/2D/mountainPeeps_03h_texs.jpg)
Une autre, simple aussi:
![nodes setup in process pics](/assets/art/2D/mountainPeeps_06b_texs.jpg)
- on peut en faire de plus complexes, notamment en utilisant une texture comme facteur de notre node de mélange.
![nodes setup in compositor window](/assets/art/2D/mountainPeeps_06c_struct.jpg)
![nodes setup in process pics](/assets/art/2D/mountainPeeps_06c_texs.jpg)

[> partie suivante: impressions 3D >](/illu/2026-06-19_PeopleInPlaces_3_FR.html)
