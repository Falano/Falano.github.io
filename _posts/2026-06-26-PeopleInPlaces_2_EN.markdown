---
layout: post_cera_EN
title: "People in Places - 2 : procedural textures"
tags: EN illu
categories: 3D EN illu
last_updated: 26 june 2026
description: tutorial about the People in Places 3D series
permalink: /illu/2026-06-26_PeopleInPlaces_2_EN.html
topnav: topnav_Portfolio_illu_EN
---
\
[< previous part: 2D prints <](/illu/2026-06-19_PeopleInPlaces_1_EN.html) | [> next part: 3D prints >](/illu/2026-06-19_PeopleInPlaces_3_EN.html)

# People in Places: Mountains

|![mountain peeps: 100](/assets/art/2D/mountainPeeps_0100_wm.jpg)|![mountain peeps: 160](/assets/art/2D/mountainPeeps_0160_wm.jpg)|
|![mountain peeps: 140](/assets/art/2D/mountainPeeps_0140_wm.jpg)|![mountain peeps: 200](/assets/art/2D/mountainPeeps_0200_wm.jpg)|

## An aside about procedural textures
I tried making a bunch of different textures, using the same principle of layered Noise as for the People in Places series, but for my 2D drawings: to be exported as is, without any 3D geometry underneath, so that I could export just the texture as an image file that I could then add to my 2D drawings. 
- previous version of the project was not procedural: in the example here below I used a scan of real paper on which was spilled real tea:
![pictures with and without overlay scanned texture](/assets/art/2D/mountainPeeps_05_texs_nat.jpg)

- new versions are procedural: some try to mimic the not procedural ones, others go off vibes.
- You've got the basic ones, that go: small texture, bigger texture, mix. Add some white noise (tiny Noise texture of any kind) if it's too smooth.\
\
The one used for the Mountain People:
![mountain peeps: texture overlay node structure](/assets/art/2D/mountainPeeps_03h_texs.jpg)
Another basic one:
![nodes setup in process pics](/assets/art/2D/mountainPeeps_06b_texs.jpg)
- and then you've got more complex ones like this (use a texture as factor and have fun)
![nodes setup in compositor window](/assets/art/2D/mountainPeeps_06c_struct.jpg)
![nodes setup in process pics](/assets/art/2D/mountainPeeps_06c_texs.jpg)

[> next part: 3D prints >](/illu/2026-06-19_PeopleInPlaces_3_EN.html)
