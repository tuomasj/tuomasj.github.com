---
layout: post
title: Generating Static HTML with Sinatra and Hating Meetings
---
This blog post is about rendering templates into actual files with Sinatra. If you are looking to render a static text file with Sinatra, try this:

{% highlight ruby %}
get '/' do
  send_file File.join('public', 'index.html')
end

{% endhighlight %}

If you don't want to read the backstory, jump to part about [generating HTML with Sinatra](#rendering_templates_into_files_with_sinatra)

## Meetings, Meetings, Stop Wasting My Time ##

I've always considered too many meetings are waste of time. Yes, you can get things done, but usually there are just too many participants, the meeting lacks a clear agenda, and just when the meeting is about to get into the point, time runs out and everybody scatters. Running a useful meeting is really hard.

So I did what any hacker would do: I created an app that would fix the meetings.

The plan was to spend minimal amount of time to come up with a solution that would be helpful in meetings. It was really simple online meeting timer. You start as you begin the meeting and timer starts running. You share the link with remote participants. Everyone is aware how much time the meeting has taken. Very minimal app, very limited functionality. 

I have had it running neglected for many years, without any love or attention from me. Surprisingly though, it has steady organic traffic. Very, very small, but steady. Based on the analytics, there are people actually using it! They press the "Start Timer" button! I'm making a better world by helping out few people to run meetings more efficiently. Not exactly making a better world on Nobel-prize scale, but it's still better than nothing :)

## The Rewrite of My Minimal Web App ##

Few weeks ago, we had a Coding Dojo in Oulu. During the event, We had a very good chat about the usefulness of Coffeescript, is the productivity gains really worth of learning Coffeescript. So when I got back home, I got this itch on my fingers. The kind of itch which makes you open up your code editor and write some code... I needed to write some Coffeescript.

The meeting timer looked like a perfect candidate for a rewrite. Really limited functionality, few page web application. Besides, It was my last app running on PHP. Like I said, a perfect candidate. 

It took few evenings to finish the rewrite using Coffeescript and Backbone. During the rewrite, I stripped down the functionality bit more, leaving just the timer. Big thanks to [@sakamies](http://twitter.com/sakamies) for helping out with the minimal user interface.

I discovered that I could get HTML5 PushState to handle the URL functionality, so a server-side component was not even needed. I could host it on Amazon S3 as a static website.

I forgot the original point my rewrite five minutes after writing the first line of code. I think there was some point during the chat that I wanted to test for myself, but it's all gone now :)

## Running Sinatra as Part of Your Development Environment ##

I developed the app using [Sinatra](http://www.sinatrarb.com) and [Sinatra-assetpack](https://github.com/rstacruz/sinatra-assetpack) as part of my development environment. Assetpack complies Javascript into Coffeescript and SCSS into CSS. It runs on development mode, serving all JS/CSS assets as separate files and on production mode it squashes all assets into one file. Minified Javascript code has one file and minified CSS code has one file.

Hosting it with Sinatra as a server felt overkill, since Sinatra only compiles the coffeescript and scss. I like to keep things simple and tidy. The alternative solution, running Sinatra locally and copying the HTML code from browser's "view source" window just felt so wrong. 

Generating a static website using Sinatra, that's the solution I was after.

(For the record, I have LiveReload and I have written Guard tasks which compiles Coffeescript and SCSS)

## Rendering Templates into Files with Sinatra ##

Rack has a MockRequest helper, which allows to simulate a HTTP request and outputs the request body. Sinatra is running on top of Rack, it spits out HTML which is rendered through Sinatra templating engine.

Below is an example how to use it to get the response body without actually running Sinatra.

## Example Usage ##

### Sinatra Application ###

{% highlight ruby %}
# app.rb

require 'sinatra'

get '/' do
  erb :index
end
{% endhighlight %}

### Application Layout File ###

{% highlight ruby %}
# views/layout.erb

<html>
<head>
    <title>Sinatra Test</title>
</head>
<body>
    <h1>Sinatra Test</h1>
    <div id="content">
    <%= yield %>
    </div>
</body>
</html>
{% endhighlight %}

### Index.erb Layout File ###

{% highlight ruby %}
# views/index.erb

<p>Content from index.erb</p>
{% endhighlight %}

### How to Simulate a HTTP Request ###

{% highlight ruby %}
sinatra/ $ irb
irb(main):001:0> require './app.rb'
=> true
irb(main):002:0> request = Rack::MockRequest.new(Sinatra::Application)
=> #<Rack::MockRequest:0x007fa842978b68 @app=Sinatra::Application>
irb(main):003:0> puts request.get('/').body
<html>
<head>
    <title>Sinatra Test</title>
</head>
<body>
    <h1>Sinatra Test</h1>
    <div id="content">
    <p>Content from index.erb</p>
    </div>
</body>
</html>
=> nil
{% endhighlight %}

The part which does all the heavy lifting is
{% highlight ruby %}
request = Rack::MockRequest.new(Sinatra::Application)
puts request.get('/').body
{% endhighlight %}

## The End ##

I deploy the site with combination of Assetpack's rake tasks and my own custom rake task. Index.html gets built through Sinatra, using Assetpack's JS and CSS helpers. Assetpack compiles and minifies coffeescript and scss files.

This is the way my minimal web app called [Meetingtimer.net](http://www.meetingtimer.net) was done and deployed.

Yet another web app polluting the Internet :)
