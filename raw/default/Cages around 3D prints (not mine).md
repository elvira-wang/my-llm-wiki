---
title: "Cages around 3D prints (not mine)"
source: "https://www.reddit.com/r/resinprinting/comments/1pb9r1c/cages_around_3d_prints_not_mine/"
author:
  - "[[FelixxCatus]]"
published: 2025-12-01
created: 2026-07-15
description: "https://x.com/fzr_araken/status/1995387490572861680 Has anyone seen anything like this before? I came across this on twitter, fro"
tags:
  - "clippings"
---
[https://x.com/fzr\_araken/status/1995387490572861680](https://x.com/fzr_araken/status/1995387490572861680)

Has anyone seen anything like this before? I came across this on twitter, from what I understand he's putting those cages to prevent inconsistent layers from sudden cross area changes?

Seems like a lot of wasted resin, but his prints are looking good

![r/resinprinting - Cages around 3D prints (not mine)](https://preview.redd.it/cages-around-3d-prints-not-mine-v0-9gns807bok4g1.jpeg?width=1080&crop=smart&auto=webp&s=e903bc33e24241a01704a9add2381913e29a6cb9)

---

## Comments

> **Saigh\_Anam** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nroy1gu/) · 76 points
> 
> From the links, it appears the theory is to provide anchor points for the initial peeling stress of the FEP. Each corner of the cage bears the brunt of the initial lift rather than small corners of the print.
> 
> I can't say I buy into the theory, but if it works for them...
> 
> Personally, I just try to avoid printing in the middle of the FEP until I've filled up the corners first. That may be the same in practice.
> 
> > **Nepu-Tech** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrpd7nt/) · 16 points
> > 
> > This doesn't make sense to me, there's no need for the cage to take the force of the peeling FEP because the Island where the supports rest already do the same thing. Or am I missing something? I have never had any problems completely filling out the FEP.
> > 
> > > **OwnZookeepergame6413** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrpxwrd/) · 9 points
> > > 
> > > When your print peels from the fep it is pulled on. Especially small details can get deformed by that. If you add a cage you slightly increase the pulling force required but the area the force is applied to is a lot bigger (as big as the cage compared to just the models surface on that layer). So the force applied to the model itself will be lower. I can’t tell you how much this changes in practice, but from the physics standpoint it makes sense. Personally I think they add this cage to compensate for all kind of printers people may have. This probably helps all printers that have aged a bit now, badly adjusted fep tension etc. so overall with the cages those sellers have less people complain about failed prints. For a modern and well maintained printer the difference is probably pretty small
> > > 
> > > > **Mindbulletz** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrs2dgb/) · 4 points
> > > > 
> > > > Sorry but as an engineer that physics just doesn't add up. The area of the contact patch of the desired part doesn't change, so the total force on the desired part can't change appreciably. All it does is increase force on the film, and change the time profile of the force applied by the lift. If it does anything, it increases the force spike at the beginning of the release, smooths out layer inconsistency caused by pressure changing from drastic total contact patch area changes, and probably most importantly cleans up any failed bits from the print.
> > > > 
> > > > > **DarrenRoskow** · [2025-12-02](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrszzcn/) · 6 points
> > > > > 
> > > > > The release film stretches and comes up with the part. The exterior posts slow the time where the release propagates to the part, increasing the time and angle and thus an easier release than when the film is dead flat. Release force is also much lower once the release film has some air under it. Like explosions in a car engine, you have to slow it down in your head to see what is happening.
> > > > > 
> > > > > There is also a trick of putting painter's masking tape at the edge of the LCD screen to make air admittance under the release film a lot easier. On the printer I have force sensor data this was good for a roughly 25% reduction in release force with identical prints + resin conditions. This had great results as far as reducing support failures with sketchier supports.
> > > > > 
> > > > > Adding spacers to the resin vat was worth another 10-20% but had the drawback of letting air get trapped under the film. This can result in some small layer lines, so the easier you make it to get air under the release film, the longer you have to set a rest after retract / wait time before cure so all the air bubbles are gone.
> > > > > 
> > > > > Engineering trigonometry is hard...
> > > > > 
> > > > > > **Mindbulletz** · [2025-12-02](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nru3dq3/) · \-1 points
> > > > > > 
> > > > > > > the area the force is applied to is a lot bigger (as big as the cage compared to just the models surface on that layer). So the force applied to the model itself will be lower
> > > > > > 
> > > > > > This doesn't add up as an explanation. The area where the force is applied between the film and cured resin is not magically bigger than the contact patch that quite literally defines it, no matter how you cut it up and space it out.
> > > > > > 
> > > > > > The one good point you brought up is with the squeeze film effect acting on both sides of the film and how it changes the time profile of the force in a different way than I hypothesized. I am willing to believe that you are seeing lower *peak* force on your load cell. However, I am not convinced that the time integral of that force is lower.
> > > > > > 
> > > > > > Lastly, I already accounted for the film flex over time and angles involved, so I have no idea why you're being a condescending twat. No need to mince words, please instead fuck off if you're going to continue the discussion like that.
> > > > > > 
> > > > > > > **DarrenRoskow** · [2025-12-02](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrued4u/) · 4 points
> > > > > > > 
> > > > > > > The whole "As an engineer..." thing is what earned you the condescension and assuming other people can't do integrals and calculus will get you a lot more.
> > > > > > > 
> > > > > > > Nice of you to quote someone else's statement I had nothing to do with. I was merely correcting your misunderstanding -- especially because "as an engineer" you were hoping people would find credit in your shortsighted opinion.
> > > > > > > 
> > > > > > > The area under the curve is much lower with various release aids like tape, I have a pretty good number of graphs of all 1000+ release events and granular CSV logs.
> > > > > > > 
> > > > > > > More importantly though, peak force matters for plastic deformation and yield of supports. It's common enough for poorly supported models to print successfully but bear the marks of plastic deformation where the supports attach. More delicate details on parts benefit from undergoing less strain while being formed in the case of resin printing.
> > > > > > > 
> > > > > > > Lifting the edge of the release film with rough masking tape works because the release film locks with suction against the LCD glass otherwise. When the models lift up, they have to break that lock. If it is easier to air to rush in with an established path for air. Same reason vat spacers work, they place the perimeter of the release film in tension upwards so breaking the lock is easier.
> > > > > > > 
> > > > > > > In the case of a protective cage or other structure around the perimeter, they help lift the release film and break the lock and allow air to more easily flow in. Mechanically, they act as a break where the peel force on the model in the middle is delayed.
> > > > > > > 
> > > > > > > You can actually see this effect in print failures. It is common for objects to fail in the middle of an overcrowded build plate. This failure mode is exactly the perimeter objects relieving the middle ones of release force sufficiently that they never end up letting go of the film.
> > > > > > > 
> > > > > > > As for the angles, the greater the angle of the film to the surface of the model, less force is needed to propagate a peel. Similar concept as to why tilt release printers put much less stress on prints than straight lift release.
> > > > > > > 
> > > > > > > > **wentzr1976** · [2025-12-02](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nruop2e/) · 2 points
> > > > > > > > 
> > > > > > > > Personally i appreciate when someone cites their background in context of their questioning a line of thought that might require more expertise to understand ….
> > > > > > > > 
> > > > > > > > Shouldnt need to get weird when a theory or explanation is challenged. Thats how people learn and grow. Even the smartest most experienced people 😉
> > > > > > > > 
> > > > > > > > Its too bad this cant be explained without the insecurity. Most folks into 3d printing are hobbyists. It is perfectly legit and reasonable for someone to give their background when challenging a concept someone else is trying to explain.
> > > > > > > > 
> > > > > > > > Context on your audience is typically thought of as useful to those explaining a topic so it can be described and discussed in terms mutually understood.
> > > > > > > > 
> > > > > > > > **Mindbulletz** · [2025-12-02](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nruv09b/) · \-2 points
> > > > > > > > 
> > > > > > > > You decided I meant something I didn't mean. You seem to have decided I said I was the smartest person in the room. I did not. I said I know a particular thing for context, and I said nothing at all about what anybody else knows except for the person I originally responded to. I quoted their statement because challenging their incomplete explanation was the only reason I commented in the first place. You seem to have taken my comment out of context, additionally misread what I said to them, and used it to ragebait yourself.
> > > > > > > > 
> > > > > > > > If you presented your data without all the bullshit, everyone including myself would've gladly learned something from it.
> > > > > > > > 
> > > > > > > > Instead, your behavior says you decided it was your duty to "teach somebody a lesson." We've learned that you're not someone worth engaging with, and we've learned nothing else.
> 
> > **IsenMike** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrqb3co/) · 6 points
> > 
> > Makes some sense for the corners. That the corners end up connecting with a canopy, after the print is done, doesn't seem quite as useful though. Seems more like a waste of resin and print-time.
> > 
> > I have seen some small-run model kit producers pack and ship their printed parts fully washed-and-cured still connected to their supports, leaving all support removal and clean-up to the model-maker. I suspect that these "cages" may be created with that in mind, and may have more to do with protecting fragile parts from shipping damage rather than any quality benefit the cages might provide during printing.
> > 
> > **foltranm** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrp8h15/) · 2 points
> > 
> > that makes a lot of sense as well. I think it might be a bit of both purposes - both that and reducing the proportional variations in cross-section area by adding a bit more constant area. sounds like a good idea, i wonder if that's something that is easily added in any slicer
> > 
> > **DrStalker** · [2025-12-02](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrue6fd/) · 1 points
> > 
> > why extend the cage beyond the print in that case? You don't need a fancy roof, you just need four pillars that end just after the piece they are protecting.
> > 
> > This would make a lot more sense if it was to protect parts during shipping.
> > 
> > **TheSheDM** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrsmcxg/) · 1 points
> > 
> > Why is it so high above the model, and why waste resin to complete the arch after the model is done printing? Once the corners release, wouldn't there still be more or less the same strain on the rest of the print? I can't imagine the difference being substantial enough to use that much resin, and why not just do some sacrificial corner columns instead of a whole tent? That raft is massive anyways, if there's any success improvement its probably more from that than the tent.
> > 
> > The only thing I see the tent/dome/cage thing doing is catch failures instead of leaving them on the FEP. [I've used failure-catching roofs](https://www.myminifactory.com/object/3d-print-safety-roof-135003) before when I printed a bunch of these fiddly basing bits.

> **\--0\_\_\_0---** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrp2h0d/) · 21 points
> 
> Saw another person doing similar but the reason was so they could ship the prints directly to customers and they would be safer and less likely to print. They also had absolutely tiny supports so removal would be a piece of cake even if fully cured.
> 
> > Seems like a lot of wasted resin, but his prints are looking good
> 
> Its only a couple of cent of resin getting wasted, if it prevents failures dramatically I would say its well worth the wastage.
> 
> > **Nepu-Tech** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrpdlbv/) · 3 points
> > 
> > This makes sense to me, plus the wasted resin is offset by not having to do any clean up or support removal and leaving it to the costumers. I rather receive cleaned parts without supports though. The Gundam resin kits all have the parts in separate plastic pouches and protected by the packaging, but I guess these cages are the lazy way of just print and ship without a care.

