---
layout: post
title:      "CLI Project Thoughts"
date:       2020-02-16 14:20:25 +0000
permalink:  cli_project_thoughts
---


Have you ever had the experience in life where you think to yourself 'what am I doing here?'. That’s the way this project started out for me. I have no prior coding experience so looking at a blank screen trying to pull all my thoughts together as to where to start was like nailing Jello to a tree. And picking a website to work with, was like trying to invent the light bulb, okay maybe it wasn’t that bad, but you get my point. That's not to say I didn't have the resources to do the work involved.  learn.instruct was an incredibly important resource, as are all of the labs leading up to the project, but sitting there thinking of all the possibilities was (at first) mind numbing. So, I have a little advise for you, make a plan.

First, decide whether to use an API or scrape a website. Scraping seemed to be the better choice for me. I know what you’re thinking 'what happens when the website gets updated or changed, your program may not work anymore'. You're right that is a distinct possibility, but this is a learning project, and if it does not work forever that’s okay, I just need it to work until the review is over.

Now this (to me) is the hard part, trying to figure out what website to use. I can't tell you how many times I thought I had the right website only to find that it used java script to display the information I needed. At one point I started the project and the website, I was using, was updated and I couldn't get the information the way I needed it anymore. Anyways I found the most useful tool to use in searching for a good website is on repl.it. Here's the link to it: [https://repl.it/@gwheeler45/ScraperChecker](http://). Once you've got your site picked it's time to begin.

Second, starting the gem. The lesson on CLI Project Planning walks you through all the set-up steps. This is pretty straight forward, there are a few tricky spots trying to get the 'require' and 'require_relative' for the program to know where to look for your code, but the 'live CLI build' video will get you through that.

Third, stubbing the program out. I started by defining my classes and deciding what each one is responsible for. Writing methods for my controller(CLI) class was harder than I thought it would be. I used fake data to start with and that was all well and good, but then as I got real data I found that quite a few of my methods either needed to be moved in the order I called them or were useless altogether. The scraper class was problematic at times as well. I found that I was using the wrong css selectors at first so when I tried to turn the data into objects it was one big array. What’s that definition of crazy again - doing the same thing over and over again and expecting different results, that was me trying to get the wrong data to be objects. Then one night I figured out what I was doing wrong and things started to work, and it was like a light from the heavens shown down and there was beautiful music in the background, okay obviously that’s nowhere near the truth, but it was very satisfying to see things work the way I wanted them to. After things were working, I tweaked the controller class just to make the displayed data easier to read for the user.

Finally, my CLI application is basic, but when you go from idea to final product it's a good feeling. The project helped me solidify some of the concepts from the labs. The office hours and the slack channel for the CLI project are great resources. I haven't been through the review process yet so I'm not sure how things will work out, but even if I have to do some revisions I don't think I'll be disappointed, I'll see it as something more to learn, after all that’s what I'm here for, *right*? Anyways, happy coding.


