---
title: Redesign and Relaunch of Yourdream.io
layout: post
tags:
  - sideproject2013
---
Past few weeks I have been improving my savings calculator, [yourdream.io](http://www.yourdream.io).
I was not very happy with it, it had some rough edges and the code was not that structured. That is quite
surprising,  since I used [backbone.js](http://documentcloud.github.com/backbone/) to structure my code.
The codebase got totally out of control, it took ridiculous amount of time to figure out all the moving parts.
That is what you get when you write code in a hurry, without thinking. But it didn't matter, since I wanted to launch it.

Once I launched it, I left it in semi-finished state. I would call it a minimum viable product.
The visitors could calculate a savings plan and see how long it takes to reach the goal. That was the only thing it did.
I build just enough so I could verify my first hypothesis, would the visitors want to see how long it takes to save for certain financial goal.
Based on the analytics, there are people using my app, making plans to reach their dreams. Not 100% verified, but
it's enough for me.

After I relaunched [buildcraftcreate](http://www.buildcraftcreate.com), I decided to give some attention to my other launched side projects as well.
I took [yourdream.io](http://www.yourdream.io) and decided to fix few things to offer better experience for visitors. I had forgotten how bad the code was.
After I had fought few evenings with yourdream codecase, wasting time with bad code, I decided to rewrite the whole thing from scratch.

## Paying the Technical Debt ##

I have very limited time to spend on my side projects per week. Basicly, I have just rewritten the application.
There are no new features. It looks a bit different, I redesigned the user interface, but it's still the same application.
It's still validating the same hypothesis. Considering that I have one year to [reach my goal](http://rebelcode.net/2013/01/01/in-2013-i-will-build-a-side-project-that-generates-income.html),
spending two weeks doing something what I have already done, does not sound very good idea. I sounds like a waste of time.

But there is one thing certain in software projects. You have to pay the technical debt. If you do not pay it,
it will grow bigger and bigger. The debt manifests itself as tight coupling, complex classes with multiple purposes and
non-existing software architecture. These are the things that will make new feature implementation really hard.

## Faster Hypothesis Validation ##

It is the reason I rewrote the whole application. I can build features faster. I can validate hypothesis faster.
I can iterate around the problem faster. The codebase is now pretty solid. It still has few problems here and there,
but I can live with them.

Now I am able to spend my time even more efficiently. I can learn faster. And it was fun to rewrite it, and that is the most important factor :)

