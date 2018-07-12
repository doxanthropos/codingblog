---
layout: post
title:  "GD50 Lecture 1 - Pong: What I have learned"
date:   2018-07-12
exzerpt: >
  Havard has some new online courses around the main Computer Science intro "CS50" and I have started to watch the lectures and code the code from the Game Development course that is taught by Colton Ogden who already has had some appearances on the main CS50 course.
categories: [game-dev, GD50, lua, love2d]
---

* [Delta Time](#delta-time)
* [Versions of Löve2D matter](#versions-of-löve2d-matter)
* [Virtual Width and Height](#virtual-width-and-height)
* [Using Max and Min Functions for Movement Boundaries](#using-max-and-min-functions-for-movement-boundaries)
* [State Machines and Game State](#state-machines-and-game-state)


# Delta Time

Not to confuse with the [song by the same name][delta-time-song] by the band CAPITAL PUNISHMENT (where Ben Stiller made Punkrock in his youth), [delta time][delta-time] refers to the time delay between update of the game state.
Using delta time to modify the speed of objects allows for a game to have the same playing speed, even when the framerate varies due to hardware differences. So for example in the Pong example, the speed of the ball has a speed variable set to 200 that is always multiplied by delta time in the actual game. Delta time is [provided by Löve2D][love-dt] through the love.update() function.

# Versions of Löve2D Matter

Löve2D is very actively developed, which makes itself noticable in frequent changes.
Colton wrote the code for the Pong versions starting in January this year (2018) and Löve2D had one version change since then. This version change broke the [push][push] library and the color settings of these examples.
So it seems prudent, to always note the version of Löve2D that was used to create a game to be able to run it with the same version of Löve2D or to look for changes in the engine to make it run on newer versions.
Luckily the documentation of Löve2D takes care of noting these changes in an easy to find way at the top of every function that was subject to change in the past:
![A screenshot showing a notification about changed behaviour in a Löve2D function](/images/posts/love.color.png)

# Virtual Width and Height

Using the [push][push] library, it is possible to use a virtual resolution for a game. This virtual resolution will be mapped to the real resolution. So you define a width and a hight for your game to run on, that will produce a game window of this size, but also define a virtual width and a virtual height, that will actually be used for calculations and display in the game.
In the Pong example, Colton uses a significantly smaller virtual resolution for the game to achieve a pixely retro look.

# Using max and min functions for movement boundaries

This one is quite easy and I am a little embarrassed, that I needed to learn it here:
When you have player movement, like the paddle in Pong, you will want to restrict that movement to the actual game screen and not allow the paddle to leave it.
I have until now usually done that using a second conditional inside the conditional that evaluates the players keypresses, like this:

```lua
if love.keyboard.isDown('w') then
  if (player1Y + -PADDLE_SPEED * dt) < 0 then
    player1Y = 0
  else
    player1Y = player1Y + -PADDLE_SPEED * dt
  end
end
```
As the headline says, this can be done much simpler using min or max at these boundaries, like here:

```lua
if love.keyboard.isDown('w') then
  player1Y = math.max(0, player1Y + -PADDLE_SPEED * dt)
end
```

# State Machines and Game State

Colton uses the concept of a [state machine][state-machine] for the different states a game can have, which are in the Pong example the "serve"-state, where the ball stands still, but it is defined in which direction it will move when the player starts the game by pressing "enter" and the "play"-state, in which the ball is on the move until one of the players scores a point.
At this point it seems a bit of overdefining to use this concept here, as the two states are easily undrestood and also coded, without thinking in these more abstract computer science terms. I suppose this will change with games that are more complex then Pong.

This is also one of the many points where this first lecture, while walking through making a Pong clone differs significantly from the 1001 Pong clone tutorials that you can find on the internets: Odgen is clearly building a foundation to work with in more complex games in the future lectures.

# sfxr (bfxr) Tool for Simple Sound Effects

Another part that is often missing from these simple "Build a Pong clone with X in X minutes" tutorials is sound.
For minimalist retro games, like Pong and probably most of the other games of this course, there is a nice tool to generate random game sounds, called [bfxr][bfxr], that is easy to use and is based on the slightly simpler [sfxr][sfxr], that I will use, because it has a Linux version.

That's it for the first lecture. I think it was quite entertaining and helpful.

Let's see what the other lectures will bring.

[push]: https://github.com/Ulydev/push
[delta-time]: https://en.wikipedia.org/wiki/Delta_timing
[delta-time-song]: https://www.youtube.com/watch?v=ijfg5wRZ_t0
[love-dt]: https://love2d.org/wiki/dt
[lua-oop]: https://www.lua.org/pil/16.html
[class]: https://github.com/vrld/hump/blob/master/class.lua
[state-machine]: https://en.wikipedia.org/wiki/Finite-state_machine
[sfxr]: http://www.drpetter.se/project_sfxr.html
[bfxr]: https://www.bfxr.net/
