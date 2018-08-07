---
layout: post
title:      " Rails Project # 2"
date:       2018-08-07 01:56:35 +0000
permalink:  rails_project_2
---

Welp I decided to change my rails project when I had basically finished the Event Organizer that I had done originally. Why would I do such a thing you might be asking? Well I didn't love it, actually I kind of hated it (but more on that in my next blog)..

My new project is a Street Art App. In this app a user can add, edit and view murals located in NYC. New users first have to create an account. I made it easy to create a new account by integrating a google login. One click and the user is good to go.. (ok almost one click). 

To create an acount there a few validations. Username must be present and unique, password must be at least 5 characters and it must match the password confirmation.

If the user chooses to use google I set it up so that the username would be equal to whatever is before the @ on the email address used. If the user wants to change this they can edit their account and pick a unique username. If that username is already taken, they will get an error message and must select something else. 

Once the user is logged in, they are directed to the 'artists' page. In the artist index page, they will see all the artists that have murals in NYC. Here they can click to view any artist listed. This takes them to the selected artist's page where they will see a brief bio, link to instagram (if one has been provided) and links to all the murals currently on the site. Since the links are in the individual artist's page, I have set them up as a nested routes. So if they click on link the address bar will containt the artist id and the mural id.

In the 'mural' show page, basic information will be displayed. There is a picture, a description of where it is located and the neighborhood.  There is also a link to edit that is available to all users. If any of the information is not filled in or needs to be updated then any user can easily do it. If the user is an admin, they will see a delete link in addition to the edit link. 

Some other features of the website include a 'Most Popular' link that returns the top 5 artists by most murals listed. There is also the most popular neighborhood which returns the 3 neighborhoods with the most murals.

A user can also go into their profile to see how many murals they have entered, by clicking on the link 'murals' shown at the top of the page. If they don't have any added, there is a link to the artist page to add one. I set it up so that every mural added has to be from an artist that is already on the site. If the artist isn't on the site the user must first add the artist. I thought this made sense because every mural belongs to an artist, there would be no mural without the aritst, so the artist must go first!

I've really enjoyed working on this new project, street art is something I am personally interested in and I think that factored into my enthusiam. For example, realizing I could add the artist's instagram page truly excited me!
Switching projects was hard, but I think it's more important to work on something you're proud of, more on that topic in my next blog!














