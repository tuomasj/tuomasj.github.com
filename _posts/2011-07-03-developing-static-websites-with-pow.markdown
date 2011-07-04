---
title: Developing Static Websites With Pow and Mac OS X 10.6
layout: post
---
## Would you like to develop your static website on http://mystaticsite.dev? ##

This blog post describes a way to use Pow web server to host your static website. Pow will host your website locally, allowing access only from same computer.

## Pow!! ##

[Pow](http://pow.cx) is a zero configuration Rack server for Mac OS X. Rack is a small software component written in Ruby. It is used to develop web servers, for example Ruby on Rails. Pow was developed by [Sam Stephenson](http://twitter.com/#!/sstephenson) from [37Signals](http://www.37signals.com) and you can follow the development at [Pow Github repository](https://github.com/37signals/pow).

Since you are running Mac OS X, you already have Apache web server. There is nothing wrong with Apache, but if you feel like trying something new, try Pow. You might like it :)

## Install Pow ##

Installing Pow is easy, but you need to use console a bit. Just go to Pow homepage, and follow the [installation instructions](http://pow.cx/manual.html#section_1). On the same page, there are uninstall instructions as well.

To try if it really worked, open your browser and type some nonsense address with '.dev' at the end. Like http://nonsense.dev

If you something like "Application not found", it means Pow is running. There is also instructions how to create an app for that domain.

## Concerning Your Static Site ##

To make things simple, let's assume you have a static website called "MyStaticSite" which is located in your Projects directory as "MyStaticSite".

Before you are ready to go, there is just one requirement for your static site. All your files must be located in "public" directory. So if your files are located at 

    /Users/bobbytables/Projects/MyStaticSite

You need to add a directory called "public" and move your files over there.

When you created the directory and moved the files, your directory structure should be something like this:

    /Projects/MyStaticSite/
      public/
        index.html
        stylesheet.css


## Put Your App Online ##

This is the hard part. You need to use console and create a symlink. [Symbolic link](http://en.wikipedia.org/wiki/Symbolic_link) is a "fake" file which points to another file. If you edit the fake file, you will change the original file. If you delete the original file, you will lose the fake file also. On the other hand, if you delete the fake file, you just lose the fake file. A fake file can also be a directory (folder) too and the same rules apply. This is the way Pow determines what directories it needs to serve.

To get your static site to appear as http://mystaticsite.dev, you need to create a symbolic file from your site's directory, pointing to Pow configuration directory. You can create as many symlinks as you need. Open a console and type the following:

    cd ~/.pow
    ln -s ~/Projects/MyStaticSite

If you are wondering why the ".pow" directory does not show up on finder or directory listing, it because it's an hidden directory. Every file or directory starting with period is hidden on Mac OS X . But even it's hidden, you can still access it. If you want to know more, [this](http://en.wikipedia.org/wiki/Hidden_file_and_hidden_directory#Unix_and_Unix-like_environments) is a wikipedia article you need to read.

Let's check, if your symlinking worked. Type is on console: 

    ls -l

The extra parameter will make symlinks show up properly. You should see a directory listing with arrows describing a symbolic link to the original directory. 

Another way of testing did it work is to launch up a browser and surfing to **http://mystaticsite.dev**.

If it did not work, check that your symbolic link is pointing to right directory and it is created inside ~/.pow directory.

## Is Pow Running Forever and Eating Up My Precious CPU and Battery? ##

No. If you read the [Pow manual](http://pow.cx/manual.html#section_2), it says that Pow will start a worker process on first connection and then terminates them after 15 minutes of inactivity. So, basicly a single Node.js application is waiting for connections to your static website address (e.g. http://mystaticsite.dev) and on first connection, it will start up two worker processes which server your files to you.

## What Next? ##

Well, this is it. You're done! :)

If you want to know more about Pow, go to [Pow website](http://pow.cx). 
