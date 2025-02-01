---
layout: page
title:  "Cours Paris 8: introduction à la 3D avec blender"
last_updated: October 24, 2024
permalink: /cours/introduction_3D/modelisation.html
topnav: topnav_P8_3D
---

# II. Modélisation
(ne pas oublier d'activer Screencast Keys, *alt shift C*)

![Interface Vue 3D de Blender](/assets/cours/blender/001_blender_3Dview_highlights.jpg)

## 0) Le plus important
- barre de recherche: *F3* ou *Edit > Menu Search*
- 1) le plus important: se souvenir qu'une fonctionnalité existe. Une fois qu'on sait ça on peut retrouver comment l'appliquer (et chercher dans les menus). 2) Si possible, se souvenir du nom ou d'une approximation pour utiliser plus facilement la barre de recherche ou internet. 3) Et si vous l'utilisez souvent, vous allez retenir son raccourci clavier et/ou dans quel menu elle est.
- en général il y a plusieurs manières d'appeler une fonctionnalité (par ordre décroissant de commodité d'usage, et croissant de facilité à s'en rappeler): un raccourci clavier, par son nom avec F3 ou Edit > Menu Search, parfois il y a une icône sur un des menus flottants, souvent il y a un menu qui y mène.

## 1) Vocabulaire
Pour la plupart disponibles dans les icônes horizontaux en haut à gauche (sur l'image: 3, Menus de cette fenêtre)
- Points / Sommets / Vertices
- Arêtes / Edges
- Côtés / Faces
- Maillage / Mesh
- Mode Edition & Mode Objet / Edit Mode & Object Mode
- une liste de raccourcis claviers: [ici](http://fablab.web-5.org/lib/exe/fetch.php/ateliers:ateliers:blender:blenderguru_keyboardshortcutguide_v2.pdf) ou [là](https://christiansamek.at/play/blender-shortcuts-hotkeys/)

## 2) Navigation
### a) Navigation de base
Pour la plupart disponibles dans les icônes verticaux en haut à droite (sur l'image: 6, outils de navigation; ou dans le menu View > Navigation (3: Menus de cette fenêtre))
- Tourner la vue: *Cliquer glisser molette* ou *glisser deux doigts au trackpad*
- Zoomer: *Scroll molette* ou *ctrl cliquer glisser molette* ou *ctrl glisser deux doigts au trackpad*
- Déplacer la vue: *shift cliquer glisser molette* ou *shift glisser deux doigts au trackpad*
- Centrer sur la sélection: *Shift S > Cursor to Selected* puis *F3 > Center view to Cursor*  (View > Align View > Align View to Active)
- Edit Mode / Object Mode: *Tab* (pour changer entre tous les modes: *Ctrl Tab*)
- Modes de visualisation des objets/ Wireframe Shading & Solid Shading: *Z* (sur l'image: 5, outils de visualisation)
- Changer de vue: les chiffres du clavier (*1*: face; *ctrl 1*: dos; *3*: côté gauche; *ctrl 3*: côté droit; *7*: vue du dessus; *ctrl 7*: vue du dessous; *9*: inverser la vue; *5*: dés/activer la vue perspective; *2*: tourner vers le bas; *8*: tourner vers le haut; *4*: tourner vers la gauche; *6*: tourner vers la droite; *0*: dés/activer la vue caméra) (sur l'image: 6, outils de navigation)

### b) EXERCICE 1: trouver toutes les balles magenta dans le projet
[projet à télécharger et ouvrir dans blender](https://drive.google.com/file/d/1Xfb--nWN8O554KVzoWfwkGJ16izp3uGI/view?usp=drive_link) (+- 20 minutes)

## 3) Bases de la modélisation
- tout d'abord, augmenter le nombre d'annulations possibles. Par défaut c'est 32, passer à 64 et voir si ça suffit mais ne ralentit pas trop l'ordi (Edit > Preferences > System > Memory and Limits > Undo Steps: 64)
### a) actions
Pour la plupart disponibles dans la barre verticale d'icônes d'outils à gauche (sur l'image: 1, Outils courants, ou dans le menu 3: Menus de cette fenêtre)
- choisir différents modes de sélection: *W* (utiliser shift pour ajouter à la sélection, ctrl pour enlever à la sélection (ou: menu Select))
- Extruder (créer une copie liée): *E*
- Déplacer / Grab: *G*
- Tourner / Rotate: *R*
- Redimensionner / Scale: *S*
- Menu pour ajouter des sommets: *ctrl E*; contient Subdivide (ajouter des vertices aux edges/faces sélectionnés sans modifier l'aspect extérieur de l'objet, juste sa géométrie), Loup Cut and Slide (raccourci direct: *ctrl R*) pour ajouter une boucle d'arêtes (on peut en ajouter plusieurs d'un coup en scrollant)
- pour valider une action, *clic gauche* ou *enter*; pour l'annuler, *clic droit* ou *echap*
- montrer une poignée pour déplacer/tourner/redimensionner: icônes horizontaux en haut à droite: Viewport gizmos > Active Object

### b) EXERCICE 2: modéliser une table

### c) préciseurs d'actions
Pour la plupart disponibles dans la barre horizontale d'icônes de menus au milieu en haut (sur l'image: 4, Centres, axes, magnétisme)\
Utilisables pour les actions de base (déplacement notamment) mais aussi pour n'importe quelle action suivie d'un mouvement (extrusion, duplication, etc.)
- contraindre à un axe: *clic molette* ou *Z*, *X*, ou *Y* en fonction de de quel axe il s'agit
- modifier par incréments: *ctrl*
- édition proportionelle / proportional editing: *O*
- Transform Orientation!
- Transform Pivot Point

### d) plus d'actions
- pour info la plupart des actions ont des options (menu temporaire en bas à gauche de la vue 3D, qui n'apparaît que quand on fait une action)
- menu d'ajout de mesh: *shift A* (ou Add > le mesh qu'on veut)
- Supprimer: *Suppr / Del*
- Créer une face ou un côté entre les points/côtés sélectionnés / Fill: *F* (parfois si on ne sélectionne qu'un côté il arrive à deviner comment remplir les autres et on peut appuyer plusieurs fois sur F pour remplir rapidement tout un "couloir" vide)
- Fusionner / Merge: *M*
- Recentrer la vue sur la sélection: *Shift S > Cursor to Selected* puis *F3 "center" > Center View to Cursor*
- Tout sélectionner: *A*
- Tout désélectionner: *A A*
- Sélection de sommets/arêtes/faces (menu en haut dans la vue 3D, à droite de Edit Mode - n'est pas disponible en Object Mode)
- Sélectionner une boucle de sommets/arêtes/faces: *double clic* ou *alt clic* selon votre configuration
- Pour les arêtes spécifiquement: la commande précédente crée une boucle dans la continuité de l'arête. Pour une boucle d'arêtes transversales (comme les poutres d'un chemin de fer), c'est: *ctrl double clic* (ou, j'imagine, *ctrl alt clic*)
- Dupliquer un objet / des sommets: *Shift D*
- Diviser la vue: tirer un des angles. Tirer vers l'intérieur d'une vue la divise, tirer en traversant la délimitation entre deux vues les fusionne.
- plein écran: *ctrl espace*
- changer entre sélection de points, arêtes, ou faces (ne marche que si pas "emulate numpad"): *1*, ou *2*, ou *3* (sinon, utiliser la souris et le bouton du menu en haut à gauche)

### e) EXERCICE 3: modéliser une chaise

### f) encore plus d'actions
- Déchirer (dé-fusionner) / Rip: *V* (si seul un vertex est sélectionné, l'arête sur l'axe le plus proche de la souris reste entière, celle le plus loin s'ouvre)
- Relier deux suites d'arêtes par plusieurs faces / Bridge Edge Loops: *ctrl E*
- Couteau / Knife: *K*; ajouter des sommets et des arêtes sans modifier la forme de la surface
- si on sélectionne un sommet/arête/face, et avec *ctrl* appuyé on en sélectionne un autre, ça sélectionne un chemin entre les deux
- Sélectionner tout ce qui est lié: *L*
- Joindre deux sommets en un: *M* (Mesh > Merge)
- joindre deux objets en un: *ctrl J* (Object > Join) (ça ne change pas la géométrie, mais maintenant les vertices des deux sont considérés comme appartenant au même objet, donc on peut y accéder en même temps en edit mode)
- séparer un objet en deux (ou plus): *P* (Mesh > Separate) (l'inverse du précédent)
- déplacer le centre d'un objet: il y a un mini menu "Options" juste en bas de 5 du screenshot (haut droite vue 3D)
- pour décaler un vertex ou un edge le long de la surface de leur objet (donc ça change la géométrie mais ça ne change pas son aspect), c'est *GG*
- tester les différents modes de suppression des vertices/edges/faces (delete simple fait un trou, dissolve remplit ce trou, collapse crée un vertex au centre)

### g) Faire un terrain rapidement
- pour info, dans les option des actions: pour Subdivide (*ctrl E*), si on augmente la valeur "fractal", on peut faire des terrains rapidement (ajouter un Modifier Subdivision Surface après, éventuellement, pour lisser) (penser à tout sélectionner avant, en edit mode)
- de temps en temps quand vous utilisez une action pensez à regarder quelles sont ses options. Au cas où il y en aurait d'intéressantes.
- sinon faites un plan, ajoutez-lui un Modifier Deform > Displace, et mettez une texture voronoi
- sinon sélectionnez quelques vertices et bougez-les (plusieurs fois, avec plusieurs groupes de pixels différents) avec Proportional Editing (milieu haut de la vue 3D) activé et en changeant de temps en temps le type de Falloff
- ou un mélange de tout ça

### h) EXERCICE 4: faire un terrain

## 4) Modificateurs / Modifiers
icône clé de bricolage dans la colonne d'outils à droite (pas dans la vue 3D, mais dans la vue des Propriétés / Properties), puis cliquer sur Add Modifier
### a) Miroir / Mirror
- Pour n'avoir à modéliser que la moitié de l'objet.
- Penser à supprimer la moitié en trop en edit mode.
- Generate > Mirror
- Axis: l'axe de symmétrie
- Merge: la distance à laquelle on fusionne deux points très proches (utile pour la limite entre ce qu'on a modélisé et son autre moitié)
- après avoir fait des changements vérifier que la ligne des pixels qui sont au centre de l'objet (entre les deux moitiés), vérifier qu'elle est bien droite. Si non, ou si pas sûr, la sélectionner (par exemple en vue du haut avec *B* la sélection rectangulaire) et faire *S*, *Y*, *0* pour l'aplatir sur l'axe Y (ou un autre axe si applicable)
- par précaution après l'avoir appliqué essayer de faire aussi un Merge > Merge by distance avec une distance très courte (pour supprimer les vertices en double)
- ou un Modifier Generate > Weld (un Merge sous forme de Modifier)

### b) Subdivion Surface
- Pour rendre plus rondes les formes. Utile pour la modélisation organique.
- Generate > Subdivision Surface
- Levels 1 ou 2 suffisent. Avec level 4 ou 5 vous allez faire planter votre ordi si vous travaillez sur quelque chose de plus compliqué qu'un cube.
- Ajouter une arête tout près d'une autre existante pour rendre un angle plus aigû.
- ou utiliser *ctrl E > Edge Crease* pour définir la dureté des arêtes sans modifier la géométrie

### d) Divers
- Tester l'ordre des modifiers.
- Il est souvent utile d'appliquer un modifier avant de l'exporter dans un autre format/pour un autre programme. Mais il est aussi souvent utile de le conserver non-appliqué le plus longtemps possible en cas de changements imprévus.
- Pour info il y a un modifier pour diminuer le nombre de points d'un mesh (Decimate) - par contre éviter de l'utiliser si l'objet a une texture UV ou va être riggé et animé.
- le modifier Deform > Shrinkwrap est pour qu'un objet suive la courbe de la surface de l'objet cible (qu'on peut rendre invisible); par exemple, pour la grille d'un masque d'escrime
- le modifier Deform > Curve fait la même chose mais en suivant une courbe
- quelques [exemples d'utilisation de modifiers](https://drive.google.com/file/d/1ERQjcd20L9X6hAUbJVpHju46o36Qu-ZG)
- Shade Smooth / Shade Flat / Shade Auto Smooth (en Object Mode): est-ce que, dans la gestion des ombres / du volume des objets, on voit chaque face (flat) ou est-ce que les arêtes sont lissées (smooth) ou est-ce que le choix est fait pour chaque arête en fonction de son angle (auto smooth).

### d) EXERCICE 5: modéliser un personnage organique (humain, animal, plante, etc.)

## 5) Modélisation mécanique (machines, objets artificiels)
### a) Divers
- la duplication liée (par exemple: pour les roues d'une voiture): *alt D* pour créer des objets pour lesquels si on change la géométrie de l'un les modifications s'appliquent à toutes ses copies liées
- poser un objet sur une surface existante (par exemple: pour poser des boulons sur une machine ou des coquillages sur une baleine): dans la vue 3D, dans les options (milieu haut) avec les axes, le magnétisme et les centre de rotation, activer le magnétisme (icône d'aimant) et (quand on clique sur l'icône juste à droite de l'aimant pour définir les options du magnétisme) mettre Snap Target à Face; éventuellement si c'est un objet (comme un boulon) où l'orientation est importante, activer Align Rotation to Target et Affect > Rotate

### b) Modifier Array
- le modifier de copie espacée (par exemple: pour faire un parquet comme dans l'exercice où il fallait trouver les balles; ou un collier de perles):  modifier Generate > Array.
- Count détermine combien de copies on fait. (alternativement on peut utiliser d'autres Fit Type où la taille du modifier est déterminée autrement; faites des tests)
- Relative Offset utilise comme unité la dimension de l'objet, Constant Offset utilise une unité de mesure non liée à l'objet (les mètres)
- Pour des copies en ligne, utiliser un modifier Array. Pour des copies en rectangle, en utiliser deux (le nombre de copies sera le Count du premier fois le Count du second).
- on peut aussi utiliser un objet comme référence de modification. Ça permet de l'animer facilement (même sans objet les paramètres sont animables, mais ça peut être moins agréable d'animer des chiffres que la position d'un objet dans l'espace, selon ce qu'on veut faire), mais surtout ça permet de changer sa rotation (ce qui fait que la prochaine itération est selon le nouvel axe) et son échelle (ce qui modifie l'échelle de la prochaine itération aussi)
- couplé avec le Modifier Deform > Curve, on peut les dupliquer le long d'une courbe (si ça donne un résultat bizarre déplacer l'objet pour qu'il ait le même centre que la courbe qu'il suit) (attention: que le modifier array soit au-dessus du modifier curve, pour que la courbe influence toutes les copies générées par l'array)

### c) Courbes
- en plus des mesh, on a des objets de type "courbe" (Curve)
- utile pour par exemple les cordes
- donc on crée une courbe (Object Mode: Add (ou *shift A*) > Curve), ou bouge les poignées pour qu'elle ait la forme qu'on veut (observer ce qu'il se passe quand on bouge chacune des poignées), puis Properties > Data > Geometry > Bevel > Depth permet de lui donner une épaisseur. Si on ne veut pas que ce soit rond, on choisit Object (ou Profile) au lieu de Round (dans Bevel)
- et pour avoir un nombre pas absolument excessif de vertices, on se met en vue Wireframe (fil de fer) pour voir ce qu'on fait et on descend Properties > Data > Geometry > Bevel > Resolution à 1 ou 2, et Properties > Data > Shape > Resolution Preview U à entre 3 et 7 (ça dépend de votre projet, mais le défaut de 12 est presque toujours inutilement détaillé et lourd)
- et on peut continuer à modifier la courbe et le mesh généré suit.
- on peut passer d'un type d'objet à l'autre en utilisant en Object Mode le menu Object > Convert > Mesh (ou Curve, en fonction de dans quel sens vous le faites) (alternativement: F3: Convert) (mais vu qu'une Curve c'est une ligne, transformer un Mesh en Curve ça ne marchera que si votre Mesh aussi c'est une ligne)
- *alt S* (F3: Radius) pour changer l'épaisseur de la courbe à chaque point

### d) Autres Modifiers (wireframe, bevel, simple deform, booléen)
- le Modifier Generate > Wireframe ne remplit pas les faces mais montre les edges: par exemple pour les grillages
- le Modifier Generate > Bevel adoucit les angles (et peut le faire par valeur d'angle)
- pour faire un objet cylindrique à partir de juste sa silhouette: Modifier Generate: Array + Deform: SimpleDeform (Bend, 360°, choisir le bon axe)
- le Modifier Generate > Boolean permet de ne montrer des parties de l'objet A que celles qui sont aussi dans l'objet B (intersect), ou que celles qui ne sont pas dans l'objet B (difference) (dans le paramètre Object, mettre l'objet B). Dans la vue 3D, être en mode de visibilité (*Z*) Solid, puis avec l'objet B sélectionné, aller dans Properties > Object > Viewport Display > Display As: Wire pour voir le résultat de l'opération booléenne (et rendre l'objet B invisible au rendu, en cliquant sur l'icône de caméra dans l'Outliner).
