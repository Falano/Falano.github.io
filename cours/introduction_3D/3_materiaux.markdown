---
layout: page
title:  "Cours Paris 8: introduction à la 3D avec blender"
last_updated: October 27, 2024
permalink: /cours/introduction_3D/materiaux.html
topnav: topnav_P8_3D
---

# III. Matériaux
## 0) Shading et Rendus
### a) Shading
- *F3 > Shade Smooth* ou *Shade Flat* pour décider de si on veut que chaque face soit visible individuellement (par exemple pour un cube) ou que la limite des faces soit polie (comme pour une courbe)
- en Edit Mode on peut assigner des angles visibles à certaines arêtes (Mark Sharp ou Clear Sharp)
- Object Mode: *F3 > Shade Auto Smooth*; ou Edit Mode: *F3 > Set Sharpness by Angle*: on peut aussi dire qu'au-dessus d'un certain angle c'est Sharp, et en dessous c'est Smooth (ce qui est selon moi ce qui rend le mieux pour du low-poly mais testez)

| Shading Modes
|-|-|-|
|![flat shading](/assets/cours/blender/002a_blender_ShadingFlat.jpg)|![smooth shading](/assets/cours/blender/002b_blender_ShadingSmooth.jpg)|![autosmooth shading](/assets/cours/blender/002c_blender_ShadingAutoSmooth.jpg)|

### b) Rendus
- la plupart des matériaux peuvent être visibles dans la vue 3D
- mais pas tous; certains, pour les voir correctement, vous avez besoin d'un rendu
- un rendu c'est *F12* ou Render > Render Image dans le menu général de Blender tout en haut hors de la vue 3D (et *F11* (Render > View Render) pour réafficher la dernière image générée)
- et vous avez besoin de lumière. Mon organisation de base pour des rendus rapide c'est de mettre trois soleils (Object Mode, *shift A* > Light > Sun) et de les tourner de manière à ce qu'ils couvrent tous les angles (leur position n'a pas d'influence sur le résultat). Personnellement j'aime bien qu'ils aient tous une intensité différente (Properties > Light > Strength), et aussi une couleur très légèrement différente, avec celui qui pointe vers le bas qui est le plus fort, mais faites des tests et voyez ce que vous préférez (on verra les lumières plus en détail plus tard, là ce n'est pas le sujet).
- et positionnez bien l'objet caméra. *0* permet de voir la vue caméra dans la vue 3D, et *ctrl alt 0* ou View > Align View > Align Active Camera to View déplace et tourne la caméra pour qu'elle voie ce que vous voyiez avec votre point de vu actuel dans la vue 3D.
- par ailleurs: par défaut les rendus sont très lent. Pour les rendre plus rapides:
- Properties > Render > Sampling > Render > Samples: le mettre à entre 4 et 16 (faire des tests) (si la vue 3D en mode de visualisation Material Preview est trop lente, diminuer aussi les Samples du Viewport)
- Properties > Output > Format > %: vous pouvez baisser cette valeur (la mettre à 75 ou 50%) si vous n'avez pas besoin d'une très grande résolution et que c'est juste une preview rapide
- et dans l'Image Editor (la fenêtre dans laquelle s'affiche votre rendu), vous pouvez faire Image > Save As pour sauvegarder votre rendu

## 1) Assigner plusieurs matériaux simples
### a) Créer plusieurs matériaux
- *Z > Material Preview* pour voir ce qu'on fait dans la vue 3D
- onglet Matériaux / Material
- "+" puis "New" pour créer un nouveau matériau
- Base Color: change la couleur de base
- Metallic et Roughness c'est la réflectivité du matériau
- Alpha: transparence (0: invisible; 1: opaque)

### b) Lier les matériaux à certaines faces
- se mettre en mode sélection de faces
- sélectionner les faces qui auront le deuxième matériau
- onglet Material > Assign
- (Select sélectionne toutes les faces de cet objet qui ont été attribuées au matériau actif; deselect les déselectionne)
- d'ailleurs *ctrl +* agrandit la sélection, *ctrl -* la diminue (si on a un pavé numérique; sinon aller dans Select > More/Less > Less (ou: More))

