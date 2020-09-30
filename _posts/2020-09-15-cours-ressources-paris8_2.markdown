---
layout: default
title:  "Cours Paris 8: Création et Gestion de ressources"
date:   2020-09-15 19:05:09 +0200
categories: classes, krita, 2D, fr
permalink: /cours/creation_gestion_ressources_2.html
---

# O. [Menu](/cours/creation_gestion_ressources.html)
# I. [Introduction](/cours/creation_gestion_ressources_1.html)
# II. krita
## 1) introduction à krita: 1
- cf [Annexes X.1](/cours/creation_gestion_ressources_0.html)
- changer le nombre d'annulations possibles (Settings > Configure Krita > General > Miscellaneous > Undo Stack Size; 60 c'est bien, tester jusqu'à trouver la valeur qui nous convient)
- sauvegarder (ctrl S)
- pinceau / brush (B)
- gomme / eraser (E)
- annuler (Ctrl Z; désannuler: Shift Ctrl Z)
- couleurs (Advanced Color Selector)
- calques / layers (superficiellement)
- brosse de pixel art (taper "pixel" dans la barre de recherche des brosses, et choisir la brosse "u)\_Pixel\_Art")
- déplacement dans l'image (molette ou ctrl clic molette: zoom; espace clic ou clic molette: se déplacer)
- taille de la brosse (shift clic: changer la tailler de la brosse)

--  
**EXERCICE 1**  
faire un objet en 16*16 pixels (par exemple l'icône de la barre de vie du personnage principal du projet de fin d'année, un objet qui redonne de la vie, un icône de sort, une potion, etc.)  
--> pour se familiariser avec l'interface de krita  
--  

## 2) lisibilité
- personnage/fond: que le perso se détache sur le fond
- plateformes et éléments interactifs: qu'ils soient clairement identifiables comme tels
    - supertux plateformes invisibles
    - dead cells design clair
- personnages entre eux: qu'ils soient facilement différenciables
- personnages/ennemis: qu'ils soient différenciables en un coup d'oeil
- fond/fond: premier plan en [illustration](/assets/300_horizonZeroDawn.jpg): ajoute de la profondeur; en [level design](301_fantasiaInfogrames_gd.png): gaffe à la parallaxe qui peut cacher des éléments importants au gameplay)

**références**  
Horizon Zero Dawn, par Guerilla Games: https://www.guerrilla-games.com/play/horizon  
Fantasia, par Infogrames: https://fr.wikipedia.org/wiki/Fantasia_(jeu_vid%C3%A9o)

--  
**EXERCICE 2**  
faire un personnage en 32*32 pixels (soit le perso de son projet de fin d'année, soit un autre personnage, soit un fanart, etc.)  
--> pour se familiariser avec krita et pour s'entraîner à synthétiser des formes pour le pixel art  
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
        - pour des tests dont on pourrait décider, une fois finis, que finalement ils ne nous plaisent pas
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
    - shift: ajouter à la sélection

--  
**EXERCICE 3**  
faire des variantes d'ennemis ou de pnj avec des calques sur la même base (vêtements ou objets additionnels ou attaques feu/eau ou etc.)  
--> pour se familiariser avec les calques  
--  

## 4) introduction à krita: 3
- outils de sélection
- outils de sélection par couleur (contiguous selection tool, similar color selection tool) et leur options (dans le docker tool options)
- Fill tool (le seau) (F)
- outils de déplacement (T) et déformation (ctrl T)
- redimensionnement
    - redimensionnement de l'image (Image > Scale Image to New Size, Filtre: nearest neighbout, utiliser un multiple entier de la taille actuelle)
    - redimensionnement du canevas (Image > Resize Canvas)
    - mode de redimensionnement: plus proche voisin / nearest neighbour
    - crop tool (C)
- mentionner les brosses et la sensibilité à la pression pour l'opacité et la taille
- fenêtre secondaire de prévisualisation: Window > New Window; Window > New View; Tab; 1; mettre au premier plan

--  
**EXERCICE 4**  
faire des variantes d'ennemis ou de pnj en modifiant leur couleur, et les exporter en taille *3  
--> pour utiliser les outils de sélection, de couleur, de redimensionnement
--  

## 5) gestion ressources
- noms de fichiers: a-z, A-Z, 0-9, -, _ sont sûrs, éviter ponctuation, /, \, accents et symboles (cf [une source au pif](https://support.promax.com/knowledge/special-characters))
- organisation de répertoire et conventions de nommage communes par projet pour tout le monde, sous-répertoires.
- exports .kra incrémentiels (noms descriptifs, numérotés, dans un dossier à part éventuellement, par exemple: utiliser l'option "File>Save" (ctrl S) et/ou "File>Save As" avec le nom MonPersonnage.kra, dès qu'on y pense (toutes les cinq minutes), et utiliser l'option "File>Export" dès qu'on est à une étape importante: MonPersonnage-01-silhouette.kra, MonPersonnage-02-couleur.kra, etc.)
    - /!\ si sauvegarde en plus basse qualité, _d'abord_ sauver sous un autre nom puis réduire la qualité
- essayer de se créer des ressources réutilisables (tilemaps, icones)
- git lfs (au 2nd semestre, cours de Outils informatiques collaboratifs (git))
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

# III. [Décors](/cours/creation_gestion_ressources_3.html)
# IV. [Son](/cours/creation_gestion_ressources_4.html)
# V. [Animation](/cours/creation_gestion_ressources_5.html)
# X. [Annexes](/cours/creation_gestion_ressources_0.html)
