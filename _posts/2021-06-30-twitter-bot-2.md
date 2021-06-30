---
layout: post
title:  "Twitter bot update 2"
date:   2021-06-30 15:55:00 +1000
categories: [twitter bot, blog]
author: Case Tonkin
---

Cool so more good progress today.

The two features I've been working on are in and sorted and I've got it actually working right now. Currently set for like 1-5 minute delays between interactions (retweets and likes) while I sort out the kinks.

Thought I had it sorted out like half an hour ago but it would keep crashing when it would try to like or retweet something I've already done. So I tweaked my code to make like an if-elif thing so now it checks first if I've liked and/or retweeted it before deciding what to do.

There we go, it's ticking along nicely now!

So how it works: check current time and day of week. If it's 8am-6pm Mon-Fri, then pull the first tweet from 'work' list. Else pull first tweet from 'not-work' list.

Then it decides whether or not to retweet or like. I've got it set so that it'll only retweet if something has more than one retweet already and if a 1-4 roll comes out as a four. So a tweet with more than one retweet has a 25 per cent chance to get retweeted.

Otherwise it'll get liked (if I haven't liked it before) and the program will wait a random lenght of time before it loops again.

<strong>Hit or miss</strong>

Watching it tick over I'm wondering if I should like <em>everything</em> that goes on my lists and maybe there should be a chance that it misses as well. Maybe just a 25 per cent miss chance. Actually that's pretty high. What's the high ground miss chance in dota2? 

...

Well that's currently 25 per cent according to the <a href='https://dota2.fandom.com/wiki/Evasion'>dota2 wiki</a> so let's stick with it. I'll push that in now and then let my bot get back to it. Frequency is still an interesting question and I guess it's okay to check for interaction if it's got that miss chance as well.

Alright, changes made. 25 per cent miss rate on likes, same hit rate on retweets.

It's all going to take some tweaking but we'll get there.

Sama already asked if I could do the same for the Pop Fix Podcast group so I'll put that to them for the next meeting maybe and if they're keen get them to work out who they want to have in the list and, yeah, I'll put it together and let it run I guess.

<strong>Heartbeat</strong>

In other news, I did go and get my echocardiogram (ultrasound on my heart) done today. Was fine I guess. Hurt a bit when she was jamming the magic sound-hearing wand into my ribs but otherwise okay. 

Fingers crossed this thing works out but I'm prepared to take medication that gets my blood pressure down and helps atrophy any muscles that have gotten large from overuse or whatever.

I don't really know why it's bad to have the heart muscles getting bigger, presumably because it then has to do more work because it's bigger? 

Whatever the reason is, I'm glad to be getting on top of this now rather than like further down the line and finding out I've done 10-15 years worth of damage rather than the maybe the four or five that I suspect it's been going on for.

Have an idea for a blog about where I remember this whole blood pressure thing starting which was more than five years ago now. Sad stuff but we're working through it all.

<strong>Back to the bot</strong>

Anyway, now that I've got the likes and retweets sorted, I have to get the posting thing worked out as well.

My plan for the bot and for this blog was to make it all public kind of in one big go but that wasn't meant to happen for another month or so. I think I may have underestimated how much of it I'd get done to be honest.

The Twitter bot (maybe called CaseBOT9000, I haven't decided) was meant to hit v1.0 when I got the likes, retweets, and posting done and dusted.

Posting isn't fully automated just yet, it's kind of more like a shitty version of TweetDeck at the moment to be honest, just pulling tweets from a JSON file basically. But that's fine. 

I think I'll do the same or a similar thing and make it figure out what time of day to be running things. Then I'll just load it up with stuff including <a href='https://ia.acs.org.au/'><em>Information Age</em></a> articles while @ing people who write it or whatever.

Should be easy enough to just load shit in during the day and fire it all out as we go.

As for outside work? No idea. That'll be where I do the Markov chain and NLP stuff as I test things.

Then at some point I'm going to have to make this blog/digital garden or whatever it is public or, rather, just tell other people that it's here.