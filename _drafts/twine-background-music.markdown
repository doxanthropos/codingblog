---
layout: post
title:  "Interactive Storytelling with Twine: Making Background Music Work Even in Chrome"
date:   2018-08-05
exzerpt: >
  Providing a solution to one specific problem: background audio in Twine Games/Stories, that plays automatically and also works in Chrome
categories: [game-dev, interactive-storytelling, twine]
---

I will first explain the problem, then show how background music is usually done and at last show how to fix the Chrome issue. If you are only interested in the fix, because you already know the rest, you can jump to [Solving the Chrome Autoplay Issue](#solving-the-chrome-autoplay-issue).

For those who do not know what [Twine][twine] is, Liz England has written a [good article that answers this question][what-is-twine].

**TLDL:** To have continuous background music work in Chrome, you ha


* [The Problem](#the-problem)
* [Background Audio](#background-audio)
* [Solving the Chrome Autoplay Issue](#solving-the-chrome-autoplay-issue)

# The Problem

A lot of games and interactive stories utilize background music or sound to generate atmosphere, beginning at the very start of the game.
Sadly Google Chrome, in an effort to stop make the web better, by blocking autoplay for videos and sound, has also blocked any form of music or sound, that would be played before the first player interaction.
They have written about it in two articles:
[Autoplay Policy Changes](https://developers.google.com/web/updates/2017/09/autoplay-policy-changes) and [Improving Autoplay in Chrome](https://blog.google/products/chrome/improving-autoplay-chrome/).

The basic change is this: audio and video will not start in Chrome, before the first user interaction happened. An exception to this will be some websites, determined by some self learning algorithm, that will allow autoplay sometimes, based on if the user or many other users already listened to sound or watched video on that site before.

This makes two kinds of people unhappy for seemingly opposing reasons:

One group of people think that autoplay is the devil and should be banned from all websites with no exceptions. These people do not like the self learning exception generator very much.

The other group are the people who have develope(d) games and elearning content for the web, that now lost audio functionality it once had. There are some ways to still have the same effects, like I am showing below for background music in Twine, but these have to be implemented and creators of games and elearning content usually move on to other projects, after completing one. Revisiting all past projects is not an option for most of us.

So to narrow the problem a bit down to the specific aspect promised in the title: There are some easy ways to implement background music in Twine, that have been used and taught for some time, that now do not work anymore.

# Background Audio
![A Storyboard of a small Twine Story with three normal passages and three configuration passages](/images/posts/20180805-story-overview.png)

This is the small story that I will use as an example for background music in Twine.

To add music to it you need to first create a folder, where you are goint to export your Story into. I called mine "Twine Projects" and to keep it tidy, I also created a folder inside this project folder, with the name "audio".
![A folder inside a folder](/images/posts/20180805-folder-structure.png)

Inside this folder ("audio") I saved the music, that I want to use in my story. The file has the name `"Daniel_Birch_-_05_-_Sinking_In_The_Rain.mp3"`, so to reference this file from the project folder, the path would be `"audio/Daniel_Birch_-_05_-_Sinking_In_The_Rain.mp3"`.

To have it play from the beginning, I use some simple lines of JavaScript in the Story JavaScript file:
```javascript
var backgroundAudio = document.createElement('audio');
backgroundAudio.src = 'audio/Daniel_Birch_-_05_-_Sinking_In_The_Rain.mp3';
backgroundAudio.loop = true;
backgroundAudio.volume = 0.4;
backgroundAudio.play();
```
This is basically the way to do it that is show by the DigitalExposure Youtube video [Twine 2.0 - how to Add Music / Tutorial #15][DE]
# Solving the Chrome Autoplay Issue

[before][example-before]

[after][example-after]

You can download both examples, the one that works in Chrome and the one that does not here as a zip file:
* [Examples][example-download]


# Credits

The background music in this example is <a href="http://freemusicarchive.org/music/Daniel_Birch/Ambient_Vol3/Sinking_In_The_Rain">Sinking in the Rain by Daniel Birch</a>.
I got the basics on how to add background music to a Twine story from [Youtube tutorial by DigitalExposureTV][DE].
For the version that also works on Google Chrome:
I learned how to create JavaScript functions that can be accessed from inside a story from a <a  href="https://www.youtube.com/watch?v=JjRoHAO6nAQ">Video by Dan Cox</a>.

[twine]: http://twinery.org/
[what-is-twine]: http://www.lizengland.com/blog/2015/03/what-is-twine-for-developers/
[DE]: https://www.youtube.com/watch?v=bm9Lvd1Qg4Y
[example-before]: http://knut.codes/twine/2018-08-background-music/Techniktest.html
[example-after]: http://knut.codes/twine/2018-08-background-music/Techniktest_for_Chrome.html
[example-download]: http://knut.codes/twine/2018-08-background-music/2018-08-background-music.zip
