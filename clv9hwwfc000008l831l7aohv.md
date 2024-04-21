---
title: "A Quest To Conquer Instagram’s AI and Automate User Interactions!"
datePublished: Sun Apr 21 2024 12:19:42 GMT+0000 (Coordinated Universal Time)
cuid: clv9hwwfc000008l831l7aohv
slug: a-quest-to-conquer-instagrams-ai-and-automate-user-interactions
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1713701911648/295e8e54-1ef8-4688-986e-21eac6ec8b01.png
tags: ai, automation, selenium

---

It's so surprising how simple things can transform into huge projects that end up teaching you tons.

A few months ago, I was learning this fancy tool called Selenium, which can automate any action on the web, to create a simple bot that can export some PDFs from the web.

Not gonna lie, Selenium is super straightforward. Its simplicity opens up various possibilities after investing only a few minutes into it.

So, I thought of using it to create a social media bot called Social Media Grower to automate user following and liking. I could combine different selenium scripts to allow this functionality for any social media platform in the wild.

It wasn't a big deal since all you do is press some random buttons!

Obviously, I was wrong. Nothing's too simple in the world, my friend. In fact, it turned out to be one of the biggest projects I had ever worked on. ([find it on GitHub!](https://github.com/SenaThenu/social-media-grower))

### The Plan

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1713701088385/b3c33c94-c364-4095-b773-e6ae60e3876c.jpeg?height=512 align="center")

To be honest, I didn't do much planning because it seemed to be a simple application. So, I just opened my Notion project planning template and worked through it quite vaguely.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1713532053608/03b37afe-715e-48a4-a72c-bc351ba12cc3.png align="center")

Then, I started researching user restrictions on Instagram and Twitter (aka X).

Afterwards, the whole project idea was crystal clear:  
*Firstly, allow the bot to click on follow/like buttons and extract text from what's on the page. Then, make the bot interact only with users who are likely to follow back (by considering their following-to-follower ratio). Pressing the buttons should be timed to meet the restrictions of each social media platform.*

Since this seemed super simple, I allocated a few deadlines and estimated that I would finish the project within 2 weeks by working around 2-3 hours each week.

### Development Process

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1713701174671/5ac56ef4-f851-49d7-abbd-b36fd38d29c1.jpeg?height=512 align="center")

Full Disclosure: when I find something fairly simple, I become too optimistic about how fast I can complete it. By the end of 2 weeks, I could only finish the bot for Instagram. No Twitter. No CLI.

This was partly because I had forgotten most of what I did and had to refresh my memory by the time I jumped from one week to another.

I could have technically allocated a few consecutive days to avoid this, but Social Media Grower wasn't much of a priority.

To make matters worse, I had even announced that I would release Social Media Grower on 14th March (Pi Day). So, I had to put things together and release a Minimum Viable Version on GitHub as soon as possible!

I postponed the Twitter bot and started working on the user interface. Again, I had to change my initial plan. Instead of creating a Command Line Interface, I decided to create a Graphical User Interface even though I had never created GUIs before. Why?

1. I would have a project as evidence of my PyQt UI design and creation skills.
    
2. Anyone can use Social Media Grower. (even a granny trying to grow her Instagram)
    

But seriously? I was extremely short on time. Yet, I couldn't help it because transitioning from CLI to GUI in the future is quite hard.

The GUI became the most complex part of the whole application. It took me the next 3 weeks (around 10 hours each week) to finish it off.

### Release

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1713701271369/438f8377-74f9-4edf-8184-32b261cb761a.jpeg?height=512 align="center")

Normally, once you complete developing, you have to test it. Yet, I was too impatient and had already done small tests throughout the development process to make sure everything worked fine.

So, I just released *v1.0.0* without testing the application to its limits.

Only after 2 days did I test its limits.

It turned out that even though it could technically perform any number of follow/like actions, Instagram's bot detection AI was clever enough to detect bot actions when done in large amounts.

That realisation threw a pie in my face and reminded me of my dumbness.

I was dealing with one of the richest tech firms in the world. They have industry experts. Obviously, they would have considered all the bot automation possibilities and developed advanced algorithms to detect them.

I felt as if I should give up. Plus, what I was trying to do was against Instagram's community guidelines.

Yet, I had put too much time, effort and energy into this project. I couldn't just let that waste.

So, I spent the next few days, experimenting with different restrictions.

Finally, I released *v1.0.1* with some minor bug fixes and refined restrictions on user actions.

To this day, the Twitter bot has not yet been created. Hopefully, I'll start working on it next week and finish it relatively quickly thanks to my experience with the Instagram bot.

### What I Learnt

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1713701295341/95f9f59c-afdc-4531-9939-4fe4e43819ca.jpeg?height=512 align="center")

* I must spend more time planning no matter how small the project is.
    
* I need to even think about all the possibilities. Like factors that I can control and those I can’t.
    
* I should properly break down every aspect of the project in detail… Without being vague.
    
* Try my best to adhere to the plan and not change things on the fly unless it's strictly necessary.
    
* Summarise what I did each day in a document so that I can quickly refresh my memory when I start developing again.
    
* Never give up because there’s always a solution. (yo, that's a cliche)
    

### Conclusion

I hope my experience will prevent you from making the same mistakes I made.

Don't forget. The comment section is reserved for your thoughts.

Have a nice time developing! I'll catch you in another article... Peace!