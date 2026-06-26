---
layout: post_cera_FR
title: "Personnes et Lieux - 3 : impressions 3D"
tags: FR illu
categories: 3D FR illu
last_updated: 26 juin 2026
description: tutoriel sur la série Personnes et Lieux
permalink: /illu/2026-06-26_PeopleInPlaces_3_FR.html
topnav: topnav_Portfolio_illu_FR
---
\
[< partie précédente: textures <](/illu/2026-06-26_PeopleInPlaces_2_FR.html) | [> partie suivante: paramètres du slicer >](/illu/2026-06-26_PeopleInPlaces_4_FR.html)

# Personnes et Lieux: Montagnes

|![mountain peeps: 3D print farmer](/assets/art/2D/mountainPeeps_farmer_3Dprint_wm.jpg)|![mountain peeps: 3D print ranger](/assets/art/2D/mountainPeeps_ranger_3Dprint_wm.jpg)|

## Impression 3D

### Étapes
- Donc on a un personnage modélisé en 3D. Le mien est au format .blend.
- Il faut l'exporter en .stl, 
- puis l'importer dans un logiciel de préparation à l'impression 3D (un Slicer: "trancheur") comme Bambu Studio ou Cura Ultimaker, et l'y découper, 
- puis l'exporter au bon format (le mien est .gcode.m3f, mais je suppose qu'il existe d'autres formats qui font ça),
- puis le donner à l'imprimante pour qu'elle l'imprime.
- Pour info, la plupart de mes personnages font environ 13cm de haut et ont pris environ 5 à 8 heures chacun à imprimer, avec le plus petit qui n'a pris que 2 heures (le photographe: environ 9x9x9cm) et le plus gros (le spéléologue: environ 25x20x25cm) 31 heures. Le logiciel de tranchage fournit cette information (avant le début de l'impression), ainsi que la quantité de filament (par poids et par longueur) qui sera utilisée. J'avais les options fuzzy skin et 0.12mm activées, ce qui semble multiplier par deux le temps d'impression.

Mais il y a un certain nombre de choses auxquelles faire attention, particulièrement si vous avez fait vous-même les fichiers 3D, et ne les avez pas encore testés. Si ce sont des fichiers 3D achetés/téléchargés, ils seront probablement beaucoup plus simples d'utilisation (mais moins fun!) parce que tout ce processus de calibrage et de test aura déjà été fait.\
\
J'ai l'impression d'avoir fait chaque erreur qu'il était possible de faire, mais il est certain que j'en trouverai de nouvelles la prochaine fois que j'imprime en 3D. En voici une liste:

### Dans le logiciel de 3D
- La toute première chose à faire, si le personnage a été conçu comme destiné à rester dans l'ordinateur et non être imprimé, est vérifier qu'il peut tenir debout. La 3D dans un ordinateur peut voler, mais les *impressions* 3D sont soumises aux limitations de la physique. J'ai ajouté une base parce que j'aimais le rendu et que j'avais plusieurs personnages composés de plusieurs éléments qui ne se touchaient pas, mais faites selon votre goût.

|pour impression 2D|pour impression 3D|
|![mountain peeps: 3D print speleo](/assets/art/2D/mountainPeeps_differences_02_wm.jpg)|![mountain peeps: 3D print speleo](/assets/art/2D/mountainPeeps_differences_01_wm.jpg)|
|![mountain peeps: 3D print monk](/assets/art/2D/mountainPeeps_differences_05_wm.jpg)|![mountain peeps: 3D print speleo](/assets/art/2D/mountainPeeps_differences_04_wm.jpg)|
|![mountain peeps: farmer](/assets/art/2D/mountainPeeps_differences_08_wm.jpg)|![mountain peeps: farmer](/assets/art/2D/mountainPeeps_differences_09_wm.jpg)|


- S'assurer que le dessous de la sculpture est parfaitement plat: aller en vue de côté (en mode transparent/wireframe), sélectionner tous les vertices du plan du bas, puis les redimensionner à 0 sur l'axe Z (SZ0). Faire très attention à ce que l'origine de la transformation soit "center" (centre), que le Proportional Editing (édition proportionnelle) ne soit pas activé, et que les axes soient en mode Global. Ce sont les valeurs par défaut mais vous auriez pu les changer en travaillant.
- Si vous vous demandez si quelque chose est trop fin, la réponse est toujours oui. Si vous ne vous le demandez pas, vous avez tort et vous devriez. N'oubliez pas que la capacité à zoomer quasiment à l'infini est spécifique aux fichiers qui restent dans un ordinateur, et n'est pas conservée par les filaments d'impression 3D. 
- - Si vous avez, par exemple, des pattes ou becs d'oiseaux, des antennes radio, des choses comme ça, qui sont très fines exprès et serviront de support à quelque chose d'autre, alors: sélectionnez les edge loops (donc en mode sélection d'arêtes et pas de sommets ou de faces; alt clic, transform orgin: individual; pour que ça devienne plus large mais pas plus long) et redimensionnez-les de 1.5 ou 2. Ça semblera beaucoup trop gros. Ignorez-le. Sauvegardez et fermez le fichier, allez faire autre chose, puis ouvrez-le à nouveau. Maintenant ça a l'air ok. Redimensionnez-le à 1.5 à nouveau. Allez faire autre chose. Ouvrez-le à nouveau. Maintenant il devrait être à la bonne taille. 
- - Si vous ne faites pas ça, la partie fine soit n'imprimera pas (plus fine qu'un filament) ou sera très fine et fragile, et la partie qu'elle soutient tombera au cours de l'impression. L'imprimante essaiera alors d'imprimer par-dessus cette couche qui est absente parce qu'elle n'a pas imprimé ou est tombée; il extrudera du filament mais il restera attaché à la buse et fera des spaghetti sur la partie à imprimer suivante, et n'imprimera pas cette partie sans support.

