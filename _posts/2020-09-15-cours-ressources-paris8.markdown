---
layout: default
title:  "Cours Paris 8: Création et Gestion de ressources"
date:   2020-09-15 19:05:09 +0200
categories: classes, krita, 2D, fr
permalink: /cours/creation_gestion_ressources.html
---

L'adresse de ce cours: https://falano.github.io/cours/creation_gestion_ressources.html

Mon email: noemie. scherer @ gmail. com  
N'hésitez pas à m'envoyer un mail si vous avez des questions ou si vous êtes bloqués, j'essaierai de répondre rapidement (y compris si votre question porte sur un truc graphique qui n'est pas du pixel art).  

Programmes utilisés pendant le cours:  
Krita: https://krita.org/fr/telechargement/krita-desktop/  
Audacity: https://www.audacityteam.org/download/  

# I. [Introduction](/cours/creation_gestion_ressources_1.html)
# II. [Krita](/cours/creation_gestion_ressources_2.html)
# III. [Décors](/cours/creation_gestion_ressources_3.html)
# IV. [Son](/cours/creation_gestion_ressources_4.html)
# V. [Animation](/cours/creation_gestion_ressources_5.html)
# X. [Annexes](/cours/creation_gestion_ressources_0.html)

TODO: check all translations of tool names!

# I. [Introduction](/cours/creation_gestion_ressources_1.html)
## 1) présentation du cours

- pixel art avec krita
    - personnages
    - animation
    - décors
        - peints
        - assemblés avec une tilemap [(exemple de tilemap dans Godot)](/assets/002_tilemap.png)
- son avec audacity (écouteurs?)
    - logiciel d'écriture musicale?
- gestion de ressources
- projet final (platformer? jeu narratif? énigmes? puzzle? stratégie? contemplatif? etc.)

## 2) présentation du pixel art
pourquoi krita: autres logiciels (gimp, etc.)  
pourquoi le pixel art: relativement simple, assez répandu, ne nécessite pas de tablette graphique  
présentation et historique du pixel art:  
- absence d'[antialiasing/anticrénelage](/assets/000_anti-aliasing.png) (-> options des outils)
- racines du pixel art dans des contraintes techniques (cf [pokemon red](/assets/100_pokemon.jpg), [mario](/assets/101_mario.jpg), la [palette de couleurs](/assets/102_nes_palette.jpg) de la console nes, [final fantasy 6](/assets/103_ff6.jpg))
    - nombre de pixels limité
    - nombre de couleurs limité (cf [dithering](/assets/001_dithering.png))
    - utilisation de tilemaps
- pixel art actuel
    - nostalgie et aspect rétro ou préférence graphique (cf [A short Hike](/assets/113_aShortHike.png), [owlboy](/assets/107_owlboy_gd.png), [celeste](/assets/109_celeste.png))
    - utilisation pour la vitesse/facilité d'exécution
        - jeux de game jam ([gophers](/assets/105_gophers.png), [roguelight](/assets/106_roguelight.png))
        - jeux indé ([hyperlight drifter](/assets/108_hyperLightDrifter.png))
    - utilisation mixte avec des technologies récentes ([fez](/assets/110_fez.png), [dead cells](/assets/111_Dead-Cells.jpg), [the last night](/assets/112_TheLastNight.jpg))
- utilisation hors jeux (illustration ([exemple 1](/assets/114_jindrich-stejskal.gif), [exemple 2](/assets/115_jubilee.png)))

