---
title: "Size isn’t everything - 4 ways to print LARGE parts with a 𝘀𝗺𝗮𝗹𝗹 3D Printer!"
source: "https://www.youtube.com/watch?v=4cnJFZZRui0"
author:
  - "[[Made with Layers (Thomas Sanladerer)]]"
published: 2023-11-17
created: 2026-07-15
description: "Thanks to Micro Swiss for sponsoring this video! Check out the FlowTech hotend at https://store.micro-swiss.com/collections/micro-swiss-flowtechYou don't need to feel like you're limited in what you"
tags:
  - "videos"
---
![](https://www.youtube.com/watch?v=4cnJFZZRui0)

Thanks to Micro Swiss for sponsoring this video! Check out the FlowTech hotend at https://store.micro-swiss.com/collections/micro-swiss-flowtech  
  
You don't need to feel like you're limited in what you can do because of the size of your printer - modern tech provides plenty of options to overcome that limitation!  
  
🩵 Support the channel by shopping through my affiliate links  
Buy Bambu Lab printers and printer accessories https://go.toms3d.org/Bambu  
Buy Prusa Research printers and printer accessories https://go.toms3d.org/prusa/  
  
Tools I use:  
🔩 Onshape Cloud-native CAD (free for Makers) https://onshape.pro/ThomasSanladerer  
🎵 Epidemic Sound for video music (30-day trial) https://share.epidemicsound.com/MadeWithLayers  
📷 Camera gear and recording equipment (not free, unfortunately) https://toms3d.org/my-gear  
  
🎧 Check out the Meltzone Podcast (with CNC Kitchen)! https://www.youtube.com/channel/UCzUgJrG-w\_KQexroYkJR9XQ  
  
👐 Enjoying the videos? Support my work on Patreon! https://www.patreon.com/toms3dp

## Transcript

**0:00** · so for my last video I built a pretty massive hemp create speaker and for that I had to print some molds to make the parts but as you can see each of these parts are way larger than even my largest printer that I currently have which is the voron at this time I didn't quite print these on the tiny boy which has like an 8X 8 cm build volume I did print these on a markv but even if you have a printer that fits the size of your part it can still make sense to split them up in the middle for printability or just to sort of share

**0:29** · risks if if you have a huge printer with a huge print and something goes wrong you lose a lot more Print hours than if you have multiple smaller printers working away at like 8 to 9 hour prints and not prints that take weeks at a time so today I'm going to show you four different ways to split up your parts in different software tools which are all free both for permanent joints and for

**0:50** · joints that you have to take apart again right after message from today's sponsor microswiss makes it easy for you to upgrade your printers and fix some of the flaws that would ruin an otherwise awesome machine machine they've just announced the microsys flow Tech hotend starting with a model specifically made for the creality K1 and K1 Max the flow Tech nozzles provide a continuous melt Zone eliminating leaks and enabling one-handed cold nozzle swaps with no hot tightening required and with its all metal design it expands the K1 working range up to 300° C while requiring no

**1:22** · changes to the K1 firmware or build space check it out at the link below and we're going to start with option number one the butt joint just two flat smooth even sides butting up against each other and you really want to use these with some adhesive to stick them together I like construction adhesive just out of the cartridge that works pretty well but it does take some time to dry you can also use hot glue or

**1:48** · 5minute epoxy JB World whatever those all stick very well together on 3D prints now of course the big downside of butt joints is that they don't provide any sort of alignment between the parts you can misalign them pretty easily and you're going to still stick them together but on the other hand let's say one of these parts has some print issues it warped or whatever you're still going to be able to stick them together and align them so that it looks good of course this is also the simplest form of joint that you're going to end up with if you split a part down the middle for printability so you can place both those

**2:18** · sides flat on the print bed where you split it you get an even surface that sticks extremely well to the bill plate versus having some sort of complex geometry that would need supports or other ways of you know getting it printable you split it down the middle and that makes it perfectly printable in many cases you still have to watch out for overhangs okay so let me show you a couple ways how to split points up like this one of the applications that often comes up is Microsoft's 3D Builder I guess mostly for the reason that it used to come or still comes pre-installed on Windows um it gives you some very basic

**2:50** · viewing and editing tools like you can rotate you can settle or place on build platform um and also up here in the edit ribbon you get the split tool um which is you know exactly as you would expect you basically get a plane that you can adjust um in this case this part I want to split like that so it's smaller and fits on my build platform um you can say keep top keep bottom or keep both and once you hit split basically your part has now uh been split as you

**3:20** · would expect into two separate parts and what's pretty cool about this is that you can just drag these items and drag these over into your slicer and you know print them from there but that is Microsoft 3D Builder basically this is the extent that this is going to be useful you get some other tools you know not that spectacular okay moving on to prusia slicer and this is much of the same story just that you're staying inside the slicer from the start so you get all the same tools you get your rotate move adjust tools um and then

**3:53** · over here you also get the cut tool and this works in exactly the same way as we just saw in 3D build Builder you get a plane that you can adjust the angle and position off and you know once you're happy with the position uh you select which objects you want to keep and how the slicer should finally place them you know either you keep them in place or you automatically stack them up if you split your part for printability reasons you hit perform cut and there you go um

**4:20** · in this case neither of these parts still fits on the on the printer standing up like that so I did print these laying down and you can just place them somehow like that and there we go same idea same exact idea same process just you're staying within the slicer by the way if you're using a printer that is not supported by prer slicer or you don't want to print straight out of prer slicer you can just use it as an editing tool and say uh export as STL obj and

**4:48** · you know export your files just like that so you can you can literally just export anything you did in plier straight into any other tool and lastly if you want to do it straight in your cat tool of choice in this case I designed this entire thing in Fusion 360 um you can also do it here and the benefit that you get here is that you can do it a lot more precisely because it can work off of your existing model geometry and you can place your splitting geometry exactly where you want it so how I would do this uh here

**5:18** · in Fusion is I would say construct offset plane I would pick my plane to where to the to the position that I want to split it at and just for visualization we can extend it and check where it's going to split the object and then up here in the modify toolbar um if

**5:34** · you don't have the split tool pinned to your quick bar you can find it in the menu split body you select which part you want to split you select what you want to split it with and that's going to cut your part in half and there you go there's two separate parts that you can now export or use in your design uh to further process next up we've got butt joints with Benefits pins so these

**5:56** · pins are basically just inserts on a butt joint that help me align these parts together and they will stay in position whenever I clip them together so that is a very easy way to make sure your alignment is perfect and it also helps you glue them together or in this case because I just clamped them with some cutout uh OSB it also made sure

**6:16** · these parts didn't slat around without any glue with these parts I used some custom springy pins just to help with alignment because these parts you know needed to be disassembled in a pretty weird way but typically you can just use round pins or some other shaped inserts that can help you align these parts and still make them printable if you print with this side facing down okay so let me show you how to do these in fusion and in Pria slicer starting with preure slicer it is the same tool as before you

**6:42** · select your part you select the cut tool over here and you basically just adjust where your plane supposed to hit and then over here in the menu you get the option to add connectors now I do prefer the dowel connector um the plug basically just adds little extensions to one side side and then a hole to the other but the Dow is a separate insert

**7:03** · part that prints separately and you just you know position your camera so you can look at the cut surface and you just click where you want your connectors to be generated once you hit confirm connectors uh and perform the cut it automatically creates those uh joining connectors right there in the center those are the dowels essentially uh in their terminology uh that basically

**7:26** · connect those two parts together and it did place the parts on the cut surface which in this case was not how these parts were designed to fit together but for other parts that might work just perfectly um these parts were actually designed to fit on the on this flat side right there um but obviously you know with these other parts on there the build surface is pretty full um now one issue that I have with this is that it doesn't allow it to precisely place these connectors so for example these parts um are made so they would fit

**7:56** · together you know on four sides at identically so that all these mating connectors on this side on this other side would just be interchangeable essentially and proze it does not quite give you the control for that for simple stuff this is perfectly adequate but if you want to do more precise stuff um just like we saw with the butt connectors a second ago uh you're going to have to do it in CAD over here in Fusion it starts with the same step we split our part I created a plane that uh

**8:27** · fits perfectly between these two and there we go we have two separate bodies to create the mating part the key essentially um I'm not going to show you how to do pins that would be pretty simple you just draw your PIN here I'm going to show you how to create a key basically you just select your cut surface um you create a new sketch on here let's make sure we actually draw on this and we're first going to project this cut surface this might also be hidden in the menu we project this surface so we have it as geometry in the sketch and then we can create an offset

**8:59** · for this and we're just going to go in here like that so we get two separate key pieces and that's going to be our shape for the two keys now with this I can straight go in and say extrude we're going to create a new body and this is going to switch over in a second we say symmetric we go I don't know 5 mm new

**9:21** · body and we're actually going to add a bit of a negative taper angle to this so that's just going to make sure that we get a bit of Tolerance once we fit these two parts together so new body hit okay and now we have the keys on our parts this is a separate body now to get the

**9:38** · matching slot um either you could subtract those keys with a Boolean from this main object but that is going to give you a zero tolerance fit and probably that's not going to go together uh you could tweak it with offsets and stuff but what you can also do is you can just reuse that same sketch and you

**9:55** · just cut into your part without a taper uh um and actually we're going to make sure to do symmetric and we're also going to cut the other side of this body this one um so we get the matching slots in both sides so now both of these parts have the the cut outs essentially for

**10:15** · our keys and that is a pretty cool way to create these keyed Parts um while also maintaining printability so you could just place this Parts down onto this surface right here it is still a closed perimeter and this surface in here that we inser is just going to be a straight bridge if we print it like that so very easy to print still and you get a key that you know gives you a lot of strength and very good alignment in the end next up Dove tails and these really

**10:42** · are a great alignment help with parts that need to fit together pretty well but don't need like screws or pins to line them perfectly if you can slide these together like this then this is going to be a pretty good solution and they are very easy to generate in prer slicer now these I did glue together so they are pretty permanently bonded with some construction adhesive let me see if I can get these apart

**11:06** · actually there we go there's one of them yeah this one I don't think is coming apart but we have one here so the duve tail for the most part is an alignment help but it also does add some mechanical strength because you are keying these parts together these have some adhesive on them so they don't fit perfectly well but there we go there is the part um you can just you know hang him off of the side it does add a good bit of strength because your parts are now keyed together essentially of course

**11:36** · if you are splitting up your parts to make them printable on a smaller machine you do lose the ability to print them like that on the cut surface because one of the sides protrudes the other side I guess you could print with the cut side facing down but of course you do still have a rather large bridge that now needs spanning but it would still work as a printable option now I'm going to show you how to do these Dove tails and prer slicer but if you take it to something like Fusion you can use any sort of joint and in fact any sort of Wood joint would work even the the super complicated Japanese joinery will work

**12:08** · on 3D prints and there are plenty of videos showing you that just for novelty but you can basically cut anything into these parts and use them for strength as well all right let me show you how these are done starting a prer again all we have to do is to select our cut tool and switch it from planer to doveet tail and

**12:26** · this you know we're going to see it a bit better once we position this um basically works the exact same as the other cut tool but you can see our cutout is going to be that Dov tail now you do get a bunch of adjustment options um the tolerance for the depth and width uh 0.1 did work pretty well for me but you can go a bit closer if you want a better fit and also you can adjust the

**12:47** · groove angle to add a bit of taper which is what I did with my parts the shallower that taper angle is the more the parts are going to jam together um and you know the The Wider it's going to be the EAS easier it will be to assemble by the way if you want this to be wider and you've already maxed out the width on the setting here you can also just lower your cut geometry and it is going to make it wider as well so same as before um basically you position your cut uh you hit perform cut and that's it

**13:17** · there's our let me just select this one there's our cut part with the dove Tails cut into it and if you want to do a very similar duve tail infusion it's actually rather simple so we have our whole part again starting with that um all we need is a planer surface thankfully I've already planned for this and this is the surface that's going to stick to the bed that is nice and flat we create a sketch on that and I'm just going to do a very quick and dirty Dove tail here doesn't actually need to be perfect and that's good enough so now we

**13:45** · can do an extrude and you got to make sure that you switch it from the extrude to the thin extrude feature U because that allows you to select this line here and all we have to do is push it through the part come on there we go um now what the thin extrude feature allows us to do is to say well we want to cut through it and it allows us to say how much we want to cut away so if you want that same tolerance of 0.1 mm um now we get a 0.1

**14:12** · mm slot cut through our part you can also add a taper angle um just like in PR let's do minus5 and you can see that tapers nicely together and that's going to jam the parts together hit okay and there we go now we have two bodies that are nicely cut away from each other and with A.1 mm tolerance they're going to fit together very very nicely and lastly

**14:36** · screws so of course you're going to need a through hole side that you just poke your screws through and a threaded side in one other part and basically you just pop them through you screw them

**14:53** · together and there you go that is a very solid well aligned connection so of course from an engineering standpoint screws are not meant to be Precision Alignment features because the screw itself is not a Precision part it really is just meant to pull two parts together but honestly in the context of 3D printing screws are plenty good enough for aligning two parts together especially considering you know you have some tolerance with the parts themselves as well and if you choose a screw size that is large enough like this is M8 um you can actually directly tap into your

**15:26** · 3D printed parts and that is going to make for a very very strong fit stronger in most cases than the rest of the part itself so this is cool because you can just tap your part or print the threads directly that works with these sizes as well it's an assembly method that is very easy to take apart you just unscrew the screw and that's it unless you've glued it um and it also doesn't add any protrusions that would interfere with the part fitting onto your print surface so this is a mating option that for now

**15:54** · you can really only do in cat though thinking about it you could use the same methods in a slicer but yeah let me show you how these mates are done in Fusion 360 so these two parts that we just looked at already have some screw connectors in the back here and that's actually what I used for mating these parts worked perfectly Fusion does have

**16:12** · a ho tool and you know it does give you something like a counter Bo hole you can also make them threaded or tapped but this tool simply you know it doesn't quite give you the flexibility to create a through hole um which is what we have on this part right here and a tapped

**16:29** · side at the same time you can only really cut one part and if you want to do multiple it it gets pretty tedious so let me show you an alternative way um that you can customize pretty well and that makes doing multiple threaded holes like this very very simple so I'm just creating myself a offset plane here exactly where our screw connection is going to run through I'm going to start a new sketch on this plane and then I'm

**16:53** · just going to sketch out the first screw that I want so we're going to do some clearance up top and the threaded portion in the bottom so I've just dimensioned this in a way that the head of the screw nicely sinks into the top part and that the bottom part that we actually want to thread into has an 8 mm hole um that's

**17:15** · because I'm actually going to model threads in a second here but if you wanted to tap threads into your part of course you would need to make this a bit smaller for M8 that would be a 6.8 mm hole again since we're actually going to print the threads this is going to be 8 mm and and you're going to see why in a second um for now though all we're going to do is we're going to revolve this and create our basically uh cutout shape for

**17:38** · this screw there we go with this cutout shape done I do want to add the threads um this is what we're going to cut out of the actual part and we're going to check modeled here in the threading tool this is going to be a bit too tight for that you just grab the modify and scale tool you select a part select non-uniform and what is this this is z

**18:01** · and y and you just add I don't know 5% to the scale and that is going to give you a much better clearance on the threads and because we have cut a male thread into our tool that we're cutting out of the part we've essentially created a zero tolerance or zero clearance fit which of course is not going to work and with that scale it just has a bit of clearance in there since we do want about five screws here um I'm just going to do a linear pattern I'm going to do this along this X is right here like so and we're going to do five

**18:33** · and now we just need to use our newly created screw forms to cut out um holes from each of the halves for the first one you have to do keep tools so you can reuse them for the second cut operation but since we modeled it exactly onto our parting line uh you can see we get the clearance hole into our top part and

**18:54** · then the thread starts at the bottom so keep tools and then we do another cut and there we go there's our threaded printable hole and the matching clearance hole on the top side and if we hide one of these you can see the thread just extends into the bottom part and the clearance hole just extends into the top so that's how I like to do threads directly printing the threads works at about uh an M6 or a/4 in 20 um anything

**19:22** · smaller than that your printer is not going to reproduce so for that you will need to create basically a tab size hole but make sure to give yourself plenty of wall thickness so don't make that hole too small or otherwise your TAP will simply cut through all your perimeters and you'll be left with just info which obviously isn't going to be particularly strong um but for larger sizes this works well um for an M8 I maybe wouldn't use a 6.8 mm hole which is the regular tapping size and maybe would use a

**19:50** · 7.5 because that is still going to be plenty strong um in plastic there we have it four different mating options for your parts I hope there was one in there that was right for your project or at least inspired you to you know come up with your own mating solutions that you can draw up in cat or even Implement in your slicer so hope you learned something if you did make sure to give this video a like And subscribe uh you can support the channel through Patron by the way thank you to all the patrons who are supporting me right now you can be one of them if you want to um yeah

**20:21** · thank you for watching keep on making and I'll see you in the next one bye