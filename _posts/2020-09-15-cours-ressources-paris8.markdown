---
layout: default
title:  "Cours Paris 8: Création et Gestion de ressources"
date:   2020-09-15 19:05:09 +0200
categories: classes, krita, 2D, fr
permalink: /cours/creation_gestion_ressources.html
---

L'adresse de ce cours: 
<https://falano.github.io/cours/creation_gestion_ressources.html>

Mon email: noemie. scherer @ gmail. com  
N'hésitez pas à m'envoyer un mail si vous avez des questions ou si vous êtes bloqués, j'essaierai de répondre rapidement (y compris si votre question porte sur un truc graphique qui n'est pas du pixel art).  

Programmes utilisés pendant le cours:  
Krita: <https://krita.org/fr/telechargement/krita-desktop/>  
Audacity: <https://www.audacityteam.org/download/>  
Musescore: <https://musescore.org/en>

# I. [Introduction](/cours/creation_gestion_ressources_1.html)
# II. [Krita](/cours/creation_gestion_ressources_2.html)
# III. [Décors](/cours/creation_gestion_ressources_3.html)
# IV. [Son](/cours/creation_gestion_ressources_4.html)
# V. [Animation](/cours/creation_gestion_ressources_5.html)
# X. [Annexes](/cours/creation_gestion_ressources_0.html)

{% comment %}
[](!! ne pas oublier de faire un récap en début de cours)

# I. [Introduction](/cours/creation_gestion_ressources_1.html)
## 1) présentation du cours

- pixel art avec krita
    - personnages
    - animation
    - décors
        - peints
        - assemblés avec une tilemap <details>![(exemple de tilemap dans Godot)](/assets/002_tilemap.png)
- son avec audacity (qui a des écouteurs?)
    - logiciel d'écriture musicale?
- gestion de ressources
- projet final (platformer? jeu narratif? énigmes? puzzle? stratégie? contemplatif? tower defense? etc.)

## 2) présentation du pixel art
pourquoi krita: autres logiciels (gimp, etc.)  
pourquoi le pixel art: relativement simple (cf Selfless Heroes), assez répandu, ne nécessite pas forcément de tablette graphique ni de savoir dessiner <details>- Selfless Heroes ![Selfless Heroes](/assets/003_selflessHeroes.png)

présentation et historique du pixel art:  
- absence d'antialiasing/anticrénelage automatique (-> options des outils)<details>![antialiasing/anticrénelage](/assets/000_anti-aliasing.png)
- racines du pixel art dans des contraintes techniques (cf pokemon red, mario, la palette de couleurs de la console nes, final fantasy 6)
    - nombre de pixels limité
    - nombre de couleurs limité (cf dithering)
    - utilisation de tilemaps <details> - pokemon red ![pokemon red](/assets/100_pokemon.jpg) <br> - mario ![mario](/assets/101_mario.jpg) <br> - la palette de couleurs de la console nes ![palette nes](/assets/102_nes_palette.jpg) <br> - final fantasy 6 ![final fantasy 6](/assets/103_ff6.jpg) <br> - dithering ![dithering](/assets/001_dithering.png)
- pixel art actuel
    - nostalgie et aspect rétro ou préférence graphique (cf A short Hike, Owlboy, Celeste) <details> - A short Hike ![A short Hike](/assets/113_aShortHike.png) <br> - Owlboy ![owlboy](/assets/107_owlboy_gd.png) <br> - Celeste ![celeste](/assets/109_celeste.png)
    - utilisation pour la vitesse/facilité d'exécution
        - jeux de game jam (Gophers, Roguelight; cf [Annexes X.4](/cours/creation_gestion_ressources_0.html)), une explication et une liste de game jams
        - jeux indé (Hyperlight Drifter) <details> - Gophers ![gophers](/assets/105_gophers.png) <br> - Roguelight ![roguelight](/assets/106_roguelight.png) <br> - Hyperlight Drifter ![hyperlight drifter](/assets/108_hyperLightDrifter.png)
    - utilisation mixte avec des technologies récentes (Fez, Dead Cells, The last Night) <details> - Fez ![fez](/assets/110_fez.png) <br> - Dead Cells ![dead cells](/assets/111_Dead-Cells.jpg) <br> - The last Night ![the last night](/assets/112_TheLastNight.jpg)