> **Background-Elk-543** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrowxwb/) · 34 points
> 
> Maybe it protects the smaller prints during the washing process if multiple are being washed simultaneously, but other than that, it's a resin waste and a time waste because the cage is higher.
> 
> > **CosmicJackalop** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrp0hdq/) · 14 points
> > 
> > Actually it's apparently to protect fragile pieces from the FEP because the most force will be on the basket/cage piece instead of the desired print
> > 
> > It supposedly increases print reliability with delicate details
> > 
> > > **Neknoh** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrphwen/) · 7 points
> > > 
> > > I can see that, it makes sense to a layman. I don't know if it has any real basis.
> > > 
> > > Another benefit is that the cage also has a chance to catch any misprints and clean the FEP once it "closes"
> > > 
> > > > **Sansred** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrpvymo/) · 3 points
> > > > 
> > > > While I can't speak to the other reasons, this one does *sound* like a good idea.
> > > > 
> > > > **undeadmeats** · [2025-12-02](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrswf7q/) · 2 points
> > > > 
> > > > This is why I sometimes model my sprues with cages, but for most things it's not enough of a difference to bother
> > > > 
> > > > **HeKis4** · [2025-12-02](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrvctr0/) · 1 points
> > > > 
> > > > Idk, all parts of the print don't rip at the same exact time and at the same forces... If the pillars rip first, you have all the force applied to the print as if the pillars weren't there (since, well, they *aren't* there anymore), it will even go from 0 force to near-ripping force instantly. I don't see how the print would rip first since it is enclosed between pillars that are closer to the edge where most of the force is applied. Maybe I can see that working on flexible resins so that it deforms less before ripping ? Not for standard resin tho.
> > > > 
> > > > And in theory cleaning the FEP is done by the raft, there's no point in cleaning it after the print if it gets cleaned before.
> > > > 
> > > > To protect prints during handling/shipping though ? Amazing idea.
> > > > 
> > > > > **Neknoh** · [2025-12-02](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrvlh4k/) · 1 points
> > > > > 
> > > > > Yes and no
> > > > > 
> > > > > The print doesn't have to do the pulling of the FEP for as long of a time.
> > > > > 
> > > > > It becomes more of a bandaid-rip.
> 
> > **Neko\_3DPrintArt** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrox74h/) · 0 points
> > 
> > Probably the right answer

