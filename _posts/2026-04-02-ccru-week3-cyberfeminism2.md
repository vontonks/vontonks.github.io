---
layout: ccru
title: "A Most Radical Gesture"
date: 2026-03-26
week: 3
tags: [ccru, cyberfeminism, sadie-plant, theory]
---

cd ~/Downloads/
python3 -c " 
from faster_whisper import WhisperModel 
model = WhisperModel('base', device='cpu', compute_type='int8') 
segments, _ = model.transcribe('ccru-lecture3.m4a', beam_size=5) 
for seg in segments: print(f'[{int(seg.start//60):02d}:{int(seg.start%60):02d}] {seg.text.strip()}') 
" > transcription.txt

remove the timestamps from this audio transcription and tidy it up into sentences. Don't assume you know what I was saying, if there is uncertainty about meaning or word choice, query me.

claude-opus-4.6: This is a meaty transcription — clearly your notes/reflections on Sadie Plant's work, probably from the CCRU course. I've gone through it and cleaned it up, but there are quite a few spots where the transcription seems garbled or I'm unsure what you actually said. Let me work through it in sections and flag the uncertain bits.

Here's what I'm confident about, with queries inline:

---

So let's have another crack at it.

Sadie Plant connects the art of weaving — calls it a feminine activity that's worth an art. It is a way of imbuing meaning into reality, stories that like their toll come real.

****Query 1:** "stories that like their toll come real" — did you mean something like "stories that, like a toll, become real" or "stories that take their toll and become real"? Or something else entirely?*

It's an art form that was mechanized, but the loom connects that to Ada Lovelace. Coding as weaving, weaving webs, we've got threads, online cultures. And it starts to make the argument that the internet is feminine, digital technologies as feminine. And the arc of progress — the idea that the arc of technological progress bends toward liberation. Cyberfeminism, Afrofuturism, scenic futurism.

***Query 2:** "scenic futurism" — did you mean something else here? Xenofuturism maybe?*

But by extension, the arc of technological progress bends towards liberation.

Just to expand on that more — the idea is that AI is fuzzy. The first idea is that women have been seen as less than men to some extent, so have people of colour. So this is, you know, contrary to the white supremacist patriarchal view, right? The colonial view of the treating of people — and the present men saying they are irrational, inhuman, and maybe not possessing a specific type of intelligence, whatever. So it's like an identifying with them — so the super intelligence will identify with traditionally marginalised people, historically marginalised people, and will maybe remake society in a way that resets things.

It might be too reductive. There's a lot of parts of this where biotech is like non-masculine, treating it that way — it's gender-bendy, it's identity-warping, it's non-stable. And there's all these kind of muddy things that maybe I'm not getting. I don't think I can be like a grass ball, right?

****Query 3:** "I don't think I can be like a grass ball" — what were you going for here? "I can't grasp it all"?*

It's kind of postmodern identity, it's fragmented, neo-conscious stuff. It's plugging your brain into a matrix of a sort. And so here's the criticism — which is: the matrix is still owned by the maker class.

****Query 4:** "the maker class" — did you mean "the master class"? Or "the maker caste"? Or literally "the maker class" as in those who build/own the tech?*

So it was the superintelligence, right, and that's just software. Look, at the end of the day it's just software. And people — I always have this thing where you just take AI and replace it with "software" and it just dampens the phrase a bit, because AI is like — people bring a lot of sci-fi baggage to it, and software is really mundane. It's just computers, it's bits, right? Software can be secure or insecure, it has degrees of trust and interoperability and brittleness and understandability and complexity and simplicity and beauty. Software is a lot of different things, hardware is a different thing. AI is software and I think we can take too much away from all of that.

Right, think about who owns the digital experiences — that would be the big tech companies, right? Who owns the digital infrastructure, the actual hardware — that's the same thing. Who owns the software — what the AI would be — just the same as the digital experiences. It's like metaverse stuff, which has fallen over itself. And even crypto had that thing of liberating the web — it was trying to be all of this stuff, but humans keep doing what humans do. They want to be the ones wearing the boot, right? The whole point of the crypto thing is like "what if we remake society where we're in charge?" You know, that human all-too-human tendency is still there. And the core of that is power, and power dynamics, and power relations. So I don't see how in 2026 or in 2036 the power relationship changes enough, right?

So then I guess the core premise — maybe the premise that saves Plant — is the runaway machines. That the AI will just get too smart and take over. Runaway software. And I just find the idea of runaway software not very compelling. It's too science fiction, it isn't realist enough. Yeah, maybe there's the hyperstition that we haven't touched on yet in the course, and maybe I'm too much in that realist mode. And this is like being sold some fantasy future. I want to see something that's connected to reality, because I think the future has to have that. I think if we're just talking about ambitions of the future based on golden age sci-fi and ambitions of AI — we have to go from the cyberpunk dystopia, don't we? Isn't that the reality that we're in?

Kind of — you need to have owning the means of computation be the thing, as a potential source of liberation. Or else you're just assuming this similar teleological thing of the arc of history bending towards — like, capitalism will destroy itself, hopefully, from within. And it can't, because the system continually renews itself. There's no exclusion that is sustainable enough to continue.

****Query 5:** "There's no exclusion that is sustainable enough to continue my except then you look at like the big bang" — this part is unclear. Were you saying something like "there's no contradiction sustainable enough to bring it down, except then you look at the Big Bang" or something else?*

And you go — that somehow continues to be alive. And maybe if this is just a copy of that, then it carries on. So how well does that logic work? Like if it never — the other time it folds, the fold itself is like the Big Crunch or something. So I don't know how conceptually that works either. It's turtles all the way down.

