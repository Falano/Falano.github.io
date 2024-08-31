---
layout: page
title:  "Cours Paris 8: Introduction aux Moteurs de Jeu"
last_updated: September 29, 2023
permalink: /cours/introduction_moteurs_jeu/platformer_1.html
topnav: topnav_P8_MoteursJeu
---

# 2. Bases pour un platformer
## 1) éléments d'un platformer
exemple de platformers: 
- Super Mario Bros (1985): https://youtu.be/rLl9XBg7wSs?t=12
- céleste (2018): https://youtu.be/HqL2XkPnZes?t=169

**Exercice 2:** quels sont les éléments qu'il faudra implémenter dans un platformer?

- image
- mouvement du personnage et commandes du joueur
- animation
- collision avec le décor (montrer les colliders)
- interaction avec les ennemis

## 2) créer un personnage joueur simple
- image
- mouvement
- collision décor

## 3) ennemis
- image (CanvasItem > Visibility > modulate)
- **Exercice 3:** mouvement (changer l'input)
- collision décor
- ne pas tomber (on_detecteur_sol_body_exited():direction=-direction)
- faire demi-tour contre les obstacles (if get_last_slide_collision().get_angle() != 0) (0 est quand le perso détecte une collision avec un sol horizontal en dessous de lui, un peu plus que 3 (pi, plus précisément) est quand il détecte une collision avec quelque chose qui vient du haut
- collision joueur (print "a touché le joueur!!" ou quelque chose comme ça; puis ajouter la gestion des points de vie du joueur et sa mort)
- gestion de la vie/mort de l'ennemi aussi (quand on lui saute dessus?)
- et si plusieurs ennemis?
- faire une variante de l'ennemi (autres couleur, vitesse et dégâts)

## 4) décor: tilemaps
- importer un tileset
- régler la taille des tiles
- créer un terrain
- régler la physique
- probabilité
- calques
- objets
- anim
- enregistrer un tileset
- arrière-plan
- pour désactiver une TileMap, désactiver ses Physics Layers (et désactiver la visibilité)

## 5) animation
- animation de l'ennemi: 
  - AnimatedSprite2D (importer des images ou une spritesheet)
  - marche
  - flip
  - mort
- **Exercice 4:** implémenter l'anim d'attaque 
- interlude: trier ses fichiers parce que ça commence à faire beaucoup
  - faire un dossier pour les niveaux (et un sous-dossier pour les niveaux non-finaux, de test par exemple, s'il y en a) et un autre pour les scènes, ne pas les mélanger
- améliorer le rendu visuel si pixel art: Projet > Paramètres du projet > Rendu > Textures > Filtre de texture par défaut > Nearest
