---
layout: post
title:      "Sinatra Application"
date:       2019-02-03 00:54:23 +0000
permalink:  sinatra_application
---


My second project, a Sinatra application, is a website that would allow signed-up, logged-in users to post and share their favorite street food locations. Think of it as Yelp but without the rating system, and only for street food places. 

Starting to do this project was fairly easy with the help of 'Corneal' gem. It's a brilliant gem which could generate the required directories for a Sinatra app so I can focus on actually coding my app, rather than spending time trying to havethe correct files, folders, and gem dependency. 

The core of this app is very similar with what I've been doing with my previous labs using MVC pattern. I first created a database that can be accessed by using sqlite3 and rake. Then I created two models that have the has_many and belongs_to relationship, which in this case is the User class and the Post class. The relationship allows an user to have many posts, and a post can only belong to one user.  I then seed some info into my database (tables) by using rake so I can have something to test with later. The populated info will help with checking whether my database is correctly created and has the appropriated relationship. 

The main course lies within my 'app' folder. In the app folder I have the controllers, the models, and the views. These are what MVC stand for, and they are responsible for all of the magic behind creating a Sinatra app. The  models hold all of the raw data which then can be accessed and processed by the controller. The controller also is responsible for receiving the request from the user's browser and controll what the app would do with such request. The controller can route the user to a view based on the browser request. The view is where the user would interact with an app. 

I first create my models based on my database. Each table of the database will have its own class. Since I have two tables: users and posts, I then created the User class and the Post class. Each class will be responsible for handling raw data stored in the database, building the relationship of users and their posts. In this app, my models can validate some required information and take care of securing the user's password. The model also hold some methods that could define how my controllers access the user input. 

I then move on to create the brain of my app, the controllers. Each class in the model will have its own controller and only have actions related to such model. Each controller will have actions that corresponded to CRUD requests: create, read, update, and delete. 

I then move on to create my views. Each of my views can only be available for one controller class. Inside the directory for each view are all the routes that was defined in the controller actions. Again, each .erb files are responsible for one and only one route. I find that separation of concerns really help me streamline my work flow and reduce the amount of confusion I might have after having coded hundreds lines of code. 

This project is a long and complex one. It's definitely a step above my previous project and is something I really could use later. Doing this project really strengthen my knowledge about basic signup and login system, as well as my ability to solve complex problems. 



