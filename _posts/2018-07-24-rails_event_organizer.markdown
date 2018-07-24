---
layout: post
title:      "Rails Event Organizer"
date:       2018-07-24 15:17:03 +0000
permalink:  rails_event_organizer
---


And so a month later I have arrived at project # 3. Getting here felt a lot harder than the previous projects. Meaning that rails is tough one. 

I decided to stick with the Event Organizer that I had done for my sinatra project as I wanted to see the differences between creating it with sinatra vs rails. The first thing I noticed is how easy it is to get the project started. One line command  in the terminal , ` rails new event-organizer`,  and the initial setup with all the folders and enviroments is all set! Automagically like Avi likes to say. Rails is already in the lead, given that for sinatra it took me a while to set up my project and by the time I knew there was the cornmeal gem, which basiciallly does what the one line of code does in rails, I already had my project folders and environment all setup. 

*Mental note: Don't forget to use cornmeal next time you want to create a sinatra app.*

Besided the `rails new` for creating a new project, rails has other generators which saved me a bunch of time on the initial setup. I was able to generate  migrations, models and controllers; granted sometimes I would have to look up the syntax, which is time consuming, but the upside is that it is setup correctly the first time.  There is another generator, scaffold, that one generates migrations, models, controllers and more with just one line command in the termianl but it's more code than I would probably need. So per the project instructions and because I didn't think I needed scaffold I didn't use that generator. 


One of the major differences I noticed between sinatra and rails, is that rails has a lot helper methods for avoiding  writing html. 

`form_for ` - this easily helped me create the forms for creating events and editing them. The best part is that rails is so smart, that you don't have to change the form from a new event to editing that event.  You pass an instance variable to `form_for` and if doesn't have any values, as in it was just instantiated, then it knows that it's a form to create an event. But, if the variable contains data then it knows to pass in the information and show it so that the user can edit it. 

`link_to ` - This is another helper that I used a lot. This one creates links, so it's much better than having to write out the `<a>` tag with the href that it should be pointing to. Also because rails has route paths for every route that is created.  So for example this is what the link to would look like for creating a new event.  `<%= link_to 'Create Event', new_host_event_path(@host)%>`. 'Create Event' is what the clickable link  and it is pointing at the page where a user can create a new event. 

Another very helpful method that rails has are partials. A partial is  'partial' template and this helps keep the code DRY.  Remeber how I was explaining that the `form_for` is smart enough to know if it's a form for creating or editing, then I don't really need this code twice and that's the perfect way to use the partial. I added `form_for`  code to the partial template and then called it on the new and on the edit page. 

Already rails has saved me tons of keystrokes and helped me keep my code clean!

So I think rails is definitely the winner although it isn't as easy to learn and I got stuck in a few points but I had to choose between the 2 for another project  I would go with rails. It's Automagical!