- utilisation hors jeux (illustration) <details> - Jindrich Stejskal ![exemple 1](/assets/114_jindrich-stejskal.gif) <br> - Jubilee ![exemple 2](/assets/115_jubilee.png)

**références**  
Selfless Heroes, par Félicien Brochu: <https://selflessheroes.fr/>  
Pokemon Version Rouge Feu, par Nintendo  
Super Mario Bros, par Nintendo  
Final Fantasy 6, par Square Enix  
A Short Hike, par Adam Robinson-Yu: <http://ashorthike.com/>  
Owlboy, par D-Pad Studio: <http://www.owlboygame.com/>  
Celeste, par Matt Makes Games: <http://www.celestegame.com/>  
Gophers, par Hyperlink Your Heart: <https://hyperlinkyourheart.itch.io/gophers>  
Roguelight, par Daniel Linssen: <https://managore.itch.io/roguelight>  
Hyperlight Drifter, par Heart Machine: <https://heartmachine.com/hyper-light>  
Fez, par Polytron: <http://fezgame.com/>  
Dead Cells, par Motion Twin: <https://dead-cells.com/>  
The Last Night, par Odd Tales: <http://oddtales.net/>  
The World is Leaking, par Jindrich Stejskal: <https://www.artstation.com/artwork/QzA3D4>  
Summer's Passing, par Jubilee Payne: <https://www.artstation.com/artwork/w8eebY>  
game jams: cf [Annexes X.4](/cours/creation_gestion_ressources_0.html), une explication et une liste de game jams

## 3) considérations générales
- de l'importance de savoir chercher sur internet
- penser à utiliser des références pour dessiner (cf un dessin médiéval d'éléphant par des gens qui n'en avaient jamais vu) <details> ![manuscrit](/assets/200_elephant.jpg)
- l'anglais c'est pratique, la majorité de la documentation est en anglais

**références**  
un manuscrit du 13ème siècle: <https://www.bl.uk/manuscripts/FullDisplay.aspx?ref=Royal_MS_12_f_xiii> page f.11v

## 4) jeux cools sans savoir dessiner
cf [Annexes X.5](/cours/creation_gestion_ressources_0.html), une liste de jeux cools
- video de gameplay (et, avant la minute donnée dans le lien, timelapse de dessin des assets) de gophers: <https://youtu.be/0jPLMCfSE0w?t=348>

[](TODO: vids de pxart simple (gophers et autre ), ou de trailers de jeux simples et cools.)

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

[](fin lundi matin 1 (plus un peu de krita2) --)

