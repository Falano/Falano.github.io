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
- cf [Annexes X.1](/cours/creation_gestion_ressources_0.html), un schéma de l'interface de krita
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
- transparence!

--  
**EXERCICE 3**  
faire des variantes d'ennemis ou de pnj avec des calques sur la même base (vêtements ou objets additionnels ou attaques feu/eau ou etc.)  
--> pour se familiariser avec les calques  
--  

## 4) introduction à krita: 3
- outils de sélection
- outils de sélection par couleur (contiguous selection tool, similar color selection tool) et leur options (dans le docker tool options)
- Fill tool (le seau) (F)
- outils de déplacement (T) et déformation (ctrl T) (ne l'utiliser que pour les symmétries, pas pour redimensionner)
- redimensionnement
    - redimensionnement de l'image (Image > Scale Image to New Size, Filtre: nearest neighbout, utiliser un multiple entier de la taille actuelle)
    - redimensionnement du canevas (Image > Resize Canvas)
    - mode de redimensionnement: plus proche voisin / nearest neighbour
    - crop tool (C)
- mentionner les brosses et la sensibilité à la pression pour l'opacité et la taille
- fenêtre secondaire de prévisualisation: Window > New Window; Window > New View; Tab; 1; mettre au premier plan
- les courbes doivent être régulières; le nombre de pixels doit faire par exemple 3,2,1,2,3 et non 3,1,2,1,2,3
    ![courbes](/assets/mine/courbes.png)

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
Ici, j'appelle "fichier de travail" un fichier contenant toutes les informations utilisées pour l'édition d'un fichier, et "fichier de lecture" un fichier utilisé uniquement pour le visionnage du fichier (plus largement lisible et plus léger).  
Un fichier de travail est généralement lisible uniquement par le logiciel qui l'a produit, alors que la plupart des fichiers de lecture dont je parle ici sont lisibles sur les lecteurs de fichier par défaut et sur les pages web.  
Même une fois le travail fini, il est mieux de toujours conserver un fichier de travail de ce qu'on a fait.  

Formats 2D principaux pour ce cours-ci:
- **.jpg**: très léger, forte compression (pas très bonne qualité), ne l'utiliser que comme fichier d'export final, et jamais pour le pixel art (la compression abîme l'image), lisible partout, ne contient jamais de transparence ni de calques
- **.png**: assez léger, lisible partout, **très bon format pour l'export final de pixel art**, très léger s'il y a peu de couleurs ou de grandes plages de la même couleur (typiquement: le pixel art), peut contenir de la transparence mais pas de calques
- **.kra**: fichier de travail de krita, lisible uniquement par les ordinateurs ayant krita installé, pas de compression (très bonne qualité), lourd, peut contenir de la transparence, des calques, des animations, etc.

autres:
- **.gif**: utilisé pour des animations de petite taille (l'animation se lance automatiquement dans la plupart des lecteurs et des pages web), peut contenir de la transparence. À qualité visuelle équivalente, souvent plus lourd qu'un autre format vidéo bien compressé, mais est traité comme une image, donc ne nécessite pas de lecteur vidéo pour être lu, ce qui est parfois pratique. Pas de son.
- **.avi**, **.mov**: fichier vidéo, souvent compressé
- **.mkv**: fichier vidéo open source, souvent compressé, pouvant contenir plusieurs pistes audio et de sous-titres différentes
- **.xcf**: fichier de travail de gimp
- **.psd**: fichier de travail de photoshop
- **.pdf**: utilisé pour des documents à plusieurs pages et/ou avec des charactères écrits

## 7) un chouilla de théorie des couleurs
- éviter a priori les couleurs trop saturées
    - éviter encore plus deux complémentaires très saturées côte-à-côte; ça brûle les yeux
        -  les couleurs complémentaires sont celles qui sont opposées sur le cercle des teintes: rouge et vert, violet et jaune, bleu et orange
    - mais pour faire ressortir un détail (de petite taille) et attirer l'attention, on peut saturer davantage ses couleurs (sur un _petit_ espace)
        - ou utiliser une couleur complémentaire à celles généralement utilisées dans le niveau
- pour info: un gris entouré de rouge sembrera rougeâtre (ça marche pour tous les couples de complémentaires)

## 8) Recap général
- ombres et lumières de teintes différentes (typiquement un vert clair sera plus jaune, un bleu clair plus cyan, et un rouge clair ou un jaune foncé plus orange)
    - choisir la complémentaire de la couleur de base pour les ombres (des ombres marron foncé pour un personnage bleu ou vert, violettes pour un personnage jaune, etc.) les fait ressortir davantage
    - mais il ne faut pas non plus que les couleurs des ombres changent à chaque objet
- styliser et simplifier
    - choisir consciemment ce qu'on représente
    - il n'est pas toujours nécessaire, par exemple, que les personnages aient une bouche
- partir d'une forme simple (carré, rond, triangle) et sculpter avec le pinceau et la gomme pour les détails
    - commencer avec une silhouette monochrome pour être sûr qu'elle soit bien lisible
- PENSER À DÉZOOMER RÉGULIÈREMENT; le pixel art n'est pas très lisible de très près, c'est normal, il faut juste qu'il soit lisible quand on joue
    - mettre une deuxième fenêtre de krita dézoomée si besoin

## 99) plus de ressources (principalement en anglais)
- le [canal youtube de Brandon James Greer](https://www.youtube.com/channel/UCC26K7LTSrJK0BPAUyyvtQg)
    - notamment:
    - [lignes et courbes](https://www.youtube.com/watch?v=ye21r27kN9I&list=PLxfQIomHccxvoTON6hXhfZyAUdFXd-z1P&index=3)
    - [une analyse des graphismes de pokemon](https://www.youtube.com/watch?v=gwF0L55kIgg)
        - dont [un mini-tuto sur des objets en perspective vu du haut](https://www.youtube.com/watch?v=gwF0L55kIgg&feature=youtu.be&t=179)
    - une [nouvelle version (commentée) de son premier personnage en pixel art](https://www.youtube.com/watch?v=kOotrzumpco&list=PLxfQIomHccxtHHzSNfHrymaDq8CRGwTre&index=6)
    - [hue shifting](https://www.youtube.com/watch?v=PNtMAxYaGyg&list=PLxfQIomHccxvoTON6hXhfZyAUdFXd-z1P&index=5)
    - [comment réduire la taille d'un objet](https://www.youtube.com/watch?v=PtYoLFKkgoQ&list=PLxfQIomHccxvoTON6hXhfZyAUdFXd-z1P&index=4)
    - [finitions](https://www.youtube.com/watch?v=lHGDz_sz-gk&list=PLxfQIomHccxvoTON6hXhfZyAUdFXd-z1P&index=8)
- un [tutoriel général qui contient des trucs intéressants](http://pixeljoint.com/forum/forum_posts.asp?TID=11299), notamment IV., parties Banding, Pillow-shading, Noise, et V. Color ramps et Hue Shifting
- un [autre tutoriel général avec des concepts intéressants](http://androidarts.com/pixtut/pixelart.htm), notamment de bonnes explications sur les choix de couleurs et les contours 
- plein de tutoriels format gif, courts et efficaces: [https://blog.studiominiboss.com/pixelart](https://blog.studiominiboss.com/pixelart)
    - [principes généraux de pixel art](https://www.patreon.com/posts/pixel-art-1-6971422)
    - [contours](https://www.patreon.com/posts/outlines-14106192)
    - [character design](https://www.patreon.com/posts/character-design-7530899)

## 100) quelques ressources en français
- une traduction d'extraits du tuto de Arne ([http://androidarts.com/pixtut/pixelart.htm](http://androidarts.com/pixtut/pixelart.htm)):
    - Palettes:
![Palettes](/assets/arnesTuto/01_Skintone.gif)  
Sauf à travailler avec de très petites palettes (de 3 couleurs par exemple), on aura probablement besoin de mettre en place des rampes de couleurs (dégradés) à un moment. Quand on crée sa rampe je déconseille de mélanger du noir et du blanc à la couleur de base pour créer les deux bouts de la rampe. Dans la nature, la teinte d'une couleur change souvent avec la lumière, donc une rampe noir-rose-blanc peut sembler terne et artificielle. En plus, un objet, comme un visage par exemple, a souvent des teintes différentes selon les endroits. Pour de la peau, j'aime faire l'ombre un violet sombre un peu gris, garder le ton moyen orange, et la lumière presque jaune. Dans les scènes d'extérieur je mélange aussi des tons gris plus froids pour l'ombre (à cause de la lumière du ciel) et du jaune dans les couleurs claires (à cause de la lumière chaude du soleil)
    - Fluo:
![Fluo](/assets/arnesTuto/02_Supergreen.gif)  
Il existe de nombreuses couleurs, mais certaines sont plus facilement utilisables que d'autres, particulièrement quand on fait des trucs réalistes. J'éviterais de construire des ramples entières à partir de couleurs très saturées, sauf si on fait un travail sur le fluo ou expérimental. Ça ne veut pas dire que toutes les couleurs devraient être grises ou pastel; les couleurs très saturées peuvent être très efficaces pour ajouter une dimension supplémentaire à certains points, mais je pense que leur fréquence dans la palette devrait être proportionnelle à leur utilisation. Ici j'ai dessiné une petite créature fluo étrange parce que ça correspond à la palette. Pour des visages ou de la nature je devrais avoir une approche plus artistique.
    - Contours:
![Contours](/assets/arnesTuto/03_Blacklining.gif)  
Un excès de contours noirs peut naître d'une sorte de compulsion à marquer et séparer chaque détail. Quand les couleurs sont entourées de noir elles ont l'air plus sombres et ternes. On perd aussi de l'espace et tout le personnage est aplati parce que les lignes poussent tous les détails au même plan (surtout si les rampes de couleur utilisées sont peu contrastées). Une autre manière de séparer les détails est d'utiliser le contraste et des lignes additives plus claires (les lignes noires sont soustractives). Le style que j'utilise a l'avantage d'un mélange de lignes soustractives, de lignes perdues (suggérées mais pas explicitement dessinées) et de lignes additives.
    - Contours au sol:
![Contours au sol](/assets/arnesTuto/04_Bottomlines.gif)  
Une autre considération quand on travaille avec des contours noirs est que les lignes à la base de la forme ressemblent un peu à une ombre et peuvent donner l'impression que la figure entière flotte. Si on enlève les contours au contact avec le sol, la forme semble solidement posée.  
Si on enlève tout le contour on gagne plus de place pour les détails internes, mais après il faut se reposer sur le contraste avec le fond pour la lisibilité de la silhouette.
    - Lignes:
![Lignes](/assets/arnesTuto/05_Cleanlines.gif)  
Des lignes de pixels posées rapidement semblent irrégulières et désordonnées, un peu comme un croquis au crayon d'un débutant qui repasse plusieurs fois sur les lignes (lignes barbelées). Certains détails utilisent des lignes irrégulières, mais en général on voudra utiliser des courbes de type 1, 1, 2, 3, ou 2, 1, 2, ou quelque chose du genre. Dans l'ombre des objets je remplis parfois les diagonales, mais parfois ça peut ne pas sembler très propre.
    - Bruit:
![Bruit](/assets/arnesTuto/06_Noise.gif)  
Du bruit et des pixels inutilement orphelins (non reliés à d'autres pixels de la même couleur), c'est ce qu'on obtient quand on essaie d'incorporer trop de détails. Il est tentant d'en inclure autant que possible, mais il faut considérer l'échelle du pixel art et comment être clair, et aussi la facilité d'animation (des détails lisibles sur une image pourraient être difficiles à dupliquer sur l'image suivante, légèrement tournée). L'artiste connaît peut-être l'intention derrière chaque pixel, mais le joueur généralement pas, et les verra donc probablement comme du bruit (et l'artiste aussi en y retournant plus tard).  
Cela dit, il est intéressant de conserver quelques endroits avec plus de bruit pour ajouter des variations dans la texture.

# III. [Décors](/cours/creation_gestion_ressources_3.html)
# IV. [Son](/cours/creation_gestion_ressources_4.html)
# V. [Animation](/cours/creation_gestion_ressources_5.html)
# X. [Annexes](/cours/creation_gestion_ressources_0.html)
