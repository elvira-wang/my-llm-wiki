---
title: "Questions about printing and issues with suction"
source: "https://www.reddit.com/r/resinprinting/comments/1vatw4x/questions_about_printing_and_issues_with_suction/"
author:
  - "[[Anzio_tankette]]"
published: 2026-07-30
created: 2026-08-03
description: "So I've been printing for a few days now with a Saturn 4 ultra using abs like resin 3.0 and when I print smaller / thinner models I have no"
tags:
  - "reddit"
---
So I've been printing for a few days now with a Saturn 4 ultra using abs like resin 3.0 and when I print smaller / thinner models I have no issues the majority of the time but I'm having issues printing larger things, the very first large thing I printed came out perfectly but everything else I print just have issues, primarily suction, I always print the larger pieces hollow with many large drill holes and no matter what thickness of wall (1mm, 2mm or 3mm) and no matter support placement and type and orientation (30°-60° degree) and temperature range is 30°c-40°c (can't seem to control the temperature) I keep getting suction even at the initial support layer and I'm wondering how I can resolve the issue. I also use chitubox for a slicer as well so if there are any changes I need to make to my print in the slicer I use that.

Another question as well with a few of the failed prints the damage is minimal overall so how would you recommend repairing them after sanding without printing the entire thing from scratch.

Would lubricating the FEP help with suction? If so would a mold release spray work?

---

## Comments

> **charmio68** · [2026-07-30](https://reddit.com/r/resinprinting/comments/1vatw4x/comment/p0os3h5/) · 3 points
> 
> Do not lubricate the FEP, you'll just contaminate your resin with no benifit past the first couple layers (I haven't tried, but that's my belief).  
> If you want to tinker with the "FEP" then remember you can get different types: standard FEP, nFEP (PFA), and ACF.  
> Especially for larger parts you want to change to ACF. It's more fragile, but it makes a massive difference to suction force.
> 
> Your current print really should be printed directly on the build plate without supports (grab a magnetic build plate sticker if you're doing this often to make it easier to remove the parts without damage).
> 
> As for the sound, it sounds completely normal.
> 
> The problem you're coming up against is that EVERY part you print with SLA will come out slightly deformed in some way. There is skill in minimizing it involving part orientation, placement on the build plate (remembering that other parts on the build plate will interact with each other even at a distance), printer tuning, support settings, minimizing suction, resin selection, temperature, etc...
> 
> To be frank I'd need to write a book to explain it all, there's far too much to it to condense into a reddit post.  
> However, one thing I think will help is keeping in mind that auto generated supports don't completely support the part sufficiently, you still need to manually go in and tweak it (and I don't care what slicer you're using, so far none get it perfect). That looks like your main issue.  
> Your supports also look like they might be a bit on the slim side, although I can't get a good grasp on the scale of that part, so maybe not.
> 
> The printer's also moving quite fast. If you slow everything down you'll get more accurate parts, though at the obvious cost of it taking longer.
> 
> > **Anzio\_tankette** · [2026-07-30](https://reddit.com/r/resinprinting/comments/1vatw4x/comment/p0piayg/) · 1 points
> > 
> > This is helpful thank you, I'll definitely need to look into a few of these thing but I'll definitely try to slow down the lift speed.
> > 
> > As for the supports I am using a medium in general with heavy on the very bottom initial islands, not sure about the thickness but I want to say the medium is 0.8mm-1mm and the heavy is about 1mm-1.2mm
> > 
> > **Anzio\_tankette** · [2026-07-30](https://reddit.com/r/resinprinting/comments/1vatw4x/comment/p0piup4/) · 1 points
> > 
> > Also just based on your experience would you say that slowing the lift speed will decrease the noise, got my printer set up in the attic and would want it running through the night for the longer prints but at the moment it sounds like a slow hammering noise from the room beneath it
> > 
> > > **charmio68** · [2026-07-30](https://reddit.com/r/resinprinting/comments/1vatw4x/comment/p0qbvhc/) · 1 points
> > > 
> > > 😂 might do slightly, but not by much. However fortunately i do have a solution. Again, it comes down to the type of film you choose. When I swapped to ACF the first thing I noticed was there was absolutely zero peeling noise anymore.  
> > > I even paused the print because I was convinced the part had failed with how quiet it was (I did actually later find out I had the ACF film upside down which made it even quieter than usual for some reason 😅, but even when installed the correct way up it's done narn near silent. ).
> > > 
> > > Although... I've actually just noticed you've got a Saturn 4 ultra with the tilting vat. I'm yet to use one of those so can't say if it will have the exact same effect, but I think so.  
> > > I believe the recommendation for tilting vats is generally to stick with PFA, though if sound is a higher priority for you, then I would try ACF.  
> > > Another thing that potentially changes about my recommendation is I believe the Saturn 4 Ultra doesn't allow you to change the speed at which the vat tilts? Given that the vat tilting is what detaches the print, I'm not sure you'll get as much benefit out of lowering the lift speed as you would with a regular non-tilting printer. It should still help, but maybe not as much? I can't really say as I don't have any experience with tilting vats, but it would seem to make sense.

> **Anzio\_tankette** · [2026-07-30](https://reddit.com/r/resinprinting/comments/1vatw4x/comment/p0o39a5/) · 1 points
> 
> How it sounds and moves as well when pulling up
> 
> ![media poster](https://preview.redd.it/dmbe0gzgedgh1.jpg?vthumb=1&s=cf9d50b119e3f61158dfeb61bfcf09b7676ceaa3)
> 
> > **AdamLikesBeer** · [2026-07-30](https://reddit.com/r/resinprinting/comments/1vatw4x/comment/p0obx3d/) · 1 points
> > 
> > Sounds like mine.
> > 
> > I would drain and check your FEP if it was me.
> > 
> > > **Anzio\_tankette** · [2026-07-30](https://reddit.com/r/resinprinting/comments/1vatw4x/comment/p0okeam/) · 1 points
> > > 
> > > I have done this 3 time and it does look fine though it would definitely try buying more replacements as a precaution after payday

> **c008644** · [2026-07-30](https://reddit.com/r/resinprinting/comments/1vatw4x/comment/p0o7b3o/) · 1 points
> 
> I dont see your lift speed or distance (maybe you included it, but i just cant see it) if its at default, try lowering it to say 65 100. You also really dont need to angle your print all that much, the idea is to get as little surface area on the build plate as possible (angle the print maybe 15 degrees off from stantihg verticle). You can also try a wait after cure of 1 second to try letting the liqued resin escape. Sure it will take longer to print, but its better than ripping you pfa sheet (and watching your print fail)
> 
> > **Anzio\_tankette** · [2026-07-30](https://reddit.com/r/resinprinting/comments/1vatw4x/comment/p0obmrq/) · 1 points
> > 
> > Would have to double check after work but I think chitubox may not have the option to change lift speed
> > 
> > > **c008644** · [2026-07-30](https://reddit.com/r/resinprinting/comments/1vatw4x/comment/p0orx3o/) · 1 points
> > > 
> > > Chitubox does, its just harder to find all the settings. its under the print tab. For my large prints, I use a lift speed of 40 mm > 60 mm yes its very slow, and I could probably move it higher, but I have not had a failure since using that speed.
> > > 
> > > > **Anzio\_tankette** · [2026-07-30](https://reddit.com/r/resinprinting/comments/1vatw4x/comment/p0pfpz0/) · 1 points
> > > > 
> > > > Alright then, I'll try it out, don't particularly mind the print speed just so long as it does cause any warping
> > > > 
> > > > > **Lito\_** · [2026-07-30](https://reddit.com/r/resinprinting/comments/1vatw4x/comment/p0rgb8o/) · 1 points
> > > > > 
> > > > > Ignore that person, your printer doesn't have lift speed or distance because it has a tilting vat. They would know if they read your post.

> **Sloiter** · [2026-07-30](https://reddit.com/r/resinprinting/comments/1vatw4x/comment/p0o9hqr/) · 1 points
> 
> This may be an unpopular opinion but can you try printing it without supports and just have the base flat on the plate?
> 
> > **AdamLikesBeer** · [2026-07-30](https://reddit.com/r/resinprinting/comments/1vatw4x/comment/p0oc813/) · 1 points
> > 
> > Yeah I agree, that certainly isn't the angle I would choose but c'est la vie
> > 
> > **Anzio\_tankette** · [2026-07-30](https://reddit.com/r/resinprinting/comments/1vatw4x/comment/p0ok6uo/) · 1 points
> > 
> > I have tried this, though with supports on a far thinner piece as a first print and it didn't go well, it's just too much suction due to a large surface area and caused it to crack and warp during print, plus without supports and raft removing it from the base plate would be a pain and could cause damage due to there being no thin flexible piece to allow the print to be removed easily