**références**  
Pokemon Version Rouge Feu, par Nintendo  
Super Mario Bros, par Nintendo  
Final Fantasy 6, par Square Enix  
A Short Hike, par Adam Robinson-Yu: http://ashorthike.com/  
Owlboy, par D-Pad Studio: http://www.owlboygame.com/  
Celeste, par Matt Makes Games: http://www.celestegame.com/  
Gophers, par Hyperlink Your Heart: https://hyperlinkyourheart.itch.io/gophers  
Roguelight, par Daniel Linssen: https://managore.itch.io/roguelight  
Hyperlight Drifter, par Heart Machine: https://heartmachine.com/hyper-light  
Fez, par Polytron: http://fezgame.com/
Dead Cells, par Motion Twin: https://dead-cells.com/  
The Last Night, par Odd Tales: http://oddtales.net/
The World is Leaking, par Jindrich Stejskal: https://www.artstation.com/artwork/QzA3D4  
Summer's Passing, par Jubilee Payne: https://www.artstation.com/artwork/w8eebY

## 3) considérations générales
- de l'importance de savoir chercher sur internet
- penser à utiliser des références pour dessiner (cf [dessin médiéval d'éléphant](/assets/200_elephant.jpg))
- l'anglais c'est pratique

**références**  
un manuscrit du 13ème siècle: https://www.bl.uk/manuscripts/FullDisplay.aspx?ref=Royal_MS_12_f_xiii page f.11v

# II. krita
## 1) introduction à krita: 1
- changer le nombre d'annulations possibles (Settings > Configure Krita > General > Miscellaneous > Undo Stack Size)
- sauvegarder (ctrl S)
- pinceau / brush (B)
- gomme / eraser (E)
- annuler (Ctrl Z; désannuler: Shift Ctrl Z)
- couleurs (Advanced Color Selector)
- calques / layers (superficiellement)
- brosse de pixel art (superficiellement)
- déplacement dans l'image (molette ou ctrl clic molette: zoom; espace clic ou clic molette: se déplacer)
- taille de la brosse (shift clic: changer la tailler de la brosse)

--  
**EXERCICE 1**  
faire un objet en 16*16 pixels (par exemple l'icône de la barre de vie du personnage principal du projet de fin d'année, un objet qui redonne de la vie, un icône de sort, une potion, etc.)  
--  

## 2) lisibilité
- personnage/fond
- plateformes et éléments interactifs
    - supertux plateformes invisibles
    - dead cells design clair
- personnages entre eux
- personnages/ennemis
- fond/fond (premier plan en [illustration](/assets/300_horizonZeroDawn.jpg): ajoute de la profondeur/en [level design](301_fantasiaInfogrames_gd.png): gaffe à la parallaxe)

**références**  
Horizon Zero Dawn, par Guerilla Games: https://www.guerrilla-games.com/play/horizon  
Fantasia, par Infogrames: https://fr.wikipedia.org/wiki/Fantasia_(jeu_vid%C3%A9o)

--  
**EXERCICE 2**  
faire un personnage en 32*32 pixels (soit le perso de son projet de fin d'année, soit un autre personnage, soit un fanart, etc.)  
--  

## 3) introduction à krita: 2
- les sous-fenêtres additionnelles sont à Settings > Dockers > ?
- si on laisse la fenêtre sur une option son nom apparaît
- cacher les menus: Tab
- nouveau document, ouvrir un document, etc.
- couleurs (principale et secondaire, historique des couleurs)
- Opacité / taille
    - si on clique droit sur un slider on peut entrer une valeur précise
- Calques / Layers
    - ajouter/supprimer/déplacer un calque
    - opacité de calques
    - [modes de calques](/assets/400_modesCalques.png)
        - overlay et/ou multiply pour les ombres
        - overlay et/ou normal à faible opacité pour la lumière
        - erase
        - tester les autres pour voir ce qu'ils font
    - groupes de calques
    - verrouiller un calque / lock layer
    - verrouiller la transparence / lock alpha
    - hériter la transparence / inherit alpha
        - par exemple pour avoir un calque couleur et un calque forme
        - ou pour les ombres/lumières
    - utilisation
        - pour des éléments superposés séparés (pour la p1eau d'oignon)
        - pour des éléments secondaires (fumée de cigarette, queue de cheval, cape)
        - pour des éléments non-permanents (pour avoir plusieurs versions du même personnage, avec ou sans chapeau par exemple, ou avec ou sans tatouages)
        - pour des tests
    - transparence
- Options des Outils / Tool Options
- Aperçu / Overview
- Suppr: tout effacer
- V cliquer-glisser: ligne droite (+ shift: 0°, 15°, 30°, 45°, etc.) (ou outil ligne / line tool)
- globalement, dans beaucoup de programmes graphiques:
    - utiliser la souris et ctrl/alt/shift pour se déplacer,
    - shift pour maintenir les proportions (par exemple quand on redimensionne)
    - ctrl C copier, ctrl V coller, ctrl X couper, ctrl Z annuler
    - ctrl S sauvegarder, ctrl shift S sauvegarder sous
    - ctrl W fermer la fenêtre, ctrl Q quitter
    - ctrl A tout sélectionner

--  
**EXERCICE 3**  
faire des variantes d'ennemis ou de pnj avec des calques sur la même base (vêtements ou objets additionnels ou attaques feu/eau ou etc.)  
--  

## 4) introduction à krita: 3
- outils de sélection
- outils de sélection par couleur (contiguous selection tool, similar color selection tool) et leur options
- Fill tool (le seau) (F)
- outils de déplacement/déformation (ctrl T)
- redimensionnement
    - redimensionement de l'image
    - redimensinnement du canevas
    - mode de redimensionnement: plus proche voisin / nearest neighbour
    - crop tool
- mentionner les brosses et la sensibilité à la pression pour l'opacité et la taille
- fenêtre secondaire de prévisualisation: Window > New Window; Window > New View; Tab; 1; mettre au premier plan

--  
**EXERCICE 4**  
faire des variantes d'ennemis ou de pnj en modifiant leur couleur, et les exporter en taille *3  
--  

## 5) gestion ressources
- organisation de répertoire et conventions de nommage communes par projet pour tout le monde, sous-répertoires.
- exports .kra incrémentiels (noms descriptifs, numérotés, dans un dossier à part éventuellement)
    - /!\ si sauvegarde en plus basse qualité, _d'abord_ sauver sous un autre nom puis réduire la qualité
- essayer de se créer des ressources réutilisables (tilemaps, icones)
- git lfs
- plusieurs supports de sauvegarde des fichiers importants

## 6) les formats graphiques
Ici, j'appelle "fichier de travail" un fichier contenant toutes les informations utilisées pour l'édition d'un fichier, et "export" un fichier utilisé uniquement pour le visionnage du fichier (plus largement lisible et plus léger).  
Un fichier de travail est généralement lisible uniquement par le logiciel qui l'a produit, alors que la plupart des fichiers d'export dont je parle ici sont lisibles sur les lecteurs de fichier par défaut et sur les pages web.  
Même une fois le travail fini, il est mieux de toujours conserver un fichier de travail de ce qu'on a fait.  

Formats 2D principaux pour ce cours-ci:
- .jpg: très léger, forte compression (pas très bonne qualité), ne l'utiliser que comme fichier d'export final, et jamais pour le pixel art (la compression abîme l'image), lisible partout, ne contient jamais de transparence ni de calques
- .png: assez léger, lisible partout, **très bon format pour l'export final de pixel art**, très léger s'il y a peu de couleurs ou de grandes plages de la même couleur (typiquement: le pixel art), peut contenir de la transparence mais pas de calques
- .kra: fichier de travail de krita, lisible uniquement par les ordinateurs ayant krita installé, pas de compression (très bonne qualité), lourd, peut contenir de la transparence, des calques, des animations, etc.

autres:
- .gif: utilisé pour des animations de petite taille (l'animation se lance automatiquement dans la plupart des lecteurs et des pages web), peut contenir de la transparence. À qualité visuelle équivalente, souvent plus lourd qu'un autre format vidéo bien compressé, mais est traité comme une image, donc ne nécessite pas de lecteur vidéo pour être lu, ce qui est parfois pratique. Pas de son.
- .avi, .mov: fichier vidéo, souvent compressé
- .mkv: fichier vidéo open source, souvent compressé, pouvant contenir plusieurs pistes audio et de sous-titres différentes
- .xcf: fichier de travail de gimp
- .psd: fichier de travail de photoshop
- .pdf: utilisé pour des documents à plusieurs pages et/ou avec des charactères écrits

# III. Décors
## 1) Tiles
- doivent s'emboîter sans que ça se voie
- pour les décors naturels: avoir plusieurs variantes excentrées
- perspective au choix
    - vu de haut (jrpgs) TODO: illo
    - vu de côté (platformers) (TODO: illo: SuperMeatBoy!!)
    - vue isométrique (stratégie); supporté par Godot  (TODO: quels angles en general?) TODO: illo
    - vue de haut non-carrée (type jeu de plateau) (TODO: illo wesnoth)

## 2) Krita: 4
- grilles
    - magnétisme (TODO: check if works for last ver)
    - grilles isométriques
- wrap around mode
- mirror tools

## 3) Décor plein
- perspective: couleurs
- parallaxe

## 4) Krita: 5
- outils perspective
- outils forme
- gomme lasso

# IV. Son
## 1) intro
- de l'importance du son
- effets sonores / musique
- (enregistrer / télécharger)->(modifier) / produire numériquement
    - les écouteurs-enregistreurs ont trois bandes sur le port jack, les non-enregistreurs n'en ont que deux

## 2) Audacity
- audacity
    - pour enregistrer
    - pour modifier/monter
        - changer le volume
        - enlever les bruits de fond parasites
        - sélectionner une partie spécifique du clip audio

## 3) 


# 2) musique
- enregistrer sa musique: -> enregistreur + audacity
- générer sa propre musique (en 2ème année 2ème semestre il y a un cours de "synthèse d'images, animation et sons")
    - avec un logiciel d'écritures de partitions qui exporte en MIDI (TODO: y a pas une étape supplémentaire pour mettre du beau son sur le midi?)
        - musescore
        - lilypond
    - avec un logiciel de création de musique
        - https://beepbox.co/ (musique bitbox, simple d'utilisation)
        - LMMS? (TODO: )
        - Yoshimi? (TODO: )


en L1S2: cours de Outils informatiques collaboratifs (git)
à venir

# V. Animation
à venir

# X. Annexes

## 1) notions de game design:  
- si jeu de plateforme/énigmes: introduire une seule mécanique de jeu à la fois (bg)  
- lisibilité (perso)  
- vitesse de réaction du jeu: éviter les animations longues en début d'action (anim)  
- de l'importance du son (son)  
- de l'importance des retours visuels (feedback) (anim)  

## 2) Ressources externes
/!\ Toujours vérifier la licence des assets qu'on utilise, et la respecter.
- licences (CC-0, CC-BY, CC-BY-SA-NC)
- graphique
    - https://opengameart.org/ (assets graphiques et sonores CC)
    - https://www.dafont.com (polices de caractères avec filtre par licence)
    - https://itch.io/game-assets/assets-cc0/tag-pixel-art : assets de pixel art CC0
- audio
    - sons
        - https://freesfx.co.uk/Default.aspx : un site de sons (gratuit avec attribution au site (pas par son))
        - https://freesound.org/ : un site de sons CC (licences différentes par son)
        - https://www.bfxr.net/ : un outil open source de génération de sons. Nécessite flash.
    - musique
        - https://www.hongkiat.com/blog/creative-common-music-download/ (liste)
        - https://audionautix.com/ (site de musiques CC-BY)
        - https://freemusicarchive.org/ (site de musiques CC)
        - https://filmmusic.io/search (site de musiques principalement CC BY)
        - liens: https://incompetech.com/music/royalty-free/faq.html (site de musiques CC-BY-ish)
