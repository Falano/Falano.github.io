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
        - nombre d'images par seconde (Frame Rate / Fréquence d'images) (24 pour les mouvements rapides (le nombre d'images de la télé TODO: ou du cinéma? en Europe), 12 c'est bien, 6 c'est possible mais limite);
        - Timeline / Timing: là où se passe le gros de l'animation, où on passe d'une image à l'autre, et peut déplacer des images

## 2a) notions de game design
- si jeu de plateforme/énigmes avec plusieurs niveaux: introduire une seule mécanique de jeu à la fois et laisser le temps d'expérimenter (cf III.x) (cf [une vidéo en anglais intéressante mais où il parle vite](https://www.youtube.com/watch?v=8FpigqfcvlM))
- lisibilité (cf II.2)
- vitesse de réaction du jeu: éviter les animations longues en début d'action (cf V.1)
- de l'importance du son (cf IV.1)
- de l'importance des retours visuels (feedback) (cf V.1)
- essayer d'avoir une unité graphique
    - et une unité entre le graphique, l'audio, l'histoire et le gameplay
    - ou au contraire qu'ils soient opposés, pour un effet de malaise bizarre
        - cf Happy Tree Friends (attention: gore), [Limbo](/assets/995_limbo.jpg) par Playdead: <https://playdead.com/games/limbo/>
- à propos de la musique: pour chaque musique différente, penser à son utilisation
    - une musique de fond doit avoir un cycle long (ne se répéter qu'au bout d'un certain temps)
        - mais on peut avoir plusieurs variations sur le même thème
        - tester de l'écouter en boucle pendant dix minutes (y compris en faisant autre chose) pour vérifier qu'elle ne devient pas irritante à la longue
    - une musique de fin de combat par exemple peut avoir un cycle beaucoup plus court
- à propos du son: penser aussi à son utilisation
    - si vous mettez des bruits de pas, envisager de prévoir plusieurs variations
        - pas trop différents non plus, qu'on sente que c'est la même personne qui marche sur le même matériau
            - juste pour éviter d'avoir exactement le même son plein de fois de suite
                - (on fait beaucoup de pas quand on marche)
    - même pour un son qui est censé être très fort, strident ou un peu désagréable, ne pas le rendre trop fort/strident/désagréable
        - penser aux tympans du joueur
    - plus on entend un bruit souvent plus il devrait être discret
        - un bruit de pas n'a pas besoin d'être très fort
        - la super attaque du boss final qu'il n'utilise qu'une fois toutes les cinq minutes peut avoir un son plus fort, et durer plus longtemps, et avoir un son plus remarquable
            - et avoir un screen-shake
            - et un flash sur le perso
            - et des particules!

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

## 2c) accessibilité
En gras les propositions qui ne demandent quasiment aucun effort.  
Tous ces paramètres doivent être accessibles avant le début du jeu (y compris avant la cinématique de début s'il y en a une).  
- possibilité de changer tous les contrôles
    - y compris celui d'accès au menu
    - y compris les boutons de la souris
    - idéalement, un jeu devrait pouvoir n'être joué qu'avec un seul dispositif (s'il se joue au clavier, que le menu puisse être navigué aussi avec uniquement le clavier)
    - idéalement, on devrait pouvoir y jouer avec une seule main
- si vous avez des dialogues audio: sous-titres, et possibilité de les activer ou non
    - je sais que ce n'est pas hyper important vu qu'a priori vous n'aurez pas le temps d'enregistrer de l'audio pour tous vos dialogues, et encore moins de les sous-titrer
        - mais sachez que c'est important si vous faites un jeu qui a des dialogues enregistrés et qui n'est pas une démo de moins d'une demi-heure
- daltonisme
    - envisager de mettre des motifs, en plus des couleurs, pour différencier deux types, ou ajouter des formes pour l'identification.
    - **ou changer la luminosité de manière à ce que ce soit reconnaissable aussi en niveaux de gris**
        - un [site qui transforme une image en "vue daltonienne", pour tester si elle reste lisible](https://www.color-blindness.com/coblis-color-blindness-simulator/)
    - choisir orange/bleu au lieu de rouge/vert comme couleurs opposées est plus souvent lisible par les daltonien
        - idéalement laisser le choix
    - éventuellement leur mettre un son différent
    - ou laisser les gens choisir les couleurs eux-même
- épilepsie
    - si vous avez des flashs de couleurs très contrastées (blanc, ou rouge vif) qui prennent une grosse partie de l'écran (plus d'un quart)
        - ou des mouvements aléatoires de motifs de couleurs très contrastées, qui prennent une grosse partie de l'écran
    - **alors mettre un écran d'avertissement au début du jeu**
        - et éventuellement la possibilité de les désactiver
        - et éviter le rouge très vif pour les flashs
        - et éviter d'avoir trois ou plus flashs par seconde
- **contrastes du texte**
    - augmenter la taille du texte aide aussi à la lisibilité
    - le fond derrière le texte peut avoir une légère texture, mais pas trop forte ou elle peut nuire à la lisibilité
    - cf <https://webaim.org/resources/contrastchecker/>
- dyslexie et problèmes de vue
    - ne pas utiliser de polices serif
    - ni l'italique
    - ne pas rogner sur l'interligne (un interligne de 1.5 est plus lisible)
    - **utiliser des majuscules et des minuscules, pas tout majuscule ou tout minuscule**
    - préférer du texte non justifié
    - utiliser des lignes courtes: pas plus de 70-80 caractères par ligne
    - helvetica, arial et verdana sont, selon [une étude](http://dyslexiahelp.umich.edu/sites/default/files/good_fonts_for_dyslexia_study.pdf), facilement lisibles
- possibilité de passer les cinématiques

**références**  
un site extrêmement bien fait qui regroupe plein de conseils pour l'accessibilité, avec des exemples et des explications (en anglais malheureusement): <http://gameaccessibilityguidelines.com/full-list/>
à propos de l'épilepsie: <https://videogameseizures.wordpress.com/2018/02/15/seizures-from-2017s-best-video-games/>  
<https://www.w3.org/TR/UNDERSTANDING-WCAG20/seizure-does-not-violate.html>  
à propos du daltonisme: <https://www.color-blindness.com/coblis-color-blindness-simulator/>  
à propos du texte: <https://webaim.org/resources/contrastchecker/>
à propos de la dyslexie: <https://bigelowandholmes.typepad.com/bigelow-holmes/2014/11/typography-dyslexia.html> et <http://dyslexiahelp.umich.edu/sites/default/files/good_fonts_for_dyslexia_study.pdf>

## 3a) Licences
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

## 3b) Ressources externes
-/!\ Toujours vérifier la licence des assets qu'on utilise! cf Annexes X.3a, une explication des principales licences libres utilisées pour les assets
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
    - + [The Ur-Quan Masters](http://sc2.sourceforge.net/): exploration spatiale <details> ![uqm](/assets/994_uqm.png)

- style graphique simple mais qui marche
	- + [thomas was alone](http://www.thomaswasalone.com/thomaswasalone/): platformer
		- graphisme simple mais:
		- textures et lumières
		- voix des personnages
	- + [*you must gather your party before venturing forth*](https://ldjam.com/events/ludum-dare/46/ymgypbvf-you-must-gather-your-party-before-venturing-forth): puzzle
		- très stylisé
		- mais les informations importantes sont facilement lisibles (la race des persos, qui influence le gameplay) <details> ![ymgypbvf](/assets/998_ymgypbvf.png)
	- + [Selfless Heroes](https://selflessheroes.fr/): intro à la programmation
		- très stylisé
		- mais les informations importantes sont facilement lisibles
			- les persos sont des chevaliers
			- chacun est un personnage différent
			- la différence entre chaque type de tile est claire
		- et pour éviter la monotonie visuelle, il y a plusieurs types de chaque tile <details> ![selfless heroes](/assets/003_selflessHeroes.png)
	- + [Mini Metro](https://dinopoloclub.com/games/mini-metro/), par Dino Polo Club: un jeu de gestion de métros
	    - utilise des symboles plutôt que des illustrations <details> ![mini-metro](/assets/997_minimetro.jpg)
	- + [*Gophers*](https://hyperlinkyourheart.itch.io/gophers)(/assets/105_gophers.png): narration
		- les palettes de couleurs limitées, utilisées à bon escient, marchent souvent bien
		- un travail sur l'atmosphère (accord graphisme-son-histoire-gameplay) <details> ![*Gophers*](/assets/105_gophers.png)
	- [Night in the Woods](http://www.nightinthewoods.com/) par Infinite Fall: narration
	    - très chouette style graphique
	        - soutenu/contrasté par la musique et l'histoire
	    - mais composé quasi exclusivement de formes simples
	    - simplification et stylisation des textures <details> ![night in the woods](/assets/996_nightInTheWoods.png)
	- + [capsule](https://finji.itch.io/capsule) par Finji [](__TODO__)

- mécanique de jeu inhabituelle
	- [World of Goo](https://2dboy.com/), par 2DBoy: construction d'échelles et de pyramides avec des blobs de truc gluant
	- [A Blind Legend](http://www.ablindlegend.com/), par Dowino: un jeu d'aventure où l'ouïe est le sens le plus important
	- + [The Stanley Parable](https://store.steampowered.com/app/221910/The_Stanley_Parable/), par Davey Wreden: un "jeu narratif expérimental à la première personne"

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
        - https://github.com/git-lfs/git-lfs/releases/tag/v2.12.0
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
