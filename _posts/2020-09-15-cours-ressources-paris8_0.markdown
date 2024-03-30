---
layout: page
title:  "Cours Paris 8: Création et Gestion de ressources"
last_updated: July 27, 2023
permalink: /cours/creation_gestion_ressources/annexes.html
topnav: topnav_P8_Ressources
---
# X. Annexes
## 1) schéma de l'interface de Libresprite
![Interface Libresprite](/assets/999_interfaceLibresprite.jpg)
- **1**: menus:
    - File:
        - nouveau document (New),
        - ouvrir un document (Open ou Open Recent),
        - sauvegarder (Save: *ctrl S*),
    - Edit (opérations sur le calque courant):
        - annuler (Undo: *ctrl Z*),
        - refaire (Redo: *ctrl Y*),
        - tout gommer sur le calque courant (Clear: *Suppr*)
        - tourner le calque courant (Rotate)
        - Miroir (Flip Horizontal: *Shift H* ou Flip Vertical: *Shift V*)
        - Déplacement, rotation et étirement manuel (Transform: *Ctrl T*)
        - Changer sur le calque courant une couleur par une autre (Replace Color: *Shift R*)
        - Raccourcis clavier (Keyboard Shortcuts)
        - Préférences (Preferences; si ça rame, cocher Experimental > Use Native Mouse Cursor, Experimental > Use Native File Dialog et Cursors > Brush Preview > None)
    - Sprite (opérations sur tous les calques)
        - Modifier le niveau de détails (Sprite Size)
        - Changer la tailler de l'espace de travail (Canvas Size)
        - Miroir ou Rotation de tous les calques (Rotate Canvas / Flip Canvas)
        - Supprimer les marges inutiles (Trim)
    - Layer (calques):
        - Nouveau calque (New Layer)
        - Supprimer le(s) calque(s) sélectionné(s) (Remove Layer)
        - Dupliquer le calque (Duplicate)
        - Mélanger le calque sélectionné avec celui d'en dessous (Merge Down)
        - Mélanger tous les calques pour ne plus en avoir qu'un seul (Flatten)
    - Frame (animation):
        - Ajouter une image d'animation après l'image sélectionnée; pour tous les calques, elle continendra une copie de l'image active (New Frame)
        - Ajouter une image d'animation vide après l'image sélectionnée (New Empty Frame)
        - Dupliquer l'image sélectionnée sur l'image d'après (ne touche que le calque sélectionné); s'il n'y a pas d'image d'après, en crée, s'il y en a une, l'écrase (Duplicate Cell(s))
        - Dupliquer l'image sélectionnée sur l'image d'après; si le calque est en mode "continu", lier les deux (Duplicate Linked Cell(s))
        - Supprimer l'image d'animation sélectionnée (pour tous les calques)
    - Select (Sélections):
        - Tout sélectionner (All: *Ctrl A*)
        - Tout désélectionner (Deselect: *Ctrl D*)
        - Inverser la Sélection (Inverse: *Ctrl Shift I*)
    - View (Fenêtres et options de visualisation):
        - Grille (Grid)
        - mode infini pour faire des tiles qui bouclent (Tiled Mode)
        - si une de vos fenêtres/onglets/bouts de programme a disparu cherchez là
- **2**: couleurs:
    - Palette
    - Sélecteur de couleurs (redimensionnable pour une sélection plus précise; ou cliquer sur le nom de la couleur en bas)
    - Échanger couleur d'arrière-plan et de second plan: *X*
- **3**: couleurs:
    - Changer une couleur de la palette (Edit Color: *F4*)
    - Créer une palette à partir de l'image actuelle (Options > Create Palette from current Sprite)
- **4**: pinceau:
    - Forme du pinceau (Brush Type)
    - Taille du pinceau (Brush Size)
    - Type de dessin (Ink): Normal (Simple Ink), semi-transparent (Alpha Compositing), sans dépasser (Lock Alpha)
- **5**: onglets:
    - Onglets avec les différents fichiers ouverts
- **6**: outils (certains en contiennent plusieurs qui apparaissent quand on laisse appuyé)
    - Outils de sélection
    - Pinceau (Pencil Tool: *B*)
    - Gomme (Eraser: *E*)
    - Sélecteur de couleurs (Eyedropper: *I*)
    - Zoom (*Z*) / Déplacement de la caméra (*H*)
    - Bouger un objet (*V*)
    - Remplir une zone de couleur (Paint Bucket Tool: *G*)
    - Ligne (*L*) / Courbe (*Shift L*)
    - Formes géométiques
    - Outil Lasso (Contour Tool)