--  
**EXERCICE 2**  
faire un personnage en 32*32 pixels (soit le perso de son projet de fin d'année, soit un autre personnage, soit un fanart, etc.)  
--> pour se familiariser avec krita et pour s'entraîner à synthétiser des formes pour le pixel art  
--  

## 3) introduction à krita: 2
- les sous-fenêtres additionnelles sont à *Settings > Dockers > ?*
- si on laisse la fenêtre sur une option son nom apparaît
- cacher les menus: *Tab*
- nouveau document, ouvrir un document, etc.
- couleurs (principale et secondaire, historique des couleurs)
- Opacité / taille
    - si on clique droit sur un slider on peut entrer une valeur précise
- Calques / Layers
    - ajouter/supprimer/déplacer un calque
    - opacité de calques
    - modes de calques
        - overlay et/ou multiply pour les ombres
        - overlay et/ou normal à faible opacité pour la lumière
        - erase
        - tester les autres pour voir ce qu'ils font<details>![modes de calques](/assets/400_modesCalques.png)
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
- *V cliquer-glisser*: ligne droite (+ *shift*: 0°, 15°, 30°, 45°, etc.) (ou outil ligne / line tool)
- globalement, dans beaucoup de programmes graphiques:
    - utiliser la souris et *ctrl/alt/shift* pour se déplacer,
    - *shift* pour maintenir les proportions (par exemple quand on redimensionne)
    - *ctrl C* copier, *ctrl V* coller, *ctrl X* couper, *ctrl Z* annuler
    - *ctrl S* sauvegarder, *ctrl shift S* sauvegarder sous
    - *ctrl W* fermer la fenêtre, *ctrl Q* quitter
    - *ctrl A* tout sélectionner
    - *shift*: ajouter à la sélection
- transparence!

[](fin lundi aprèm 1 moins lisibilité plus formats)
[](fin mercredi aprèm 1 + gestion ressources + formats - lisibilité)

--  
**EXERCICE 3**  
faire des variantes d'ennemis ou de pnj avec des calques sur la même base (vêtements ou objets additionnels ou attaques feu/eau ou etc.)  
--> pour se familiariser avec les calques  
--  

[](fin lundi matin 2 moins lisi fond/fond, plus formats)

## 4) introduction à krita: 3
- outils de sélection
- outils de sélection par couleur (contiguous selection tool, similar color selection tool) et leur options (dans le docker tool options)
- Fill tool (le seau) (*F*)
- outils de déplacement (*T*) et déformation (*ctrl T*) (ne l'utiliser que pour les symmétries, pas pour redimensionner)
- redimensionnement
    - redimensionnement de l'image (*Image > Scale Image to New Size*, *Filtre: nearest neighbour*, utiliser un multiple entier de la taille actuelle)
    - redimensionnement du canevas (*Image > Resize Canvas*)
    - mode de redimensionnement: plus proche voisin / nearest neighbour
    - crop tool (*C*)
- mentionner les brosses et la sensibilité à la pression pour l'opacité et la taille
- fenêtre secondaire de prévisualisation: *Window > New Window; Window > New View; Tab; 1; mettre au premier plan*
- les courbes doivent être régulières; le nombre de pixels doit faire par exemple 3,2,1,2,3 et non 3,1,2,1,2,3 <details>![courbes](/assets/mine/courbes.png)

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
- essayer de se créer des ressources réutilisables (tilemaps, icones, UI)
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

[](fin lun aprèm 2 moins lisi fond)
[](fin mercr aprèm 2 moins lisi)

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
- ORGANISATION DU PROJET (couper en petits bouts finis) (cf [Annexes X.2b](/cours/creation_gestion_ressources_0.html))

[ ](2. fin lundi matin 1 moins lisi, moins formats)

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

## 3a) lisibilité
- personnage/fond: que le perso se détache sur le fond
    - pensez à mettre votre personnage dans votre fond quand vous travaillez
        - pour tester sa taille
        - et sa lisibilité
- plateformes et éléments interactifs: qu'ils soient clairement identifiables comme tels
    - supertux (bonus)
        - plateformes invisibles
        - murs creux
    - dead cells / celeste
        - plateformes qui se détachent bien
        - arrière-plan dé-contrasté <details> - dead cells ![Dead Cells](/assets/111_Dead-Cells.jpg) <br> - Celeste ![Celeste](/assets/109_celeste.png)
- personnages entre eux: qu'ils soient facilement différenciables
- personnages/ennemis: qu'ils soient différenciables en un coup d'oeil
- fond/fond: premier plan en illustration: ajoute de la profondeur; en level design: gaffe à la parallaxe qui peut cacher des éléments importants au gameplay) <details> - Horizon Zero Dawn ![horizon zero dawn](/assets/300_horizonZeroDawn.jpg) <br> - fantasia ![fantasia](/assets/301_fantasiaInfogrames_gd.png)

**références**  
Horizon Zero Dawn, par Guerilla Games: <https://www.guerrilla-games.com/play/horizon>  
Fantasia, par Infogrames: <https://fr.wikipedia.org/wiki/Fantasia_(jeu_vid%C3%A9o)>  
Supertux [](__TODO__)

## 3b) Décor plein
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

[](GIT LFS!!!)

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

[](2. fin L1C12)


# IV. Son
## 1) intro
- de l'importance du son
    - donne aussi des infos supplémentaires
        - ce qui se passe offscreen
        - matériaux des objets
        - attire l'attention sur un détail
        - feedback
- deux types de son:
    - 1. effets sonores, 2. musique
        - moyen de production assez différents
- (enregistrer / télécharger)->(modifier) / produire numériquement
    - les écouteurs-enregistreurs ont trois bandes sur le port jack, les non-enregistreurs n'en ont que deux
- à propos du MIDI et des soundfonts
- différence mono/stéréo (mono: une piste (son identique pour les deux oreilles), stéréo: deux pistes (un son différent pour chaque oreille: peut donner une impression de mouvement dans l'espace))
- couper un son au plus près, sans plage de silence au début (surtout pour les effets sonores d'action, dont il ne faut pas qu'ils soient en retard)
- éviter les différences de niveau (volume sonore) trop importantes
    - il n'y a rien de plus irritant qu'un son trop fort

## 2) licences
/!\ Toujours vérifier la licence des assets qu'on utilise.  
cf [Annexes X.3a](/cours/creation_gestion_ressources_0.html), une explication des principales licences libres utilisées pour les assets

[](3. fin L1A12 + un peu de 3 et 4)
[](3. fin L1B12 + un peu de 3 et 4 - intro)

## 3) Audacity
- navigation
    - en bas à gauche: project rate (Hz): choisir 44100 (qualité cd) ou 48000, pas plus bas
    - en haut à droite: 2 sliders pour régler le volume d'enregistrement et de lecture
    - barre espace ou bouton triangle vert: play, lancer le son
    - barre espace ou bouton deux traits noirs: pause, arrêter temporairement le son
    - double clic sur une piste son: sélectionner toute la piste
    - scroll molette: se déplacer sur la timeline
    - ctrl scroll molette: zoom / dézoom
    - cliquer-glisser sur une piste son pour sélectionner
- pour enregistrer
    - lancer l'enregistrement
        - bouton pause (deux traits noirs)
        - bouton enregistrement (un rond rouge)
        - régler le volume de son micro dans les paramètres de l'ordinateur
        - puis quand on est prêt, appuyer de nouveau sur pause pour lancer l'enregistrement
    - arrêter l'enregistrement
        - pour une simple pause, bouton pause
        - à la fin, bouton stop (un carré noir)
    - écouter l'enregistrement
        - *une fois l'enregistrement arrêté*, bouton play (triangle vert)
- pour modifier/monter
    - supprimer les 'clics' de début et de fin de son
        - sélectionner les deux-trois frames de début du son
        - Effect > Fade In
        - sélectionner les deux-trois frames de fin de son
        - Effect > Fade Out
        - plus de deux-trois frames et le fade s'entendra
    - changer le volume
        - sélectionner la partie qu'on veut modifier
        - Effect > Amplify
        - attention: trop monter le volume nuit à la qualité du son
    - enlever les bruits de fond parasites
        - !! quand on enregistre, inclure dix secondes de silence avant ou après
        - sélectionner une plage de silence
        - Effect > Noise Reduction
        - Get Noise Profile
        - sélectionner la partie qu'on veut nettoyer
        - Effect > Noise Reduction
        - jouer avec les sliders et Preview jusqu'à obtenir un résultat satisfaisant
        - Ok
    - réverbération, écho
        - ajoutez-le sur godot, c'est plus efficace

## 4) musique
- enregistrer sa musique: -> enregistreur + audacity
- générer sa propre musique (en 2ème année 2ème semestre il y a un cours de "synthèse d'images, animation et sons")
    - avec un logiciel d'écritures de partitions qui exporte aussi en MIDI ou avec du beau son
        - musescore
            - plein de soundfonts incluses de base
    - avec un logiciel de création de musique
        - https://beepbox.co/ (musique bitbox, simple d'utilisation)
            - éventuellement exporter en MIDI, importer dans musescore, mettre de belles soundfonts et réexporter en .wav ou .ogg
        - LMMS [](TODO: )
- télécharger une musique sous licence libre

## 5) les formats audio
- **.aup**: format de travail de audacity
- **.flac**: très bonne qualité (lossless), comparativement relativement léger, open source
- **.mp3**: pas très bonne qualité (compressé), très léger, lisible presque partout (le jpg du son)
- **.aiff**: historiquement le format bonne qualité de mac (sans compression); assez lourd
- **.wav**: historiquement le format bonne qualité de windows (sans compression); assez lourd mais rapide à lire pour godot; **lisible par godot**, conseillé pour les bruitages
- **.ogg**: meilleure qualité que mp3 à poids égal (compressé), open source, léger, un peu lent à lire pour godot; **lisible par godot**, conseillé pour les voix, les musiques, et les sons qui durent

# V. Animation
## 1) principes d'animation
- savoir d'où tu viens où tu vas
- anticipation - action - réaction
    - pour la défense/esquive du joueur, diminuer l'anticipation pour augmenter la réactivité (cf __lien joueur du grenier__)
    - pour l'attaque des ennemis, augmenter l'anticipation pour donner au joueur le temps de réagir
- anims décalées
- changement de direction: plus de temps, ralentissement
    - impression soulignée par s'il y a un élément qui suit (cheveux, corde, etc.)
- strong key poses
- de l'importance de l'anim de "personnage blessé" (cf __faire un exemple hurtanim avec/sans__)
- anim vague/fumée/vent/queue
- squash and stretch, déformations (__lien ou images/vid de bugsBunny__)
- anim de marche
    - head bob
    - jambe/bras opposés
    - torse inclinaison
- saut en jeu
    - pas juste une anim mais jusqu'à trois bouts d'anim

**références**  
anim bugsBunny  

## 2) outils d'animation
- docker Timeline
	- ajouter / supprimer une frame
	- déplacer / copier des frames
	- utiliser les calques pour ajouter / enlever un élément sur plusieurs frames d'un coup
- docker Animation
	- nombre d'images par seconde (24 pour le cinéma en europe; 12 c'est bien; 6 c'est possible mais un peu limite)
- docker Onion Skin
	- cliquer sur les numéros en haut pour l'activer/désactiver pour cette frame
	- cliquer sur le 0 pour le désactiver complètement
	- il faut l'activer pour chaque calque

## 3) export
- suite d'images
    - __TODO__
- spritesheet
    - krita
        - installer ce plugin <https://github.com/Falano/kritaSpritesheetManager>
    - gimp
        - __TODO__


## 99) Plus de ressources (principalement en anglais)
- plein de tutoriels format gif, courts et efficaces: [https://blog.studiominiboss.com/pixelart](https://blog.studiominiboss.com/pixelart)
    - notamment:
    - [boucles d'animation](https://www.patreon.com/posts/seamless-7346998)
    - [motion blur](https://www.patreon.com/posts/motion-blur-11596285)
    - décomposition d'une [animation d'attaque à l'épée](https://www.patreon.com/posts/attack-animation-7820106)
        - mais qui donne des principes utiles pour n'importe quelle animation
    - [très petits mouvements](https://www.patreon.com/posts/1-pixel-movement-7652033)
    - [fumée/explosion](https://www.patreon.com/posts/smoke-animation-6851636)
    - [explosions](https://www.patreon.com/posts/explosions-part-7719254)
    - [timings en animation](https://www.patreon.com/posts/animation-easing-8030922)
- un gros bouquin sur les principes d'animation (pas spécifique au pixel art ni au jeu; a été traduit en français): The Animator's Survival Kit, de Richard Williams
- quelques [principes généraux d'animation]((https://www.youtube.com/watch?v=uDqjIdI4bF4)) (vidéo)  

## 100) Ressources en français
- un [rapide aperçu des outils d'animation de krita](https://youtu.be/6NWJ119jJaI) (vidéo, pas de son)

# VI. UI
https://docs.godotengine.org/en/3.0/classes/class_ninepatchrect.html

## 99) plus de ressources (principalement en anglais)
- un tutoriel sur la [UI](https://www.patreon.com/posts/ui-9-slice-14798512) sur le site de studiominiboss (les tutos en .gif)


# VII. Imports et exports divers
1) importer une spritesheet dans krita

2) exporter du pixel art pour des réseaux sociaux

3) exporter son jeu
- itch.io


# X. Annexes
## 1) schéma de l'interface de Krita
![Interface Krita](/assets/999_interfaceKrita.png)
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
    - *double clic* ou *F2* sur le nom du calque pour le renommer
        - bien nommer ses calques!
    - icone "oeil" à gauche de chaque calque: visibilité du calque
    - à droite de chaque calque:
        - icone "ampoule": dés/activer l'ionion skin (aussi appelé "table lumineuse")
        - icone "verrou": rendre le calque non sélectionnable et non modifiable (temporairement)
        - icone "alpha": option "inherit alpha"; ne seront visibles que les pixels à l'emplacement desquels il y a un pixel opaque sur un calque plus bas (en tenant compte des groupes de calques)
        - icone "quadrillage/transparence": option "lock alpha": quand on dessine sur ce calque, on ne change que la couleur des pixels, ils gardent leur transparence (du coup sur un pixel transparent on ne voit pas de changement)
    - *ctrl G*: faire un groupe de calques avec tous les calques sélectionnés
        - pratique pour l'organisation
    - tout en haut (là où il y a écrit "Normal" sur le screenshot), changer le mode du calque actif
    - juste en dessous, changer l'opacité du calque
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

## 2a) notions de game design
- si jeu de plateforme/énigmes avec plusieurs niveaux: introduire une seule mécanique de jeu à la fois (cf III.x)
- lisibilité (cf II.2)
- vitesse de réaction du jeu: éviter les animations longues en début d'action (cf V.1)
- de l'importance du son (cf IV.1)
- de l'importance des retours visuels (feedback) (cf V.1)
- essayer d'avoir une unité graphique
    - et une unité entre le graphique, l'audio, l'histoire et le gameplay
    - ou au contraire qu'ils soient opposés, pour un effet de malaise bizarre
        - cf Happy Tree Friends, [Limbo](/assets/995_limbo.jpg) par Playdead: [https://playdead.com/games/limbo/](https://playdead.com/games/limbo/)

## 2b) notions de fabrication de jeu
(ce sont principalement des conseils de game jam, mais ils s'appliquent à votre cas aussi)
- vous serez en retard sur le planning
    - prévoyez un temps conséquent pour résoudre les bugs.
        - pour trouver les bugs, **faites tester votre jeu** par des amis qui n'ont pas participé à sa création. On ne voit pas facilement ses propres bugs parce qu'on sait comment le jeu doit marcher alors on ne fait rien d'inattendu.
            - demandez aussi à vos testeurs si les tutos et le but du jeu sont clairs.
    - faites un jeu modulaire
        - globalement identifiez ce qui est essentiel et commencez par là, et faites le cool mais optionel en dernier.
            - beaucoup plus de choses sont optionnelles qu'on ne croit.
        - pour les jeux où les mécaniques de jeu sont importantes: isolez le centre, la partie la plus importante du jeu, et commencez par là. Une fois que ça marche bien, vous pouvez en ajouter une autre. Une fois qu'elle marche bien et se mèle bien à l'autre, ajoutez-en une troisième.
        - pour les jeux où il y a de la narration: faites le début. Faites la fin. Puis faites le milieu. Comme ça si vous n'avez pas eu le temps de faire le milieu on ne s'en rendra pas compte.
        - pour les jeux où les graphismes sont importants: faites des placeholders qui vous satisfont mais ne sont pas parfaits, et sachez que vous pourrez les retravailler après.
    - d'expérience: si vous vous dites: après le rendu je finirai / polirai / ajouterai ce truc cool, il y a 96,8% de chances que vous ne le fassiez pas.
- FAITES TESTER VOTRE JEU
    - c'est important
- la présence de son a une importance disproportionnée: si vous passez une heure à faire un son basique, ça aura à peu près autant d'impact que si vous passiez vingt heures à fignoler les assets graphiques.
- éventuellement: faites un niveau de test, juste pour vous, avec les différentes parties du jeu toutes ensembles, histoire si vous devez tester un boss de ne pas avoir à rejouer tout le jeu.
    - alternativement ou en plus: des cheat keys.
        - Par exemple, pour un rpg, appuyer sur 'A' change le booléen "a fini la mission 1" à vrai.
        - ou des raccourcis vers de niveaux.

## 3a) Licences
- /!\ Toujours vérifier la licence des assets qu'on utilise.
    - [licences Creative Commons](https://creativecommons.fr/licences/#toc-les-licences-) (en 3ème année 2nd semestre vous avez un cours de "droit, éthique, informatique")
        - **CC-0**: on cède tous les droits cédables: permet de faire à peu près tout (sauf prétendre qu'on l'a fait soi-même: c'est le droit moral, qui est inaliénable en loi française; et sauf dire que l'auteur soutient l'utilisation qu'on en fait)
        - **CC-BY**: il faut [citer le nom de l'auteur, le titre de l'oeuvre, sa licence originale, et des liens vers chaque (par exemple dans l'écran de crédits du jeu vidéo, et un fichier texte avec les crédits et des hyperlinks)](https://creativecommons.org/use-remix/attribution/)
        - **CC-BY-SA-NC**: il faut citer l'auteur, l'oeuvre, la licence (BY: by), l'oeuvre dérivée doit avoir la même licence (SA: share alike), et on ne peut pas l'utiliser commercialement (NC: non commercial)
        - **CC-BY-ND**: a priori, ne pas l'utiliser pour un jeu: il faut citer l'auteur, l'oeuvre, la licence (BY: by), et on ne peut pas en diffuser d'adaptation (ND: non derivative; l'utilisation de sprites ou le montage d'audio pour un jeu compte très probablement comme "derivative")
        - si vous n'êtes pas sûr de la licence ou de si vous pouvez l'utiliser, et que vous pouvez contacter l'auteur, faites-le, très souvent il vous donnera la permission d'utiliser ses assets

## 3b) Ressources externes
-/!\ Toujours vérifier la licence des assets qu'on utilise! cf Annexes X.3a, une explication des principales licences libres utilisées pour les assets
- ressources graphiques
    - https://opengameart.org/ (assets graphiques et sonores CC)
    - https://www.dafont.com (polices de caractères avec filtre par licence)
    - https://itch.io/game-assets/assets-cc0/tag-pixel-art : assets de pixel art CC0
    - https://kenney.nl/assets (assets graphiques et audio CC-0)
- ressources audio
    - sons
        - https://freesfx.co.uk/Default.aspx : un site de sons (gratuit avec attribution au site (une attribution globale suffit, pas forcément une par son))
        - https://freesound.org/ : un site de sons CC (licences différentes par son)
        - https://www.bfxr.net/ : un outil open source de génération de sons. Nécessite flash.
        - https://kenney.nl/assets?q=audio (assets graphiques et audio CC-0)
    - musique
        - https://www.hongkiat.com/blog/creative-common-music-download/ (liste de sites de musique libre)
        - https://audionautix.com/ (site de musiques CC-BY)
        - https://freemusicarchive.org/ (site de musiques CC)
        - https://filmmusic.io/search (site de musiques principalement CC BY)
        - liens: https://incompetech.com/music/royalty-free/faq.html (site de musiques gratuites avec attribution)
        - https://musescore.org/en/handbook/soundfonts-and-sfz-files (lien vers des soundfonts (polices de son: fichiers qui traduisent un fichier .midi en du beau son))

## 4) game jams
- une game jam c'est, en gros, faire un jeu en (souvent) 48h, seul ou en groupe, avec d'autres gens qui font la même chose en même temps (proche des jams d'improvisation musicale et des hackatons)
    - ludum dare: deux fois par an (avril et octobre), probablement la jam la plus connue: ldjam.com
    - global game jam: une fois par an (en janvier), probablement la jam physique la plus connue: ggj.com
	- un agenda des jams en cours et à venir, sur un site où on peut publier ses jeux: https://itch.io/jams

## 5) jeux cool
J'ai noté en italique les jeux de jam, donc faits dans un temps très limité et nécessairement plus simples et courts que les autres.  
Les jeux avec un + devant sont gratuits ou ont une démo gratuite.
Les catégories sont assez floues, la plupart des jeux entrent dans plusieurs à la fois.  
- en pixel art
	- [Fez](http://fezgame.com/): puzzle <details> ![fez](/assets/110_fez.png)
	- + [*bonsai*](https://ldjam.com/events/ludum-dare/46/bonsai): un jeu de création de bonsais
    - [The Ur-Quan Masters](http://sc2.sourceforge.net/): exploration spatiale <details> ![uqm](/assets/994_uqm.png)

- style graphique simple mais qui marche
	- + [thomas was alone](http://www.thomaswasalone.com/thomaswasalone/): platformer
		- graphisme simple mais:
		- textures et lumières
		- voix des personnages
	- [*you must gather your party before venturing forth*](https://ldjam.com/events/ludum-dare/46/ymgypbvf-you-must-gather-your-party-before-venturing-forth): puzzle
		- très stylisé
		- mais les informations importantes sont facilement lisibles (la race des persos, qui influence le gameplay) <details> ![ymgypbvf](/assets/998_ymgypbvf.png)
	- [Selfless Heroes](https://selflessheroes.fr/): intro à la programmation
		- très stylisé
		- mais les informations importantes sont facilement lisibles
			- les persos sont des chevaliers
			- chacun est un personnage différent
			- la différence entre chaque type de tile est claire
		- et pour éviter la monotonie visuelle, il y a plusieurs types de chaque tile <details> ![selfless heroes](/assets/003_selflessHeroes.png)
	- [Mini Metro](https://dinopoloclub.com/games/mini-metro/), par Dino Polo Club: un jeu de gestion de métros
	    - utilise des symboles plutôt que des illustrations <details> ![mini-metro](/assets/997_minimetro.jpg)
	- [*Gophers*](https://hyperlinkyourheart.itch.io/gophers)(/assets/105_gophers.png): narration
		- les palettes de couleurs limitées, utilisées à bon escient, marchent souvent bien
		- un travail sur l'atmosphère (accord graphisme-son-histoire-gameplay) <details> ![*Gophers*](/assets/105_gophers.png)
	- [Night in the Woods](http://www.nightinthewoods.com/) par Infinite Fall: narration
	    - très chouette style graphique
	        - soutenu/contrasté par la musique et l'histoire
	    - mais composé quasi exclusivement de formes simples
	    - simplification et stylisation des textures <details> ![night in the woods](/assets/996_nightInTheWoods.png)
	- [capsule](https://finji.itch.io/capsule) par Finji [](__TODO__)

- mécanique de jeu inhabituelle
	- pikuniku?
	- *rangement d'inventaire*(https://globalgamejam.org/2020/games/apothe-care-9)
	- world of goo?

## 6) Vocabulaire
- **tile**: une image (en général un fragment de décor) utilisée pour composer une image plus grande (un niveau entier) avec d'autres tiles, espacées régulièrement; elle sera typiquement réutilisée de nombreuses fois dans le même niveau.
    - un ensemble de tiles est un **tileset**
    - un niveau composé de tiles est une **tilemap**; on utilise parfois "tilemap" pour dire "ensemble de tiles"
- **asset**: un élément composant le jeu. Dans sa définition la plus étroite, se réfère uniquement aux assets graphiques (les tiles, les personnages, etc.), mais souvent aussi aux assets sonores, et parfois inclue des scripts.
- **palette**: un ensemble de couleurs qu'on utilise dans l'image (et on n'en utilise aucune autre). Les palettes de pixel art sont souvent assez réduites.
- **prop**: littéralement, "accessoire"; un objet composant de décor, souvent avec lequel le personnage peut interagir
- termes spécifiques au pixel art, en anglais:
    - **jaggies**: des sortes d'accrocs créés par une courbe irrégulière ou une ligne à la largeur illogiquement irrégulière
    - **hue shifting**: le fait de changer la teinte d'une couleur en fonction de sa clarté au lieu de la rendre uniquement plus claire ou plus sombre
    - **orphan pixel**: un pixel tout seul, non relié à d'autres de la même couleur.
- **frame**:
    - soit une image d'une animation, en tant que plus petit élément de temps disponible
    - soit une image de l'animation dessinée par un être humain.
        - cf la différence entre le "frame rate" (plus petit élément de temps) et "new frame" (image dessinée)
    - **keyframe**: image clé; peut signifier
        - soit une image d'une animation sur laquelle on a effectué des changements (ce qui correspond à la deuxième définition de "frame")
        - soit une image importante pour le mouvement, les autres (**inbetweens** ou **tweens** ou **intervalles**) n'étant qu'une étape intermédiaire directement entre deux images clés.

{% endcomment %}
