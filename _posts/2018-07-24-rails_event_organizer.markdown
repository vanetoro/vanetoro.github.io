---
layout: post
title:      "Rails Event Organizer"
date:       2018-07-24 11:17:04 -0400
permalink:  rails_event_organizer
---


A month later and I have arrived at project # 3. Getting here felt a lot harder than the previous projects. 
Spoiler alert: rails is a tough one. 

I decided to stick with the Event Organizer that I had used for my sinatra project as I wanted to see the difference between creating it with sinatra vs rails. The first thing I noticed is how easy it is to get the project started. One line command  in the terminal , ` rails new event-organizer`,  and the initial setup with all the folders and enviroments is all set! "Automagically" as Avi likes to say. Rails is already in the lead. With sinatra it took me a while to set up my project and by the time I knew there was the cornmeal gem, which basiciallly does what the one line of code does in rails, I already had my project folders and environment all setup. 

*Mental note: Don't forget to use cornmeal next time you want to create a sinatra app.*

Besided the `rails new` function for creating a new project, rails has other generators which saved me a bunch of time on the initial setup. I was able to generate migrations, models and controllers; granted sometimes I would have to look up the syntax, which is time consuming, but the upside is a correct set up the first time.  There is another generator, scaffold, that generates migrations, models, controllers and more with just one line command in the terminal but it's more code than I would probably need. So per the project instructions and because I didn't think I needed scaffold I didn't use that generator. 

One of the major differences between sinatra and rails is that rails has a lot of 'helper' methods to avoide writing html. For example:

`form_for ` - This helper created the html code for a form. Rails is so smart that you don't have to change the form from a new event to editing that event.  You pass an instance variable to `form_for` and if doesn't have any values, as in it was just instantiated, then it knows that it's a form to create an event. But, if the variable contains data then it knows to pass in the information and show it so that the user can edit it. 

`link_to ` - This is another helper that I used a lot. This one creates links, so it's much better than having to write out the `<a>` tag with the href that it should be pointing to. Also because rails has route paths for every route that is created.  For example this is what the 'link to' would look like for creating a new event.  `<%= link_to 'Create Event', new_host_event_path(@host)%>`. 'Create Event' is the clickable link and it is pointing at the page where a user can create a new event. 

Another very helpful method that rails has are partials. A partial is 'partial' template that helps keep the code DRY.  Remeber how I was explaining that the `form_for` is smart enough to know if it's a form for creating or editing, well now I don't need this code twice and that's the perfect way to use the partial. I added `form_for`  code to the partial template and was able to call it on the new and on the edit page, keeping the code DRY.

Already rails has saved me tons of keystrokes and helped me keep my code clean!

Rails is definitely the winner! Eventhough it isn't as easy to learn and I got stuck in a few points, if I had to choose between the two for another project I would go with rails. It's Automagical!


