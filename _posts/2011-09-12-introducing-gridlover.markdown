---
layout: post
title: Introducing Gridlover
---
Web is 85% typography. That's why we built [Gridlover](http://www.gridlover.net). It is a web app to building a vertical rhythm for your web typography. It has interactive sliders and will spit ready-made CSS for you. Go try it out!

### Screenshot of Gridlover ###

![Screenshot of Gridlover](/images/gridlover-screenshot.png "Screenshot of Gridlover")

## Background for Gridlover ##

I practice continous learning. I cannot help it, it's built inside me. I like learning new stuff because it's fun. About a 5-6 months ago I got interested in typography. I have always liked design and I have understood some aspects of typography, but I had really limited understanding about the insights of typography. 

One day I set my sight on web typography. That was something I liked to know more. How do you learn? I do it by asking questions. A lot of them. Naturally it involves a great deal of searching the web and consuming content. [Ville](http://www.pumpula.net) was the prime target for my questions, he answered my questions about web typography and pointed me to right directions. One concept that stuck in my head after one typography related question-bombing was vertical rhythm. Ville explained the idea and pointed me to [A List Apart](http://www.alistapart.com/articles/settingtypeontheweb) article. I read it and somewhat understood it, but I still needed something tangible, something visual.

What programmer/hacker does in a situation like this? Yep, you guessed it! I built a small prototype. So instead of learning broad range of information of typography, I took one specific thing and taught that to myself. Sometimes you just have to go with the flow...

Three sliders that control the vertical rhythm of the layout. When adjusting the sliders the wrong way, it had lorem lipsum bouncing all over the screen because of some bugs. That was the first minimum viable product. I showed that to Ville and he got excited about it as well. We built it at the point where the technical debt became too high to pay, so we started from scratch. In a projects like these, it's not a big deal.

### Here is screenshot of Gridlover before we started again from scratch ###

![Screenshot of Gridlover prototype](/images/gridlover-early-prototype.png "Screenshot of Gridlover prototype")

## One Lesson Learned about Deployment ##

The next prototype didn't actually get too far. I think I have pinpointed to reason pretty accurately. The reason the prototype did not go anywhere is me. I can take the blame for this one.

There is just no point of concentrating building most sophisticated deployment system first if you have nothing to deploy. Now, It sounds pretty obvious, but when you are totally pumped about the "doing it the right way this time", you might not recognize the things that matter. I think this falls near the premature optimization category.

__Do not build sophisticated deployment system at first. When you have something to deploy, only then worry about automating it.__

As for technical side note, it was [Rakefile](http://rake.rubyforge.org) which had tasks sprockets, JS minification, deployment, all that cool stuff. I have still it somewhere, so it might be handy in the future.

Luckily, after failed second prototype, Ville built third prototype. In fact it would not be fair to call it a prototype. It is the one you see online and it looks great!

## This is a Start For Our Minimum Viable Product ##

Launching Gridlover is definitely not laying back and watching site visitor number going through the roof. This is just a start. We built something and we put it out there to see if anyone likes it. I think we have a great vision for Gridlover. Yet, it's not a detailed plan. So who knows where the road takes our small web app.

By the way, I still want to learn more about typography, so one day I probably get back on it.

If you read this far, go test the [Gridlover](http://www.gridlover.net)! We would love any feedback from it.
