---
layout: post
title:  "Twitter Bot 5"
date:   2022-03-28 11:42:35 +1100
categories: blog, twitter-bot
author: Case Tonkin
---

Another update about my Twitter bot since I've been fiddling with it a bit over the past week.

First off I unfollowed everyone. This was partly as a disincentive to use: if my timeline is empty, there's no point uselessly scrolling for hours on end. 

But also a few years ago I started following everything. This was back when I was working at Radio Adelaide and in the mornings would follow every account Twitter suggested.

I even used some tools to automate the following process, finding accounts with large followings and hitting follow on everyone.

I think the intention was to maybe catch a few auto-following bots or something but also just to create a lot of noise because, I dunno, reasons. That was a while ago.

And so ever since I'd been stuck following thousands of accounts that didn't mean anything to me and it was kinda crap. So I wrote a script to automatically unfollow all accounts.

The rate limit on pulling Twitter follows is pretty low so I hit it regularly and left the bot running quietly behind the scenes for a day while it did its work.

That was a fun little task and refreshed my follow count. Now I'm building it back up with a script that automatically follows accounts that mention me, while liking their mention as well.

I've hosted this on <a href='https://pythonanywhere.com'>pythonanywhere.com</a> so it should be running in the background as we speak.

At first it would reply something inane and auto-generated but that got old quick and I haven't installed the module I use for generating nonsense on Python Anywhere yet -- though I suspect it's trivial to do so.

Maybe now it's also worth thinking a bit about what this project is about, something I'm not sure I've properly articulated. 

The idea is to create an extension of myself on Twitter; understanding social networks and the like as extensions already, digital likenesses that sound like you and so on.

Unlike your non-digital self, a social profile doesn't have automated processes: you have to actively manage it, use the account, hit like, scroll, etc.

So I want to give my Twitter profile a heartbeat of sorts, a way for it to always be doing <i>something</i> even when I'm not actively looking at it.

Twitter-bot-v1 simulated this presence by going through and liking/retweeting things from lists. Now we're back to basics with liking and following just mentions alone.

Now that I've found Python Anywhere and can get things running remotely, I can at least keep the bot running without having my PC turned on.

Anyway, that's where we're at at the moment. Gotta go. Bye!
