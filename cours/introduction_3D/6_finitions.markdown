---
layout: page
title:  "Cours Paris 8: introduction à la 3D avec blender"
last_updated: October 27, 2024
permalink: /cours/introduction_3D/finitions.html
topnav: topnav_P8_3D
---

# VI. Finitions
## 1) Importer
### a) à partir d'un autre format
- File > Import > choisir le bon format (entre celles par défaut et celles inclues dans Edit > Preferences > Get Extensions, il y a au moins obj, fbx, gltf et 3ds)
### b) à partir d'un autre fichier blender
- pour importer dans un nouveau fichier blender un objet (mesh, material, light, animation, etc.) qui est présent dans un fichier blender différent:
- File > Link: pour créer un lien/raccourci vers l'objet: le projet aura besoin du fichier de base pour marcher. Sinon ça fera un lien vide et donc ne marchera pas.
- File > Append: pour copier l'objet dans le nouveau fichier. On n'a plus besoin du fichier de base, mais du coup le nouveau fichier est un peu plus lourd
- Globalement si vous avez sept scènes dans le même projet qui toutes utilisent le même perso, utilisez plutôt Link. Si c'est juste une fois, et/ou si le fichier de base contient pas mal d'autres choses en plus de l'objet importé, utilisez plutôt Append.
### c) à partir du site web d'IKEA
- (wtf)
- dans Edit > Preferences > Get Extensions > IKEA Browser
## 2) Lumières
- on peut changer leur intensité et couleur (dans Properties > Data > Light), et désactiver les ombres portées créées par cette lumière (les ombres propres sont les ombres liées au fait que cette face de l'objet n'est pas orienté vers la lumière; les ombres portées sont les ombres qu'un objet projette sur un autre en se trouvant entre lui et la lumière)
- sun: peu importe où on le place, seule sa rotation importe. Crée des rayons lumineux parallèles dans la direction de sa rotation.
- point: la lumière est émise dans toutes les directions à partir du point où se trouve la lampe. Plus le radius est petit, plus la lumière baisse d'intensité en s'éloignant de la lampe. Plus le radius est grand plus la baisse d'intensité sera graduelle.
- spot: projette de la lumière en forme de cône à partir de la lampe et dans la direction indiquée par sa rotation.
- area: plus diffus que Sun.
## 3) Effets de Post Production
### a) Depth of Field (Profondeur de Champ)
### b) Motion Blur
- dans Properties > Render
## 4) Exports et Imports
### a) Généralités
- comment est-ce que vous allez utiliser votre scène 3D?
- une image / animation comme produit final?
- un objet 3D pour un jeu / un autre logiciel d'animation?
- faites attention aux axes (x, y, et z), qui ne sont parfois pas dans le même sens selon les logiciels (si votre perso arrive dans votre moteur de jeu couché sur le côté, c'est que les options d'export des axes sont mauvaises)
- penser à appliquer location et rotation
- faire attention à la position du centre par rapport à l'objet (par exemple, souvent c'est utile d'avoir le centre au pied de l'objet, pour qu'une position de 0 sur l'axe vertical corresponde à un objet/personnage posé sur le sol)
### a) rendu d'une image simple
- voir III 0 b
### b) rendu d'une animation
- rendu animation : Render > Render Animation (ou *ctrl F12*)
- dans la Timeline on peut changer la longueur de l'animation (quelle est la portion qu'on veut exporter)
- dans Properties > Output on peut changer aussi la longueur de l'animation, mais aussi la résolution de l'image et le nombre d'images par secondes, et dans Properties > Output > Output on peut changer dans quel dossier sont sauvegardés les fichiers exportés, et dans quel format. Par défaut c'est exporté comme images individuelles (si vous utilisez After Effect il y a une option pour importer une séquence d'image et les placer automatiquement les unes à la suite des autres, en choisissant la longueur d'une image et s'il y a un fade entre deux images TODO: trouver le nom de la commande) mais vous pouvez choisir de l'exporter en format vidéo.
- avec les options d'export il y a aussi des options de gestion des couleurs (mais il vaut mieux les gérer au niveau de la scène, dans Properties > Render)
### c) export gtlf
- visualiseur gltf: https://sandbox.babylonjs.com/
- options auxquelles faire attention:
- Include > Limit to: Selected Objects (par défaut off; peut permettre de n'exporter qu'un objet de la scène par exempl)
- Data > Mesh > Apply Modifiers (par défaut off; l'appliquer si on n'a pas de shape keys et qu'on a un modifier Mirror et Smooth By Angle, par exemple)
- Animation > Animation mode: Actions (si plusieurs animations; attention à avoir bien configuré les actions)
- Animation > Rest & Ranges > Set all glTF Animation starting at 0 (par défaut off) (s'il y a une anim qui n'a pas la bonne longueur et boucle bien dans blender mais refuse dans le viewer babylon, c'est peut-être parce que cette option n'est pas cochée)
- matériaux:
- les matériaux procéduraux ne s'exportent pas bien
- les UV maps devraient bien s'exporter. Si ce n'est pas le cas, vérifier que Data > Mesh > UVs est bien coché, et éventuellement regarder les options dans Data > Material
- les matériaux de couleur simple, plusieurs par objet, s'exportent très bien
### d) godot
### e) unity
- unity peut lire les fichiers .blend directement, mais nécessite que blender soit aussi installé sur l'ordinateur.

### f) unreal engine
