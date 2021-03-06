---
layout: default
title:  "Cours Paris 8: Création et Gestion de ressources"
date:   2020-09-15 19:05:09 +0200
categories: classes, krita, 2D, fr
permalink: /cours/creation_gestion_ressources_5.html
---  

# O. [Menu](/cours/creation_gestion_ressources.html)
# I. [Introduction](/cours/creation_gestion_ressources_1.html)
# II. [Krita](/cours/creation_gestion_ressources_2.html)
# III. [Décors](/cours/creation_gestion_ressources_3.html)
# IV. [Son](/cours/creation_gestion_ressources_4.html)
# V. Animation
## 1) intro
- c'est quoi l'anim
    - différentes techniques d'animation
        - stop-motion
            - [animation d'objets (PES)](https://www.youtube.com/watch?v=qBjLW5_dGAM)
            - [pâte à modeler (shawn the sheep)](https://www.youtube.com/watch?v=0_4vs0nCCUI)
            - [marionnettes (L'étrange Noel de Mister Jack)](https://www.youtube.com/watch?v=Wy7yv44vjIo)
            - [marionettes (ma vie de courgette)](https://www.youtube.com/watch?v=OEwycy4aaFw)
            - [marionettes (le petit prince)](https://vimeo.com/164860211)
            - Jiri Trnka
        - pixilation
            - [luminaris](https://vimeo.com/24051768)
            - [Neighbours](https://vimeo.com/39056719)
        - papier découpé
            - [lotte reiniger](https://www.youtube.com/watch?v=ZXQPZqOqe58)
            - [the breadwinner / parvana](https://www.youtube.com/watch?v=bIEZ5c4kPn8)
        - dessin tradi
            - [un pencil test de Milt Kahl (Shere Kahn)](https://www.youtube.com/watch?v=K4Hq1vNhxs0)
            - [un extrait des 101 dalmatiens](https://www.youtube.com/watch?v=ulsjuiFO2J0)
            - [le roi et l'oiseau](https://www.youtube.com/watch?v=VeBDbAaLu1w)
            - [un making of de cuphead](https://www.youtube.com/watch?v=wRRV7TIQTX0)
        - 2D numérique
            - [tangle tower](https://www.youtube.com/watch?v=4n9LbvdkEtI)
            - [later alligator](https://www.youtube.com/watch?v=YbmKuBrDhow)
            - [jotun](https://www.youtube.com/watch?v=a8HG2fWlsns)
        - vectoriel
            - [teen titans Go!](https://www.youtube.com/watch?v=C1hIp-UxXfA)
        - 2D rigs
            - [démo du logiciel Spine](https://www.youtube.com/watch?v=alSrwNV8YkU)
        - 3D
            - [Team Fortress 2](https://www.youtube.com/watch?v=N7ZafWA2jd8)
            - [abzu](https://www.youtube.com/watch?v=P2G54w8H4oM)
- différence 2D-3D, tweening
- onion skin et tables lumineuses
- de l'importance du mime (si vous le sentez)

**références**  
Western Spaghetti, par PES: <https://www.youtube.com/watch?v=qBjLW5_dGAM>  
Shawn the Sheep, série et film produits par Aardman Animation: <https://www.youtube.com/user/aardmanshaunthesheep>  
L'étrange Noel de Mister Jack (The Nightmare Before Christmas), réalisé par Henry Selick  
Ma vie de Courgette, réalisé par Claude Barras  
Le petit prince (2015), réalisé par Mark Osborne, stop-motion animée par le studio TouTenKartoon <https://toutenkartoon.ca/>  
Luminaris, par Juan Pablo Zaramella  
Neighbours, réalisé par Norman McLaren, produit par l'ONF/NFB (Office National du Film canadien)  
Parvana (the breadwinner), réalisé par Nora Twomey  
Les 101 Dalmatiens, produit par Disney  
Le Roi et L'oiseau, de Paul Grimault et Jacques Prévert  
Cuphead, par Studio MDHR  
Tangle Tower, par SFB games <https://sfbgames.com/press/sheet.php?p=tangle_tower>  
Later Alligator, par PillowFight Games et SmallBu Animation <https://press.pillowfight.io/later_alligator/index.html>  
Jotun, par Thunder Lotus Games <https://thunderlotusgames.com/jotun/>  
Teen Titans Go!, produit par Cartoon Network  
Team Fortress 2, par Valve  
Abzu, par GiantSquid <https://abzugame.com/>  

## 2) principes d'animation 1
- timing
    - plus les images sont rapprochées dans l'espace (plus le personnage est à un endroit proche de l'image d'avant), plus ça bouge lentement
    - plus les images sont rapprochées dans le temps (sur la timeline), plus ça bouge vite
    - plus le framerate (fréquence d'images) est élevé plus ça va vite
    - par exemple:
        - pour une action très rapide, on voudra une image différente par frame (pour la partie très rapide en tous cas), et éventuellement un framerate de 24
        - pour une action très lente (un idle par exemple), un framerate de 12 et une image toutes les une ou deux frames selon les images peuvent suffire
        - mais globalement essayer de ne pas avoir moins de 12 images/secondes à part pour un idle
        - utiliser l'espace plutôt que le temps pour gérer le rythme dans l'anim finale
- varier les rythmes
    - les robots/machines ont tendance à avoir des mouvements plus réguliers
    - typiquement un mouvement organique est plus lent au départ et à l'arrivée
        - s'il y a beaucoup de force derrière ce mouvement, il aura une très forte anticipation et un rebond à l'arrivée
    - changement de direction: plus de temps, ralentissement (cf [vidéo de mouvement de pendule](https://www.youtube.com/watch?v=B573sEUDLw8))
        - le ralentissement est d'autant plus visible que l'objet mouvant est lourd et qu'il va vite
        - impression soulignée s'il y a un élément qui suit (cheveux, écharpe, queue, etc.) ([un exemple](https://www.youtube.com/watch?v=Fliz85Kgnww), [un autre exemple](https://www.youtube.com/watch?v=KFWgrzgj7xQ))

## 3) outils d'animation
- docker Timeline
	- ajouter / supprimer une frame
	- déplacer / copier des frames
	- utiliser les calques pour ajouter / enlever un élément sur plusieurs frames d'un coup
	- scroll molette pour se déplacer dans le temps (avec la souris sur le docker Timeline)
	- clic droit sur le nom d'un calque > show in timeline
- docker Animation
	- nombre d'images par seconde (24 pour le cinéma en europe; 12 c'est bien; 6 c'est possible mais un peu limite)
	    - quand on change le nombre d'images par seconde pour ajouter/enlever des détails: sélectionner toutes les frames de la plage concernée dans la timeline, et clic droit sur la sélection > Insert hold frame (ou remove hold frame)
- docker Onion Skin / Pelure d'Oignon
	- cliquer sur les numéros en haut pour l'activer/désactiver pour cette frame
	- cliquer sur le 0 pour le désactiver complètement
	- il faut l'activer pour chaque calque

--  
**EXERCICE 7**  
faire traverser l'image à un trait suivant différents rythmes  
- régulier
- début lent, accélération
- fin lente, décélération
- quasi instantané (sans dessiner dans l'espace entre l'image de début et l'image de fin)  

--  
[](4. fin l1C12)
[](5. fin L1A12 + anticipation)

## 4) principes d'animation 2
- anticipation (prendre de l'élan) - action - réaction (cf [un gif](https://twitter.com/yvesbalak/status/859337493883301888))
    - pour la défense/esquive du joueur, diminuer l'anticipation pour augmenter la réactivité
    - pour l'attaque des ennemis, augmenter l'anticipation pour donner au joueur le temps de réagir
    - l'anticipation sert à préparer le joueur pour qu'il lise mieux l'action
        - et aussi ça fait des animations plus vraisemblables
        - mais quand c'est le personnage que le joueur contrôle il sait déjà ce qu'il va faire
            - donc on n'a pas besoin de prévenir le joueur
                - on perd en vraisemblance mais c'est la vie
                    - si vous voulez pouvoir faire des anims vraiment dans les règles ne faites pas un jeu d'action
- intervalles réguliers
- courbes
    - savoir d'où tu viens où tu vas
- anims décalées
    - une bonne boucle c'est une boucle pour laquelle on peut pas distinguer quelles sont la première et la dernière image (il n'y a pas d'à-coup)
        - pour certains types d'animation (feu, vent dans un arbre, etc.), avoir plusieurs sous-boucles qui commencent à des frames différentes peut aider
- les poses-clé doivent être très claires, aussi bien pour le personnage que pour l'action
    - les intervalles peuvent être un peu moches
        - ce qui compte c'est que l'anim globale soit bien
- squash and stretch, déformations (cf [une animation des looney tunes](https://youtu.be/h8NrKjJPAuw?t=53) à regarder image par image)
- de l'importance de l'anim de "personnage blessé" [](TODO: faire un exemple hurtanim avec/sans)
    - parce que FEEDBACK!!!
- anim de marche (différence marche/course)
    - head bob
    - jambe/bras opposés
    - torse inclinaison
- saut en jeu
    - pas juste une anim mais trois à cinq bouts d'anim
        - début du saut
            - tenir
        - transition
            - tenir
        - atterrissage
- anim vague/fumée/vent/queue
- animations standard d'un personnage d'un jeu de combat:
    - idle
    - marche et/ou course
    - une ou plusieurs attaques
    - mort
    - personnage touché
    - saut (si platformer)

[](5. fin L1B12 - vague; marche rapidement)

**références**  
Looney Tunes, par Warner Bros

## 3) export
- suite d'images
    - File > Render Animation Frames (Fichier > Rendu de l'animation)
        - les images de début et de fin doivent être comprises entre les images de début et de fin du docker Animation
- spritesheet
    - installer ce plugin <https://github.com/Falano/kritaSpritesheetManager>
        - avant l'export, désactiver l'onionskin et les calques superflus (par exemple l'arrière-plan)

## 97) exercices
1) étude du timing
- dessiner un trait.
- Une anim où il traverse l'écran de gauche à droite à une vitesse régulière.
- Une autre où il accélère.
- Une autre où il ralentit.
- Une autre où il le traverse quasi instantanément.

2) courbes d'animation
- dessiner un perso; qu'il soit en position de base de idle; rendre le calque animable et copier cette frame à la frame 3O. Activer l'onionskin avec trois frames devant et trois frames derrière, d'opacité décroissante quand on s'éloigne de la frame actuelle (ou d'une autre manière si c'est plus confortable pour vous). Sur un autre calque, non animé, se faire une palette dans un coin des couleurs du personnage.
- En s'aidant de l'onionskin, faire une anim qui boucle (éventuellement au cours du processus d'animation déplacer la frame de fin si l'anim ne fait pas 30 images): esquive, saut, ou attaque.
- Sur un autre calque, non animé, noter dans une couleur non utilisée ailleurs la position des yeux à chaque frame, et de l'extrémité de chaque membre (mains, jambes, pattes) dans d'autres couleurs.
- Vérifier si ça suit autant que possible une courbe, et que les espacements entre deux points sont réguliers; si non, modifier l'animation pour que ça soit davantage le cas.

3) intervalles (et silhouettes)
- dessiner un perso, choisir une action.
- Décrire l'action en trois à cinq silhouettes (possibilité de marquer l'oeil, mais c'est tout).
- Ajuster le timing en déplaçant les keyframes dans le temps.
- Une fois que c'est bon, ajouter des couleurs.
- Ajouter des silhouettes entre.
- Ajuster le timing et les courbes du mouvement (cf exercice 2)
- ajouter des silhouettes.
- Quand le mouvement a suffisament d'images, mettre en couleur ce qui ne l'est pas.

4) illustration du principe de l'inertie
- tenir un tissu entre ses doigts, en en laissant pendre une grosse partie (par exemple un t-shirt, tenu aux épaules). Avancer les mains brusquement de 30 centimètres, observer le délai avec lequel le reste du tissu suit le mouvement. Tester une action unique (avancer les mains une fois) et une boucle (faire un mouvement de va-et-vient sans s'arrêter). Tester avec des matériaux plus ou moins rigides et lourds (veste en cuir, chemise légère, etc.)
- Dessiner un perso avec un élément secondaire inerte ou semi-inerte (un gosse qui traine un doudou, un personnage avec une queue, une ceinture, une écharpe, ou des cheveux longs, une cape, une pousse de plante sur la tête, etc.).
- Animer un mouvement brusque.
- Etudier comment l'élément secondaire agit.

## 99) Plus de ressources (principalement en anglais)
- anticipation:
    - explication très courte (gif animé): <https://twitter.com/yvesbalak/status/859337493883301888>
    - explication moyenne (article + vidéo): <http://www.dsource.in/course/principles-animation/anticipation>
    - explication plus longue (article + vidéos): <https://www.animationmentor.com/blog/anticipation-the-12-basic-principles-of-animation/>
- anims décalées (article + vidéo): <http://www.dsource.in/course/principles-animation/follow-through-and-overlapping-action>
- timing (vidéo): <https://www.youtube.com/watch?v=rHEJZXvFc5I>
- déformation (vidéo): <https://youtu.be/h8NrKjJPAuw?t=53>
- course (article écrit illustré de gifs): <http://www.lessmilk.com/tutorial/pixel-art-run-cycle>
- intervalles non réalistes pour guider l'oeil: <https://youtu.be/Ih65Kg4DTw8?t=710>

- les 12 principes de l'animation:
    - le bouquin qui en parle à l'origine, jamais traduit en français apparement: The Illusion of Life: Disney Animation, de Frank Thomas et Ollie Johnston
    - un explication sur wikipedia: <https://en.wikipedia.org/wiki/Twelve_basic_principles_of_animation>
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
- quelques [principes généraux d'animation]((https://www.youtube.com/watch?v=uDqjIdI4bF4)) (vidéo)  

## 100) Ressources en français
- un gros bouquin sur les principes d'animation (pas spécifique au pixel art ni au jeu): Techniques d'Animation (The Animator's Survival Kit), de Richard Williams
- les 12 principes de l'animation: https://fr.wikipedia.org/wiki/12_principes_de_base_de_l%27animation
- une [démo vidéo: rapide aperçu des outils d'animation de krita](https://youtu.be/6NWJ119jJaI) (vidéo, pas de son)
- une [vidéo humoristique (par le Joueur du Grenier) sur les choses à ne pas faire dans un jeu](https://www.youtube.com/watch?v=5I7pukuy8sQ)
- une série de photographies décomposant le mouvement: [Animal Locomotion, d'Edward Muybridge (sur wikibooks)](https://fr.wikibooks.org/wiki/Photographie/Personnalit%C3%A9s/M/Eadweard_Muybridge)
- des [vidéos montrant différents mouvements, dont plusieurs marches, à utiliser comme références](https://www.youtube.com/c/endlessreference/videos)
- [plein de marches différentes](https://www.youtube.com/watch?v=cVjIqr8CTtQ)
- une [vidéo (pas de son) de démo d'animation dans krita](https://youtu.be/6NWJ119jJaI)
- [début du cours d'animation (mercredi)](https://youtu.be/cUXbnengUY8)
    - 00:00:00 timing
    - 00:08:00 anticipation
    - 00:11:30 amorti (ralentissement en début ou fin de mouvement)
    - 00:13:45 outils d'animation de krita
    - 00:26:33 exercice
- une [autre démo rapide sur l'animation (timing et animations secondaires, inertie)](https://youtu.be/BscB06QlFfI)

[](5. fin L1C12)
[](6. fin L1AB12; spritesheet rapidement)


# VI. [Finitions](/cours/creation_gestion_ressources_6.html)
# VII. [Exports](/cours/creation_gestion_ressources_7.html)
# VIII. [Game Design](/cours/creation_gestion_ressources_8.html)
# X. [Annexes](/cours/creation_gestion_ressources_0.html)
