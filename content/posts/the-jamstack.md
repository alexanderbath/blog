---
title: "The JAMStack"
date: 2020-04-17T12:18:11+09:30
author: "Alexander Bath"
---

## What is the JAMStack?
Maybe somewhat confusingly, this new “JAMStack” term being thrown around in the web development world recently doesn’t refer to a specific set of tools. It’s a concept based around building sites at deployment, rather than at runtime. 

The standard process for viewing a website in recent times has involved receiving a request from the client, running the Node/PHP/Python code to make requests to a database, retrieving a page template and content, rendering it all together and then serving this final markup to the client. While this affords the developer a huge amount of flexibility, it’s slow, riddled with failure points and fundamentally less secure.

The JAM acronym stands for Javascript, API’s, and Markup. The concept being that all server-side processes are passed off to an API, all the pages are built into static HTML markup at build time, and frontend tasks are handled with Javascript. 

This has a massive list of benefits, some more significant than others. One being page loading times, which are significantly improved because no processing is required on the server side, but also because JAM sites are static. This means no centralized server is required, and they can be deployed to a CDN. This almost completely removes the potential for site downtime caused by server issues because if one node of the CDN goes down, the load is instantly picked up by another node. There is also the obvious benefit of clients pulling down files from a node that is geographically close to them.

## Everything lives in Git.
A huge benefit of this workflow is a super simple implementation of Continuous Deployment pipelines. Instead of having separate development and production environments, and inevitably having to deal with the issues that causes when you attempt to deploy new code when dependencies don’t match up, databases don’t play nice and whatever else, the build environment is consistent.

This blog for example is built using a static site generator called Hugo (https://gohugo.io). All the projects dependencies are included in the git repository. This makes building the site as simple as running ‘hugo’ on the command line and the static site is dumped into a directory ready to be transferred to a file server. That simple. 

We can take this process a step further with JAM hosting services such as Netlify. Deploying a JAM site on Netlify is as simple as specifying your repository on Github (or another git provider), defining your build command, the directory that contains the static files and away you go. The best part? Netlify will automatically rebuild your site from source and deploy it to their CDN every time you push a new commit to your repository. DevOps has never been so easy.

## But my clients are used to WordPress?
One downside of the current JAM space is ease of use for a client who wants to control their own content using a CMS like WordPress. They’re likely not interested in learning how to write Markdown and pushing changes to Github, and why should they be. That’s our job. There is the possibility of using a headless CMS like Ghost (and many others) to provide content for your site – although this isn’t a completely static implementation as something like Hugo. For the moment at least these new technologies are reserved for people with at least a basic development knowledge, but I have no doubt that this will change in the future. Building a web app in Angular? No problems whatsoever. Welcome to the club.

Would you like to see how my website and my blog were built using the JAMStack? Visit my [Github](https://www.github.com/alexanderbath).