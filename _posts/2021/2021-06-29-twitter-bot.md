---
layout: post
title:  "Twitter bot update 1"
date:   2021-06-29 22:43:00 +1000
categories: [blog, twitter-bot] 
my_number: 69
author: Case Tonkin
---

So I've had a really productive night on my Twitter bot. Probably almost time to hit the hay actually.

Good night overall, really. We had some dinner and a good conversation, Sama and I, then did dishes and talked some more. I love her.

After that I got cracking back onto the Twitter bot.

<strong>The CaseBOT 9000</strong>

Tonight's task was to get my bot automatically liking and retweeting things.

First step: liking (or favouriting as the API still calls it).

The way I wanted to get this happening was by setting up lists to correspond with whatever it was that I'm doing at the time. Initially this will be two lists: 'work' and 'not-work'.

During work hours, the bot will take the first tweet from my 'work' list and smash that like button. It'll then wait a random length of time (somewhere between say 5 and 25 minutes) and do the same thing again.

Outside work hours, the bot will run the same function but with my 'not-work' list.

Before tonight I had been able to pull the Tweet ID from the first tweet in a list's timeline. Didn't even know if I was pulling the right thing, but turns out I was so tonight I made it interact with that ID -- by liking the tweet -- which was much easier than I expected.

I've really spent the last hour or so working out the if/and function thing for deciding if it's work time or not and getting the delay sorted. Looks like it's working just fine now. I've got a terminal open with the script running and it tells me the time of interaction, the function -- work or not work -- the tweet text, and when the next interaction will happen.

<strong>Heartbeat</strong>

The whole idea for this thing is to create a heartbeat for my Twitter presence. A heartbeat is something you don't actively control -- it just <em>happens</em>.

I figure I can have other interactions the rest of the time but as long as the heartbeat is still going, then it's like my Twitter presence is kind of passively there. I don't have to try then, I guess.

Why not automate it?

I dunno. That's the basic idea. I've been meaning to kind of write down what the point of all this is and I'm sure there's something else there. Best metaphor I have for now is just that it's the 'heartbeat'.

It's the vibe, man.

So what else? Thinking possibly it's not worth leaving my bulky PC on constantly to do this crap so might be a good use-case for a Raspberry Pi to have sitting around doing various Twitter things as the bot gets going. 

<strong>Tomorrow</strong>

Tomorrow's task should be getting my lists in order so I don't just have the same thing sitting there stinking up the place. I look forward to getting back and fiddling around.

Actually I've also got an appointment to get my heart scanned because of high blood pressure or whatever so there's that, too. Good luck, me!

Then yeah it'd be nice to play around with this more and add more of that digital garden stuff like <a href='https://tomcritchlow.com/'>Tom Critchlow</a> has done. No idea who the dude is but hey he's led me down this path and it's been a lot of fun and I haven't played any video games tonight doing it so that's even better!

P.S Just noticed how I talk about heartbeat and also my heart's a bit dodgy. What's up with that? Some kind of sub-conscious thing going on? You decide.
