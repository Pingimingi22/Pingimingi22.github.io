---
layout: fantasy-blog
title: Raylib/Swift Visualisation - Surface Normal For An Irregular Terrain
---

The other day I was looking for a little code project I could do. I wanted it to be something which had some maths involved. I've been really into video game maths for the past few months but I realised that I have only been studying in the traditional sense. Reading textbooks, doing practice questions, etc. I remembered that back in school we'd always learn some theory and then apply the theory, putting it into practice, by implementing it with code, since we were programmers!

It had been a long time since I'd done anything like that... BUT! I'm happy to say that I've done it again!

I present to you a maths, program, thingy, visualisation!

But before I show you I'll lay down the technical details of this sweet program.

- Raylib
- Swift
- Maths

## Raylib
Back in school we used Raylib for a few of the visualisations and games we made. At the time I remember sort of bagging on Raylib. I can't remember why exactly, but looking back it was probably me not understanding how things worked and blaming it on something other than myself. But anyways, I had another look at the Raylib website a few days ago and I fell in love! The documentation, exquisite! The ideology, fantastic! You know, Raylib is a tool which enables programmers to quickly and easily create THINGS just by coding in the "spartan" way. I just love that. And I think I appreciate that so much more now that I've been exposed to other technologies. Out in the big world there are game engines, frameworks, a bunch of heavy duty tech which is really awesome, but in all their grandeur I think they lose something. The little things, like the ease of use for doing basic operations. I'm talking about stuff like drawing lines on the screen, displaying rectangles, quickly drawing text, that sort of thing. And it was those things that taught me so much and made me fall in love with programming in the first place.

## Swift
The other major technology I used was Swift. I wrote this program in Swift because it's a language I've been learning recently and I thought this would be a good chance to get some reps in. So I found some Swift bindings for Raylib and just started coding away. Of course, Swift is different to C# and C++ but really it felt very familiar.

## What did I make??
You're probably wondering what did I even make. Well you wont be disappointed when you see it. But first!

I remembered a blog my old programming teacher wrote. (Can be found at snakehillgames.com). This blog talks about a lot of really cool sophisticated techniques and research, mostly way above my pay grade! (You should check it out btw). But there was one section which seemed perfect for a small project. It was the part about exploring techniques used to calculate surface normals for irregular terrain. This part was specifically written to show the reader the technique in a generic way. Using black and white pixels to describe the terrain and "void", an image accompanied the technical description.

The gist of it is, imagine you have a 2D world made up of black and white pixels. The black pixels represent the terrain and the white is "void" or the sky. Each black pixel has surface normals but since pixels are squares, the surface normals are always aligned with the cardinal axes, always being either horizontal or vertical.

I like to think of this algorithm as grabbing a bunch of black pixels and attempting to calculate a surface normal for the group of pixels, rather than each individual pixel. This way we don't have to be stuck with a bunch of horizontal and vertical surface normals, and get one nice surface normal.

## The algorithm
The way it works is:

Grab the position of all the black (terrain) pixels
Calculate the average position of them.
Grab the position of all the white (void/sky) pixels
Calculate the average position of these as well.
The surface normal is the normalised vector from the average position of the black pixels to the average position of the white pixels.
Done!
Short and simple but very cool nonetheless.

And here's what it looks like!

[Link to YouTube video](https://youtube.com/shorts/7bV1cbSMbsc?feature=share)

![Image1](/assets/irregular_terrain_surface_normal_01.png)

![Image2](/assets/irregular_terrain_surface_normal_02.png)

![Image3](/assets/irregular_terrain_surface_normal_03.png)