- **7**: Layers/ Calques:
    - rendre un calque visible ou non (icône oeil)
    - rendre un calque modifiable ou non (icône cadenas)
    - frames d'animation continues ou non (pour rendre indépendante une frame précise, clic droit > Unlink) (icône deux points)
    - paramètres de la transparences des images d'avant et d'après, la "peau d'oignon" (Onionskin) (icône sliders)
    - activation ou non de la peau d'oignon (Onionskin) (icône deux carrés)
    - *double clic* sur le nom du calque pour afficher les options
        - le renommer
            - bien nommer ses calques!
        - changer son opacité
        - changer son mode de calque
    - *clic droit* sur le numéro de frame permet, entre autres, de changer son tag (pour si on a plusieurs actions à la suite par exemple)
    - en haut: options de lecture de l'animation
        - aller à la première frame
        - aller à la frame précédente
        - jouer/mettre en pause l'animation (*Enter* et *Echap*)
        - aller à la frame suivante
        - aller à la dernière frame
- **7**: Espace de dessin:
    - pour zoomer et se déplacer dans l'image, les raccourcis claviers sont:
    - *molette*: zoom;
    - *clic molette*: se déplacer;
    - *shift clic molette* ou *shift espace clic*: rotation;
    - *pav num 1 à 6*: raccourcis pour le zoom;
    - il y a aussi un outil zoom et un outil déplacement dans la barre des outils à droite (la loupe et la croix fléchée)
    - *ctrl clic*: sélectionner le calque contenant le pixel sur lequel on a cliqué
