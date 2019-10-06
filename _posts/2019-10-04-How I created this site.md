---
layout: post
title: How I created this site
description: Tools and tech used for the job
image: assets/images/pic06.jpg
---

There are many ways to build and deploy a website these days, plenty of technologies to use and learn, unfortunately trying to get into it with close-to-zero knowledge can be daunting.
This portfolio exists in an attempt to learn and practice something new while having something to show for it.

<h3>Jekyll</h3>
I knew I wouldn't need a very complex and feature rich website, so my first order of business was trying to find a way to build and deploy a static site with ease and no prior experience.
That's how I stumbled upon **JAMstack**. The <a href="https://jamstack.org">JAM "stack"</a> involves creating static sites using JavaScript, APIs, and Markdown, all tools I knew but never used or programmed with.
<br>Apparently there are a lot of players in this space, I ended up using **Jekyll**, an open-source *Static Site Generator* written in ruby developed by GitHub.
There are a plethora of Jekyll themes on the web to choose from, thanks to all the talented people who shared their work for free (and premium) use. The Jekyll theme I'm using is called <i>Forty</i> and is developed by Andrew Banchich on <a href="https://github.com/andrewbanchich/forty-jekyll-theme">GitHub</a>. *Forty* looks cool and has character.


<h3>GitHub</h3>
Although I don't use it as much for my day to day work-flows, GitHub was a no brainer for this project. I created a private repository and synced Jekyll's work directories in it, both for simplicity's sake and to take advantage of CircleCI automation to later deploy the site to a web host.
<br>Honorable mention to <a href="https://atom.io">Atom</a> (+ *emmet_essentials* addon), an awesome text editor that makes writing code and integrating with GitHub a breeze.


<h3>AWS</h3>

Truth be told, this project was just a way to experiment with some (inexpensive) AWS services, since I'm currently studying to become a solution architect and felt I needed something to get my hands dirty with.
I have always been intrigued by web development and design, so this was the chance to tackle something new in a new environment.

<div class="box">
Disclaimer: you could use GitHub Pages and Netlify to achieve all this without paying a dime, but again: I wanted to play around with AWS so I went all in!
</div>

This is the idea:

1. **AWS Route53** to buy a domain name;
2. **AWS S3** to host Jekyll-built site;
3. **AWS CloudFront** to cache and deliver the bucket content on the web.







<h3>CircleCI</h3>

To be Implemented
