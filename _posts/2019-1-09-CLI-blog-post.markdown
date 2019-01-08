---
layout: post
title:      "Inventory Manager: My CLI Project"
date:       2019-01-08 11:59:10 -0500
permalink:  cli_blog_post
---

The idea behind Inventory Manager is simple but important. Keeping track of inventory is a very important thing at any store, whether it is just an office, grocery or department store. 
With Inventory Manager, managing your store’s inventory can be simple. With its many powerful commands, you can add, change, modify, store by department, category and sub-category, all the items you need. When you close the program, it automatically saves to JSON files. Worrying about running out of an item? No problem! Inventory Manager can keep track and let you know what items are low, and it can also keep track of the last time you ordered more of that item.

**Enough of the commercial!**
For real, Inventory Manager can do a lot. Not only was it made from scratch with love. It gets data (to show that it works well) using nokogiri, to scrape data from publix.com.
The process was quite complicated, I started by drawing out, on a large poster board, the object structure, how the objects relate to each other and what their attributes are. From there I made the object structure, which can be seen under the structure directory in the lib folder. Next I made the scraper and a few tests to see that my structure of objects has the right relationships. Making the scraper was quite complicated, since it was dealing with at least 8,000 individual items scraped from publix.com. The same could be said about designing the CLI from scratch. I made sketches of what I wanted my home screen to look like. I made lists of commands I want, and countless sessions of thinking about how to make it all work together. Eventually, I did it, Inventory Manager was completed!
