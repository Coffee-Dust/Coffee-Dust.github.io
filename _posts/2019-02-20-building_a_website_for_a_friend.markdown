---
layout: post
title:      "Building a website for a friend."
date:       2019-02-20 18:35:50 +0000
permalink:  building_a_website_for_a_friend
---


My friend was needing a website for his sister's business, she crafts flowerpots and flower arrangements. I let him know that I'm in school for such a thing and that from what I have learned in html and css, I could make an awesome looking website for his sister. I went to work, and must say, it was fun. I also knew a little bit of javascript, and was able to create some responsive webpages for full mobile support, the ability to view items by category, the ability to view items fullscreen, and thanks to css a modern 3D effect on the 'wrapper' of the page.
**The Bug**
I encounter the oddest bug, one that google could not turn up results for, my website appeared and worked fine on apple mobile devices, however on android devices, my responsive media queries would not fire, it looked like a zoomed in desktop page. After a long time of putting my debugging cap on, so to speak, I finally figured it out, turns out android browsers didn't set the window's width to the viewport width, so it looked like a desktop page, but zoomed in. Nothing a little javascript couldn't take care of.

The site is currently(at the time of this post) all front-end. So I would like to improve on that by adding a dynamic server, making it with the ability to add items from the owners log in page, and dynamically adding new content to the webpages.

You can view the site on [github-pages](https://coffee-dust.github.io/plant-site/index.html)
