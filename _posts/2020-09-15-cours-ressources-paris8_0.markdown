---
layout: default
title:  "Cours Paris 8: Création et Gestion de ressources"
date:   2020-09-15 19:05:09 +0200
categories: classes, krita, 2D, fr
permalink: /cours/creation_gestion_ressources_0.html
---

# O. [Menu](/cours/creation_gestion_ressources.html)
# I. [Introduction](/cours/creation_gestion_ressources_1.html)
# II. [Krita](/cours/creation_gestion_ressources_2.html)
# III. [Décors](/cours/creation_gestion_ressources_3.html)
# IV. [Son](/cours/creation_gestion_ressources_4.html)
# V. [Animation](/cours/creation_gestion_ressources_5.html)
# VI. [Finitions](/cours/creation_gestion_ressources_6.html)
# VII. [Exports](/cours/creation_gestion_ressources_7.html)
# VIII. [Game Design](/cours/creation_gestion_ressources_8.html)
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
    - Onion Skins / pelure d'oignon: permet de voir en transparence les images précédentes et suivantes de l'animation (activable/désactivable par calque dans la timeline, ou pour tous les calques en cliquant sur le 0 dans le docker Peau d'Oignon);
    - Animation:
        - Lancer/Pauser l'animation,
        - Images de début et de fin (Start et End),
        - nombre d'images par seconde (Frame Rate / Fréquence d'images) (24 pour les mouvements rapides (le nombre d'images du cinéma en Europe), 12 c'est bien, 6 c'est possible mais limite);
        - Timeline / Timing: là où se passe le gros de l'animation, où on passe d'une image à l'autre, et peut déplacer des images

## 2) Licences
- /!\ Toujours vérifier la licence des assets qu'on utilise.
    - domaine public
    - [licences Creative Commons](https://creativecommons.fr/licences/#toc-les-licences-) (en 3ème année 2nd semestre vous avez un cours de "droit, éthique, informatique")
        - **CC-0**: on cède tous les droits cédables: permet de faire à peu près tout (sauf prétendre qu'on l'a fait soi-même: c'est le droit moral, qui est inaliénable en loi française; et sauf dire que l'auteur soutient l'utilisation qu'on en fait)
        - **CC-BY**: il faut [citer le nom de l'auteur, le titre de l'oeuvre, sa licence originale, et des liens vers chaque (par exemple dans l'écran de crédits du jeu vidéo, et un fichier texte avec les crédits et des hyperlinks)](https://creativecommons.org/use-remix/attribution/)
        - **CC-BY-SA-NC**: il faut citer l'auteur, l'oeuvre, la licence (BY: by), l'oeuvre dérivée doit avoir la même licence (SA: share alike), et on ne peut pas l'utiliser commercialement (NC: non commercial)
        - **CC-BY-ND**: a priori, ne pas l'utiliser pour un jeu: il faut citer l'auteur, l'oeuvre, la licence (BY: by), et on ne peut pas en diffuser d'adaptation (ND: non derivative; l'utilisation de sprites ou le montage d'audio pour un jeu compte très probablement comme "derivative")
        - si vous n'êtes pas sûr de la licence ou de si vous pouvez l'utiliser, et que vous pouvez contacter l'auteur, faites-le, très souvent il vous donnera la permission d'utiliser ses assets
- pour votre jeu, vous pouvez utiliser la licence que vous voulez (qu'elle soit ou non creative commons); parfois les gens ont une licence pour le code et une autre pour les assets graphiques et audio (par exemple MIT pour le code et CC-BY pour les assets).
    - /!\ SAUF SI vous avez utilisé des assets CC-SA (CC-BY-SA, CC-BY-SA-NC, etc.), dans ce cas vous êtes obligés de réutiliser la même licence qu'eux.

## 3) Ressources externes
-/!\ Toujours vérifier la licence des assets qu'on utilise! cf Annexes X.2, une explication des principales licences libres utilisées pour les assets
- ressources graphiques
    - persos, décors et UI
        - <https://opengameart.org/> (assets graphiques et sonores CC)
        - <https://itch.io/game-assets/assets-cc0/tag-pixel-art> : assets de pixel art CC0
        - <https://kenney.nl/assets> (assets graphiques et audio CC-0)
        - <https://www.procjam.sekritforum.com/art/> (assets graphiques CC-BY-NC)
    - polices de caractères
        - <https://www.dafont.com>
        - <https://www.fontspace.com/>
        - <https://www.fontsquirrel.com>
        - et plein d'autres
- ressources audio
    - sons
        - <https://freesfx.co.uk/Default.aspx> : un site de sons (gratuit avec attribution au site (une attribution globale suffit, pas forcément une par son))
        - <https://freesound.org/> : un site de sons CC (licences différentes par son)
        - <https://www.bfxr.net/> : un outil open source de génération de sons. Nécessite flash.
        - <https://kenney.nl/assets?q=audio> (assets graphiques et audio CC-0)
        - <https://sonniss.com/gameaudiogdc18/> et <https://sonniss.com/gameaudiogdc2017/> et <https://sonniss.com/gameaudiogdc2016/>: entre 10 et 30 Gb chaque de sons .wav gratuits et utilisables commercialement sans attribution
    - musique
        - <https://www.hongkiat.com/blog/creative-common-music-download/> (liste de sites de musique libre)
        - <https://audionautix.com/> (site de musiques CC-BY)
        - <https://freemusicarchive.org/> (site de musiques CC)
        - <https://filmmusic.io/search> (site de musiques principalement CC BY)
        - liens: <https://incompetech.com/music/royalty-free/faq.html> (site de musiques gratuites avec attribution)
        - <https://musescore.org/en/handbook/soundfonts-and-sfz-files> (lien vers des soundfonts (polices de son: fichiers qui traduisent un fichier .midi en du beau son))

## 4) game jams
- une game jam c'est, en gros, faire un jeu en (souvent) 48h, seul ou en groupe, avec d'autres gens qui font la même chose en même temps (proche des jams d'improvisation musicale et des hackatons)
    - ludum dare: deux fois par an (avril et octobre), probablement la jam la plus connue: <https://ldjam.com/>
    - global game jam: une fois par an (en janvier), probablement la jam physique la plus connue: <https://globalgamejam.org/>
	- un agenda des jams en cours et à venir, sur un site où on peut publier ses jeux: <https://itch.io/jams>
	- une jam fondée en france qui a lieu trois fois par an: https://alakajam.com/article/about/welcome

## 5) jeux cool
J'ai noté en italique les jeux de jam, donc faits dans un temps très limité et nécessairement plus simples et courts que les autres.  
Les jeux avec un /+ devant sont gratuits ou ont une démo gratuite (tous les jeux de jam sont gratuits).
Les catégories sont assez floues, la plupart des jeux entrent dans plusieurs à la fois.  
- en pixel art
	- [Fez](http://fezgame.com/): puzzle <details> ![fez](/assets/110_fez.png)
	- /+ [*bonsai*](https://ldjam.com/events/ludum-dare/46/bonsai): un jeu de création de bonsais
    - /+ [The Ur-Quan Masters](http://sc2.sourceforge.net/): exploration spatiale <details> ![uqm](/assets/994_uqm.png)
    - /+ [Roguelight](https://managore.itch.io/roguelight): un roguelike où la seule source de lumière sont les flèches enflammées qu'on tire <details> ![roguelight](/assets/106_roguelight.png)

- style graphique simple mais qui marche
	- /+ [thomas was alone](http://www.thomaswasalone.com/thomaswasalone/): platformer
		- graphisme simple mais:
		- textures et lumières
		- voix des personnages
	- /+ [*you must gather your party before venturing forth*](https://ldjam.com/events/ludum-dare/46/ymgypbvf-you-must-gather-your-party-before-venturing-forth): puzzle
		- très stylisé
		- mais les informations importantes sont facilement lisibles (la race des persos, qui influence le gameplay) <details> ![ymgypbvf](/assets/998_ymgypbvf.png)
	- /+ [Selfless Heroes](https://selflessheroes.fr/): intro à la programmation
		- très stylisé
		- mais les informations importantes sont facilement lisibles
			- les persos sont des chevaliers
			- chacun est un personnage différent
			- la différence entre chaque type de tile est claire
		- et pour éviter la monotonie visuelle, il y a plusieurs types de chaque tile <details> ![selfless heroes](/assets/003_selflessHeroes.png)
	- /+ [Mini Metro](https://dinopoloclub.com/games/mini-metro/), par Dino Polo Club: un jeu de gestion de métros
	    - utilise des symboles plutôt que des illustrations <details> ![mini-metro](/assets/997_minimetro.jpg)
	- /+ [*Gophers*](https://hyperlinkyourheart.itch.io/gophers)(/assets/105_gophers.png): narration
		- les palettes de couleurs limitées, utilisées à bon escient, marchent souvent bien
		- un travail sur l'atmosphère (accord graphisme-son-histoire-gameplay) <details> ![*Gophers*](/assets/105_gophers.png)
	- [Night in the Woods](http://www.nightinthewoods.com/) par Infinite Fall: narration
	    - très chouette style graphique
	        - soutenu/contrasté par la musique et l'histoire
	    - mais composé quasi exclusivement de formes simples
	    - simplification et stylisation des textures <details> ![night in the woods](/assets/996_nightInTheWoods.png)
	- /+ [capsule](https://finji.itch.io/capsule) par Finji [](__TODO__)

- mécanique de jeu inhabituelle
	- [World of Goo](https://2dboy.com/), par 2DBoy: construction d'échelles et de pyramides avec des blobs de truc gluant
	- [A Blind Legend](http://www.ablindlegend.com/), par Dowino: un jeu d'aventure où l'ouïe est le sens le plus important
	- /+ [The Stanley Parable](https://store.steampowered.com/app/221910/The_Stanley_Parable/), par Davey Wreden: un "jeu narratif expérimental à la première personne"
	- /+ [Dorfromantik](https://twitter.com/_Toukana): jeu de pose de tuile (esthétique jeu de plateau) pour former des motifs/paysages spécifiques <details> ![dorfromantik](/assets/993_dorfromantik.jpg)

- jeux de jam qui n'entrent pas dans les autres catégories
    - [*primed*](https://gimblll.itch.io/primed): un shooter simple qui met en place certains des conseils des deux vidéos sur le "juice"
    - [*around the world*](https://alakajam.com/10th-alakajam/1014/around-the-world/#results): exploration navale et commerce
    - [*hello operator*](https://cloakedninjas.itch.io/hello-operator): connection de téléphones
    - [*abyss meal*](https://kweej.itch.io/abyss-meal): manger des petits poissons sans se faire manger par des grands
    - [*pirate's trial*](https://alakajam.com/10th-alakajam/1006/pirates-trial-a-scavenger-hunt/): chasse au trésor
    - [*pandemia*](https://www.lexaloffle.com/bbs/?tid=31451): pzzle/stratégie


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
    - soit une image de l'animation dessinée/créée directement par un être humain.
        - cf la différence entre le "frame rate" (plus petit élément de temps) et "new frame" (image dessinée)
    - **keyframe**: image clé; peut signifier
        - soit une image d'une animation sur laquelle un humain a effectué des changements (ce qui correspond à la deuxième définition de "frame")
        - soit une image importante pour le mouvement, les autres (**inbetweens** ou **tweens** ou **intervalles**) n'étant qu'une étape intermédiaire entre deux images clés.
- **placeholder**: version temporaire d'un asset qui a pour but d'être remplacée par une meilleure version, à terme, mais qui pour l'instant suffit (par exemple, pour tester la physique du saut du personnage, avant que l'équipe qui s'occupe du graphisme n'ai fini le perso, on peut mettre un carré rouge; c'est un placeholder).

## 7) git lfs
- /!\ git lfs ne marche pas avec github pages
- qu'est-ce que c'est:
    - lfs: "large file system"
    - git lfs permet d'héberger les fichiers lourds dans un endroit à part
        - le repository ne contient que des pointeurs vers les fichiers
        - et il ne les télécharge que quand on en a besoin
        - les "fichiers lourds" contiennent aussi les fichiers binaires (ou graphique ou son), même légers, parce qu'à la longue, vu qu'on doit à chaque fois ré-enregistrer tout le fichier au lieu de juste ce qui a changé, ils finissent par peser lourd dans le repo
        - les "fichiers lourds" contiennent un peu ce qu'on veut, c'est l'utilisateur qui les définit
- installation
    - installer git lfs
        - <https://github.com/git-lfs/git-lfs/releases/tag/v2.12.0>
        - ou git-lfs dans votre gestionnaire de paquets
    - aller dans le dossier du projet versionné
    - > git lfs install
    - > git lfs track "\*.png,\*.jpg"
        - avec la même syntaxe que pour le .gitignore; par exemple:
            - \*.kra : tous les fichiers .kra, où qu'ils soient
            - assets/ : tous les fichiers dans le dossier assets, y compris dans des sous-dossiers
            - anim/\* : tous les fichiers dans le dossier anim (sous-dossiers non inclus)
            - \*\*/test/\*.png : tous les fichiers png dans un dossier "test", où que soit le dossier
            - \*spritesheet\*.png : tous les fichiers png qui contiennent le mot "spritesheet"
            - animation/spritesheet\* : tous les fichiers qui commencent par "spritesheet" dans le dossier animation
        -/!\ ne pas oublier les guillemets ou il suivra tous les .png (par exemple) actuels individuellement
            - au lieu de en général tous les .png toujours
    - > git add .gitattributes
        - le .gitattributes est l'endroit où il a noté les fichiers à suivre
    - > git commit -m "initialize lfs"
        - ou "add .gitattributes"
        - ou ce que vous voulez
            - si vous ne commitez pas le .gitattributes, git lfs ne saura pas, quand il clone le projet chez quelqu'un d'autre, ce qu'il faut suivre
    - et ensuite c'est juste du git normal: git add, git commit, git push, etc.
- utilisations un peu spécifiques
    - > git lfs ls-files
        - afficher la liste des fichiers suivis par lfs
    - > git lfs migrate info --everything --include="\*.jpg,\*.png"
        - afficher une liste des fichiers impliqués par un migrate
        - --everything: sur toutes les branches locales et distantes
        - --include: quels fichiers inclure
    - > git lfs migrate import --no-rewrite -m "Import test.zip, .mp3, .psd files in root of repo" test.zip *.mp3 *.psd
        - changer les fichiers par leur version lfs
        - sans le --no-rewrite, ça le fait rétroactivement dans les anciens commits
            - du coup ça change l'historique et les identifiants des commits
            - ce qui n'est pas trop gênant si on bosse seul
            - mais qui peut foutre la merde dans un repo commun
            - si on n'a pas le --norewrite, les autres doivent re-cloner le projet une fois qu'on a fini
- désinstallation
    - > git lfs uninstall
    - enlever du .gitattributes tous les trucs lfs
        - ou supprimer le .gitattributes si il ne contient que des trucs lfs
    - > git lfs migrate export --everything --include .
        - changer tous les fichiers lfs par leur version non-lfs
            - par contre ça le fait rétroactivement dans les anciens commits
                - du coup ça change l'historique et les identifiants des commits
                - ce qui n'est pas trop gênant si on bosse seul
                - mais qui peut foutre la merde dans un repo commun
                - donc bien prévenir tout le monde qu'on va faire ça, et quand,
                - qu'ils se soient organisés et aient mergé ce qui doit être mergé
                - et qu'ils re-clonent le projet quand on a fini
    - et pour complètement enlever les fichiers lfs du repo distant qui hébergeait les version lourdes, il faut supprimer et refaire le repo
- doc
    - documentation officielle <https://github.com/git-lfs/git-lfs/tree/master/docs/man> (en)
    - un article plus lisible <https://www.atlassian.com/fr/git/tutorials/git-lfs>
    - un article court et encore plus lisible <https://dzone.com/articles/git-lfs-why-and-how-to-use> (en)

## 8) Règles du rendu
- à propos des projets:
    - les projets peuvent se faire soit en groupe soit seul;
    - si vous voulez utiliser un autre logiciel que ceux montrés en cours, demandez-moi; a priori s'il est open source et que j'ai l'impression qu'il fera le boulot je dirai oui (gimp, libresprite, etc.), s'il est propriétaire non (photoshop, sai, etc.).
- à propos des personnages:
    - ils doivent faire au max 64x64 pixels
    - les fanarts sont autorisés, mais il est obligatoire de préciser dans l'écran des 'credits' (là où vous écrivez le nom de tous les participants au jeu) de quel perso et quel oeuvre c'est tiré (et si après le cours vous vous rendez compte que votre idée de jeu est géniale et que vous allez le publier sur steam/gog/epic/itch et gagner des fortunes, je vous conseille de changer le design du perso)
- à propos de l'audio:
    - vous pouvez utiliser des sons et des musiques disponibles en ligne tant que leur licence l'autorise et que vous les mentionnez comme il faut dans les crédits (mais si le son/la musique vous intéresse, je vous encourage à les faire vous-même, ça sera pris en compte)
- à propos des décors:
    - il est conseillé (c'est beaucoup plus simple pour le level design) de faire des tilemaps, mais ce n'est pas obligatoire.
    - tiles ou pas, ça doit être du pixel art (dessiné avec une brosse dure).
    - un décor non-constitué de tiles peut faire max 640x360
- la date de rendu du projet est le lundi 4 janvier, à 7h du matin au plus tard
- à rendre dans le rendu:
    - l'exécutable du jeu
    - le projet godot
    - vos fichiers source (.kra, .aup, lien beepbox, etc.) finaux ainsi que plusieurs versions intermédiaires
    - les fichiers des ressources externes que vous avez utilisées (n'oubliez pas aussi qu'il est obligatoire de les attribuer (dire "musique: 'Jazzy', de Kevin McLeod, lien-vers-son-site, CC-BY" par exemple) dans l'écran des crédits, et/ou dans un fichier texte joint à l'exécutable s'il y en a trop)
    - vous pouvez aussi inclure si vous le souhaitez:
        - des trucs graphiques/audio que vous avez fait pour le projet (et que vous trouvez bien) et que vous n'avez pas eu le temps d'inclure (ou vous avez changé de direction artistique depuis et ça ne colle plus à cette version du jeu)
        - un texte explicatif (pas trop long) pour expliquer des trucs pas clairs dans le jeu, ou qui demandent des connaissances préalables que je pourrais ne pas avoir
- à propos de la notation:
    - je prendrai en compte le jeu lui-même (est-ce que le graphisme et l'audio vont bien ensemble et avec le jeu, est-ce que vous les utilisez efficacement, feedback, tout ça) et si j'ai l'impression que si vous avez besoin de faire du graphisme/son pour un jeu vous pourrez vous débrouiller (anim, son, fond, musique, etc.)
