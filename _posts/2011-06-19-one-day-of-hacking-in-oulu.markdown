---
title: CSSMesta - One Day of Hacking in Oulu
layout: post
---
I have been talking with [my friend](http://www.pumpula.net) about building a small web app for at least six months. The idea has been evolving almost everytime we discussed about it, but it never got any further except few prototypes. 

I guess good things need time to develop. Our schedules cleared up for one weekend so the time had come! We decided to do two man hack festival for one day.

Last saturday, we went down to Oulu city centre with our laptops.
We had no plan, except the general idea what we have been discussing. The plan was to find a nice cafe, open our laptops and develop a web app.

## Our Ad-hoc Development Environment

[Oulu](http://en.wikipedia.org/wiki/Oulu) has [Panoulu](http://www.panoulu.net), open wireless network spread across the city. Did I mention it is free? It's completely free. So we had wlan sorted out. And we had 3G as a backup.

As a die-hard Git fan, I have a confession to make. We did not use Git. Instead, we used Dropbox. We had a shared folder where I ran the development server. Both of us edited the files and it worked pretty well. We had just few occasions when editing a file ended up in conflict but they were easy to fix. So this was our development environment:

**Dropbox &rarr; Rails (WEBrick) &rarr; Browser**

For brief moment, Panoulu did not work for both of us, so then we had this setup:

**Dropbox &rarr; Rails (WEBrick) &rarr; Localtunnel &rarr; Browser**

[Localtunnel](http://progrium.com/localtunnel/) is just awesome. It's simple and easy and it just works.

## Mobile Office

First batch of developing we spent at coffeehouse. Unfortunately, I don't remember the name. It is a nice little cafe. The place was quiet, so that's a big plus if you want to do some hacking. Too bad I didn't took any pictures.

For second part, we walked around a bit and saw a cafe called Puistola.
From outside, the place looked nice, so we decided to give it a try.

We took seats by the window and setup our gear:

![Our mobile office at Puistola](/images/cssmesta-mobile-office.jpg "Our Mobile Office at Puistola Deli")

Now, that looks pretty awesome! Only downside was the occasional loud noise that came from coffee machines. But overall, it was good place to do some serious developing. 

When we do our next tiny hack-festival, Puistola most likely will be one of our destinations. 

## The App We Developed

We built [CSSMesta](http://cssmesta.heroku.com). It's a small webapp for CSS galleries. We provide the markup and you provide the CSS. Go try it, it might even like it! :)

Currently, we are hosting it on Heroku. It's still a [MVP](http://en.wikipedia.org/wiki/Minimum_viable_product). If we get positive reaction from the internets, then we have to think about domains, hosting and stuff, but for now we settle on Heroku. 

The day was totally fun! Our tiny hack-festival was a success! We managed to make a small web app and it feels just awesome!

I recommend this spending a day this way for everyone!
