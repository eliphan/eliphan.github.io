---
layout: post
title:      "Rails Project"
date:       2019-03-03 22:18:29 +0000
permalink:  rails_project
---


For this third project, I chose to do an app that allows its users to be able to self-publish their books and receive comments from readers. The idea was originally small and simple, yet it's no where near easy to complete and I'm so glad that I chose to do it.

My main focus with this project was to get myself more comfortable with creating app with many models with complex relationships and nested resources.

After creating a new rails app with rails generator, I created the User model with the help of an amazing gem called  'devise'. This gem allows users to log in to my app with their facebook account or sign up with their emails. It also takes care of encrypting passwords and basic users routes. However,  it takes awhile for me to fully understand how this gem works. In fact, I don't think I really understand the magic behind it, but it doesn't prevent me from using this gem to speed up the process of setting the new User model. 
Since my idea was having users creating their books throught their accounts page, I didn't know that I have to create another Users Controller for my app for this idea to work. It was very confusing at first because 'devise' doesn't generate a Users Controller even though the routes were set when cheking with 'rake routes'. But some quich Google searches helped me through this without much troubles. Setting the User table and model were also relatively easy after watching the recording of one of our study groups. The hardest part was allow users to log in via their facebook accounts. It requires a lot of copy and pasting and scratching my head in confusion. But eventually I got a hold of it thanks to a guide I found on the internet.  The User model is now complete and it's time to move on to setting up other models.

Using rails generate resource, I create the Category, Book, and Chapter models. These model have has_many and belongs_to, as well as has_many, through relationship with each others and the the newly-created User model. A user has many books and a user has many categories in case they want to change their genre; eventhough in real life not many authors choose to do so, but at least they have the option to in my app. A book belongs to a user and a category. Therefore, a category has many books and many users through books. A books also has many chapters and a chapter belongs to a book. While it was logical to assume that a user has many chapters, adding the relationship between users and chapters broke my app so I still need to look further into this issue. I also plan to implement the Book_Comment model and Chapter_Comment model. According to their name, users can comment on the book or on each individual chapters. I tried creating one Comment model for both books and chapters but it didn't work so it's better (for now) to have two different models and tables for the comments of books and chapters. 

I'm really glad that I chose to do this app as while it was simple enough to finish in a week, it really helped me to understand more about how to set up and modify nested resources. But most importantly, it allows me to get used to the flow of coding and DRYing up my codes. I was confused at first when doing my learn lessons on helpers method and DRY, but after spending couple days on coding, it eventually become a habit to avoid repeating myself just to save time and clear up clusters of codes. It's also much more natural to use helpers methods to avoid putting to much logic into the views. These are things that I can only understand by coding a single app for several days in a row.


