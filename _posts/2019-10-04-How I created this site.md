---
layout: post
title: How I created this site
description: Tools and tech used for the job
image: assets/images/s1.jpg
---

There are many ways to build and deploy a website these days, plenty of technologies to use and learn, unfortunately trying to get into it with close-to-zero knowledge can be daunting.
This portfolio exists in an attempt to learn and practice something new while having something to show for it.

<h3>Jekyll</h3>
I knew I wouldn't need a very complex and feature rich website, so my first order of business was trying to find a way to build and deploy a static site with ease and no prior experience.
That's how I stumbled upon **JAMstack**. The <a href="https://jamstack.org">JAM "stack"</a> involves creating static sites using JavaScript, APIs, and Markdown, a pretty brilliant approach with various benefits.
<br>Apparently there are a lot of players in this space and I ended up using **Jekyll**, an open-source *Static Site Generator* written in ruby developed by GitHub.
To make things easier and quicker on myself I picked a theme among a plethora of Jekyll themes available online, thanks to all the talented people who shared their work for free (and premium) use. The Jekyll theme I'm using is called <i>Forty</i> and is developed by <a href="https://github.com/andrewbanchich/forty-jekyll-theme">Andrew Banchich</a>. *Forty* looks cool and has character.


<h3>GitHub</h3>
Although I don't use it as much for my day to day work-flows, GitHub was a no brainer for this project. I created a private repository and synced Jekyll's work directories in it, both for simplicity's sake and to take advantage of a future and possible implementation of CircleCI.
<br>Honorable mention to <a href="https://atom.io">Atom</a> (+ *emmet_essentials* addon), an awesome text editor that makes writing code and integrating with GitHub a breeze.


<h3>AWS</h3>

Truth be told, this project was just a way to experiment with some (inexpensive) AWS services, since I'm currently studying to become a solution architect and felt I needed something to get my hands dirty with.
I have always been intrigued by web development and design, so this was the chance to tackle something new in a new environment.

<div class="box">
<b>Disclaimer:</b> you could use GitHub Pages and Netlify to achieve all this without paying a dime, but again: the core of this project is to use AWS!
</div>

This is the idea:

<center>
  <span class="image"><img src="/assets/images/infra1.png" alt="" /></span>
  Created using <a href="https://cloudcraft.co">CloudCraft</a>.
</center>
<br>
1. **AWS Route53** for the domain name and manage its DNS;
2. **AWS S3** to host the Jekyll-built site;
3. **AWS Certificate Manager** to issue a valid certificate;
3. **AWS CloudFront** to serve HTTPS and deliver a cached version of the content worldwide.


Some insights: the website will respond to both www.domain.com and domain.com requests thanks to specific Route53 and S3 configurations. Every HTTP request will be redirected to HTTPS and also be served with a valid certificate. The end-user will access the content via Cloudfront distribution rather than the S3 buckets.

I expect this site to never go past AWS free tier, so the total cost will be a mere $15/year for the domain.


I might make an indepth post that go into the nitty-gritty of making this site down the road, but honestly the AWS documentation is plenty to get started with a basic static site.

<h3>CircleCI</h3>

To be Implemented


<div class="box">
Credits: Photos by Maik Jonietz, Michael Weidner, dhe haivan, Bryan Goff on Unsplash
</div>
