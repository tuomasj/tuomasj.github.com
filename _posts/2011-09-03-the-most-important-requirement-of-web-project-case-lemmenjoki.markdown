---
layout: post
title: The Most Important Requirement of Web Project - Case Lemmenjoki.fi
---
This post was originally supposed to be a simple case study, describing how I got the idea for my little web project. It still describes it, but I write more about vision and how that vision turned into requirements. Now, when I say small, I really mean small web site. One page small. 

I built a web site for [Lemmenjoki National Park](http://www.lemmenjoki.fi). It's a beautiful area of almost untouched wilderness at north of Finland. It's not really a page for national park, it's scope is much more narrow than that. But I'll explain that in a bit.

## Background ##

Lemmenjoki is a small town next to Lemmenjoki National Park. It's pretty remote, so getting there using public transportation may be difficult for tourists. A town called Inari is closest town which is on route of public transportation going all the way to Norway. Schedules for these lines are accessible through various websites and route to Lemmenjoki is there too, but the usability of those web sites might prevent the access to the schedule information. Many times tourists have trouble finding information how to get to Lemmenjoki. Hey, this sounds like a problem that can be solved by building a small website!

I haven't done any tourist websites and I don't have any domain specific knowledge on tourism websites. Yet, that did not stop me for solving a problem I have witnessed numerous times. If I keep it small and simple, I might be able to pull it off...

## Figuring Out The Vision ##

My first step was to think about a typical scenario how the website would be used. I call it hypothesis. Hypothesis means that I take a educated guess of the way the web site would be used. It describes the problem and how it is going to be solved. Naturally, I haven't validated my hypothesis at all, but it's ok, this is just a small web site. 

Here is my hypothesis: 

*"A english speaking tourist is at Inari and wants to travel to Lemmenjoki National Park for few days. He doesn't quite know how to get there, so he searches for Lemmenjoki public transportation schedules with his smartphone. He opens [Lemmenjoki.fi](http://www.lemmenjoki.fi) through search results and finds the schedules, and some local activities."*

Ok, now I have the vision for my little web project. So... Whats the next step?

## Requirement Gathering Process ##

Wow, that sounds like I am building a enterprise class software, which takes 4 years to built with 100 developers, located in three different continents, with end result nobody wants to use. Luckily, the situation is not that bad at all. The fancy title just means that I did think about few basic things I want the website to have. Even with small website like this, it makes sense of figuring out the main points before you open up Vim or any other code editor, like Textmate.

Here are few requirements I came up:

 * Schedule information should be the first priority of the website
 * Website must be very light so it loads fast and it does not cost must if user is paying for every transferred bit when using mobile on the road
 * Tourist might want to check the schedule information on the road, so it must be accessible with mobile browsers
 * It does not compete with websites of local Lemmenjoki tourism entrepreneurs
 * I want it to be a "fire and forget" website, only updating the schedules when they change

Looking the list of my requirements, I began to wonder that something is missing. A one requirement that would put everything else in line. Those are perfectly valid requirements, but I need more than that. I want a requirement that constantly reminds me what I'm doing. To some people it might be totally obvious, but since I have hundreds of unfinished projects stored in the dark corners of my hard drives, I keep that requirement just in case...

So let's add one more requirement.

## Keeping It Real ##

 * **This must be launched today**
 * Schedule information should be the first priority of the website
 * Website must be very light so it loads fast and it does not cost must if user is paying for every transferred bit when using mobile on the road
 * Tourist might want to check the schedule information on the road, so it must be accessible with mobile browsers
 * It does not compete with websites of local Lemmenjoki tourism entrepreneurs
 * I want it to be a "fire and forget" website, only updating the schedules when they change

Now it is really a list of requirements for my small web project! There is the most important requirement, which puts all other requirements into perspective. Now I can see if the requirements are realistic or are they just some bunch requirements with no real connection to each other.

The requirements state that I need to build a website today, it has schedues, lightweight layout and it must work with mobile browsers. Since I had the hypothesis that tourists will use search engine for public transport schedules from Inari to Lemmenjoki, it was really easy to focus to solving that problem.

For a small site like this, requirement gathering process took about 4-5 minutes. And same thing in human language: it took 4-5 minutes for me to figure out what kind of stuff the web site needs.

## Launch It! ##

Launching a web site is fun! Put something out there, something that creates value to somebody, and see if people like it. If you don't launch your web projects, you're missing lot of fun. If you write down a list of requirements on a yellow note, make sure you write your your first and most important requirement:

"This web project must be launched"
