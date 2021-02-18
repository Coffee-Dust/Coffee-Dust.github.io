---
layout: post
title:      "Coffee-Beans: My Rails Project"
date:       2021-02-017 11:59:10 -0500
permalink:  rails_project_blog_post
---

**Coffee-Beans Social Media Site**
**(Rails Portfolio Project)**
Are you tired of social media and all of the negativity? Are you tired of all the division and political strife on social media platforms? Oh and do you like coffee? Well if you answered yes to any or all of the above questions, you are the perfect candidate for an ALL NEW and totally original social media website called CoffeeBeans.io. With this website, meet fellow coffee enthusiasts, read about their favorite coffee drinks even view pictures of fancy latte art(feature pending). Share your own thoughts on different types of coffee, maybe even your favorite Local Coffeeshop in the area. Oh and be sure every coffee-bean you post is about coffee, otherwise the auto-mod will permanently delete your ENTIRE account(we can’t be letting this website turn into other stressful social media sites, so keep your posts about coffee or ELSE!)
Join today and you will probably regret it when you post something without the word coffee in it.
NOTE: Auto-mod may delete accounts even if the post was about coffee. We do not apologize if this happens but it cannot be undone… 
Happy sharing your own Coffee-Beans @ CoffeeBeans.io

If you think that advert was bad, wait until you see the code behind it all.

*The Process:*
 When beginning a huge project like this, it is easy to get overwhelmed. You might think to yourself, “where do I even start?”. 
Well, first thing I always do is draw (and I mean literally draw) a diagram of how my database will work. insert diagram picture here
I write out every model and their attributes in their own box. Next, I draw lines to represent how data will associate with each other. Only after the point where I know the in’s and out’s of my database domain, I will start implementing it into code, such as writing migrations and models with the appropriate ActiveRecord association macros.

What is a Polymorphic?
When coming up with this domain, I ran into a problem. I wanted users to be able to react(like/dislike) to both posts and comments. But how could I do this in the DRYest way possible? I thought about maybe having two tables, a comments_reactions and posts_reactions table. I knew there had to be another way cause this was pattern was just too much of a code smell. I kept thing of possible ways and then I thought to myself, “I know if I just have one Reactions table, the foreign id key won’t be unique since a post and a comment can have the same id. So what if I have a key that will store the name of the table(i.e. post or comment) as well as the foreign key in that table.” At this point I realized that was the solution, but the question now is, how do I get active record to automagicly incorporate both foreign keys, would I have to write out my own query methods in order to get it to work? Well, after some time googling, I discovered that this database pattern not only already exists, but it is fully supported in ActiveRecord! It is called Polymorphic Relationships. I read through the docs and breathed a sigh of relief knowing I wouldn’t have to manually write out a bunch of sql queries for my Post and Comment models to both have many Reactions associated to them.

Now the tricky part… Controlling these objects.
When I am programming. My mind is constantly trying to be one step ahead, figuring out how to solve the puzzle and alerting me of any roadblocks. When I was writing out the Reactions controller. I ran into a lot of roadblocks because of this polymorphic model relationship. Like what if my Reactions controller was expecting a dependency of a Post but couldn’t find it and error because it was a Comment? After a short while, it all started to fall into place. Adding helper methods to make the controller more semantic, a little refactoring here and Voilà! We have one smart controller that can create or delete a reaction regardless of whether it is of type Post or Comment. Oh and of course we can’t have a user “like” a post twice, so I had to make sure that it would ONLY create a new reaction if that user had not reacted to the post/comment with that specific reaction type before. Just as any like button acts as a toggle switch, I had to make the controller smart enough to figure out if it needed to create a reaction or delete it, all in one route! This seemed like the best course of action since there was so much logic involved because of it being polymorphic. With this much logic, needing to find what the reaction belongs to and all of those database queries, it seemed like a concern of the Controller and Model.

With the most challenging part out of the way, the rest of it all just fell into place. Now to just make the website look pretty even though me and css don’t get along very well: Peter griffin css meme gif thing
