---
layout: post
title:  "#CNC2018 Blog More: Pre-Mission"
date:   2018-01-19
exzerpt: >
  Where I get a mission to read 3 blog posts and write about what I read,
  which is: one article about WebRTC, one about looping GIFs and one about creating a newsletter.
categories: [cnc2018, blog-more]
---

* [The Tutorial: WebRTC Video Chat in 20 Lines of JavaScript](#the-tutorial-webrtc-video-chat-in-20-lines-of-javascript)
* [The Explainer: Drawing from noise, and then making animated loopy GIFs from there.](#the-explainer-drawing-from-noise-and-then-making-animated-loopy-gifs-from-there)
* [The Project: How I set up an automatic weekly blog digest](#the-project-how-i-set-up-an-automatic-weekly-blog-digest)
* [Wrapping Up](#wrapping-up)


I enrolled into the [CodeNewbie 2018 Challenge][cnc2018] not just for one, but for two goals: "Code More" and "Blog More".

Both are activities, that I like to do, but fail to do as regularly as I would like to.

Before the first official mission starts, there is a "pre-mission" for both tracks. For the Blog More track it is to find three blog posts from three different categories: tutorial, explainer and project, read them and then write three things that I liked and three things that I might do differently.


## The Tutorial: WebRTC Video Chat in 20 Lines of JavaScript

For the tutorial, I had a look into my bookmarks, where I have a "to read" folder and found an article about [WebRTC][webrtc]: [WebRTC Video Chat in 20 Lines of JavaScript (Part 1)][tutorial]. This is a web technology, that I find interesting and want to learn more about, but did not actually do that for quite some time. For this reason, I had this article in my bookmarks, but have not followed the tutorial yet.

The first thing, that I like is that they take the time and space to explain how to set up a temporary local server for use in this tutorial. While it might be considered beside the actual topic, I have often experienced, that people who are new to web programming have trouble to find how to test their code, if it contains functionality, that will be blocked by the browser if it is not on a server.

Another part that I like about this article is that the code examples are hosted on github, so they are available also as raw files to copy and paste in case something goes wrong.

The third aspect of this article, that I like is that while it is short, as the name suggests, it ends with a complete functional app.

On the other hand, I think I did not learn that much about [WebRTC][webrtc]. While it is good to have someone get their feet wet before exposing too much detail. At least a little more info about the protocol that this tutorial is based on would help getting the feeling to have learned something valuable.

This might be directly related to the fact that this article is somewhat of a marketing article for the pubnub service, which, as the tutorial shows makes using WebRTC really easy. That is nice for someone who wants to use WebRTC, but for someone learning, it might be a bit too easy and to oversimplified.

## The Explainer: Drawing from noise, and then making animated loopy GIFs from there.

There is a blog article, that I have read a few weeks ago, it is called "[Drawing from noise, and then making animated loopy GIFs from there.][explainer]".

In this article Etienne Jacob explains a nice trick to solve a common problem that arises, when you generate random animations and want to create animated gifs from these programs: looping gifs do look jerky and broken, when the last frame of the animation does not fit to the first. It is filed unter tutorials, but since it explains a common principle to achieve the desired effect, I would rather categorize it as an explanation.

The very first thing you see about this article is one amazing example of a gif that was produced with the technique covered in this very article. I like this very much, because the topic is visuals, so it is only fitting to lead with a great visual example.

The explanation itself goes from simple examples to rather complex programmatic art. This makes it easy to understand, but also useful for more experienced creative coders.

Also every example comes with a short explanation and a link to the source code. This is enough to understand whats going on and not to much, so that the whole article stays at a reasonable size.

It's hard to find something that I would do another way, because this is a very good and useful article. Maybe I would include more links to other material, that goes deeper into the topics of randomness.

## The Project: How I set up an automatic weekly blog digest

As the title says, in [How I set up an automatic weekly blog digest][project] Julia Evans writes about how (and not to forget: why) she set up and email newsletter based on her blog.

This might be of interest to other people doing this Blog More challenge!

What I like about not only this article, but about all of Julias posts and talks: she does not pretend to know everything just out of thin air. Instead she is always careful to include how she came to the knowledge that she has. This is one of the topics she is famous for: showing that it is good to admit, not to know something and to ask questions, even if they might sound stupid at first. For example in one of her older posts, she wrote about the answers she got on the questions "[What does a shell even do?][shell]" only shortly after followed by the question (and some answers) "[What does the Linux kernel even do?][kernel]".

So at least one of the paths to writing good blog posts seems to be to find a good question to answer (which must not necessarily look good at first glance), to find answers and to write about them in a way, which you would have understood before understanding the answer.

The process to set up the newsletter sounds simple and doable and the reasons for doing so make sense, especially that people asked her about it.

## Wrapping Up

I realize, that I have strayed from the path of the mission. I did not find 3 good aspects and 3 to make differently for every of the 3 articles. But I think I have had a good look into what it is that works with these articles and what doesn't work.

I'm curious about the next (first) mission.

[cnc2018]: http://2018.codenewbie.org/
[tutorial]: https://www.pubnub.com/blog/2015-08-25-webrtc-video-chat-app-in-20-lines-of-javascript/
[webrtc]: https://developer.mozilla.org/en-US/docs/Web/API/WebRTC_API
[explainer]: https://necessarydisorder.wordpress.com/2017/11/15/drawing-from-noise-and-then-making-animated-loopy-gifs-from-there/
[project]: https://jvns.ca/blog/2017/12/28/making-a-weekly-newsletter/
[shell]: https://jvns.ca/blog/2013/09/30/hacker-school-day-2-what-does-a-shell-even-do/
[kernel]: https://jvns.ca/blog/2013/10/02/day-3-what-does-the-linux-kernel-even-do/
