---
layout: post
title:  "**Creating a To Do app - Sinatra Assessment**"
date:   2016-07-10 01:15:14 +0000
---



This app was a fun project to work on. It was a journey creating my first original project with a ruby framework. I ran into a roadblock immediately after creating the folder setup and initial file setup. I received an error message saying Boot Error cannot load config.ru NameError: uninitialized constant ActiveRecord::ConnectionAdapters::ConnectionManagement. After an evening of trying to solve it, I turned to my really resource, SLACK. The learn group has many active and helpful people. The problem ended up being that Active Record 4.5.0 was acting weird with sinatra so I specified that the app use version 4.2.5 and we were up and running. 

My next hurdle was actually a simpler fix. I was working on organizing my public folder and linking it correctly to my layout.erb file. The bootstrap classes I was trying to apply to my home page were not working. After adding to my styles.css file to test out whether or not the link route was correct, I found the issue was not with the route it was with the bootstrap css file itself. I tried redownloading the file but it didn't work. I ended up just linking the CDN. Everything was then smooth and I got to continue designing the index page.

Probably the most difficult road bump that has an easy fix popped up when I tried getting my app to create a new task and post it, updating the task list and displaying all of the tasks a user added to their list. I had a ruby statement in the show task section of the page that displayed all tasks in the database on the user's list, not just the tasks that they created. This stumped me for so long. I tried altering the logic on a couple different routes in my application controller, I tried altering the code when calling .all and .each for the task list. In the end it was a really simple fix that irritated me when I thought to myself, "why didn't I think of that?". It ended up just needing a simple if statement within the each method to verify that an inidividual post's user id matched the user id of the currently logged in user. 

After that it was smooth sailing. I spent a bit of time, not heavily detailing, but adding css to the various pages so that all the text and input boxes were centered and more towards the middle of the screen, not on the top left corner of the web page. What I learned from this project is that you will face all new errors and complications as well as the most simple little mistakes when coding an application. Thank goodness for google and networking. 
