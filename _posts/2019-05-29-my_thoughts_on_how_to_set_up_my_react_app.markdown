---
layout: post
title:      "My thoughts on how to set up my React app"
date:       2019-05-30 00:17:41 +0000
permalink:  my_thoughts_on_how_to_set_up_my_react_app
---


I want to write more about the process of setting up a React app with Rails as backend while using another API to fetch data, as it was the thing that nobody really talk about but could be tricky enough to hinder the process of creating your app. What I really want to talk here is not about how difficult to set up the app, but more about how confusing it was for me when creating my app. This is not a tutorial.

First I need to create a Rails app. There are many ways to do this, including calling rails new or rails generate in the terminal. Then I need to create a React app with create-react-app. Very simple and straightforward. Then I need to connect them together by proxying to port 3001 so the app will run Rails (my backend) as an API. So this is it. There's really no command or function to connect Rails and React. Instead, we will be running a React app and fetching and posting data to an API, in this case the API will be our own database. So the process is exactly the same as using any API out there. But what if I want to use another API as well? 

I was running around with "should I create a table in my Rails database to store the fetched data from the other API?", "Where do I put the calls for the other API, in Rails side or in client side?", and stuff like that. Looking back at it now, it seems pretty dumb of me to making myself stuck for a couple of days just to figure out how I could do it. But at that time, those were legitimate questions to ask because I simply haven't done this before. Remember, we don't even have a lesson on how to set up Rails as an API for React app so I had to rely on whatever tutorials I could find on Google. The thing with online tutorials is that they are not reliable and tend to show very specific problems. I was lost trying to find a decent tutorial which features how to use two APIs in one React app. At one point I even wish that I'd chosen to do something more familiar for the final project and wanted to start over with something else.

So what was the actual problem here?

It's true that I can fetch data from the external API from my client side, but why would I want to do that when I have a backend already? Since I set up Rails as my backend, I want every data to be post to and fetch from it. So, behind the scene, this is what's gonna happen when fetching data from the external API: React (front end) requests the data from Rails (backend). Rails (backend) requests the data from the external API and return the fetched data to front end through an action. My client side doesn't need to know about the other API at all. 

Now that I'm done with this app, I really appreciated that I did choose to do it, not because I want to torture myself, but because I realized that it was actually the best time to wet my feet with using API to create a more realistic and professional website. Trying out something new and a bit unfarmiliar really pushed my ability and help prepared me more for future projects. I would not say I'm ready for job at this moment, but I'm definitely more confident with trying out new challenges after this app.