### c) Note
- un matériau partagé entre deux objets changera sur les deux à la fois s'il est modifié sur l'un d'eux (sauf si on duplique ce matériau et applique une version à un objet et une autre à l'autre)
- les propriétés des matériaux peuvent s'animer. L'animation aussi est partagée. Par exemple dans une simulation de conduite il faudra un matériau "phares voiture 1" et un "phares voiture 2" si on ne veut pas qu'elles mettent le clignotant en même temps.

### d) EXERCICE 1: Assigner deux ou plus matériaux à la table précédemment modélisée

## 2) UV-unwrapping
### a) général
- peut être traduit comme "dépliage UV" ou parfois "découpage UV"
- c'est comme le patron d'un habit
- ou pour un quadrupède: comme un tapis de fourrure
- il y a deux manières principales d'UV-unwrapper: soit on unwrappe puis on peint dedans (donc il faut que les faces aient plus ou moins la même taille/orientation relatives les unes aux autres que sur le mesh), soit on fait une image avec des dégradés et on unwrappe en positionnant les faces exprès sur les dégradés qu'on veut, sans se soucier de la forme/taille des faces.

### b) unwrapper et peindre
- Dans la vue 3D en Edit Mode, sélectionner les arêtes qui serviront de couture, puis U > Mark Seams
- puis sélectionner toutes les faces (ou juste celles de la partie actuelle si on veut le faire en plusieurs fois), et soit U > Unwrap, soit U > Project from view, en fonction de ce qu'on veut et du mesh.
- à noter: si deux faces sont exactement superposées, elles auront la même texture (pratique pour gagner de la place sur les objets symmétriques; et du coup tout changement sur la texture de l'une affectera aussi l'autre)
- dans une vue, mettre en mode UV Editor (et garder une autre vue en vue 3D)
- Sélectionner tout dans la vue 3D en Edit Mode
- dans l'UV editor (avant de peindre), on peut sélectionner les vertices, scaler ou tourner des faces et edges (observer les changements dans la vue 3D, en Material Preview)
- quand on est sûr de notre unwrappage, sélectionner les faces/points dont on est sûr, puis *P* ou Menu UV > Pin pour être sûr que ça ne bouge plus (il faudra les unpin si on veut re-unwrapper le mesh)
- Maintenant qu'on a unwrappé, on peut peindre, soit dans la vue 3D, soit dans un éditeur graphique externe en exportant l'UVMap
- pour exporter l'UV map, aller dans la vue UV Editor, et UV > Export UV Map. On peut maintenant l'ouvrir avec un éditeur graphique externe, et quand on a fini (ne pas oublier quand on sauve l'image de l'éditeur de cacher l'UV Map si on ne veut pas voir en noir les lignes d'arêtes de notre objet) réimporter l'image avec le bouton Open dans l'UV Editor.
- pour peindre dans la vue 3D, passer en mode Texture Paint
- en haut milieu, cliquer sur Texture Slots > + > Base Color
- et là on peut commencer à peindre dans la vue 3D et regarder ce que ça fait dans l'UV editor (juste à gauche de New (milieu haut), cliquer sur l'icône de montagne, et sélectionner le nom de la texture qu'on vient de créer)
- si besoin créer une brush en blanc sur fond noir, puis dans Texture Mask (dans la vue 3D en Texture Paint) créer une texture (cocher "Random" pour l'angle) et dans les Properties (bas droite) > Textures sélectionner cette texture et lui assigner l'image; maintenant quand on peint ça ne fait pas un rond mais la forme de la brosse
- peindre notre objet et observer les changements dans l'UV editor
- pour sélectionner une couleur en mode pipette, dans l'UV editor clic droit, puis clic sur l'échantillon de couleur en haut à gauche du mini pop up

| UV painting|
| --- | --- |
|![UV painted lynx](/assets/cours/blender/003a_UVpaint-lynx_2.jpg)|![UV painted sheep](/assets/cours/blender/003b_UVpaint-sheep_2.jpg)|

### c) EXERCICE 2: ajouter un cube, l'UV-unwrapper, le peindre

### d) unwrapper et appliquer sur un dégradé
- ça permet des images beaucoup plus petites, et éventuellement la même image pour plusieurs objets de la scène - et donc une unité visuelle
- importer dans l'UV editor l'image de dégradé ("Open")
- dans la vue 3D, sélectionner chaque face / groupe de faces (soit à la main avec *shift click gauche* ou *B* ou *C*, soit en les ayant séparées par des Seams et sélectionnés avec *L*)
- se mettre en *Z* Material Preview pour voir ce qu'on fait
- dans Properties (bas droite) assigner au cube un matériau avec une texture image, et assigner comme image le dégradé
- dans l'UV Editor placer les faces comme il faut (en général en sélectionnant un groupe de faces, en allant dans la vue où il est le plus lisible, et en faisant U > Project from View)

### e) EXERCICE 3: UV-unwrapper son objet organique précédemment modélisé et l'appliquer sur une texture de dégradés

## 3) éditeur de shaders
- le Shader Editor sert pour pour des matériaux plus complexes et des textures procédurales (générées par l'ordinateur au lieu d'être liées à une image, et donc très animables et infinies).
- input / entrée, output / sortie
- ajouter une node: *shift A*
- grouper des nodes pour un matériau complexe: *ctrl G*
- renommer un groupe de nodes: *F2*
- passer de l'intérieur d'un groupe de nodes à la vue globale: *Tab*
- la node *Material Output* est le résultat final. Ne pas hésiter à avoir plusieurs nodes Material Output dans son shader pour tester rapidement les étapes intermédiaires sans avoir à lier/délier des trucs à chaque fois; une seule node Material Output peut être active à la fois. Une node Material Output dans un groupe ne marche pas: elle doit forcément être au niveau 0 de la texture
- si le fil entre deux nodes est rouge c'est qu'on a essayé de lier un output et un input incompatibles
- dans les explications de nodes ci-dessous, j'ai mis un "!" avant chacune des nodes que je trouve les plus utiles.

### a) quelques exemples de matériaux simples
- *Voronoi Texture*: Distance -> Material Output: Surface; éventuellement ajouter une ColorRamp au milieu (output: color)
- *Wave Texture*: Color -> Bump: Height; Bump: Normal -> Specular BSDF: Normal; Specular BSDF: BSDF -> Material Output: Surface
- *Noise Texture:* Fac (Ridged Multifractal, Lacunarity: 10, offset: .8 ) -> Glossy BSDF: Roughness; Glossy BSDF: BSDF -> Material Output: Surface
- *Diffuse BSDF:* BSDF -> Shader to RGB: Shader; Shader to RBG: Color -> Color Ramp: Fac (interpolation: Constant au lieu de Linear, bouger les poignées pour que le blanc ne soit pas à 1 mais à un peu moins); Color Ramp: Color -> Material Output: Surface (pour avoir les ombres à contours nets aussi, aller dans Proprerties > Render > Shadows > Steps: 1)

|Exemples de Shaders |avec des Textures| Procédurales|
|-|-|-|-|
|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_01.jpg)|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_02.jpg)|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_03.jpg)|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_04.jpg)|
|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_05.jpg)|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_06.jpg)|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_09.jpg)|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_10.jpg)
|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_11.jpg)|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_12.jpg)|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_13.jpg)|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_14.jpg)
|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_15.jpg)|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_16.jpg)|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_17.jpg)|![Matériau Procédural](/assets/cours/blender/004_blender_shaderMats_18.jpg)

