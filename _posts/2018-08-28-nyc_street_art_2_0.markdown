---
layout: post
title:      "NYC Street Art 2.0"
date:       2018-08-28 10:50:46 -0400
permalink:  nyc_street_art_2_0
---


For project #5 I was asked to add some jquery to my rails project. Love it! I was very happy with how my rails project came out and I was excited to add to it. Just to recap my rails project is an app to keep track of all the street murals around NYC.

For this project I was required to use Active Model Serialization and a JSON backend to append to the DOM. I explained this to my girlfriend as bringing my app closer to the present. No need to go to a new page for new content to appear, just like most of the apps on your phone do.

Instead of going through the way I built it, I want to talk about a few issues that I hit along the way.

The biggest one I think was turbolinks. I didn’t even know what turbolinks were but, when I was creating this project in rails and I was getting some weird bugs my Technical Coach kept bringing them up. My rails app eventually worked that way I expected so I didn’t bother to take them out. Not the case this time around. I was having issues with my event listeners; sometimes they would work fine and other times they didn’t. This had me trying to figure out what was going on for a while and then I was told by me Technical Coach to remove the turbolinks and poof my app was working like I programmed it too. Peskly little turbolinks! So I asked him what they were and he explained that they are there to make the app faster. The turbolinks make it so the app isn’t constantly reloading pages. But that’s a problem when you attach event listeners cause then they aren’t getting called and therefore the app doesn’t respond the way it’s supposed to. For now I don’t see a reason to have them but that will probably change in the future when I have a bigger and heavier app.

Another issue I ran into was with my JS files. The way I started writing the JS in this project was in script tags in each view. I wanted to do it this way because it was my first time writing JS code for a project and I wanted to keep myself organized. Once I got the code to work I proceeded to refactor it and place it in one  JS file. Again this was just for organization, I knew that I would eventually move each function to the JS  file it pertained to and here is where I ran into the problem.

First, let me explain a little how my code is setup. I have a document.ready function that calls an attachListeners function which is where I put all my event listeners and finally I pass in a callback function which is the main function.

I started refactoring by moving the main functions to the other JS files. Here I was assuming that all JS files were connected. I quickly realized that didn’t work. Then I figured I would just copy over my document.ready function and attachListeners function, this didn’t work either. Since neither of these approaches worked I decided to ask Cernan, my cohort lead, thinking I was missing some code to tell it to look in the other JS files but he immeditately started debugging it and that’s when he realized that I couldn’t name the attachListeners function the same even though they are in different JS files. So we changed the name on both functions and the app was up and running again.
I feel like although I already had this project up and running with Rails it took me just as long to add a few features with JS.  It was a lot of fixing, breaking and debugging but at the end of the day it’s part of the learning experience. Also, I definitely feel like JavaScript is not as user friendly as Ruby but it’s definitely a lot more powerful and I am excited to learn how to do more things with it, so on to the next one!