> **Cypher\_Aod** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrowcri/) · 7 points
> 
> Fascinating, I'd love to know more too
> 
> > **FelixxCatus** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrowmpo/) · 7 points
> > 
> > I scrolled a bit on his twitter and he retweeted that from someone else, it seems to be an explanation of why it would help
> > 
> > [https://x.com/STALIN3EXE/status/1995368709851074605](https://x.com/STALIN3EXE/status/1995368709851074605)
> > 
> > > **Cypher\_Aod** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrox7xw/) · 1 points
> > > 
> > > Cheers!
> > > 
> > > **Chirimorin** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrpzc01/) · 1 points
> > > 
> > > But once it peels from the cage, doesn't it just pull on the model anyway?
> > > 
> > > [https://i.imgur.com/CWFMBWj.png](https://i.imgur.com/CWFMBWj.png)

> **SecretAsianFlan** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrozr4y/) · 6 points
> 
> That’s a setting in blueprint slicer it’s called rafts with casing.
> 
> > **FelixxCatus** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrpi2vr/) · 2 points
> > 
> > Naming the software "Blueprint" is a terrible decision, it makes search engines useless
> > 
> > > **HorrorInternal640** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrq5v7n/) · 4 points
> > > 
> > > It’s “Blueprint” from HeyGears. The automatic supports generated by it are great. I use it for all my minis and never had a failure while using it
> > > 
> > > > **SecretAsianFlan** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrrnb0h/) · 2 points
> > > > 
> > > > Agreed! and yes I’m surprised blueprint slicer didn’t bring up.
> > > > 
> > > > **TheSkinnyD** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrskdyv/) · 1 points
> > > > 
> > > > Do you just do the supports in Blueprint, then slice elsewhere? Or does Blueprint support a wider range of printers than what comes installed by default?
> > > > 
> > > > > **HorrorInternal640** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrso636/) · 2 points
> > > > > 
> > > > > I just use it for supports, then export the stl and use it in lychee.
> > > > > 
> > > > > To be honest I never tried to slice a file on blueprint. I doubt you can use anything other than heygear machines. You have to select the heygears printer, resin and layer height before it lets you import stls.
> > > > > 
> > > > > One cool thing you can do is exporting your newly supported stls as either, one big stl or multiple individual stls
> > > > > 
> > > > > > **TheSkinnyD** · [2025-12-02](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrst4q1/) · 1 points
> > > > > > 
> > > > > > Oh, nice! Always looking for better auto supports, and I already use lychee, so I’ll see about adopting it into the workflow. Thanks for the reply!
> > 
> > > **agathorn** · [2025-12-07](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nstf32t/) · 1 points
> > > 
> > > I use a Git client called Git Fork which is equally useless haha
> 
> > **xtopherpaul** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrpfj3l/) · 1 points
> > 
> > Those don’t look like blueprint supports. They’re usually a scaffold with multiple individual tips

