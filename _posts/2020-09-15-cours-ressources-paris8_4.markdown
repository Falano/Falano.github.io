---
layout: default
title:  "Cours Paris 8: Création et Gestion de ressources"
date:   2020-09-15 19:05:09 +0200
categories: classes, krita, 2D, fr
permalink: /cours/creation_gestion_ressources_4.html
---

# O. [Menu](/cours/creation_gestion_ressources.html)
# I. [Introduction](/cours/creation_gestion_ressources_1.html)
# II. [Krita](/cours/creation_gestion_ressources_2.html)
# III. [Décors](/cours/creation_gestion_ressources_3.html)
# IV. [Son](/cours/creation_gestion_ressources_4.html)
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
    - <https://www.bfxr.net/> un site de génération d'effets sonores
    - les écouteurs-enregistreurs ont trois bandes sur le port jack, les non-enregistreurs n'en ont que deux
- à propos du MIDI et des soundfonts
- différence mono/stéréo (mono: une piste (son identique pour les deux oreilles), stéréo: deux pistes (un son différent pour chaque oreille: peut donner une impression de mouvement dans l'espace))
- couper un son au plus près, sans plage de silence au début (surtout pour les effets sonores d'action, dont il ne faut pas qu'ils soient en retard)
- éviter les différences de niveau (volume sonore) trop importantes
    - il n'y a rien de plus irritant qu'un son trop fort

## 2) licences
/!\ Toujours vérifier la licence des assets qu'on utilise.  
cf [Annexes X.2](/cours/creation_gestion_ressources_0.html), une explication des principales licences libres utilisées pour les assets

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
        - tester l'effet "clic removal" ou "suppression de clics", sûrement il marche très bien; sinon:
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
        - <https://beepbox.co/> (musique bitbox, simple d'utilisation)
            - éventuellement exporter en MIDI, importer dans musescore, mettre de belles soundfonts et réexporter en .wav ou .ogg
        - LMMS
- télécharger une musique sous licence libre

## 4b) LMMS
- aide: bouton 'i'
- navigation
    - se déplacer dans le temps: *clic gauche* sur la ligne du temps au-dessus de l'espace de travail
    - zoom/dézoom: ctrl molette
    - commencer/arrêter la lecture: *espace*
    - solo/mute
- song editor
    - là où on assemble le contenu de tous les autres editors
    - dupliquer un module *ctrl cliquer glisser*
    - piste Sample Track: accepte un fichier audio
        - cliquer sur la partie droite du song editor
        - puis double-cliquer sur le rectangle orange pour choisir le fichier audio à insérer
    - piste Automation Track: animer un contrôle (par exemple changer le volume d'une autre piste)
        - edit song-global automation
        - controller rack: cyclic automation qui peut être controllé par un autre contrôle
    - piste Triple Oscillator
        - plein de presets, les tester
    - loop point (début: *clic molette* fin: *clic droit*)
    - changer un instrument
    - sauver ses presets
- My Presets
    - si on clique sur un preset on l'entend
- My Instruments
    - audio file processor
        - pour enregistrer ses propres instruments
            - options de boucle
    - SF2 player
        - File: le fichier .sf2 de la soundfont
        - Patch: choisir parmi la liste des instruments disponibles dans la soundfont choisie
    - sfxr
        - fonctionne comme sfxr (qui l'eût cru)
        - boutons random et mutation
- beat editor
    - possibilité d'ajouter autant d'instruments qu'on veut
- piano editor
    - input midi ou clavier ordi
        - tempo
    - raccourcis claviers habituels:
        - *ctrl A* sélectionner tout
        - *ctrl C* copier
        - *ctrl V* coller
        - probablement d'autres
    - outil dessin
        - dessin (*shift D* puis *clic gauche*)
        - gomme (*clic droit*)
        - adapter la durée (*clic gauche* en fin de note)
        - déplacement
            - *cliquer glisser*: déplacer
            - *shift cliquer glisser*: copier
    - chords (harmoniques)
    - outil selection
        - pour déplacement (*cliquer glisser* avec l'outil dessin)
        - sélectionner des notes une par une *shift clic gauche*
        - pour suppression (*suppr*)

## 4c) utilisation habituelle des instruments
- des cloches, des xylophones ou des hangs (percussions délicates qui résonnent) aigus pour une atmosphère féerique/magique/nature
- des trompettes, cors et autres cuivres pour un air épique et impressionnant
- une flûte, hautbois, ou violon pour la ligne mélodique
- de la musique chiptune pour un effet rétro
- plein d'effets ou des instruments synthétisés pour un air plus sci-fi/futuriste/urbain
- des choeurs ou des orgues peuvent donner un air musique sacrée/impressionnant
- une voix qui chante (ou fredonne) peut donner un caractère plus intimiste/berceuse
- un saxophone ou une trompette ( + batterie, + contrebasse) pour une atmosphère jazz/New York/1960
- accordéon: musique de rue, France urbaine ou de village, etc.
    - généralement: pas mal d'endroits ont des instruments qui leur sont propres, ne pas hésiter à les utiliser si on trouve une soundbank (ou un instrumentiste) adaptée
- ne pas hésiter à mélanger sons et musique (cf [une musique qui utilise des bruits comme notes](https://www.youtube.com/watch?v=fOCaNBGMMgE), [une autre](https://www.youtube.com/watch?v=SAUKJNCQK6U))
    - par exemple une musique militaire peut utiliser comme rythme de fond le bruit d'une armée en marche (cf [le chant des partisans tel que chanté par Yves Montand](https://www.youtube.com/watch?v=DeXraool4QE))
    - un son informatif, comme un bruitage de "tu as trouvé un coffre" ou "tu as été touché" peut être une musique courte (cf [Zelda](https://www.youtube.com/watch?v=CGBO_Xbz3Dk))
- globalement: chercher "best /_style recherché/_" sur youtube et voir ce qui sort et tenter de faire quelque chose qui semble respecter les mêmes règles; éventuellement se renseigner un peu sur les règles théoriques du genre (les rythmes fréquents, les tonalités favorisées, etc.)
- une bonne base pour faire une musique qui sonne bien c'est d'utiliser beepbox et se contraindre à n'utiliser que les notes d'une de ses "scales" (gammes).

**références**  
vidéo "Making Music with STUFF FROM KITCHEN" de l'utilisateur youtube JRinne Films: <https://www.youtube.com/watch?v=fOCaNBGMMgE>  
vidéo "Using household objects to make music" de l'utilisateur youtube electroviolence: <https://www.youtube.com/watch?v=SAUKJNCQK6U>  
le Chant des Partisans, de Anna Marly, traduit en français par Joseph Kessel et Maurice Druon, chanté par Yves Montand  
The Legend of Zelda, Nintendo  


## 4d) spécifités des musiques de jeu
- la boucle
    - de base: juste une boucle
    - potentiellement intro (une fois) -> boucle (qui se répète autant de fois que nécessaire) -> conclusion/transition (une fois)
    - voire intro -> boucle1 -> boucle2 -> transition -> boucle3 -> conclusion
        - les "->" entre les boucles indiquant un événement dans le jeu qui cause le changement de musique
    - plein de variations possibles mais: on sait quand ça commence on ne sait jamais quand ça finit
    - il est possible aussi d'avoir plusieurs points de changement de musique potentiels:
        - soit d'une part les fragments A B C et D, qui forment une boucle, et d'autre part A' B' C' D', qui forment une autre boucle, et de base ça joue la première boucle: ABCDABCDABCDABCD...,
        - mais une action du joueur peut passer à la deuxième boucle dès qu'une fin de segment est atteinte:
        - si le joueur agit pendant que la musique jouait B, à la fin au lieu de passer à C on passe à C', puis ça continue en D'A'B'C'D'A'B'...
        - ou alors à la fin de B au lieu de passer à C ça passe à A', et continue en B'C'D'A'B'C'...
- possibilité d'ajouter des effets à toute la bande son, lié aux événements du jeu
    - par exemple progressivement ajouter de la réverbération quand le perso descend dans une caverne
    - ou baisser progressivement le son d'une piste et augmenter celui d'une autre
    - ou lancer la piste des cuivres (par exemple) à un moment précis (prévoir plusieurs points d'entrée possibles)
- visée informative
    - par exemple changer de thème musical quand un ennemi approche
    - ou augmenter le tempo pour prévenir qu'il reste peu de temps pour finir une tâche
    - ou ajouter un filtre ou une piste si on a trop peu de vie
    - etc.
- ou alors on peut aussi inclure dans son jeu dix minutes d'un opéra qu'on a composé spécialement pour lui, comme Final Fantasy 6 ¯\_(ツ)_/¯

## 5) les formats audio
- **.aup**: format de travail de audacity
- **.flac**: très bonne qualité (lossless), comparativement relativement léger, open source
- **.mp3**: pas très bonne qualité (compressé), très léger, lisible presque partout (le jpg du son)
- **.aiff**: historiquement le format bonne qualité de mac (sans compression); assez lourd
- **.wav**: historiquement le format bonne qualité de windows (sans compression); assez lourd mais rapide à lire pour godot; **lisible par godot**, conseillé pour les bruitages
- **.ogg**: meilleure qualité que mp3 à poids égal (compressé), open source, léger, un peu lent à lire pour godot; **lisible par godot**, conseillé pour les voix, les musiques, et les sons qui durent
- **.midi**: fichier pour la musique: il enregistre les paramètres de chaque note (hauteur, durée, etc.), et on peut ensuite y appliquer le son qu'on veut, soit généré par l'ordinateur, soit enregistré et stocké dans une banque de sons appelée 'soundfont' (souvent utilisées pour les instruments de musique). Une sorte de partition lisible par l'ordinateur, qui ne contient en tant que tel aucun son, mais peut être jouée par n'importe quel instrument.

## 97) exercices
1) patchwork
- prendre dix à quinze morceaux de musique (sans paroles) que vous aimez bien, de plusieurs styles différents
- composer un morceau en utilisant des fragments d'au moins sept d'entre eux
- observer où et comment les transitions passent le mieux, y compris quand l'instrumentation et le style musical sont différents

2) compatibilité verticale
- choisir un instrument, et écrire un thème musical simple.
- ajouter un autre instrument après deux à six fragments, qui habille le thème et lui donne un peu plus de poids
    - faire attention à ce que le changement ait l'air naturel et pas trop brusque: faire attention à quand le nouvel instrument entre
- le faire plusieurs fois
- ajouter un instrument et en enlever un ou plusieurs pour changer l'atmosphère du morceau
- le faire plusieurs fois

3) compatibilité horizontale
- composer un thème musical de quatre à sept phrases musicales
- composer un autre thème musical compatible (rythme et tempo similaires, au moins deux instruments identiques)
- choisir des points de passage, le même nombre sur chaque thème
- vérifier que l'on peut passer d'un thème à l'autre en utilisant chacun des points de passage


## 98) exemples
- un thème avec plusieurs niveaux: le [thème de terra dans ff6](https://www.youtube.com/watch?v=a6t_uyg_pF8)

## 99) ressources en anglais
- un livre sur la musique de jeu vidéo, souvent utilisé dans des cours d'unifs ou d'écoles: A Composer’s Guide to Game Music, de Winifred Phillips
- un [compositeur de musique de jeu très intéressant qui analyse des musiques de jeu](https://www.youtube.com/c/jakebutineau/featured)
    - [canal Game Music Discussions](https://www.youtube.com/playlist?list=PLn9G57Vo6gadLUEzzvz38tKQ5x1P-1g4h)
    - [canal The Game Music Podcast](https://www.youtube.com/playlist?list=PLn9G57Vo6gafeDzvegH-nmD5IGbDz5k0s)
- une [vidéo d'analyse générale de la musique de jeux prenant comme exemple plein de jeux différents](https://www.youtube.com/watch?v=XkndjIA-WVY)
- un [compositeur qui explique comment il a fait une musique alternative pour le Witcher 3](https://www.youtube.com/watch?v=mp06Yoo6bNM)
    - à [3:54](https://youtu.be/mp06Yoo6bNM?t=224) il joue the witcher avec sa musique
    - à [5:35](https://youtu.be/mp06Yoo6bNM?t=337) il montre chaque piste (et il explique des trucs, mais on peut aussi juste l'ignorer)
- une [vidéo expliquant tout le processus](https://www.youtube.com/watch?v=1qPfH95ry84)
- une [interview écrite des sound designer et game developer de Untitled Goose Game](https://www.fmod.com/blog/untitled-goose-game-interview)
- un [court article sur la musique de jeu vidéo en général](https://audient.com/tutorial/composing-music-video-games/)
- un [article académique sur la musique de jeu vidéo](https://www.researchgate.net/publication/329210926_Designing_a_game_for_music_Integrated_design_approaches_for_Ludic_music_and_Interactivity)
- une [vidéo sur la théorie musicale](https://www.youtube.com/watch?v=rgaTLrZGlk0)
- un [tuto sur LMMS au pif](https://www.youtube.com/watch?v=TrMTlpeSw8Y)

## 100) ressources en français
- un [mémoire sur la musique de jeu vidéo](https://www.ens-louis-lumiere.fr/sites/default/files/2017-08/Soulier_Son_2016.pdf)
- un [musicien/sound designer qui raconte comment il fait les musiques de jeu](https://www.youtube.com/watch?v=ctoGioZNYTM)
- le [cours sur le son, avec une démo de tiles au début](https://youtu.be/XDcndwQZyQ4)
    - 00:00 démonstration des tiles vue du haut
    - 00:26:25 faire plusieurs niveaux (escaliers, terrasses, etc.) en tiles vu du haut
    - 00:34:26 la lisibilité
    - 00:46:43 décors "pleins" (pas en tiles, mais dessinés d'un bloc)
    - 00:56:10 outils Assistants, formes géométriques et lasso de krita
    - 01:05:17 intro son
    - 01:11:52 format midi
    - 01:13:50 beepbox
    - 01:20:07 musescore
    - 01:23:04 réexplication du format midi
    - 01:31:04 les licences
    - 01:43:31 sites de ressources audio
    - 01:44:14 git lfs
    - 01:50:43 audacity

[](probs: 3. fin L1C12)
[](4. fin L1A12 + V.3 timeline e V.3 onionskin + annexes game design e accessibility)
[](4. fin L1B12 + V.3 timeline e V.3 onionskin + annexes game design e accessibility)


# V. [Animation](/cours/creation_gestion_ressources_5.html)
# VI. [Finitions](/cours/creation_gestion_ressources_6.html)
# VII. [Exports](/cours/creation_gestion_ressources_7.html)
# VIII. [Game Design](/cours/creation_gestion_ressources_8.html)
# X. [Annexes](/cours/creation_gestion_ressources_0.html)
