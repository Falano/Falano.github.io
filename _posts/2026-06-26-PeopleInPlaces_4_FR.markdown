---
layout: post_cera_FR
title: "Personnes et Lieux - 4 : paramètres du slicer"
tags: FR illu
categories: 3D FR illu
last_updated: 26 juin 2026
description: tutoriel sur la série Personnes et Lieux
permalink: /illu/2026-06-26_PeopleInPlaces_4_FR.html
topnav: topnav_Portfolio_illu_FR
---
\
[< partie précédente: 3D pour impression <](/illu/2026-06-19_PeopleInPlaces_3_FR.html) | [> partie suivante: animation >](/illu/2026-06-19_PeopleInPlaces_5_FR.html)

# Personnes et Lieux: Montagne

|![mountain peeps: 3D print farmer](/assets/art/2D/mountainPeeps_farmer_3Dprint_wm.jpg)|![mountain peeps: 3D print ranger](/assets/art/2D/mountainPeeps_ranger_3Dprint_wm.jpg)|

## Impression 3D

### Paramètres du slicer
- Quand on lui demande de commencer à trancher l'objet (déterminer le trajet de la buse d'impression), il devrait dire "oh non :( il y a besoin de supports, ou ça ne marchera pas du tout. Pourrais-tu, stp, activer la génération de supports?" (pas tout à fait formulé comme ça). Il faudra l'écouter et activer la génération de supports (je n'ai aucune idée de pourquoi ce n'est pas activé par défaut. Je fois le faire à chaque fois, et les impressions pour lesquelles ce n'est pas utile il n'en met de toute façon pas).
- Si vous farfouillez dans les options et que vous voyez l'option "on build plate only" ("sur la plaque d'impression seulement", plus ou moins), vous pensez probablement Mais quelle excellent idée! Après tout, les supports pourraient laisser des traces si on les laisse s'appuyer sur une partie de notre objet, ce qui serait laid. Il vaut mieux lui dire explicitement de l'éviter! Mais c'est une très mauvaise idée. 
- - Du filament qui n'est pas assez soutenu (parce qu'en limitant d'où les supports peuvent partir on limite où ils peuvent arriver) va s'affaisser, ce qui est laid (même si pas super visible si c'est sur le dessous), ou même ne pas imprimer et faire des spaghetti plus loin. Le logiciel essaie déjà de, autant que possible, ne pas mettre de supports sur une partie imprimée de l'objet; donc s'il le fait c'est que c'est nécessaire. Il est inutile de le lui interdire. 
- - La gravité des conséquences dépend des sculptures; pour certaines ça pourrait marcher raisonnablement bien. Mes sculptures à large base étaient probablement particulièrement peu adaptées à cette option. J'ai eu notamment une impression où le support ne pouvait pas atteindre un membre en suspension parce qu'il était trop loin des bords et trop bas, et il ne m'a pas donné de message d'erreur, et a juste commencé à imprimer au milieu du vide. Ce qui, évidemment, n'a pas marché, et a gâché environ un tiers de ma bobine et une dizaine d'heures.
- si vous farfouillez encore et que vous voyez l'option  "only strictly necessary supports" ("uniquement les supports absolument nécessaires"), vous pensez probablement quelle excellente idée! Après tout, retirer les supports est ennuyeux, potentiellement dangereux, et peut parfois laisser des traces. Mieux vaut lui dire explicitement d'en mettre le moins possible! C'est une mauvaise idée pour les mêmes raisons que la précédente: filament qui s'affaisse et problèmes d'impression. Ça dépend de votre filament et de vos autres options (l'angle auquel ajouter des supports, par exemple), mais si vous n'avez pas eu le temps de faire des tests je laisserais cette option décochée. \
\
Filament affaissé au bout de l'objectif:
![a print of mountain peeps: photographer](/assets/art/2D/mountainPeeps_printError_02b.jpg)
Filament affaissé sous le short:
![a print of mountain peeps: hiker](/assets/art/2D/mountainPeeps_printError_02a.jpg)
- J'ai utilisé l'option fuzzy skin (Others > Special Mode; j'utilise le "noise type" Classic). Ça efface un peu les lines d'impression en ajoutant une légère texture (la buse, au lieu d'aller en ligne droite, ajoute un peu d'aléatoire sur le plan horizontal à sa trajectoire), et donne un effet plus mat. Personnellement, je l'aime beaucoup. Je trouve que ça ressemble moins à du plastique.\
\
Comparaison entre trois textures d'impression 3D: à gauche, fuzzy skin en couches de 0.12mm (le choix final pour toute la série); au milieu, la texture de bois procédurale et fuzzy skin en 0.12mm; à droite l'aspect par défaut en 0.20mm.
![mountain peeps: comparison between three 3D prints with different textures](/assets/art/2D/mountainPeeps_04a_textures.jpg)
- l'option "ironing" (Advanced: on; Quality > Ironing) rend les surfaces horizontales plus plates, et leurs lignes d'impression moins visibles; ne fonctionne pas particulièrement bien s'il y a une grande quantité de surfaces presque (mais pas tout à fait) horizontales, mais marche sans doute très bien pour les objets non-organiques.
- le "top surface pattern" (motif de surface horizontale) Hilbert Curve produit un quadrillage de petits trous (même avec l'option "ironing"). Je ne le recommande pas pour les formes organiques.
- le "top surface pattern" Archimedean Chords fait des cercles au centre de la surface. Pour des bases plates circulaires ça m'évoque vaguement un tronçon de bois, ce qui était adapté au reste de l'esthétique de la série.
- le "top surface pattern" Concentric a l'air d'être une bonne idée mais a tendance à produire des sortes de cicatrices bizarres au centre des formes irrégulières. Pour les autres "top surface pattern", je n'ai pas aimé celles avec des lignes droites, qui selon moi détonnaient sur mes bases rondes. Ça dépend de la forme de ce que vous imprimez.\
\
Un exemple de Concentric:
![mountain peeps: a base with weird seams](/assets/art/2D/mountainPeeps_printError_13.jpg) 
- ajouter un petit "brim" (rebord) améliore probablement la stabilité, mais je n'ai pas fait assez de tests pour avoir vu des résultats certains.
- au moment de retirer les supports à la fin de l'impression, le plus efficace a l'air d'être de les attraper délicatement et de les faire basculer de droite à gauche en maintenant fermement (mais délicatement!) la partie permanente de la sculpture. Ce n'est souvent pas possible à cause de parties permanentes de la sculpture qui contraignent notre amplitude de mouvement. Dans ce cas, j'utilise un couteau de peintre et/ou un tournevis, mais il faut faire attention à ne pas endommager la sculpture ou ses doigts.\
\
Un couteau de peintre:
![scrapper](/assets/art/2D/mountainPeeps_printError_03.jpg)
- On m'a dit que si j'érafle la surface, la chauffer doucement avec un sèche-cheveux enlèverait la marque (à ne pas utiliser si on a imprimé avec l'option "ironing"). Je n'ai pas testé.
- Si vous faites des erreurs ou imprimez en plusieurs parties, la colle à bois blanche a l'air très solide sur du PLA (un fois sèche). La glue instantanée que j'ai essayée est restée molle et n'a pas bien marché.

[> partie suivante: animation >](/illu/2026-06-19_PeopleInPlaces_5_FR.html)
