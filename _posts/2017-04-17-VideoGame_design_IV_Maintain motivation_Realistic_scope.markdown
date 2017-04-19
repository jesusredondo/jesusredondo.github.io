---
layout: post
title:  "Video Game Design IV: MAINTAIN MOTIVATION: REALISTIC SCOPE"
date:   2017-04-17 13:13:00 +0100
categories: project
---

As you already know if you have read my previous blog posts, I am developing my first videogame using [LibGDX]( https://libgdx.badlogicgames.com/) framework.
Like many others, I started with the clear idea that I could build more or less the game I wanted with enough time. My definition of what I wanted to achieve was this:


```
	The game is a 2D shooter platformer with RPG elements using pixel art graphics. The story will be tailored by the player actions and choices. The skills our character is going to learn are determined by in-game decisions, this means, no level ups, no stats system needed. Game mechanics are based around two pillars:

	1. Player’s ability to jump, shoot, hide, evade, rappel, parachuting… All this skillset is determined by player decisions ingame.

	2. History is tailored by dialogs between main and secondary characters and by the player’s decisions during the game. What I mean by this is that there are going to be moral decisions during the game and they will modify game playability.
```

Hey! That is something feasible, it is not a MMORPG, nor a 3d game, it wouldn’t even use complex graphics, I could draw the Pixel art. In fact, I painted some screens with the style I wanted to use:

<img alt="harbor-level" src="/images/gameDevelop/4/1.jpg" width="450">
*Harbor level*

This was the main character:

<img alt="main-character" src="/images/gameDevelop/4/2.gif" width="100">
*Main character*

I even had a “technical document” with some game ideas I could use for the game (*ROLF*):

<img alt="main-character" src="/images/gameDevelop/4/3.png" width="400">
*Game ideas*

It looked like I was progressing well, I had open fronts in different parts of the development, but all of them would become useful for the videogame. And then I started coding… **And I realized I had no idea how to approach even the more basic stuff!**

How can I represent the world? What screen resolution am I going to use? What size must the sprites have? How I handle the camera so it follows the main character? How I keep track of the decisions and choices of the game? …

Facing so many questions and so little responses was discouraging. Instead of throwing in the towel, what I have done is refocus the game I want to create, basically I need to start with something simpler, something **feasible for me given my circumstances**.  What I decided to do is developing an archetype game, have a very clear goal and organize myself so I won't lose time in parts of the project I don't know if will ever come to the final game.

My priority changed to having a demo that could clarify what I wanted to develop.

## 1 Redefining the game:

I changed my game definition to:
```
	A 2d racing videogame for mobile platforms. The goal of the game is driving from one part to another of the level avoiding obstacles and jumping from different platforms in less than a maximum time. The player controls the rotation of the car’s wheel, accelerating or braking the car. The camera will follow the car during the entire itinerary. The game levels are generated using R.U.B.E.. Graphics right now are just placeholders.
```

After one week of development I came up with the following demo that run in my mobile phone:

<img alt="first-demo" src="/images/gameDevelop/Sueltas/reddit_camera/car_prototype_1.gif" width="400">
*First demo*

For the first time I started to see real progress. Even though the demo was really basic, I consider that doing that for a beginner using LibGDX was a success. 

I started to love a game idea that wasn’t the initial idea I had.

## 2 Work organization. Tools and focus:

I have a steady job, I am doing this as a hobby, so when I started I didn’t plan what stuff I must do first. I knew there was a lot of stuff to do so I just did what I felt like more, switching from one part to other without any clear objective. In the end all parts must be done…

I created a lot of things during that time… but how useful were those things? My work organization has changed since then, now I have a [Trello]( https://trello.com/) with all the stuff I have to do in three columns and ordered by importance. 

<img alt="My-Trello" src="/images/gameDevelop/4/5.png" width="500">
*My trello at the moment of writing this entry*

I always update my Trello with concise tasks I can finish in one day (sometimes complications arise and tasks take longer). It might look stupid writing what you have to do in a board on Internet, especially if we work as solo-developers. But for me it has been day and night, it is key to know in every moment what you have to do next, and focus effort on that without further delay. 

<img alt="Archived-trello" src="/images/gameDevelop/4/6.png" width="300">
*Some of the stuff I have already finished*

## 3 Graphics:

I like drawing, I think I'm not too bad at it, so I could produce decent graphics for the game, problem is: I'm not used to doing that, so it would take very long to produce graphical assets for the game.

In fact, I had already created the main char animations:

<img alt="Idle" src="/images/gameDevelop/4/2.gif" width="100">
*Idle char*

<img alt="Walking" src="/images/gameDevelop/4/9.gif" width="100">
*Walking char*

<img alt="Running" src="/images/gameDevelop/4/8.gif" width="100">
*Running char*

<img alt="Firing" src="/images/gameDevelop/4/7.gif" width="100">
*Firing char*

And more scenes as the harbor I showed before:

<img alt="Firing" src="/images/gameDevelop/4/10.png" width="150">
*Terrain layers*


I decided to change the chip and dedicate myself to programming and making a fun game. That is why I am using free repositories like [OpenGameArt]( https://opengameart.org/). This has been positive in two respects:

1. I can spend time programming, not painting.

2. I discover styles that I did not intended to use, but I still like them (something beyond pixel art).

The good thing about using CC0 licensed graphics is that I can modify and use them at my whim.


## 4 Current state of the project:

Far from being a finished project, I think I have made significant progress and I really want to squeeze all the juice from the project. My original idea is quite different from the idea in am carrying out, but it is advancing steadily and I am liking it more each day. This is the current state of the game:

<img alt="Current-state" src="/images/gameDevelop/Sueltas/reddit_camera/car_prototype_7.gif" width="600">
*Current state of the game*


## 5 Conclusions:

It is never too late to learn, modify the concept and adapt it to realistic goals. In my case the original video game I had thought is very different from the one I'm developing. I was aware that I had a wrong approach given my abilities, so stteping back has been the right choice to move forward stronger.

Yet all what I did has served me as a tool to realize how important it is to focus the project on something that is temporarily and emotionally viable. **Now I see real and continuous progress in a game, not in a plan**, and that is making me like more my hobby and my new approach every day. 


#### Do not hesitate to comment on doubts and to leave me new proposals for the following entries!

Follow me on twitter for more entries like this → [@Musicaligera_](https://twitter.com/Musicaligera_)





