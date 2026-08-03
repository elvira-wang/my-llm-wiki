---
title: "Can't get a successful print after 8+ attempts"
source: "https://www.reddit.com/r/resinprinting/comments/1v2cg43/cant_get_a_successful_print_after_8_attempts/"
author:
  - "[[EternalVirgin237]]"
published: 2026-07-21
created: 2026-08-03
description: "Folks, I've been resin printing for a bit now with overall good success. However, lately I can't get a single thing printing correctly and I"
tags:
  - "reddit"
---
Folks, I've been resin printing for a bit now with overall good success. However, lately I can't get a single thing printing correctly and I have no idea why. I have been trying to print some 1:100 scale tank models and there are just gaping holes in the supports and gaps to where the resin actually hangs on. Some supports just decide "Nope, not today".

A few months ago, I was printing these exact files over and over again in an assembly line fashion with zero failures. Now, I can't do anything right.

I've tried all sorts of settings: Lowering the Lift speed, Increasing bottom exposure time,  
increasing support density all the way up to 80%, using different sized supports, re-leveling the bed, increasing lift distance, etc (see settings below).

The latest settings I tried (Elegoo Mars 3, Chitubox):

\- Releveled the bed completely  
\- Layer Exposure Time: 2.5 secs  
\- Bottom Exposure Time: 40 secs  
\- Lift Speed: 60 (mm/min)  
\- Lift Distance: 7 mm  
\- Layer Height: 0.05 mm  
\- Retract Speed: 210 mm/min  
\- Idle Temperature sits between 75-78 degrees  
\- Using Elegoo Standard photopolymer resin

The only possible thing I can think of now is my FEP? But not entirely sure how that would be causing anything?.. Any ideas? Thank you in advance, and I apologize for adding to the plethora of posts like this.

---

## Comments

> **PoorAnalysis** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyu2wd7/) · 2 points
> 
> Have the temperatures dropped since a few months ago? Those failures could be the result is resin that's too cold.
> 
> > **EternalVirgin237** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyu32en/) · 1 points
> > 
> > Quite the opposite actually.  I live up north and have to use a space heater during winter to get successful prints. But now the garage sits right around 75-80 or so.
> > 
> > > **JuneBugWhisperer** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyukq7q/) · 1 points
> > > 
> > > I’ve had to reduce my exposure time with the summer months. I keep my printer in an exclosure all year at 82f, but my garage where the printer has been 90-95 since late May. I’ve had to run a couple calibration tests and dropped my exposure from 2.1s to 1.75s. I’ve kept my bottoms layers the same.
> > > 
> > > > **EternalVirgin237** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyvxqv7/) · 1 points
> > > > 
> > > > Really?? Huh... interesting 
> > > > 
> > > > > **naghavi10** · [2026-07-22](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oz3qd34/) · 1 points
> > > > > 
> > > > > afaik higher viscosity means longer curing time so it makes sense the inverse would be true too.
> > > > > 
> > > > > edit: higher instead of lower

> **sdigian** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyu5p08/) · 2 points
> 
> I would try a different resin. I started with elegoo and I had similar issues. About 50% of my prints failed. I have since been using anycubic and haven't had a failed print since.
> 
> > **EternalVirgin237** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyvxjxl/) · 1 points
> > 
> > I'll definitely consider this.. but i feel like my resin has been working fine so far?. Not sure. Thank you!

