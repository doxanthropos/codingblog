---
layout: post
title:  "Game Idea: Scream Maze"
date:   2018-02-07
exzerpt: >
  Where I describe a game I would like to build, why I think it is a fun idea and what it will take to do so.
categories: [game-dev, code-more]
---

**TLDR**: I thought about what I would like to built: A "horror" maze game, where you have to scream to move.

* [Will there be a maze?](#will-there-be-a-maze)
* [VR, but how?](#vr-but-how)
* [Screeeaam!!!](#screeeaam)
* [Next Steps](#next-steps)

## Will there be a maze?

So I have decided to be more productive and creative in my free time. But what exactly will that be? "Code more" even with the great help from the Codenewbie-community is something that has to be fleshed out.

One direction that I always wanted to explore since I started coding, but somehow never did until now, is game making. After stumbling upon more blog posts, articles and forums questions on making games than usual[^1], I began to think about what kind of game I would like and also be able to do.

One simple idea that can be quite sophisticated in the execution is a maze, especially if it is to be explored in first person perspective. After having thought this, I immediatly thought about VR and at first was fine with that. So I will try to make a first person, maze solving game that can be played in VR (preferable with one of the cheaper VR sets[^2]).

## VR, but how?

But VR, and especially the cheaper gear, has one problem: they only track rotational movement, not translational (in other words: you can choose where to look, but not move). So how does one move through a maze with this? Common solutions are: markers that you can focus/click to go in their direction or using a seperate handheld controller. I did not like the thought of both these solutions, because the marker solution is kind of clumsy, it does not make sense in the game worlds and because most people do not have a seperate handheld controller for their phones.

So I thought about the possibilities: what kinds of sensors does a phone have, that could be used? The rotatinal tracking is already in use with the VR. The touchscreen is not reachable, because it will be inside a headset. The buttons on the sides are different with different phones and also covered with the headset. GPS is not fine grained enough and also: it could be quite dangerous to make people move with a headset over their eyes. The camera? I have no idea how to reasonably map movement to the camera input. But what about sound input? Every phone has a mic. I only need to control speed anyway, so it could be mapped to the volume. But does that make any sense?

## Screeeaam!!!

If the maze is in a horror setting, screaming while trying to escape does not seem to far fetched. So it might be fitting.

The moment, I really considered it an interesting idea to move through a maze by screaming, I remembered that I had heard about a game that was controlled by sound before: ["SCREAM 'EM UP1"][seu][^3]

Of course I have no idea if this is a mechanic that works well or if it is fun, but I at least imagine it to be.

The game mechanic I imagine is this: you can change direction and look via moving your head and/or turning around and you can move by making noise, scream louder and you will be faster, be silent and you do not move at all.

One negative aspect of this mechanic will be that it can't be played everywhere, because it will disturb people around you. If I were planning on making a game for the masses, I would see this as a problem, but since it is more for fun, for myself and if I succeed, for people who might like strange things, this does not concern me very much.

It will certainly be a challenge for me to develop and test something like this, because beside the technical challenges, I am a rather quiet person and do not like to make noise, but that is one part of why this idea intrigues me. Like you can see in the effect that the scream em up, that I mentioned had at the players, I think that this can be something that makes the player open up, dare to be heard and have fun.

## Next Steps

The next steps, after having this initial idea will be to plan the project, to choose the appropriate technology, basically the whole design part. Will I make my own game art, use free assets or try to find someone to team up with? Will I use [Processing][processing] (which I know), [Godot][godot] (which I don't know, but which looks interesting and runs on Linux) or like many game creators [Unity][unity] (which I do not know, but for which there are a lot of tutorials and courses, but which does not really run on Linux)[^4]. Will there be designed levels or will there be generated levels (I really need to watch the [Coding Challenge on this topic][coding-maze]), will there be enemies, treasure, time limits, multi-player options?

### Footnotes

[^1]: One of these articles, that I really recommend, is the entertaining [history of "The Faery Tale Adventure"][faery-tale].
[^2]: I only have a rather old phone (Galaxy 5S) and a 20€ headset for it, to use with google cardboard apps.
[^3]: I am not sure, where I first heard about this. It was one of the interviews the maker of this game, [Jane Friedhoff][jf]  gave on youtube, either the one with [Daniel Shiffman][coding-train] or the one with [Jonathan Holmes][holmes], both are worth watching.
[^4]: There will definitively be sound and music.

[faery-tale]: https://medium.com/@dreamertalin/the-faery-tale-adventure-a-personal-history-4fae0617a18d
[coding-train]: https://www.youtube.com/watch?v=VIEwBm7PWQM
[holmes]: https://www.youtube.com/watch?v=aH0aY5ilCfo
[coding-maze]: https://www.youtube.com/watch?v=HyK_Q5rrcr4
[processing]: https://processing.org/
[godot]: https://godotengine.org/
[unity]: https://unity3d.com/
[seu]: https://vimeo.com/41629022
[jf]: http://janefriedhoff.com/