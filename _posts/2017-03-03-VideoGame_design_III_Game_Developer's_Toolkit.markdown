---
layout: post
title:  "Video Game Design III: GAME DEVELOPER'S TOOLKIT"
date:   2017-03-15 16:37:00 +0100
categories: project
---

In this entry we will review a bunch of tools that are key to develop our video game. This time all the tools are important no matter what framework/engine we are using: LibGDX, Cocos2d-x, Corona, Unity …

Let’s see what we got! 

<br>
## 1 Pixel Art graphic editor & Animator: [PyxelEdit](http://pyxeledit.com/)
<br>

PyxelEdit is a multiplatform (Mac, Linux, OSx) graphic editor for pixel art that costs 0€. It is completely designed to create sprites, animations and tiles for our games. Its main advantages are its lightweight design and ease of use.

PyxelEdit allows working with layers, just like Photoshop. It supports exporting in many different formats. In the following example I have exported an animation as a TextureMap:

<img alt="running-texturemap" src="/images/gameDevelop/3/1.png" width="400">
*Running textureMap*

And here I have exported the same animation as a GIF:

<img alt="running-gif" src="/images/gameDevelop/3/2.gif">
*Running GIF*

Of course this tool can be used with Unity, LibGDX, Cocos2d-x…

<br>
## 2 Tile Map Editor: [Tiled](http://www.mapeditor.org/)
<br>

Tiled is a multiplatform tool completely free. It is the perfect tool to imagine and plan levels and maps made of cells.

It supports square cells: 

<img alt="square-cells" src="/images/gameDevelop/3/3.png" width="400">
*Square cells*


Hexagonal:

<img alt="hexagonal-cells" src="/images/gameDevelop/3/4.png" width="400">
*Hexagonal cells*


Isometric:

<img alt="Isometric-cells" src="/images/gameDevelop/3/5.png" width="400">
*Isometric cells*

But what it is really useful in Tiled is its ability to add extra information to our maps. The following example shown an area of the map in which I have added extra information: 
1 → Where the player is going to be when I load the map.  
2 → A dangerous area: when the player enters that area, monster will appear.

<img alt="metadata-tiled" src="/images/gameDevelop/3/6.png" width="400">
*Metadata in Tiled*

The maps created in Tiled are exported into a file that includes all the features we described using the editor. This file can be opened and read by any framework/engine (LibGDX, Unity, Cocos2d-x…) and it will have to be used as the basis for creating all the objects, textures, metadata, conditions of our map in the game.

<br>
## 3 Physics Engine: [Box2D](https://github.com/erincatto/Box2D)
<br>

Box2D is a physics engine that simulates all the physics for recreating a realistic world. In this world we define bodies: our main character, the floor, the walls… and the properties for these bodies: density, friction, elasticity, position… you get the idea. The physics engine is in charge of simulating how all these objects react when interacting with other forces and collide.

For basic games or games with no realistic physics like platformers, we could try to create or own physics mini-engine. But if we want to create realistic physics iterations in our games like [Angry Bird](https://www.angrybirds.com/) or [Cut the Rope](https://www.cuttherope.net/) a physics engine is the way to go (both of them use Box2D).

Unity uses Box2D as Physics Engine by default. There are ports of the library for C, C++, Java, Javascript… So you can leverage its power no matter what framework/engine you choose. 

In the following example I am using Java’s Box2D implementation with LibGDX to simulate a square that moves to right at a constant velocity. The ball is affected by gravity and I move it by applying forces to it. 

<img alt="box2D-simulation" src="/images/gameDevelop/3/7.gif" width="400">
*Box2D simple simulation*

<br>
## 4 Graphical editors for Physics Engines: [R.U.B.E.](https://www.iforce2d.net/rube/)
<br>

Graphical editors are an aid to work with physics engines. We could define all the entities in the game by directly coding them… but in order to create complex worlds including many entities things can get too much complicated. 

R.U.B.E. is a graphical editor that allows us place all the bodies and properties of a simulation in a very easy way.

Similar to Tiled, R.U.B.E. generates a file that can be read by Unity, LibGDX, Cocos2d-x… to be interpreted. The file is converted to a world in our game that Box2D can simulate.

Rube costs about 40€, but it is an indispensable tool if we want to work woth realistic and complex physics. The editor itself allows us to do simulations before exporting them:

<img alt="RUBE-simulation" src="/images/gameDevelop/3/8.gif" width="400">
*R.U.B.E. can run simulations*

<br>
## 5 Particle editors: [2D Particle Editor](https://github.com/libgdx/libgdx/wiki/2D-Particle-Editor)
<br>

The particle effects are the confetti of video games. They are images, colors and shapes shown on the screen that follow some determined pattern (sometimes a random pattern). 

2D Particle Editor is an editor for LibGDX, so it can't be used in Unity, Cocos2d-x an. This time I present a tool that is not the easiest to learn neither the easiest to install… but hey, it’s what we've got in LibGDX and besides… it is free.

In the following example you can see how we can play around with the editor to simulate a fire effect:

<img alt="2DParticleEditor" src="/images/gameDevelop/3/9.png" width="300">
*2D Particle Editor*

And here it is the result:

<img alt="2DParticleEditor-fire" src="/images/gameDevelop/3/10.gif" width="250">
*Fire particle Effect*

<br>
## 6 Other Tools:
<br>

Of course there are many other tools, but hey, this post has to end sometime.
Here I left you some other tools I use in case you want to further explore:

- [Github](https://github.com/).

- [Github Pages](https://pages.github.com/).

- [Java Tween engine](http://www.aurelienribon.com/blog/projects/universal-tween-engine/).

- [Aseprite](https://www.aseprite.org/).

- [OpenGameArt](http://opengameart.org/).

<br>

## Conclusions:

<br>

That is the arsenal of basic tools we need as programmers / designers. 

Of course there are other alternatives to the tools I have reviewed. But at least I hope you can get an idea of the different elements that play a role in the video game creating process, so you ultimately end up using the ones you like most.

Here it is a gif from a bizarre/random project that conglomerate all the tools used in this entry:

<img alt="Bizarre-project" src="/images/gameDevelop/3/11.gif" width="400">
*A bit of everything*

#### Do not hesitate to comment on doubts and to leave me new proposals for the following entries!

Follow me on twitter for more entries like this → [@Musicaligera_](https://twitter.com/Musicaligera_)

