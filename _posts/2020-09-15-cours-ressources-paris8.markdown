---
layout: default
title:  "Cours Paris 8: Création et Gestion de ressources"
date:   2020-09-15 19:05:09 +0200
categories: classes, krita, 2D, fr
permalink: /cours/creation_gestion_ressources.html
---

L'adresse de ce cours: 
https://falano.github.io/cours/creation_gestion_ressources.html

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
{% comment %}
TODO: check all translations of tool names!
!! ne pas oublier de faire un récap en début de cours

# I. [Introduction](/cours/creation_gestion_ressources_1.html)
## 1) présentation du cours

- pixel art avec krita
    - personnages
    - animation
    - décors
        - peints
        - assemblés avec une tilemap [(exemple de tilemap dans Godot)](/assets/002_tilemap.png)
- son avec audacity (qui a des écouteurs?)
    - logiciel d'écriture musicale?
- gestion de ressources
- projet final (platformer? jeu narratif? énigmes? puzzle? stratégie? contemplatif? tower defense? etc.)

## 2) présentation du pixel art
pourquoi krita: autres logiciels (gimp, etc.)  
pourquoi le pixel art: relativement simple (cf [Selfless Heroes](/assets/003_selflessHeroes.png), assez répandu, ne nécessite pas forcément de tablette graphique ni de savoir dessiner  
présentation et historique du pixel art:  
- absence d'[antialiasing/anticrénelage](/assets/000_anti-aliasing.png) automatique (-> options des outils)
- racines du pixel art dans des contraintes techniques (cf [pokemon red](/assets/100_pokemon.jpg), [mario](/assets/101_mario.jpg), la [palette de couleurs](/assets/102_nes_palette.jpg) de la console nes, [final fantasy 6](/assets/103_ff6.jpg))
    - nombre de pixels limité
    - nombre de couleurs limité (cf [dithering](/assets/001_dithering.png))
    - utilisation de tilemaps
- pixel art actuel
    - nostalgie et aspect rétro ou préférence graphique (cf [A short Hike](/assets/113_aShortHike.png), [owlboy](/assets/107_owlboy_gd.png), [celeste](/assets/109_celeste.png))
    - utilisation pour la vitesse/facilité d'exécution
        - jeux de game jam ([gophers](/assets/105_gophers.png), [roguelight](/assets/106_roguelight.png); cf [Annexes X.4](/cours/creation_gestion_ressources_0.html))
        - jeux indé ([hyperlight drifter](/assets/108_hyperLightDrifter.png))
    - utilisation mixte avec des technologies récentes ([fez](/assets/110_fez.png), [dead cells](/assets/111_Dead-Cells.jpg), [the last night](/assets/112_TheLastNight.jpg))
- utilisation hors jeux (illustration ([exemple 1](/assets/114_jindrich-stejskal.gif), [exemple 2](/assets/115_jubilee.png)))

**références**  
Selfless Heroes, par Félicien Brochu: [https://selflessheroes.fr/](https://selflessheroes.fr/)  
Pokemon Version Rouge Feu, par Nintendo  
Super Mario Bros, par Nintendo  
Final Fantasy 6, par Square Enix  
A Short Hike, par Adam Robinson-Yu: [http://ashorthike.com/](http://ashorthike.com/)  
Owlboy, par D-Pad Studio: [http://www.owlboygame.com/](http://www.owlboygame.com/)  
Celeste, par Matt Makes Games: [http://www.celestegame.com/](http://www.celestegame.com/)  
Gophers, par Hyperlink Your Heart: [https://hyperlinkyourheart.itch.io/gophers](https://hyperlinkyourheart.itch.io/gophers)  
Roguelight, par Daniel Linssen: [https://managore.itch.io/roguelight](https://managore.itch.io/roguelight)  
Hyperlight Drifter, par Heart Machine: [https://heartmachine.com/hyper-light](https://heartmachine.com/hyper-light)  
Fez, par Polytron: [http://fezgame.com/](http://fezgame.com/)  
Dead Cells, par Motion Twin: [https://dead-cells.com/](https://dead-cells.com/)  
The Last Night, par Odd Tales: [http://oddtales.net/](http://oddtales.net/)  
The World is Leaking, par Jindrich Stejskal: [https://www.artstation.com/artwork/QzA3D4](https://www.artstation.com/artwork/QzA3D4)  
Summer's Passing, par Jubilee Payne: [https://www.artstation.com/artwork/w8eebY](https://www.artstation.com/artwork/w8eebY)  
game jams: cf [Annexes X.4](/cours/creation_gestion_ressources_0.html)

## 3) considérations générales
- de l'importance de savoir chercher sur internet
- penser à utiliser des références pour dessiner (cf [dessin médiéval d'éléphant](/assets/200_elephant.jpg))
- l'anglais c'est pratique, la majorité de la doc est en anglais

**références**  
un manuscrit du 13ème siècle: https://www.bl.uk/manuscripts/FullDisplay.aspx?ref=Royal_MS_12_f_xiii page f.11v

## 4) jeux cools sans savoir dessiner
cf [Annexes X.5](/cours/creation_gestion_ressources_0.html)
- video de gameplay (et, avant la minute donnée dans le lien, timelapse de dessin des assets) de gophers: [https://youtu.be/0jPLMCfSE0w?t=348](https://youtu.be/0jPLMCfSE0w?t=348)
- 
TODO: vids de pxart simple (gophers et autre ), ou de trailers de jeux simples et cools.

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

-- fin lundi matin 1 (plus un peu de krita2) --

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

-- fin lundi aprèm 1 moins lisibilité plus formats--
-- fin mercredi aprèm 1 + gestion ressources + formats - lisibilité --

--  
**EXERCICE 3**  
faire des variantes d'ennemis ou de pnj avec des calques sur la même base (vêtements ou objets additionnels ou attaques feu/eau ou etc.)  
--> pour se familiariser avec les calques  
--  

-- fin lundi matin 2 moins lisi fond/fond, plus formats --

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

-- fin mercr aprèm 2 moins lisi fond --

# III. Décors
## 1) Tiles
- doivent s'emboîter sans que ça se voie
	- pour les décors naturels: avoir plusieurs variantes excentrées
- perspective au choix
    - vu de haut (jrpgs) (cf: [chrono trigger](/assets/501_chronoTrigger.png))
    - vu de côté (platformers) (TODO: illo: SuperMeatBoy!!)
    - vue isométrique (stratégie); supporté par Godot  (TODO: quels angles en general?) TODO: illo
    - vue de haut non-carrée (type jeu de plateau) (TODO: illo wesnoth)

## 2) Krita: 4
- grilles
    - grilles isométriques
- wrap around mode
- mirror tools
- remplir une zone d'une tile répétée: select tile > pattern icon (entre les couleurs et le bouton d'annulation) > use as pattern > sélectionner la zone > fill tool > use pattern

--
**EXERCICE 5**
faire une tilemap, et la monter soit sur krita soit sur godot
-> pour apprendre à faire des tilemaps
--

## 3) Décor plein
- rappel: lisibilité (perso/fond, plateformes, fond/fond)
- perspective atmosphérique (TODO: illo)
- parallaxe (TODO: illo vid?)
- lumière
	- comme unificateur (une seule source de lumière)
	- comme évidenciateur (les endroits importants et interactifs sont dans la lumière)
- règle des tiers?

## 4) Krita: 5
- outils perspective
    - règle parallèle / parallel ruler
    - concentric ellipse
    - vanishing point? pers?
- outils forme (*shift* pour conserver la proportion 1/1)
- gomme lasso

# IV. Son
## 1) intro
- de l'importance du son
- effets sonores / musique
- (enregistrer / télécharger)->(modifier) / produire numériquement
    - les écouteurs-enregistreurs ont trois bandes sur le port jack, les non-enregistreurs n'en ont que deux

## 2) licences
/!\ Toujours vérifier la licence des assets qu'on utilise.
cf [Annexes X.2](/cours/creation_gestion_ressources_0.html)

## 3) Audacity
- audacity
    - pour enregistrer
    - pour modifier/monter
        - changer le volume
        - enlever les bruits de fond parasites
        - sélectionner une partie spécifique du clip audio

## 4) musique
- enregistrer sa musique: -> enregistreur + audacity
- générer sa propre musique (en 2ème année 2ème semestre il y a un cours de "synthèse d'images, animation et sons")
    - avec un logiciel d'écritures de partitions qui exporte en MIDI (TODO: y a pas une étape supplémentaire pour mettre du beau son sur le midi?)
        - musescore
        - lilypond
    - avec un logiciel de création de musique
        - https://beepbox.co/ (musique bitbox, simple d'utilisation)
        - LMMS? (TODO: )
        - Yoshimi? (TODO: )
- télécharger une musique sous licence libre

# V. Animation
## 1) principes d'animation
- savoir d'où tu viens où tu vas
- anticipation - action - réaction: diminuer l'anticipation pour augmenter la réactivité (cf __lien joueur du grenier__)
- de l'importance de l'anim de "personnage blessé" (cf __faire un exemple hurtanim avec/sans__)
- anim vague/fumée/vent/queue
- squash and stretch, déformations (__lien ou images/vid de bugsBunny__)
- anim de marche

**références**
anim bugsBunny
quelques principes généraux d'animation: https://www.youtube.com/watch?v=uDqjIdI4bF4

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

à venir

# VI. UI
https://docs.godotengine.org/en/3.0/classes/class_ninepatchrect.html

à venir

# X. Annexes
## 1) schéma de l'interface de Krita
[Image](/assets/999_interfaceKrita.png) (à ouvrir dans une nouvelle fenêtre pour la voir à côté de la légende ci-dessous)
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
    - !!!!!!! more layers stuff!!!!!!!!!!!!
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

## 2) notions de game design:
- si jeu de plateforme/énigmes avec plusieurs niveaux: introduire une seule mécanique de jeu à la fois (cf III.x)
- lisibilité (cf II.2)
- vitesse de réaction du jeu: éviter les animations longues en début d'action (cf V.1)
- de l'importance du son (cf IV.1)
- de l'importance des retours visuels (feedback) (cf V.1)

## 3) Ressources externes
-/!\ Toujours vérifier la licence des assets qu'on utilise.
    - [licences Creative Commons](https://creativecommons.fr/licences/#toc-les-licences-) (en 3ème année 2nd semestre vous avez un cours de "droit, éthique, informatique")
        - CC-0: on cède tous les droits cédables: permet de faire à peu près tout (sauf prétendre qu'on l'a fait soi-même: c'est le droit moral, qui est inaliénable en loi française; et sauf dire que l'auteur soutient l'utilisation qu'on en fait)
        - CC-BY: il faut [citer le nom de l'auteur, le titre de l'oeuvre, sa licence originale, et des liens vers chaque (par exemple dans l'écran de crédits du jeu vidéo, et un fichier texte avec les crédits et des hyperlinks)](https://creativecommons.org/use-remix/attribution/)
        - CC-BY-SA-NC: il faut citer l'auteur, l'oeuvre, la licence (BY: by), l'oeuvre dérivée doit avoir la même licence (SA: share alike), et on ne peut pas l'utiliser commercialement (NC: non commercial)
        - CC-BY-ND: a priori, ne pas l'utiliser pour un jeu: il faut citer l'auteur, l'oeuvre, la licence (BY: by), et on ne peut pas en diffuser d'adaptation (ND: non derivative; l'utilisation de sprites ou le montage d'audio pour un jeu compte très probablement comme "derivative")
        - si vous n'êtes pas sûr de la licence ou de si vous pouvez l'utiliser, et que vous pouvez contacter l'auteur, faites-le, très souvent il vous donnera la permission d'utiliser ses assets
- ressources graphiques
    - https://opengameart.org/ (assets graphiques et sonores CC)
    - https://www.dafont.com (polices de caractères avec filtre par licence)
    - https://itch.io/game-assets/assets-cc0/tag-pixel-art : assets de pixel art CC0
- ressources audio
    - sons
        - https://freesfx.co.uk/Default.aspx : un site de sons (gratuit avec attribution au site (une attribution globale suffit, pas forcément une par son))
        - https://freesound.org/ : un site de sons CC (licences différentes par son)
        - https://www.bfxr.net/ : un outil open source de génération de sons. Nécessite flash.
    - musique
        - https://www.hongkiat.com/blog/creative-common-music-download/ (liste de sites de musique libre)
        - https://audionautix.com/ (site de musiques CC-BY)
        - https://freemusicarchive.org/ (site de musiques CC)
        - https://filmmusic.io/search (site de musiques principalement CC BY)
        - liens: https://incompetech.com/music/royalty-free/faq.html (site de musiques gratuites avec attribution)

## 4) game jams
- une game jam c'est, en gros, faire un jeu en (souvent) 48h, seul ou en groupe, avec d'autres gens qui font la même chose en même temps (proche des jams d'improvisation musicale et des hackatons)
    - ludum dare: deux fois par an (avril et octobre), probablement la jam la plus connue: ldjam.com
    - global game jam: une fois par an (en janvier), probablement la jam physique la plus connue: ggj.com
	- un agenda des jams en cours et à venir, sur un site où on peut publier ses jeux: https://itch.io/jams

## 5) jeux cool
J'ai noté en italique les jeux de jam, donc faits dans un temps très limité et nécessairement plus simples et courts que les autres.  
Les catégories sont assez floues, la plupart des jeux entrent dans plusieurs à la fois.  
- en pixel art
	- fez (puzzle)
	- *bonsai* (un jeu de création de bonsais) : [https://ldjam.com/events/ludum-dare/46/bonsai](https://ldjam.com/events/ludum-dare/46/bonsai)
- style graphique simple mais qui marche
	- thomas was alone (platformer)
		- graphisme simple mais:
		- textures et lumières
		- voix des personnages
	- [*you must gather your party before venturing forth*](/assets/998_ymgypbvf.png)  (puzzle) : [https://ldjam.com/events/ludum-dare/46/ymgypbvf-you-must-gather-your-party-before-venturing-forth](https://ldjam.com/events/ludum-dare/46/ymgypbvf-you-must-gather-your-party-before-venturing-forth)
		- très stylisé
		- mais les informations importantes sont facilement lisibles (la race des persos, qui influence le gameplay)
	- selfless heroes
		- très stylisé
		- mais les informations importantes sont facilement lisibles
			- les persos sont des chevaliers
			- chacun est un personnage différent
			- la différence entre chaque type de tile est claire
		- et pour éviter la monotonie visuelle, il y a plusieurs types de chaque tile
	- le jeu du métro
	- *gophers*
		- les palettes de couleurs limitées, utilisées à bon escient, marchent souvent bien
		- un travail sur l'atmosphère (accord graphisme-son-histoire-gameplay)
	- night wood thingie (test graphic style though)
- mécanique de jeu inhabituelle
	- pikuniku?
	- rangement d'inventaire

check: brandon james greer

{% endcomment %}
