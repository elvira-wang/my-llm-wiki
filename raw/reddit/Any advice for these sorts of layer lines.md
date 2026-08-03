---
title: "Any advice for these sorts of layer lines?"
source: "https://www.reddit.com/r/ElegooMars/comments/1ux5c0j/any_advice_for_these_sorts_of_layer_lines/"
author:
  - "[[TheRummyBum]]"
published: 2026-07-15
created: 2026-08-03
description: "I’m just getting back into printing with my mars 2 pro after not touching it for 4 years so I’ve got a lot to learn again. I’m pr"
tags:
  - "reddit"
---
I’m just getting back into printing with my mars 2 pro after not touching it for 4 years so I’ve got a lot to learn again.

I’m printing at 0.03mm with elegoo grey abs-like 3.0 and am pretty happy with the results overall. I’ve just been getting some noticeable stepping in certain areas, flat faces like the gun, certain flat plates, and some rounded areas like on the cape.

I’ve tried looking into anti-aliasing but keep coming up a bit short, whether I should use lychee or chitubox and what else I could do. I know the mars 2 pro has a pixel resolution of 0.05mm, are these lines an inevitability because of this or is there something I can do to mitigate them more?

Overall I’m pretty happy with the results but I really enjoy the painting part of the hobby and want to try and get my minis as good as I can

Thanks for any help

---

## Comments

> **AutoModerator** · [2026-07-15](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oxo9j8w/) · 1 points
> 
> Thank you for reaching out! Please ensure your post includes:
> 
> - **Printer model/variation** (e.g., Saturn 3, Mars 2 Pro)
> - **Resin type** (e.g., ABS Like, Tough Resin)
> - **Slicer information** (e.g., slicer used, settings tried)
> 
> Detailed information is crucial for us to assist you effectively. Posts with minimal details may be removed until updated.
> 
> **Safety Announcement:**  
> We have rules against harmful information. Going forward, posts with images of careless resin handling may be removed. Please ensure you're handling resin safely in any provided images.
> 
> *I am a bot, and this action was performed automatically. Please* [*contact the moderators of this subreddit*](https://www.reddit.com/message/compose/?to=/r/ElegooMars) *if you have any questions or concerns.*

> **Aszmodaj** · [2026-07-15](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oxodd1v/) · 5 points
> 
> How are you orienting models on build plate? By marks it looks like you put them flat to reduce print time
> 
> Sorry for bad english, I am little rusty with it
> 
> > **TheRummyBum** · [2026-07-15](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oxog21v/) · 1 points
> > 
> > ![评论图像](https://preview.redd.it/any-advice-for-these-sorts-of-layer-lines-v0-pse5vomjcedh1.png?width=1914&format=png&auto=webp&s=6a2e323398878821d380d392f39df7de5beec1f1)
> > 
> > These ones are pre-supported so I haven't been touching the orientation, they are oriented like this though
> > 
> > > **taggart65** · [2026-07-15](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oxpskaw/) · 3 points
> > > 
> > > Have you got unsupported files ?
> > > 
> > > If you have it might be worth printing at a 45 degree angle and adding auto supports , also anti aliasing is worth a go
> > > 
> > > > **TheRummyBum** · [2026-07-15](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oxsaflp/) · 2 points
> > > > 
> > > > Yeah i've got the unsupported files too, I can give that a shot

> **UKSTL** · [2026-07-15](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oxqr68x/) · 4 points
> 
> Antialiasing

> **stana32** · [2026-07-15](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oxosvrf/) · 3 points
> 
> Those are some pretty wicked layer lines, typically you would only see such obvious ones at the peaks of curved surfaces. Admittedly I am not familiar with the mars 2, so I am not sure if this is to be expected.

> **b005t3r** · [2026-07-16](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oxu24lc/) · 3 points
> 
> This is called stepping - visible layer lines that every printer produces. You won't be able to get rid of them, you can minimize them with better orientation of your prints.
> 
> You can also post-process your sliced files to make those lines completely invisible, but you'll need a printer that can print in shades of grey. Here's my script for that:
> 
> [https://github.com/b005t3r/UVtools-GaussianLayerMerger](https://github.com/b005t3r/UVtools-GaussianLayerMerger)
> 
> PS. People say AA will fix those, it won't, AA only affects vertical surfaces, your getting stepping on the more horizontal ones.

> **Sexy-Sparrow** · [2026-07-15](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oxopr5p/) · 5 points
> 
> You could try playing a bit with the antialiasing settings

> **Character\_Field\_9689** · [2026-07-16](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oxszb3o/) · 1 points
> 
> What film are you using?

> **thekinginyello** · [2026-07-16](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oxt3ybj/) · 1 points
> 
> If it was standing up in your supported image how did you get layer lines like in your printed photo? It would have to be laying down.
> 
> > **TheRummyBum** · [2026-07-16](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oxtrw1z/) · 1 points
> > 
> > I'm assuming it's stepping from the xy resolution, the mars 2 pro has 0.05mm pixels whereas my layer heights are 0.03mm, so the stepping will be comparatively more visible im guessing?
> > 
> > > **thekinginyello** · [2026-07-16](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oxv2wei/) · 1 points
> > > 
> > > That’s crazy. I had a mars2 as my first machine and I don’t recall ever seeing anything like that.
> > > 
> > > **D1s1nformat1on** · [2026-07-17](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oy17l73/) · 1 points
> > > 
> > > I don't know the mars 2, but if it's resolution only goes down to .05, then is it even capable of printing at 0.3?
> > > 
> > > I print at 0.3 on a mars 5 ultra and at 0.5 and this looks like the results I get at 0.5... 🤷
> > > 
> > > > **TheRummyBum** · [2026-07-17](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oy1nryq/) · 1 points
> > > > 
> > > > The .05 is the pixel resolution, the layer height won't be affected by this because it's a different dimension. With the settings im using, a single pixel on the mars 2 would produce a box that is 0.05mm wide, 0.05mm long, and 0.03mm tall, whereas your mars 5 ultra would do 0.018x0.018x.0.03
> > > > 
> > > > I can definitely see a difference between 0.03mm and 0.05mm layer heights haha
> > > > 
> > > > > **D1s1nformat1on** · [2026-07-18](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oy7tkzq/) · 1 points
> > > > > 
> > > > > That's part of what I'm saying though - the pictures you've shown *look* like the results I get what I (intentionally) print at .05mm layer height. Granted, we don't have a sense of scale in your pictures to figure out how close up you've taken them
> > > > > 
> > > > > I wasn't familiar with the mars 2 and what it's layer height options were.
> > > > > 
> > > > > Ultimately, these are Z-layer steps - aside from the way you orient the models, the x/y resolution being the cause isn't going to present as "stepped islands" like in your pictures, so I'm wondering if there's a disconnect between your setting of 0.03mm layer setting and (what looks like) a 0.05mm layer height outcome

> **wizardjian** · [2026-07-15](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oxoql6u/) · 1 points
> 
> Angling it would reduce some of the lines but I find it's very easy to remove them with a cheap nail dremel

> **thedisliked23** · [2026-07-15](https://reddit.com/r/ElegooMars/comments/1ux5c0j/comment/oxppuj5/) · 1 points
> 
> Orientation matters. How is yours?