[un dossier avec des aperçus de matériaux et leur composition (principalement des variantes de Voronoi, mais pas que)](https://drive.google.com/drive/folders/15yzIO3XvdR7kBonyLoHIOTJbkMwmBZ6y)

### b) EXERCICE 4: faire un matériau avec le Shader Editor, l'appliquer sur notre objet organique

### c) quelques nodes de texture
- ! *Voronoi Texture* (<https://docs.blender.org/manual/en/latest/render/shader_nodes/textures/voronoi.html>): motifs de ronds, de craquelures, de cellules rondes ou angulaires, de quadrillage régulier, de texture de toile de jute, d'étoiles, de fumée, etc. Extrêmement versatile, assez complexe.
- *Noise Texture*: petits points (bruit photographique), nuages, lines croisées (reflets d'eau, lignes de givre) (https://docs.blender.org/manual/en/latest/render/shader_nodes/textures/noise.html)
- *Wave Texture*: cercles et lignes, qui peuvent être simples ou très irréguliers, et/ou très texturés.
- ! Note: Pour Voronoi, Noise et Wave: Si on a plusieurs objets avec le même matériau, la texture sera (par défaut) posée de manière à chaque fois exactement identique et montrera exactement le même motif. Pour éviter ça et donner un peu de diversité visuelle/aléatoire, lier l'input Vector de la texture avec un output Position d'une node Geometry.
- *Brick Texture*: pour faire des briques
- *Gradient Texture*: Dégradé (on peut avoir un dégradé sphérique par exemple, pour faire un chat siamois avec Texture Coordinates (generated) -> Multiply Add (add pour bien le centrer, multiply pour régler la profondeur du dégradé) -> Gradient Texture (spherical) -> Color Ramp)
- *Checker Texture*: Damier (carreaux alternés de deux couleurs)
- *Image Texture*: applique une image (donc: non procédural). Par défaut si on a UV-unwrapped (conseillé pour des objets complexes) il utilisera les coordonnées UV.

| Noise avec les valeurs par défaut de l'input Vector | Noise avec Geometry: Position lié à l'input Vector
|-|-|
|![Shader Noise Input Vector default](/assets/cours/blender/005a_ShaderNoise_default.jpg)|![Shader Noise Input Vector Geometry: Position](/assets/cours/blender/005b_ShaderNoise_geometryPos.jpg)|

### d) quelques nodes de modification (Converter, Vector et Color)
- ! Color Ramp: pour déplacer les poignées, ne pas cliquer sur le carré de couleur mais à côté, et dans la barre de couleur. Pour changer la couleur d'une poignée, cliquer sur la barre de couleur du dessous (si on laisse la souris sur cette barre de couleur, on peut faire ctrl C et ctrl V pour copier-coller une couleur entre deux poignées); pour ajouter ou supprimer une poignée utiliser les icônes + et -; pour avoir des couleurs sans dégradé entre elles mattre l'interpolation (là où il y a écrit Linear) à Constant.
- ! Bump change l'impression de volume (pour mettre de la texture superficielle; par exemple pour des écailles de reptile ou des pores de peau ou de la rouille)
- ! Math et Vector Math: permet de mélanger deux valeurs ou  en modifier une. Les ajouter, multiplier, mettre au carré, prendre la valeur la plus grande, arrondir, etc.
- les nodes dans la catégorie Color servent à effectuer des opérations sur des couleurs. En mélanger deux (de plein de manières différentes, comme les modes de calque d'un éditeur graphique), changer la luminosité/contraste/teinte/etc., les inverser, etc.
- nodes de mélange disponibles: Mix Shader, Mix Color, Mix (float, vecteur ou couleur)
- on peut aussi séparer et recombiner des valeurs pour modifier chaque canal séparément (Separate Color, Separate XYZ, Combine Color, Combine XYZ)

### e) quelques nodes d'input
- ! Texture Coordinate: Generated et UV sont fixes; Normal change avec l'orientation de la face (ce qui peut donner un effet un peu de réflexion), et Objet est relatif au centre (point orange) de l'objet (donc ces deux-là animent la texture si l'objet est animé; objet peut être un empty qu'on déplace pour animer volontairement la texture); Camera et Window dépendent de l'écran, donc ils peuvent être  bien pour par exemple un effet texture papier (mais il est sans doute plus efficace de l'ajouter en post-production si on veut qu'elle soit globale sur toute l'image).
- Texture Coordinate: Generated est la valeur par défaut si une node a un input Vector vide. Elle est utile si on veut partir de la valeur par défaut pour la modifier (pour l'étirer sur un axe, par exemple, mettre au milieu une node Vector Math en mode Multiply et mettre des valeurs différentes aux différents axes)
- layer weight est l'angle par rapport à la caméra; particulièrement utile pour les matériaux réfléchissants ou semi-translucides, la glace, le velours, etc.; souvent utilisé comme facteur de mélange entre deux textures (texture 1 s'applique quand la face est vers la caméra, texture 2 s'applique quand la texture est oblique)
- Object info > random donne une valeur différente à chaque objet ayant cette texture; par exemple pour un tas de cubes de couleurs différentes mais de même texture (par contre pour tous les points d'un même objet ce sera la même valeur)
- Value et RGB donnent, respectivement, un nombre et une couleur; on ne peut les relier qu'à des nodes à l'intérieur desquelles il y a déjà un champ nombre ou couleur, donc à première vue elles semblent inutiles; mais c'est très pratique quand on a des valeurs liées, par exemple si on veut mettre la même valeur/couleur à plusieurs nodes et ne les changer qu'à un endroit quand on change d'avis (ou une valeur proportionnelle, avec la node Converter > Math)

### f) quelques nodes de shader
- ! si on n'utilise pas d'ombres (ni ombres portées ni ombres propres), la node de shader est inutile; on peut lier directement une texture au Material Output: on ne verra que la couleur, tel quelle, sans effet d'ombres ou de lumière
- Diffuse BSDF pour des ombres très douces - matériaux poreux ou à la surface irrégulière (tissu, papier, bois brut) (lumière diffuse)
- Glossy BSDF pour des points lumineux - matériaux très lisses (métal, solide mouillé, plastique) (lumière spéculaire)
- Specular BSDF est un mélange de Diffuse et Glossy.
- Principled BSDF (la node par défaut d'un nouveau matériau) est un mélange de toutes les autres nodes BSDF. A le paramètre "Metallic" pour des métaux (forte spéculaire réfléchissante et fort contraste). Pour le rendre réfléchissant, changer IOR et Specular > IOR Level. (doc sur la node principled BSDF: <https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/principled.html>)
- "Roughness" est si la réflexion est nette (0) ou non (1) (à quel point la surface est poreuse/texturée ou lisse)
- Principled BSDF > Alpha contrôle la transparence
- Principled BSDF > Emit (mettre à Emit > Color le même input qu'à Color) est si ça émet de la lumière; des valeurs trop hautes seront blanches
- on peut utiliser l'output BSDF d'une node de Shader BSDF pour modifier comment le matériau réagit à la lumière, par exemple pour créer un rendu toon / cel shading (quand les ombres sont plates et pas en dégradé) (une node BSDF: BSDF -> Shader to RGB -> Color Ramp (interpolation: constant) -> Output Material: Surface)
- Holdout est rendu comme des pixels transparents (on ne voit pas l'arrière-plan derrière, on voit du transparent; utile pour la manipulation d'images en post-production)
- Principled Volume est pour la fumée et le feu (doc: <https://docs.blender.org/manual/en/latest/render/shader_nodes/shader/volume_principled.html>)

### g) EXERCICE 5: créer des matériaux spécifiques
- demander à tout le monde trois noms de matériaux (et un objet sur lequel il pourrait s'appliquer: "bois" n'est pas autorisé, mais "plancher vernis", "tronc d'arbre", "planche de contreplaqué", "meuble en érable non traité" l'est; certains animaux ont des motifs amusants);
- mettre en commun les idées, en donner deux à chaque personne, pour en choisir un et le recréer (dans un fichier .blend, utiliser la fonction texte pour noter quel matériau c'est et qui l'a fait),
- puis mettre en commun les résultats (appliqué chacun sur [les mêmes quatre ou cinq mesh partagés](https://drive.google.com/file/d/1ABZQr3HL10-uVAxsvdoDB5MgUixofp7Q)) et les redistribuer (vérifier que personne n'ait reçu son propre matériau de l'étape précédente) et demander à chaque personne de deviner ce qu'est le matériau reçu.

## 4) effet contour
- c'est un effet ajouté en post-production par blender: donc ça ne se voit pas dans la vue 3D, mais uniquement sur les rendus (si vos rendus sont trop lents, voir le début de ce chapitre, III. 0) b), sur comment les rendre plus rapides)
- activer Properties > Render > Freestyle
- dans Properties > View Layer > Freestyle, changer le Crease Angle (un peu comme l'autosmooth: choisit quels angles sont assez forts pour être pris en compte)
- il y a plein d'options, je n'ai pas tout regardé; mais:
- Freestyle Color change la couleur du contour (voir le Modifier Noise, sur cette option et toutes les autres, pour des effets intéressants)
- Freestyle Alpha change la transparence/opacité du contour
- Freestyle Thickness change l'épaisseur (voir le Modifier Calligraphy)
- Freestyle Geometry change son trajet: ajouter de l'aléatoire (Perlin Noise 2D) ou le décale (2D Offset) par exemple

## 99) Tutoriels et Ressources
Principalement en anglais mais ils suffit de regarder ce qu'ils font la langue importe peu
- textures en dégradé avec l'UV mapping: <https://youtu.be/EIxwWGj28_s?t=148> (regardez jusqu'à 5:00; après c'est juste répéter ce qu'il a déjà expliqué pour appliquer le matériau aux autres objets de la scène)
