---
layout: post
title: "Automatically follow new Twitter followers"
date: 2014-01-24 17:56:48 -0500
comments: true
categories: Twitter Marketing
---
Are you getting a lot of followers on your Twitter account? Do you want to follow them also, without laboriously clicking follow for every single one? If you are a Mac or Linux user I have an easy trick for you to manage following/un-following a lot of people on Twitter at one time.<!--more-->
What I use to automate Twitter is a command line program written in Ruby, this program is a RubyGem called "T" and you can learn more about it on [GitHub - Sferik/t](https://github.com/sferik/t). Installation of this RubyGem is pretty straight-forward, if you already have Ruby installed you can install the gem itself with the following command.
```
gem install t
```
After installing the gem there are a few configuration settings you will need to get started with to authorize this application to use your Twitter account. Pretty easy, just set up an application with your Twitter account as you are directed on the GitHub page for this gem and copy some numbers to a file. Once you get it set up you can use something like the following command loop to automatically follow-back any new follower to your twitter account.
```
while true; do "t groupies | xargs t follow"; sleep 2; done
```
The above command string will check for new followers every two seconds and follow them back, without you doing anything.