|fichier pour impression 2D/animation: pieds fins|fichier pour impression 3D: pieds, têtes et ailes plus épais|
|![mountain peeps: farmer](/assets/art/2D/mountainPeeps_differences_06_wm.jpg)|![mountain peeps: farmer](/assets/art/2D/mountainPeeps_differences_10_wm.jpg)|
|![mountain peeps: hermit](/assets/art/2D/mountainPeeps_differences_07_wm.jpg)|![mountain peeps: hermit](/assets/art/2D/mountainPeeps_differences_11_wm.jpg)|

Ermite v1: les poules n'ont pas été imprimées, ainsi que la houe et le bras dont elle supportait le poids:
![mountain peeps: hermit](/assets/art/2D/mountainPeeps_printError_05b.jpg)

Ermite v2: après que les pieds et têtes des poules et la lame de la houe aient été épaissies, tout s'est raisonnablement bien imprimé; les pattes qui sur l'écran semblaient fort épaisses sont en fait tout à fait raisonnables:
![mountain peeps: hermit](/assets/art/2D/mountainPeeps_printError_05a.jpg)

Fermier v1: le corbeau d'avant-plan a d'abord été bien imprimé mais la tête est tombée parce que le bec était trop fin au niveau du sol; le corbeau d'arrière-plan a des spaghetti provenant de l'impression faillie du troisième corbeau (celui qui vole) dont les ailes étaient trop fines. L'impression a été arrêtée en cours de route:
![mountain peeps: farmer](/assets/art/2D/mountainPeeps_printError_10a.jpg)

Fermier v2: les têtes et pieds des corbeaux ont été épaissies, ainsi que les ailes du troisième. Le manche de la fourche a été imprimée à part, à l'horizontale, suite à un problème lors de l'impression précédente:
![mountain peeps: farmer](/assets/art/2D/mountainPeeps_farmer_3Dprint_wm.jpg)

- Il faut enlever les arêtes/sommmets non-manifold. 
- - Explication: Un objet modélisé en 3D et destiné à l'impression 3D est comme une forme faite d'eau, les faces étant la surface de l'eau. L'objet a un intérieur d'eau et un extérieur de non-eau. Chaque face pour être manifold (et donc correcte pour l'impression 3D) doit avoir une face interne, côté eau, et une face externe, côté non-eau. Il peut y avoir des bulles (un bout de non-eau inclus dans l'eau), mais pas deux intérieurs séparés par une seule face. Les configurations non-manifold les plus fréquentes sont une face manquante (l'intérieur communique avec l'extérieur, on ne sait plus ce qui est interne ou externe) ou une face en trop à l'intérieur (les deux côtés de la face sont des côtés internes). 
- - Note: les artistes 3D pour les éléments de décor dans les jeux n'ont pas ces contraintes et créent parfois activement des objets non-manifolds pour des raisons de performances.
- - Pour enlever les arêtes/sommets non-manifold, il est possible de télécharger un outil vérifiant la topologie (j'utilise l'addon de Blender: Topology Doctor). Parfois il me dit que j'ai des endroits non-manifold et me montre ce qui ressemble à un sommet absolument sans problème, et je n'y touche pas et ça imprime quand même, mais il est prudent de vérifier et de réparer ce que l'on peut.
- sélectionner tous les sommets et changer les normales vers l'extérieur (alt N > recalculate Outside). C'est peu souvent utile mais quand ça l'est c'est important. 
- - Si les normales ne sont pas comme il faut et que le slicer a prévu de ne pas imprimer une partie de l'objet à cause de ça, cette partie devrait être vert foncé (mais parfois c'est vert foncé sans raison et ça ne pose pas de problème). 
- - Il est aussi parfois possible de remarquer des problèmes potentiels en regardant les supports: si la partie manquante sert de support à une autre partie, le slicer aura ajouté des supports pour soutenir la partie supérieure (mais c'est dur à remarquer s'il y a des supports partout).

