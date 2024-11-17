---
layout: page
title:  "Cours Paris 8: introduction à la 3D avec blender"
last_updated: October 24, 2024
permalink: /cours/introduction_3D/modelisation.html
topnav: topnav_P8_3D
---

# II. Modélisation
(ne pas oublier d'activer Screencast Keys)

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
TODO: UPLOAD!!!!!

## 3) Bases de la modélisation
- tout d'abord, augmenter le nombre d'annulations possibles. Par défaut c'est 32, passer à 64 et voir si ça suffit mais ne ralentit pas trop l'ordi (Edit > Preferences > System > Memory and Limits > Undo Steps: 64)
### a) actions
Pour la plupart disponibles dans la barre verticale d'icônes d'outils à gauche (sur l'image: 1, Outils courants, ou dans le menu 3: Menus de cette fenêtre)
- Différents modes de sélection: *W* (utiliser shift pour ajouter à la sélection, ctrl pour enlever à la sélection (ou: menu Select))
- Extruder (créer une copie liée): *E*
- Déplacer / Grab: *G*
- Tourner / Rotate: *R*
- Redimensionner / Scale: *S*
- Ajouter des sommets à l'intérieur d'une face/côté / Loop cut: *ctrl R* (possibilité d'ajouter plusieurs boucles parallèles en scrollant) ou *clic droit > subdivide* (n'utiliser le subdivide que si on a sélectionné une boucle transversale d'arêtes)
- pour valider une action, *clic gauche*; pour l'annuler, *clic droit*
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
- menu d'ajout de mesh: *shift A* (ou Add > le mesh qu'on veut)
- Supprimer: *Suppr / Del*
- Créer une face ou un côté entre les points/côtés sélectionnés / Fill: *F*
- Fusionner / Merge: *M*
- Recentrer la vue sur la sélection: *Shift S > Cursor to Selected* puis *F3 "center" > Center View to Cursor*
- Tout sélectionner: *A*
- Tout désélectionner: *A A*
- Sélection de sommets/arêtes/faces (menu en haut dans la vue 3D, à droite de Edit Mode - n'est pas disponible en Object Mode)
- Sélectionner une boucle de sommets/arêtes/faces: *double clic*
- Sélectionner une boucle transversale d'arêtes: *ctrl clic*
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
- joindre deux objets en un: *ctrl J* (Object > Join)
- séparer un objet en deux (ou plus): *P* (Mesh > Separate)
- déplacer le centre d'un objet: il y a un mini menu "Options" juste en bas de 5 du screenshot

## 4) Modificateurs / Modifiers
icône clé de bricolage dans la colonne d'outils à droite (pas dans la vue 3D, mais dans la vue des Propriétés / Properties)
### a) Miroir / Mirror
- Pour n'avoir à modéliser que la moitié de l'objet.
- Penser à supprimer la moitié en trop en edit mode.
- Generate > Mirror
- Axis: l'axe de symmétrie
- Merge: la distance à laquelle on fusionne deux points très proches (utile pour la limite entre ce qu'on a modélisé et son autre moitié)

### b) Subdivion Surface
- Pour rendre plus rondes les formes. Utile pour la modélisation organique.
- Ajouter une arête tout près d'une autre existante pour rendre un angle plus aigû.
- Levels 1 ou 2 suffisent. Avec level 4 ou 5 vous allez faire planter votre ordi si vous travaillez sur quelque chose de plus compliqué qu'un cube.
- Generate > Subdivision Surface

### c) Divers
- Tester l'ordre des modifiers.
- Il est souvent utile d'appliquer un modifier avant de l'exporter dans un autre format/pour un autre programme. Mais il est aussi souvent utile de le conserver non-appliqué le plus longtemps possible en cas de changements imprévus.
- Shade Smooth / Shade Flat / Shade Auto Smooth (en Object Mode): est-ce que, dans la gestion des ombres / du volume des objets, on voit chaque face (flat) ou est-ce que les arêtes sont lissées (smooth) ou est-ce que le choix est fait pour chaque arête en fonction de son angle (auto smooth).
- Pour info il y a un modifier pour diminuer le nombre de points d'un mesh (Decimate) - par contre éviter de l'utiliser si l'objet a une texture UV ou va être riggé et animé.

### d) EXERCICE 3: modéliser un personnage organique (humain, animal, plante, etc.)

