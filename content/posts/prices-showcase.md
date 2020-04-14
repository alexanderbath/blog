---
title: "Showcasing the Prices App"
date: 2020-04-08T8:53:11+09:30
---

![App Image](/prices.png)  

## The Brief
Prices is a multi-platform web application designed and built for a local, family run business based in South Australia. We have had a long running working relationship together and it was great to work with them to build the next step towards their modern, digital workspace.

The salespeople previously carried paper price books to help them perform their day to day tasks, but this made it costly in both time and resources to make even the smallest updates to the pricing data. After some thought, we concluded that providing the salespeople with iPads to both supply to the minute pricing data, as well as access to the company’s other internal applications would be a great solution to the problem


## Our Solution
After a few design revisions, we settled on a UI for the application that was extremely quick and intuitive to use on a tablet screen in a sales situation, where the last thing you need is to be fumbling around trying to find the information you need. The application was equally as nice to use on a desktop browser to be right at hand when the salesperson is back at their desk.

A menu and sub-menu tree was deemed to be the best UI model, making it easy to pick a top level category and then drill down into the specific data you need at a second's notice, without being too fiddly and precise with the large amount of data we were working with. A clean, simple design was key to ensure readability and usability were at a maximum on both touch devices as well as conventional desktop machines.

To facilitate quick modifications, a desktop class web application was developed to be used back in the offices by the leadership team, enabling quick changes to the prices that were pushed out to all of the iPad clients immediately with a minimum of effort. This allowed pricing to mirror small changes in import pricing amongst other factors, which was just not possible with the previous system.

## The Technical Stuff
Both the frontend and admin panel were built using Angular, with the data being stored and served by an API built using the Django Rest Framework. We built a custom UI interface for the client facing frontend, while the admin panel was build using the brilliant VMWare Clarity framework. 

To make sure the application was flexible enough to store and display whatever data was necessary in the future, rather than storing the price data in firm database structures, each pricelist is simply rendered from HTML. This enables easy editing in the backend using a great WYSIWYG editor for angular called AngularEditor. 

The app was then deployed using Azure’s powerful DevOps pipelines to ease in rapid development and deployment in the future.