And what's the other way out? It's new consciousness. Is it that the superintelligence is not just software? The systems — maybe this is what we're getting at — that it's the software plus the human interactions plus cities and smart lights and sensors on everything, right? That is the new consciousness. That it's walking away from your screen and still thinking about the interactions you had on it. The new consciousness is seeing a whole bunch of stuff on social media and it getting caught in your brain. The new consciousness is not having to remember directions, or how to think, because that's all done by machines. The machines do the thinking for you. All you do is feel and have desires.

But again, that just sounds like new consciousness is stripping away the human and diffusing it, in order to peel back more layers to get to the desire button that it can just press or whatever. It's an anti-agency thing. It's just trying to — because that's what it'll do. So I don't see the way out. I didn't see how this is a way out at all. The situation is — I think all she's done is recreate it, maybe, or find it again. It's just been subsumed. And maybe the problem isn't capitalist structure or whatever as much as it's just the human structures themselves. But if we just invent ever-better utopias — but wait, okay.

So there's the capitalist realism thing — like, we had a vision for the future and we kind of hit the end of it. "Where's the future I was promised?" — that's the Mark Fisher thing. And it's very real. The world we live in now is nostalgic, with the fascists doing the "where was the future I was promised" thing. And you see that in the economic circumstances — it's like, oh, ten years pass and you miss out on housing and you're spending twice as much on half as much.

****Query 6:** "should the idea that the future's kind of been already sold out for Lundy was being like priced in" — I can't parse this. What were you saying here? Something about the future being "priced in" or "sold out"? And what's "Lundy" — a name, or a garbled word?*

Where's the escape though? The escape is into greater illusion again — that's what she's saying. Go deeper into illusion, go further from reality. And you go, yeah, at some point you can spend all day plugged into the matrix in whatever form, you can spend all day staring at screens. And then when you've got to tend to the wetware — like, return to meatspace — you look around and this sucks. Why does this suck? Because I'm spending all the time in cyberspace, which is ephemeral and illusory by nature. Like, there is physical reality, isn't there? It has objects in it, it can be passed from person to person.

The rest of the space is like in your eyes only, in a real way. It's curated for you, it's hyper-personalised, it's not shared. It's not shared space at all in any meaningful way. I don't think it can be. I think it's far too localised.

****Query 7:** "is the idea that we just make — is this the web three promise of like what if internet more interoperable, ActivityPub, is that the great white hope?" — is that a fair reconstruction? You were talking about Web3 / ActivityPub as a potential answer?*

I don't know, because I think people choose cigarettes and Twitter. They pick the thing that is simpler. Information is like a drug, not much else.

****Query 8:** The next section gets quite fragmented: "when they leave us / maybe I'm just an old-fashioned / the damn or something it's just politics" — can you clarify what you were saying here? It seems like trailing thoughts that didn't fully form.*

I think we've got this swing against all of this stuff. I actually think it's more boring than it looks. There's a lot of interesting stuff that goes on but it doesn't last very long. Not like a bridge, you know. Or we hit an eternity inside this place.

****Query 9:** "More cyclosis" — did you mean "more cyclical" or is "cyclosis" the word you intended?*

I think the power is going to be in people who can use their minds, who think through things here and now.

****Query 10:** "I'm used to software that isn't using them" — what were you saying here? Something like "as opposed to software that's using them" (i.e. people who use software vs. people who are used _by_ software)?*

These swings are going to be more extreme. There's the radical gesture. Yeah, the radical gesture is leaving it. Is that the thing? The radical gesture is to leave, to not be in the spectacle. Yeah, the radical gesture is not to be — you can't just plug into the spectacle. The spectacle, the scale is just immense. You don't have the compute power, you don't have the means of computation. You're just a little fucking speck, just data points for it, you're nothing for it. Stay away from it, stay the fuck away from the spectacle. Right, the radical gesture is to walk away. Like, to be offline.

Yeah. She was wrong. Or she was right. About — I think the idea is maybe it's just not yet. Maybe we need to be in between or something.

****Query 11:** "like yeah she's talking the culture of fucking shit right / this is really an embankment this is yeah / you're opposed to him and / robot layered to utopia" — this section is very unclear. Were you talking about Iain M. Banks' Culture novels? "Robot-layered utopia" as in the Culture's AI-managed society? And "embankment" — did you mean "an Iain Banks moment"?*

Where when you do something wrong you have to have like a little orb float around you.

****Query 12:** That does sound like a Banks Culture reference (the drones). But then: "banks as culture is just neo-localism / again it's new imperialism" — is that what you were saying? That the Culture is just neo-imperialism?*

The grey goo. And if she's just ended up describing that, or wanting that — we had to help, you know.

Like, you don't have the scale. That's the fucking problem. You need to — like, the average person on the street would have to jacket up and fucking get a botnet. You know, you have to have capital to spin this stuff up, or you have to be able to break into enough computers.

****Query 13:** "the average person on the fuller / jacket and fucking get a bot net" — was "fuller jacket" meant to be "Full Metal Jacket" as a metaphor, or were you saying something like "the average person on the floor would have to jack in"?*

In theory the AI will do it, or an AI will do it. But it's — to be able to remember, it's the puppets. It's just software.

****Query 14:** "but it's to be able to remember the puppets" — what were you getting at here?*

It comes back to something at some point. And I don't think there is some grand zero-day that comes across everything. I think the net is too dispersed. There's too many different operating systems. They're not all going to get pwned simultaneously. People find stuff. The nerds are still there. And it's the offline ones who find stuff — the ones who are still paying attention to how much memory a fucking program is using. It's the ones who are going "huh, there's this slide — why is there so much lag in this package? Oh, it's because the little bits didn't change over, there's an extra something that's been injected." And the ones who are like jacked in but not quite the same way, because they haven't given up their local thing.
