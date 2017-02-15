---
layout: post
title:  "Video Game Design I: FRAMEWORK SELECTION"
date:   2017-02-14 23:36:00 +0100
categories: project
---
In this series of posts I will develop a video game from bottom to top. During these series of posts, many of the assets and decisions will be taken in conjunction with the people that follows the manual. Don't miss anything and subscribe at [@Musicaligera_](https://twitter.com/Musicaligera_).

## The Video Game Itself:

At the moment of writing this post, there are many decisions which aren't determined yet: graphics style, number of levels, title of the game, how portable it will be... We will discuss all these terms in depth in following posts, it will serve as a mental exercise about how to deal with design. 

For now own we can precise it will a 2D shooter platformer with RPG elements. The story will be tailored by the player actions and choices. The skills our character is going to learn are determined by in-game decisions, this means, no level ups, no stats system needed. Game mechanics are based around two pillars:

1. Player's ability to jump, shoot, hide, evade, rappel, parachuting... All this skillset is determined by player decisions ingame.

2. History is tailored by dialogs between main and secondary characters and by the player's decisions during the game. What I mean by this is that there are going to be moral decisions during the game and they will modify game playability.


## Which framework should I use?

Ahhh, the jump of faith, becoming from zero experience, as was my case this is a very tough decision. What Have I done? I have spent several months playing around with different platforms. In this entry we are going to review the ones I have put my foot into:

### [Cocos2d-x](http://cocos2d-x.org/)

<img alt="cocos-logo" src="/images/gameDevelop/cocos2d-x.png" width="200">
*Cocos2D-x Logo*

Its main Language is C++. Assets management, animations and sounds are handled with its graphic tool [Cocos Studio](http://www.cocos2d-x.org/wiki/Cocos_Studio). Less than a year ago, they have launched a tool called [Cocos Creator](http://cocos2d-x.org/docs/editors_and_tools/creator/) which integrates all the production workflow. Unfortunately, Cocos creator doesn't support C++ (only LUA and JavaScript), and I really want an strong structured language to program. Moreover, Unity, being a Graphical Framework aswell is much more mature in case I would like a graphical interface.

To soak up Cocos2d-x I have followed this book: [Cocos2d-x by Example: Beguinner's Guide - Second Edition](https://www.amazon.com/Cocos2d-x-Example-Beginners-Guide-Second/dp/1785288857)

I have completed this two great tutorials as well: [The Game of Life](https://www.makeschool.com/online-courses/tutorials/learn-cocos-studio-and-c-by-building-the-game-of-life/what-game-of-life) and [Shushi Neko](https://www.makeschool.com/online-courses/tutorials/build-a-clone-of-timberman-in-c-with-cocos2d-x-and-cocos-studio/getting-started).

<img alt="Shushi-Neko" style="border:1px solid black" src="/images/gameDevelop/ShushiNeko.png" width="250">
*Capture of Shushi Neko*

What I like most about Cocos2d-x is the amount of freedom it provides to the developer, having access to the whole framework's code. But I have declined the idea of developing with this framework mainly because of its ABSOLUTE, NON EXISTENT, PIECE OF SHIT, GARBAGE [more billis here] Documentation. Yeah, everything is free, but the amount of open fronts they have doesn't promise a clear future. Besides, the terminology is a real mess and there is not clear roadmap. If you are into the framework... that's OK, getting into it is another history.


### [Unity](https://unity3d.com/)

<img alt="unity-logo" src="/images/gameDevelop/UnityLogo.png" width="200">
*Unity Logo*

Unity's main Languages are C#, Boo (what the hell is that) and JavaScript - personally I am interested in C#. All the develop framework is covered by its graphical tool [Unity](https://store.unity.com/products/unity-personal?_ga=1.232537051.53158089.1485866409): Animation, music, presets, coding (even though for coding is normally used MonoDevelop). It is integrated with many other programs to edit animations, sounds, tiles, models... 

The "free" version includes almost all the functionality, but it also includes the Unity logo at the start of your game. Unity is really interesting because it is becoming the "de-facto" referent of the industry for indie games. The dark side of using unity is the lack of freedom as user, you don't have access to the code behind and you have to adapt yourself to Unity's workflow.

I have learnt Unity by completing these two tutorials: [Roll a Ball (3D)](https://unity3d.com/learn/tutorials/projects/roll-ball-tutorial) and [RougueLike Tutorial (2D)](https://unity3d.com/learn/tutorials/projects/2d-roguelike-tutorial).

Unity's main drawback is lack of freedom as user and its engine opacity. Apart from that is a superb tool in terms of animation, sound, depuration and integration. 


### [LibGDX](https://libgdx.badlogicgames.com/)

<img alt="libgdx-logo" src="/images/gameDevelop/LibGDX.png" width="200">
*LibGDX Logo*

Its language is Java. LibGDX, as Unity and Cocos2d-x, is a cross-platform game development framework. The concept is clear: LibGDX creates a base project with its assets, this project is written in Java using the Framework libraries. These classes and code work as an interface between the base project and the different implementations in the different platforms, right now it supports Android (Slightly different to ordinary Java, but just in terms of the compiler), IOS (it used to work with RoboVM), Desktop (Java) and Web (GWT).

How have I learn to use it? Mainly consulting the [Wiki](https://github.com/libgdx/libgdx/wiki), which is superb. I have completed this tutorial aswell: [Zombie Bird](http://www.kilobolt.com/zombie-bird-tutorial-flappy-bird-remake.html).

I have chosen LibGDX to develop my game for several reasons:

1. It uses Java, language I am very familiarized with. This is personal, but I prefer using Java to C++. I enjoyed C# during my Unity learning process, though.

2. It is flexible enough to make the framework work for me and no the other way around.

3. The documentation and community are top notch.

4. It is free and open source.

The cons of using libGDX: It works at low level, the developer has to deal with more stuff manually, specially regarding to assets management in contrast with Unity. This doesn't translate directly to slower framework in terms o developing, but it has a steeper learning curve in this regard.


## To be continued...

This is the first part of a series of entries I plan to post as the game develops. I am actually working on the graphical assets (mockups) I am going to use. Any ideas, suggestion or advises will be welcomed. 


