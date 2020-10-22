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
- **.midi**: fichier pour la musique: il enregistre les paramètres de chaque note (hauteur, durée, etc.), et on peut ensuite y appliquer le son qu'on veut, soit généré par l'ordinateur, soit enregistré et stocké dans une banque de sons appelée 'soundfont' (souvent utilisées pour les instruments de musique). Une sorte de partition lisible par l'ordinateur, qui ne contient en tant que tel aucun son, mais peut être jouée par n'importe quel instrument.

## 100) ressources en français
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

# V. [Animation](/cours/creation_gestion_ressources_5.html)
# X. [Annexes](/cours/creation_gestion_ressources_0.html)