Sans doute à cause d'un problème de normales, le fichier pour l'imprimante a fait imprimer les jambes, le torse, mais pas la ceinture au milieu. J'ai réimprimé juste la ceinture et je les ai collés ensemble (avec de la colle à bois blanche):

|![mountain peeps: 3D print of hunter, cut in half](/assets/art/2D/mountainPeeps_printError_01a.jpg)|![mountain peeps: 3D print of hunter, glued back together](/assets/art/2D/mountainPeeps_printError_01b.jpg)|


- si la plupart de vos faces sont rectangulaires, sachez que le .stl en fera des triangles (en les coupant en deux en diagonale). Pour pouvoir vérifier ce que ça va donner (quelle diagonale il choisira, notamment), il est possible d'ajouter le modifier Triangulate (en gardant le comportement d'export par défaut, qui applique les modifiers à l'export). Si le résultat avec Triangulate ne vous satisfait pas, vous pouvez changer les options de Triangulate et/ou bouger quelques sommets, maintenant avec un aperçu en temps réel.
- si ce n'est pas trop compliqué, envisagez sérieusement d'exporter votre fichier en plusieurs parties (en séparant le personnage du décor, ou en coupant un personnage en plusieurs parties; mais faites un test avant pour vérifier si ça s'emboite bien, en prenant en compte la place perdue due à l'option fuzzy skin). 
- - Au début j'ai tout exporté en un seul fichier (par personnage), et j'ai perdu beaucoup de temps et de filament chaque fois qu'une impression avait un problème à hauteur de cheville, comme la majorité du matériau était dans la base de la sculpture. Si j'avais imprimé le personnage et sa base séparément, je n'aurais pas eu à réimprimer la base (qui elle n'avait pas de problèmes) plusieurs fois.
- - Pour le naturaliste / garde forestier, la plateforme, quand imprimée d'un bloc, nécessite énormément de supports. Quand j'ai imprimé la partie horizontale de la plateforme d'un côté, et les pieds (imprimés à plat pour qu'ils ne tombent pas) de l'autre, je n'ai presque plus eu besoin d'imprimer de supports.

Garde forestier en cours d'impression (avant-plan): beaucoup de filament utilisé sur les supports (modèle: 84g, support: 62g, total: 146g); de plus, les deux pieds de l'échelle devraient toucher le sol mais l'un d'eux semble être tombé:
![a print of mountain peeps: fire lookout](/assets/art/2D/mountainPeeps_printError_08a.jpg)

Garde forestier en plusieurs parties, avant d'avoir enlevé les supports: il y a beaucoup moins de supports (modèle: 84g, support: 26g, total: 110g) que dans la version précédente, ce qui utilise donc moins de filament (58% de filament gagné sur le poids des supports, 25% sur le poids total):
![a print of mountain peeps: fire lookout](/assets/art/2D/mountainPeeps_printError_08b.jpg)

Garde forestier recollé: des éléments s'emboitant entre la plateforme et ses pieds le rendent solide:
![a print of mountain peeps: fire lookout](/assets/art/2D/mountainPeeps_printError_08c.jpg)

- si vous avez séparé votre fichier .blend en plusieurs fichiers .stl, vous pouvez aussi arrêter seulement la partie de l'impression qui a un problème et laisser les autres continuer (moins de perte de filament et de temps)
- Je n'ai pas encore trouvé de manière efficace et marchant à tous les coups de séparer les sculptures et d'imbriquer les différentes parties, à part en les sculptant à la main (ce qui prend beaucoup de temps). Je n'ai pas réussi à faire marcher de manière fiable les modifiers Solidify et Boolean Substraction.
- Quasi-systématiquement, quand j'ai imprimé quelque chose de long et fin, vertical (le manche de la fourche du fermier, les pieds et l'échelle de la plateforme du garde forestier), c'est tombé pendant l'impression. Imprimez-le séparément, horizontalement.

Le manche de la fourche du fermier est tombé donc les couches suivantes ont fait des spaghetti courts sur le support qui longe sa jambe d'avant-plan:
![a print of mountain peeps: farmer](/assets/art/2D/mountainPeeps_printError_10b.jpg)

J'ai dû imprimer le manche deux fois suite à un problème d'impression: ça n'a gâché que très peu de matériau, comme ce n'était qu'une toute petite partie de l'impression:
![a print of mountain peeps: farmer](/assets/art/2D/mountainPeeps_printError_10c.jpg)

Le manche, collé: ça marche très bien (mais pour une version finale, il serait plus solide d'imprimer toute la fourche à part, pas juste le manche):
![a print of mountain peeps: farmer](/assets/art/2D/mountainPeeps_farmer_3Dprint_wm.jpg)


[> partie suivante: paramètres du slicer >](/illu/2026-06-26_PeopleInPlaces_4_FR.html)