> **MattRubin** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrr002r/) · 3 points
> 
> When I’ve bought resin bits for my aircraft modeling it often has these, I think it also helps protect it in shipping in that sense

> **TheRealMinibyte** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrp8dmq/) · 5 points
> 
> Honestly if it makes a resin printer behave it works, I have mini figurines I 'gift' my printer so it'll work. Don't judge me, mates that work in labs SWEAR by this trick, each machine has a 'favorite' plush/mini fig that it'll only behave when presented with. Like the duck and programming theory xD
> 
> > **Nepu-Tech** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrpe82j/) · 2 points
> > 
> > You should also pray to the Omnisiah and perform all the holy rites before starting your printers for the best results.
> > 
> > > **astrodude1789** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrq5x0s/) · 1 points
> > > 
> > > A little bit of electrical smoke as incense will create an ambience. 
> > > 
> > > **SnooGuavas2166** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrq62jb/) · 1 points
> > > 
> > > And present to it a finger, for the flesh is weak and must be replaced

> **Krytan** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrps626/) · 2 points
> 
> I've actually seen the same cages around resin pieces elsewhere. However, I assumed this was mostly to protect the pieces in packaging/shipping so they don't get knocked loose, or bent or warped. This was for models sent unassembled, some sort of resin/plastic hybrid kid.

