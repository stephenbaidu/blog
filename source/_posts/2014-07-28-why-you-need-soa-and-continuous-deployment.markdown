---
layout: post
title: "Why you need SOA and Continuous Deployment"
date: 2014-07-28 21:33
comments: true
categories: 
---

>When everyone wants to do things their way, there will be chaos.

If you work with developers of various talents, you'll understand the quote above. There is a way to leverage this scenario, and that is to have small teams take responsibilities of various aspects of your product(s). This encourages ownership hence, higher productivity. But you have to make sure there are solid structures in place. This brings us back to the topic "SOA (Service Oriented Architecture) and Continuous Deployment". You can read more about SOAs by [Martin Fowler](http://martinfowler.com/aboutMe.html) from [here](http://martinfowler.com/articles/microservices.html).

We currently adviced our team to embrace Microservices(using this synonymously with SOAs) and Continuous Deployment. Though it was a bit difficult at the beginning, we are very happy now. Not only has productivity gone up, we are happier as developers. After I encouraged the team to look at [docker](https://www.docker.com/whatisdocker/), we settled on [dokku](https://github.com/progrium/dokku) which is like a mini-Heroku, based on docker. As developers, we love to automate stuff, hence the reason for settling with something "similar" to [Heroku](https://www.heroku.com/).

With this architecture, individual teams could decide on the languages and frameworks they want to use and we still get a unified environment for various services. [Docker]() is a linux container engine and fun to play with. [Dokku]() sits on top of this (with 100 lines of bash script), to deliver continuous git deployment. I suggest playing with docker for a while before moving to dokku, and you might not even want dokku for your use case. Dokku does not support multiple hosts, that's why we are all waiting for [Flynn](https://flynn.io/), which currently has 15+ sponsors.