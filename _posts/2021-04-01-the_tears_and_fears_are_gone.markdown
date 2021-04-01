---
layout: post
title:      "The Tears and Fears Are Gone"
date:       2021-04-01 17:46:00 +0000
permalink:  the_tears_and_fears_are_gone
---

### (At least when it comes to Javascript)

I have to admit, going into Javascript made me a bit nervous. I’ve heard quite a lot of negativity about JS (and also seen really funny memes too) and that affected my view of the language, to the point where I was worried that it was something I was not going to get the hang of. All previous languages that I have learned and used before are very different. The first language I officially learned was Swift, and then Ruby. Going from Ruby to JS was quite a difference. This strange new world of curly brackets, functions, fetch, then, undefined and vague error messages took quite a while to get used to. After the Pokemon Teams lab, I really felt like I got the hang of it. I was really proud of my solution to that lab, mainly because I felt like I structured my code in a clear semantic way. At this point, the rest of the course was smooth and I finally was beginning to get comfortable with Javascript and even enjoy writing it!

### The Project
My Coffee Table. Even though it never will be optimized for mobile, ever, it is still a really cool project. I first thought of it a while back when brainstorming future project ideas. The idea you have your own virtual table to place/move objects around freely seemed like a great JS project idea.
The day finally came when I got to “Javascript Project Instructions.” At this point, my first step is to always draw out my database domain model. Initially I didn’t have many issues but then I got to the point where I asked myself, “what do I want my JSON data to look like?” So I decided to refactor the database to reflect data that is more JS friendly, data that can basically be passed in without much need for going through it and manually assigning values. 
#### A Polymorphic Join Table?
I ran into another snag. If you recall, on my rails project, I implemented a polymorphic relationship in my models. That was challenging but I enjoyed the challenge of figuring out something new that I wasn’t taught. Now when I was sketching out my database, I was wanting elements to share attributes(such as style) and different attributes(such as href in a link). My end goal after all was to have many different elements, like links, sticky notes and pictures. However a link shouldn’t have an imageLink property, and having all of these properties shared between one class just felt like a bad design that would be hard to implement and be especially difficult to add new features to, such as new elements. So at this point I decided to make Elements a polymorphic join table and making the different element types into their own table. This way my json data would be a lot more semantic and easier to implement in javascript.
 
## Conclusion
This was a difficult project, but I enjoyed every moment of it. On pretty much every step of the way, I felt like I made good, DRY design choices and structured the code in a clear and semantic way. 
****I look forward to what the future holds for me in Javascript!