> **Traditional\_Yard2741** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyu67t0/) · 1 points
> 
> What's the wait before exposure time? I find increasing that solves a large range of problems. Is the resin old? I don't know if it goes off exactly, but if it's been sitting on the shelf for a year or more it might not be good. Changing the FEP could be a good idea if it's old, if nothing else you've eliminated that as a variable. How many bottom/transition layers do you have? Have you checked the screen for damage or obstruction?
> 
> > **EternalVirgin237** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyvx8xy/) · 1 points
> > 
> > Brother i gotta be honest, idk what wait before exposure time is lol..  resin is new, and idk how many bottom layers unfortunately.  Can't find that in chitubox.
> > 
> > I checked the fep, and it does seem to be rougher in a few places rather than smooth. Hmm
> > 
> > > **Traditional\_Yard2741** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyvzxq4/) · 1 points
> > > 
> > > Yeah, if you've got rough spots then definitely replace it. The "wait before exposure" is the amount of time the machine waits after lowering the plate before it turns on the screen. I think some slicers call it "light off delay" or "wait before cure" basically if you give the resin plenty of time to settle after lowering the plate (like at least 2-3 seconds) it cures more thoroughly, adheres better to the existing layers, reduces layer lines, etc
> > > 
> > > > **EternalVirgin237** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyw36u5/) · 1 points
> > > > 
> > > > Got it! Okay ill do both of those things next chance i can and see what happens.  Thank you
> > > > 
> > > > > **Traditional\_Yard2741** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyw3xiw/) · 1 points
> > > > > 
> > > > > Don't forget to check the screen itself!
> > > > > 
> > > > > > **EternalVirgin237** · [2026-07-24](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oze3j8s/) · 2 points
> > > > > > 
> > > > > > Replacing the FEP fixed it, thank you so much for taking the time to help me out!
> > > > > > 
> > > > > > > **Traditional\_Yard2741** · [2026-07-24](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oze43wy/) · 1 points
> > > > > > > 
> > > > > > > Awesome! I love when people check back in with what fixed their problem, helps grow the knowledge base for everyone!
> > > > > > > 
> > > > > > > > **EternalVirgin237** · [2026-07-24](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oze8a5x/) · 2 points
> > > > > > > > 
> > > > > > > > Of course. I figured I owed it to ya'll. Especially since im one of the million "failed prints" posts. lol I imagine it gets annoying
> > > > > 
> > > > > > **EternalVirgin237** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyw4j5x/) · 1 points
> > > > > > 
> > > > > > Will do

> **b005t3r** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyu6ka0/) · 1 points
> 
> Give yourself 3s of wait before print for normal layers and 10s for bottom layers.

> **getfit87** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyvf5vr/) · 1 points
> 
> Have you changed your FEP ever? Have you re-calibrated? UV bulbs can lose power over time and sometimes you just need to up your exposure time.
> 
> > **EternalVirgin237** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyvydox/) · 1 points
> > 
> > I've changed my fep before... buuut that was maybe a year ago? So it's been a while
> > 
> > > **getfit87** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyvyyvc/) · 1 points
> > > 
> > > Change your FEP, and calibrate your resin again to be sure your printer is capable of being successful with the same settings.
> > > 
> > > When the FEP wears it stretches more, especially in the middle and it will either rip items/supports or won’t release completely because the lift distance isn’t high enough anymore.
> > > 
> > > > **EternalVirgin237** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyw2wuw/) · 1 points
> > > > 
> > > > Ohh dude that would make sense! In both photos it looks like the failures are both "inward" on the FEP.. of course it could be coincidence. But it's adding up.
> > > > 
> > > > > **getfit87** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyw40eo/) · 1 points
> > > > > 
> > > > > Yeah I am almost certain it’s a FEP issue, if that doesn’t solve it let me know and I can try and help more.
> > > > > 
> > > > > > **EternalVirgin237** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyx5jbw/) · 1 points
> > > > > > 
> > > > > > Will do, thanks!
> > > > > > 
> > > > > > **EternalVirgin237** · [2026-07-24](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oze2vgi/) · 1 points
> > > > > > 
> > > > > > Hey man, sorry been busy with work. I was able to replace the fep today and so far i've had 3 successful tank prints! Thanks so much for your help!
> > > > > > 
> > > > > > > **getfit87** · [2026-07-24](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oze3a2b/) · 1 points
> > > > > > > 
> > > > > > > Glad it worked out! I replace mine as soon as I start getting failed prints in the middle on bigger parts because it only get worse and more inconsistent from there.
> > > > > > > 
> > > > > > > > **EternalVirgin237** · [2026-07-24](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oze3g3e/) · 1 points
> > > > > > > > 
> > > > > > > > yeah it makes sense! Just hard to tell because my old FEP didnt look really bad at all.. but I suppose it just got stretched or got too rough..idk
> > > > > > > > 
> > > > > > > > > **getfit87** · [2026-07-24](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oze3q6s/) · 1 points
> > > > > > > > > 
> > > > > > > > > Yeah it just stretches, would never be able tell but it will sound a little different when you flick it lol. Like a bass drum vs snare. Print enough/replace enough and you can start to tell.

