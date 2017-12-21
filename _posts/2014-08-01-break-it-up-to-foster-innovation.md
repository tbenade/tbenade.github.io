---
layout: post
title:  "Break it up to foster innovation"
date:   2014-08-01 14:14:01
excerpt: "Take the opportunity to motivate innovation through simplification."
tags: [Motivation, Innovation, SOA, Microservices, Distributed Systems]
comments: true
---

<img style="float:left; padding: 0 10px 10px 0" src="/images/potato.jpg" />

As a development manager I often got asked how do you foster innovation. How do you get the crazy smart people who work for you to innovate. Wow! Tough question.

Here is a quick tip from the trenches on creating innovative opportunities *in production*. I say in production because that is where I like things to get done. Giving something to the customer is the most engaging part of building software. Ideas that sit on the bench and go nowhere are fun but have little value if done too often.

If you have a big behemoth web application consider breaking it up into services.
I am deliberately ignoring the buzzwords of SOA or microservices. For now the idea is to identify something you can slice off your application and rapidly make it a candidate for a stand alone service.

Lets take user authentication to the web application as an example.

If you were to rip your user database out of your system and move into its own service how would that foster innovation, or at a minimum provide opportunity to innovate?

<img style="float:right; padding: 0 10px 0px 0" src="/images/chips.jpg" />

* Immediately you have something smaller that you can deploy independently of the bigger solution.
* You could adopt and entirely different technology stack as long as you provide a consumable interface.
* You could start your cloud journey if you are not there already by deploying this service to the cloud.
* Not Agile yet...you could use this project to employ Agile engineering practices like continuos integration or even better continuous delivery.
* Now that authentication is sitting outside your solution you can use it to empower a mobile application [skunk works](http://en.wikipedia.org/wiki/Skunkworks_project) if you are not in that space already.

If you succeed with slicing something off, you can take the lessons learned, identify the next slice and do it all over again. Having these small self-sufficient slices will soon enough give you ample opportunity to learn, innovate and experiment without having to rebuild your entire solution.

Go far enough on your slicing and service journey you will soon be able to deploy the UI entirely independently of the backend/services...imagine all the kinds of crazy your designers and UX ninjas could come up with, with that sort of freedom?!

The last thing you want is your superstar developers who are playing with the cool new toys at home never getting the chance to put them to work in production, because eventually they will leave to go work with these new stacks.

Services/APIs call them what you want they are a great catalyst for creativity so give it a go. If you are new to serviced based system don't get to hung up on being RESTfully compliant or too sophisticated just get moving, get it working and learn. Soon enough you will be crushing each other in code reviews debating arbitrary naming conventions for collections on the wire ;).

I don't think you can make people do anything they don't want to do. If the environment you are providing is leading to no innovation one should consider not looking out into the room and rather look at ones own leadership. Be courageous and have a go!

Some more reading.
[The daddy of the current API movement.](http://kinlane.com/)
[Fowler on microservices](http://martinfowler.com/articles/microservices.html)
[The puzzle of motivation](http://youtu.be/rrkrvAUbU9Y)


photo credit: [Theresa Carle-Sanders](https://www.flickr.com/photos/islandvittles/4363231101/) via [photopin](http://photopin.com/) cc
photo credit: [banger1977](https://www.flickr.com/photos/banger1977/2914549247/) via [photopin](http://photopin.com/) cc
