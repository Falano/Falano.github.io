---
layout: page
title:  "Cours Paris 8: Introduction aux Moteurs de Jeu"
last_updated: September 29, 2023
permalink: /cours/introduction_moteurs_jeu/introduction.html
redirect_from: /cours/introduction_moteurs_jeu
topnav: topnav_P8_MoteursJeu
#sidebar: P8_MoteursJeu
---

# 1. Introduction
## 1) Présentation des moteurs de jeu

C'est quoi un jeu vidéo?
nommez différents types de jeux.
Quels sont les différentes parties d'un jeu vidéo?
C'est quoi un moteur de jeu?

différents moteurs de jeu:
- unity: gratuit pour les petits studios, donc très populaire dans la sphère indé/amateur; généraliste, mais créé au départ principalement comme moteur de fps (fait maintenant aussi de la 2D)
- unreal: autre moteur très populaire et gratuit pour les petits studios. Spécialisé dans la 3D (lié à epic games). Généralement considéré comme plus compliqué que unity, donc moins utilisé dans la sphère indé/amateur (aussi il était payant jusqu'en 2015)
- gdevelop: moteur de jeu libre, plutôt axé débutants, généraliste (2D et 3D)
- gamemaker: spécialisé 2D (undertale)
- rpgmaker: spécialisé dans les jrpg 2D
- renpy: spécialisé dans les visual novel
- twine, ink, yarn: spécialisés dans la fiction interactive, prévus pour un export basique ou une intégration dans un autre moteur de jeu.

Exercice 1: 
- choisissez un jeu que vous aimez bien (si vous n'avez pas d'idée, vous pouvez demander à la personne assise à côté de vous, mais c'est mieux si vous connaissez le jeu)
- trouvez une vidéo de gameplay du jeu
- décomposez les instructions / interactions qui composent le jeu (condition > action; ou: quand/si il se passe ça, alors faire ça)
()[correction: donnez-moi des noms de types de jeu; qui a un platformer? Qui a un fps? Qui a un rpg 3rd person? Qui a une visual novel? Qui a un rts? Qui a autre chose? (parler du feedback visuel/audio aussi]

## 2) présentation du cours
- on utilisera Godot
- on fera un platformer
- si vous avez envie de voir quelque chose de spécifique autre, demandez.

## 3) exemples d'éléments de différents jeux
- jeu narratif, rpg: système de dialogue
- rpg: inventaire
- platformer, FPS/TPS: physique
- rts: IA complexe
- tower defense: chemins
- rogue-like: génération aléatoire de niveaux
- jeu de construction: gestion des emplacements sur une grille

## 4) aperçu de l'interface de Godot
- lancer Godot 4 (un projet complet)
- onglet Scène
  - sous-scènes
  - hiérarchie noeux (nodes), script, sous-nodes
- onglet Système de fichiers (ajouter un dossier et voir la correspondance avec le système de fichiers de l'ordinateur)
- inspecteur (CanvasItem > Visibility > modulate; Node > Process > Mode; CollisionObject2D > Collision > Layer & Mask; variables exportées)
- Signaux et Groupes
- passer d'une scène à l'autre (onglets 2D/3D/Script/AssetLib, onglets horizontaux, onglets scripts verticaux, onglet Scène)
- types de fichiers:
 - .gd: script godot
 - .tscn: scène
 - .tres: ressource
