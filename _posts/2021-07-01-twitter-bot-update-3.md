---
layout: post
title:  "Twitter bot update 3"
date:   2021-07-01 14:34:00 +1000
categories: [twitter bot, blog]
author: Case Tonkin
---

Well, the liking and retweeting function works fine but I must say the result is a little underwhelming. I mean, it does exactly what it's meant to but yeah I dunno maybe the idea's the problem? Or the implementation?

By underwhelming I guess I mean that it retweets and likes kinda random stuff &ndash; again, working as intended &ndash; but like yeah it's just kinda 'meh'.

I think part of the problem is the list management thing. There's not enough to really saturate it fully and allow for a diverse range of views and things.

The other thing I could do is make it not be the first like every time and really fine-tune the conditions under which it interacts with a tweet. For example, adding certain weights to probabilities so that it is less likely to like a tweet with 0 likes than it is one with 1,000.

Next is the actual tweeting part. I still haven't got that worked out properly, kind of because I don't know what to say. I think it actually probably works just fine and needs some filling out.

So since it's work time I'm going to populate it with stories from today's newsletter &ndash; not just mine &ndash; then let it drip those out. 

It's still really rudimentary and just like runs through items listed in a JSON file but hey whatever.

So I've worked out a decent way of (hopefully) making the bot just drip out the newsletter articles with links and @s etc. 

One day I'd like to make the process fully automated. Maybe something like beautiful soup? Could I write something that maybe pulls the top 10 links from the front page and if they're new then it populates my dumb little JSON file for me? That would be cool.

Anyway, for now it seems to be working kind of so we'll just keep going about our business. Also changed the name of the bot because I noticed it was doing stuff. Dunno where else it's heading but this is kind of the first version working I think.

Something funky is going on with my Visual Studio Code thing though. It's started like running everything from the git folder of this blog, even though the Python stuff is in a different, if not adjacent, folder. I dunno. It's just acting a little funky.

But so now that I've got the interaction functions happening and the work part of the tweeting function sort of working (even if it's only a bad version of TweetDeck) I have to get on with the fun automated automated writing thing.

To do that I'm going to start with Markov chains. Take a bunch of text &ndash; ideally a lot of stuff I've written over the last few years &ndash; and markovify. Tweet the output. Ez.

That routine will run outside work hours.