/!\ Libresprite ne maintient pas sa documentation, mais c'est un fork de Aseprite, dont la doc est [ici](https://www.aseprite.org/docs/) (en anglais).
Un [fil twitter](https://twitter.com/aseprite/status/1124442198651678720) avec des astuces (sur aseprite, mais ça s'applique aussi à libresprite en général)

## 2) Licences
{% include warning.html content="Toujours vérifier la licence des assets qu'on utilise." %}
- différentes licences:
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
{% include warning.html content="Toujours vérifier la licence des assets qu'on utilise! cf Annexes X.2, une explication des principales licences libres utilisées pour les assets" %}
- ressources graphiques
    - persos, décors et UI (il est interdit de les utiliser pour ce cours, mais je vous les donne pour après)
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
        - <https://wingless-seraph.net/en/material-se.html> (des musiques et sons gratuits avec attribution; bien formattés pour du jeu (la plupart des musiques incluent une version qui boucle))
        - <https://mixkit.co/> : musiques et sons gratuits (en tant que pub pour s'inscrire sur la version payante, mais il y en a quand même une bonne quantité de disponibles gratuitement)

    - musique
        - <https://www.hongkiat.com/blog/creative-common-music-download/> (liste de sites de musique libre)
        - <https://audionautix.com/> (site de musiques CC-BY)
        - <https://freemusicarchive.org/> (site de musiques CC)
        - <https://filmmusic.io/search> (site de musiques principalement CC BY)
        - <https://wingless-seraph.net/en/material-music.html> (des musiques et sons gratuits avec attribution; bien formattés pour du jeu (la plupart des musiques incluent une version qui boucle))
        - liens: <https://incompetech.com/music/royalty-free/faq.html> (site de musiques gratuites avec attribution)
        - <https://musescore.org/en/handbook/soundfonts-and-sfz-files> (lien vers des soundfonts (polices de son: fichiers qui traduisent un fichier .midi en du beau son))

## 4) game jams
- une game jam c'est, en gros, faire un jeu en (souvent) 48h, seul ou en groupe, avec d'autres gens qui font la même chose en même temps (proche des jams d'improvisation musicale et des hackatons)
    - ludum dare: deux fois par an (avril et octobre), probablement la jam la plus connue: <https://ldjam.com/>
    - global game jam: une fois par an (en janvier), probablement la jam physique la plus connue: <https://globalgamejam.org/>
	- un agenda des jams en cours et à venir, sur un site où on peut publier ses jeux: <https://itch.io/jams>
	- une jam fondée en france qui a lieu trois fois par an: <https://alakajam.com/article/about/welcome>

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
	- /+ [*Gophers*](https://hyperlinkyourheart.itch.io/gophers): narration
		- les palettes de couleurs limitées, utilisées à bon escient, marchent souvent bien
		- un travail sur l'atmosphère (accord graphisme-son-histoire-gameplay) <details> ![*Gophers*](/assets/105_gophers.png)
	- [Night in the Woods](http://www.nightinthewoods.com/) par Infinite Fall: narration
	    - très chouette style graphique
	        - soutenu/contrasté par la musique et l'histoire
	    - mais composé quasi exclusivement de formes simples
	    - simplification et stylisation des textures <details> ![night in the woods](/assets/996_nightInTheWoods.png)

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
    - [*pandemia*](https://www.lexaloffle.com/bbs/?tid=31451): puzzle/stratégie


## 6) Vocabulaire
- **tile**: une image (en général un fragment de décor) utilisée pour composer une image plus grande (un niveau entier) avec d'autres tiles, espacées régulièrement; elle sera typiquement réutilisée de nombreuses fois dans le même niveau.
    - un ensemble de tiles est un **tileset**
    - un niveau composé de tiles est une **tilemap**; on utilise parfois "tilemap" pour dire "ensemble de tiles"
- **asset**: un élément composant le jeu. Dans sa définition la plus étroite, se réfère uniquement aux assets graphiques (les tiles, les personnages, etc.), mais souvent aussi aux assets sonores, et parfois inclue des scripts.
- **palette**: l'ensemble de couleurs qui composent une image (ou qu'on prévoit d'utiliser pour une image). Les palettes de pixel art sont souvent assez réduites.
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
- la date de rendu du projet est le **samedi 18 décembre** 2021, à **7h du matin** au plus tard
- à propos des projets:
    - les projets peuvent se faire soit en groupe de deux soit seul;
    - si vous voulez utiliser un autre logiciel que ceux montrés en cours, demandez-moi.
- à propos des personnages:
    - les fanarts sont autorisés, mais il est obligatoire de préciser dans l'écran des 'credits' (là où vous écrivez le nom de tous les participants au jeu) de quel perso et quel oeuvre c'est tiré (et si après le cours vous vous rendez compte que votre idée de jeu est géniale et que vous allez le publier sur steam/gog/epic/itch et gagner des fortunes, je vous conseille de changer le design du perso)
    - il est interdit de décalquer/recopier une spritesheet existante, même si vous lui ajoutez des éléments.
- à propos de l'audio:
    - il est obligatoire de mentionner d'où ça vient dans les crédits ("musique composée par Machin Truc avec Beepbox", par exemple); si c'est vous qui l'avez fait, mettez votre nom à la place de "Machin Truc".
    - vous pouvez utiliser des sons et des musiques disponibles en ligne tant que leur licence l'autorise et que vous les mentionnez comme il faut dans les crédits (mais si le son/la musique vous intéresse, je vous encourage à les faire vous-même, ça fera des points bonus)
- à propos des décors:
    - si vous avez plusieurs niveaux un peu longs, il est conseillé (c'est beaucoup plus simple pour le level design) de faire des tilemaps.
    - tiles ou pas, ça doit être du pixel art (dessiné avec une brosse dure).
    - il est interdit de réutiliser ce qui a été fait par quelqu'un d'autre, même si vous le modifiez.
- à rendre dans le rendu:
    - l'exécutable du jeu (linux et windows)
    - le projet godot
    - vos fichiers source (.ase, .aup, lien beepbox, etc.)
    - les fichiers des ressources externes que vous avez utilisées (n'oubliez pas aussi qu'il est obligatoire de les attribuer (dire "musique: 'Jazzy', de Kevin McLeod, lien-vers-son-site, CC-BY" par exemple) dans l'écran des crédits, et/ou dans un fichier texte joint à l'exécutable et clairement mentionné dans les crédits s'il y en a trop)
    - un fichier texte avec vos nom, prénom, celui de votre binôme le cas échéant, et, si vous avez fait le son vous-même, comment.
- à propos de la notation:
    - je prendrai en compte le jeu lui-même (est-ce que le graphisme et l'audio vont bien ensemble et avec le jeu, est-ce que vous les utilisez efficacement, feedback, tout ça) et si j'ai l'impression que si vous avez besoin de faire du graphisme/son pour un jeu vous pourrez vous débrouiller
    {% include warning.html content="ceci (ci-dessous) est le strict minimum pour passer: si vous ne rendez pas au moins ça a priori vous ne passez pas"%}
    - a priori vous passez si vous n'avez enfreint aucune consigne et que votre jeu contient *au minimum*:
        - des bruitages, implémentés dans le jeu
        - de la musique, implémentée dans le jeu
        - au moins un personnage, animé avec le système d'animation de libresprite (ou de krita), avec plusieurs animations de plus de quatre images différentes (s'il n'y a pas de personnages ou qu'ils ne peuvent pas être animés, trouver un autre endroit où faire des anims un chouilla complexes: effets spéciaux d'explosions, feu fumée, ou bien décors, ou en dernier recours menus)
        - des décors avec des tiles (qui s'imbriquent, utilisant les autotiles) (si ça ne fonctionne pas avec le style graphique de votre jeu, vous pouvez mettre les tiles dans un niveau à part non-utilisé)
    - il y a des points bonus si en plus ce que vous faites est chouette (son fait par vous-même, personnages et/ou animation efficaces, décors animés, concept de jeu particulièrement intéressant, plein de niveaux, ambiance réussie, etc.)
