---
layout: post
title:      "'CLI Data Gem'."
date:       2018-04-21 00:07:41 +0000
permalink:  cli_data_gem
---


So I have to write a little something about my first project.  

First let me show you what the requirements are.

REQUIREMENTS

1. Provide a CLI
2. CLI must provide access to data from a web page.
3. The data provided must go at least one level deep, generally by showing the user a list of available data and then being able to drill down into a specific item.
4. The CLI application can not be a Music CLI application as that is too similiar to the other OO Ruby final project. Also please refrain from using Kickstarter as that was used for the scraping 'code along'. Look at the example domains below for inspiration.
5. Use good OO design patterns. You should be creating a collection of objects - not hashes.

 Woah Woah!!
 
Yea, reading this was scary at first. I have only been in the program for a month what do you mean I have to write a program all on my own already. But ok that was my initial reaction, then I was like "I got this"!

Ok, now I have to decide what page I want to use to pull information from. This was pretty easy as I use the Fousquare app almost daily and because of this I know that they have something called Foursquare labs that creates lists of the trending places.

Great now to start working on this project!

Hit my first brick wall. How do I even start? What am I supposed to do? Thankfully Avi, our fearless leader, was nice enough to provide us with a video walk through. Took me a bit but I finally got my project started and didn't need Avi anymore to start working on it.

Basically I started by creating a #call method which greets the user and calls #cities instance method that will output a list of cities, which then theuser will get to pick from. Ok, now when the user picks a city I need to make sure that I can scrape the data from Foursquare and output a list of all the trending spots. I decided that when the user picked the city I would set the url instance variable to the Foursquare url for that list and also created a city_name instance variable so that I could use it in the method that would list the spots (#list_spots).


Here it gets a little more complicated because I can't just scrape the website, I have to convert that scraped information into something I can use or to be more precise into an instance So decide to a method that scrapes and converts that information into an object. Once I have that object I pass it on to another method which converts into an instance  and that gets passed back to #list_spots as an array. Now I have an array instances that I can just iterate over and output the information that the user has requested. 


Requierment #3 --> The data provided must go at least one level deep, generally by showing the user a list of available data and then being able to drill down into a specific item.

One level deep! Gotcha!

Well since Foursquare is so awesome, of course they have an individual page for each spot. Now I will have to write a method that scrapes the specific spots website for more information.  Once I have scraped this information, instead of creating a new instance with the additional information, I will add it to the instance that I had originally created for each spot. Again I create a new method to turn the scraped information from an object to an instance but this time I also pass in that instance and then add the new information to each instance. So now these spot instances have all the information that I was able to scrape from Foursquare. 


Great! Now I can output the list and output the additional information. Basically now it's up to the user enter in what they would want to checkout. 


Basically my program works this way:

Greet the user and ask the user has to pick a city.
Once the user picks a city a list of all the trending spots will appear and the user will be asked to pick a spot to get more information.
When that user makes their decision they will have the option of picking from a list that includes the phone number and address. 

Side note: Anytime the user gets prompted for input I made it so that they could exit, request a city (basically starts the program over) or see the list of spots again.









