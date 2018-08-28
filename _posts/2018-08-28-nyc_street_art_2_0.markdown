---
layout: post
title:      "NYC Street Art 2.0"
date:       2018-08-28 14:50:45 +0000
permalink:  nyc_street_art_2_0
---


For project #4 I was asked to user my rails project and add some jquery. Love it! I was very happy with how my rails project came out and I was excited to add to it. Just to recap my rails project is an app to keep track of all the street murals around NYC. 

For this project I was requiered to use Active Model Serialization and a JSON backend to append to the DOM. I explained this to my girlfriend as bringing my app closer to the present. No need to change pages for new content to appear, just like most of the apps on your phone do. 

So instead of going through the way I built it I want to talk about a few issues that I hit along the way.

The biggest one I think was turbolinks. I didn't even know what turbolinks were but, when I was creating this project in rails and I was getting some weird bugs my Technical Coach kept bringing them up. My rails app eventually worked that way I expected so I didn't bother to take them out. Not the case this time around. I was having issues with my event listeners, sometimes they would work fine and other times they didn't. This had me trying to figure out what was going on for a while and then I was told by me Technical Coach to remove the turbolinks and poof my app was working like I programmed it too. Peskly little turbolinks! So I asked him what they were and he explained that they are there to make the app faster. The turbolinks make it so the app isn't constantly reloading pages. But that's a problem when you attach event listeners cause then they aren't gettting called and therefore the app doesn't respond the way it's supposed to. So for now I don't see a reason to have them but that will probably change in the future when I have a bigger and heavier app. 

Another issue I ran into was with my js files.The way I started writing the js in this project was in script tags in each view.  I wanted to do it this way because it was my first time writing js code for a project and I wanted to keep myself organized. Once I got the code to work I proceeded to refactor it and place it in the artist js file. Again this was just for organization, I knew that I would eventually move each function to the fjs ile it pertained to and here is where I ran into the problem. 

Let me explain a little how my code is setup first.

I have a document.ready function that calls attachListeners() which is where I put all my event listeners and finally I pass in a callback function which is the main function. 

So when I was refactoring first I just moved the main functions to the other js files. Here I was assuming that all js files were connected. I quickly realized that didn't work. Then I figured I would just copy over my document.ready function and attachListeners function, this didn't work either. So I decided to ask Cernan, my cohort lead, thinking I was missing some code to tell it to look in the other js files but he just started debugging it and that's when he realized  that I couldn't name the attachListeners function the same even though they are in different js files.  So we changed the name on both functions and the app was up and running again. 



I definitely feel like Javascript is not as user friendly as Ruby but it's definitely a lot more powerful and I am excited to learn how to do more things with it, so on to the next one!  


