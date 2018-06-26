---
layout: post
title:      "Sinatra Project"
date:       2018-06-26 18:08:12 +0000
permalink:  sinatra_project
---


I have arrived at my second project. Now a little more confident than my first project and ready to get started. I decided for my CRUD (create, read, update and delete) app. I would go with an Event Organizer. This might have been because I had been helping my friend plan her birthday party for the last few weeks and it was fresh in my mind.

I started off by writing out how my events and hosts would be connected. I figured that events would belong to a host and a host could have many events. Once I had that in place,  I decided what information would be store in tables for host and events. This is where I realized that I wanted to have add an additional model -venues. I wanted to store my venues so as venues are added into the database the host would be able to pick from a list of available venues or add them as needed. 

Onces my tables were all step up, I was able to start working on the views, to see how many pages my controllers would need to link to. I started just as a user would if they were using this application, by signing up. So I created the sign-up page and started making my way through every page just if I were a new user. Once I had my basic pages (signup, login, create event, edit event and delete), I wanted to make it a litter nicer. Since we have already seen some css in previous lessons, I wanted to use this project to practice. This is where I hit a roadblock. I set up a css folder nested inside the 'app' folder and called it inside my html file but no matter what I tried I couldn't get the css to show. Luckily I receieved help from, Jen, my instructor, and she advised me that css works a little different in sinatra. The folder which is not named 'css' but actually named 'public' doesn't go in the app folder it goes on the same level as the app and database folders. Also, when calling it in the html file you just have to reference the actuall css file, no need to tell it in which folder to look because sinatra already knows that it's in that 'public' folder. That is definitely great to know for the next time I want to use sinatra and css. 

Now that I knew what views I need to connect to I created the controllers.  First I created a basic 'Application Controller' which sets the views, sessions and gets my index page. Then I proceeded to create a 'Host Controller' and an 'Event Controller' that inherit from my applicaction controller.  

In my host controller I have all the routes corresponding with CRUD of the host. Here I have the sign-up, login, edit, logout and also the hosts homes page which would be a list of all the events they have created.

My event controller on the other hand has the routes corresponding with CRUD of the events.  This controller contains new, create, edit, delete as well as the route to view an individual event or all the events currently stored in the database. 

On both these controllers I tried to make my routes RESTful. We have been taught this a few lessons back and it was something that I definitely tried to make sure I included in my project. 

Now it gets a little more complicated because I have to decided what routes I want to protect and how I want to go about protecting them. Here I created a helpers model that would have 2 methods. 1. 'current_user'  which checks who the current user is by their session id and 2. 'logged_in?' which checks if the user is logged in also by checking if there is a current session. I decided to protect the important routes which were the ones that would allow a user to edit and delete an event. I also made those buttons invisible on the html. So other hosts would be able to see an individual event even if doesn't belong to them but won't be able to change them in anyway. 

Finally, I added flash messages. I created a few for the login in because I wanted to make it so that if a username and/or email is already taken a new host can't use that information. I also added them when creating an event so that when a user tries to create an event and is missing information they will get an error message telling them to input all the information needed. And of course I added messages when they sucessfully created or deleted and event. 