> **folklish\_** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrrnfbe/) · 2 points
> 
> From what i know (might be wrong) those are present on comercial prints like model kits and such theyre more to protect the print in transport than during printing

> **SGTBookWorm** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrpcz96/) · 1 points
> 
> Ayy Lycoris Recoil 👀

> **baisaacs** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrqfdwr/) · 1 points
> 
> seems kinda silly for parts that big. i print 1:160 scale parts and they dont need any special cover to protect from peeling forces.

> **AbaloneEmbarrassed68** · [2025-12-03](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/ns5r8pb/) · 1 points
> 
> Seems like a cool idea to send them for shipping. Pack em in foam and they already have a cage. Lol

> **B-A-R-F-S-C-A-R-F** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrp6f7x/) · 0 points
> 
> interesting, so reading the other comments, this might be more for washing (?)
> 
> I still think your idea is interesting though.. what If thw slicersoftware would build sacrificial geometry so the surface area for each layer is similar. that could really help with consistency., even prevent failures.
> 
> > **Nepu-Tech** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrpdzas/) · 2 points
> > 
> > I wouldn't clean the cages, that would be a lot of wasted alcohol. I always remove all supports first and even do a quick pre-cleaning spray before dropping the prints in the vat. I think like another poster said the cages could be used to ship the items without having to remove supports, but then you would have to clean them.
> > 
> > > **B-A-R-F-S-C-A-R-F** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrqpw9i/) · 1 points
> > > 
> > > Was this comment ment for me? Im not talking about cleaning anything. Im talking about the potential idea to have the slicersoftware generate sacrificial geometry, (a bit like a primetower in fdm printing) so that every layer has the same surfacearea, minimizing suction variety across layers. and potentially even preventing failures.

> **\-Mechtech-** · [2025-12-01](https://reddit.com/r/resinprinting/comments/1pb9r1c/comment/nrpmnil/) · 0 points
> 
> I can see where they're thinking, but I find it unnecessary as it increases FEP wear. When printing, to reduce the pull on the FEP, you want to reduce the surface area not increase it. Using the cage just increases the FEP wear and resin usage. By the looks of the base of the cage they're putting too much surface area on the FEP then a normal island does.
> 
> I can't say I share their philosophy, as I have not encountered any problems printing normally.
> 
> I do see that a couple of their 'caged' objects have poor orientation and may have too much surface area against the FEP.