> **Usual-Purchase** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyvq8cx/) · 1 points
> 
> Looks like it’s failing at the supports, yeah? Same thing was happening to me recently, and the issue was that the first few layers of the actual print would tear off the supports. So you’d get the support printing just fine, and then a blob stuck to the fep sheet.
> 
> Simple fix for me was to increase support tip width from 0.25mm to 0.4mm. Worked fine after that.
> 
> > **EternalVirgin237** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyvy7qm/) · 1 points
> > 
> > Sometimes the supports themselves fail halfway. And sometimes it fails like you said. 0.25 to 4.0 seems like a lot. But hey, if it works it works. Maybe I'll try fiddling with that setting.
> > 
> > > **Usual-Purchase** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyw2bc3/) · 1 points
> > > 
> > > Oh whoops typo! I mean 0.4 not 4.0. lol yeah don’t make 4mm supports 😅
> > > 
> > > Fixed typo in the original comment
> > > 
> > > > **EternalVirgin237** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyw3pp5/) · 1 points
> > > > 
> > > > Lol ohh ok! I was like "What the??"

> **carnage1231jr** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oywout8/) · 1 points
> 
> Post your resin type and settings please. You've got to have calibration either way out of whack or something super wrong for that kind of fail
> 
> > **EternalVirgin237** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyx56ea/) · 1 points
> > 
> > I did post them near the end. Sorry if it wasn't more clear.
> > 
> > > **carnage1231jr** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyx79s0/) · 1 points
> > > 
> > > 40 seconds for the base layer is really long to me. When you go to remove from the plate do you have to chip at it to get it off the plate? Or does it crumble?
> > > 
> > > > **EternalVirgin237** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyxerpx/) · 1 points
> > > > 
> > > > I can try printing that when I get the chance next.
> > > > 
> > > > I tried 40 second base layer to try to help with build plate adherence. I can scrape it off with some force, but it definitely sticks really well and requires some elbow grease.
> > > > 
> > > > > **carnage1231jr** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyxfa6p/) · 1 points
> > > > > 
> > > > > It should never need to be pried off like that. Sounds like youre having resin calibration issues.. Its different with every printer and every resin. The town print is a calibration test with a well made guide ill link. [https://ameralabs.com/blog/town-calibration-part/?srsltid=AfmBOoq04xBrk3BIyjPYu6MJcPcULNeNNM552X7EEtEH0tvno3R0sALg](https://ameralabs.com/blog/town-calibration-part/?srsltid=AfmBOoq04xBrk3BIyjPYu6MJcPcULNeNNM552X7EEtEH0tvno3R0sALg)
> > > > > 
> > > > > > **carnage1231jr** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyxfphj/) · 1 points
> > > > > > 
> > > > > > Reminder not to cure the town. You wash it and check tolerances uncured. Some of the tolerances are super easy to tell, some you need a magnifying glass. But if you narrow down your resin you will have significantly less problems. Printing the town a couple of times will save you a headache
> > > > > > 
> > > > > > > **EternalVirgin237** · [2026-07-24](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oze3agf/) · 1 points
> > > > > > > 
> > > > > > > I got it working after replacing the FEP..the calibration print worked and Ive printed 2 more batches of tanks.. thank you!
> > 
> > > **carnage1231jr** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyx7ht3/) · 1 points
> > > 
> > > With all these issues can you attempt to print the Ameralabs town test print? It doesnt have supports or anything so we can narrow down the problem. Takes like 25min to print

> **riatin** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oywzgop/) · 1 points
> 
> Have you tried a slower lift speed? 40mm/m or so?
> 
> > **EternalVirgin237** · [2026-07-21](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oyx5skc/) · 1 points
> > 
> > I haven't tried that slow. But i have dropped it considerably from the default i had

> **alphawolf29** · [2026-07-23](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oz8248z/) · 1 points
> 
> try a different USB thumb drive? malfunctioning thumb drives can cause wacky problems. For what its worth I love elegoo standard gray, never had an issue with it.

> **EternalVirgin237** · [2026-07-24](https://reddit.com/r/resinprinting/comments/1v2cg43/comment/oze2y1g/) · 1 points
> 
> For anyone else having this issue.. Replacing the FEP is what did it for me.! Thank you to everyone who took time to respond