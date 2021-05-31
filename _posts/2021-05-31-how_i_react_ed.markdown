---
layout: post
title:      "How I React(ed)"
date:       2021-05-31 22:28:49 +0000
permalink:  how_i_react_ed
---


Dipping into a new framework can be confusing and scary. It’s like visiting a different country. After all you aren’t very familiar with the customs, conventions and possibly even the syntax of the language spoke there. Similarly, when diving into the world of React, it was different. I struggled to find a good pattern, some sort of conventions on how to structure my files and code. I was reading through the official docs trying to find some sort of file structure conventions for React, but came up short. I realized after reading through various blogs, there is no right or wrong pattern. Unlike in Rails, where things are convention over configuration, React is more ‘free’ and open. This of course has its pro’s and con’s, because I was not only starting out with a new approach to writing frontend code, but I also felt like I was sometimes writing code that wasn’t very DRY, hard to debug and overall, not very structured and organized.

## Redux pattern:
This pattern seemed to improve on a lot of issues I had with React. No more did I struggle with managing state and passing down so many props and callbacks that it made my brain want to power down. However, even though redux was an improvement, I still was noticing ‘code-smells’ such as repeated code and I felt like things could be organized better. So I decided to try and rethink my approach to organizing and following the programming rule of “Separation of concerns”. After learning the React pattern(but now I guess no longer recommended) of using container and presentational components, I was able to organize my code quite a lot better, but it still feels like there could be better separation of concerns.

## MVC in React?
After looking at my container components, I noticed they were very bloated and it was getting difficult to debug when a container has so much code and logic in it. Maybe this is why Container/Presentation paradigm is not really recommended anymore. I found myself thinking of better ways of organizing my code. A thought came across my mind, about how container components reminded me of Controllers in the Model View Controller architecture, and how presentational components could be considered ‘views’. Well, what about models? How could they fit in? After all, I am storing and displaying data from my server that came from and was organized as Models . Why not just abstract and separate code related to a specific model into its own file and class? At that point, I decided to make a models folder, and populate it with basic Javascript classes. Those classes would not only keep track of and organize properties/data for my server data models, but also get rid of unnecessary and repetitive code on my container components, business logic that has no real reason of being a concern of the containers. So in the end, my file structure turned out to be MVC, that is Model, View(Presentational) and Container(controller).

## Conclusion
As there are not very many rules and standards to React, most of my time was spent figuring out what patterns I wanted to follow and how I could structure my project in a clear, semantic and “code smell” free way. Although it was confusing and somewhat of a challenge at first, it was a real learning experience and I not only enjoyed it but I’m glad React is one of the things added to my stack.
