---
title: "[Troubleshooting] Wall deflection, blooming, and curing deep cavities on a large hollow print. Looking for workflow feedback!"
source: https://www.reddit.com/r/resinprinting/comments/1v0286m/troubleshooting_wall_deflection_blooming_and/
author:
  - "[[45acp1911_HD]]"
published: 2026-07-19
created: 2026-07-24
description: Hey everyone, ​I’m working on a large multi-piece battery organizer and I'm running into a few specific fluid dynamics and post-p
tags:
  - reddit
---
Hey everyone,

​I’m working on a large multi-piece battery organizer and I'm running into a few specific fluid dynamics and post-processing issues.

​My Setup:

​Printer: Elegoo Mars 5 Ultra

​Slicer: Chitubox

​Resin: Elegoo ABS-like 3.0 Red

​Wash: Super Clean purple degreaser (I don't use IPA)

​The Project:

It's a large block with cylindrical cutouts on top for batteries, and a deep cavity in the front for a slide-out drawer. I used the hollow tool in Chitubox with a 2mm wall thickness and designed in an integrated drainage hole to clean out trapped liquid during processing, but I'm still hitting some walls (literally).

Issue 1: Wall Deflection & Blooming (See photos)

The outer perimeter holes for the batteries are printing too tight. Looking closely, there is a distinct, crescent-shaped lip of cured resin protruding into the cylinder, but only on the side of the hole that sits flush against the flat outer wall.

I suspect the hydraulic pressure of the descending build plate is causing that 2mm outer wall to bow outward, trapping resin and creating this shelf (and some internal rippling/blooming). I’m planning to Dremel these out for this prototype, but to fix the file for the future:

​What Light-Off Delay / Rest Time before exposure do you recommend for thick translucent resins to let the pressure equalize?

​Is a 2mm wall inherently too thin for a print this large, or should I just thicken the exterior walls manually in CAD to prevent flexing?

​Issue 2: Curing Deep Cavities & Thermal Cracking

Because the resin is translucent red, it filters a lot of UV light. I've had issues with the print cracking under UV light, likely due to uneven curing stresses between the fully cured outer shell and the under-cured internal core. Furthermore, getting light all the way to the back of the deep drawer cavity is tough.

​I’ve built a foil-lined curing box with a turntable. I'm currently debating between:

​Bouncing light in with an angled foil reflector.

​Submerging the print in a clear container of water to refract the UV light deep into the cavity.

​Does anyone have experience using water curing for deep hollow geometries? Does it actually help diffuse the light enough to cure the deep interior walls evenly without causing stress cracks?

​Any advice on dialing in these settings or tweaking my post-processing workflow would be hugely appreciated. Thanks!

---

## Comments

> **Balerion84** · [2026-07-18](https://reddit.com/r/resinprinting/comments/1v0286m/comment/oybxxsb/) · 2 points
> 
> for 1. the real answer would be 'as long as necessary', so while 2-3s might more than enough for most simple stuff like minis, if it's something more difficult, it'd need to be longer.
> 
> 2\. I use glycerin instead of water as it's better, so I'd recommend that (but water is good too), but I don't have a comparison of light diffusion or to what degree it helps cure the inside  
> also resin prints should be fully dried, ideally with heat before post curing, with resin being hygroscopic, that means you want to use heat, although I don't know how the hygroscopic nature of resin interacts with that degreaser that you use. With IPA, it absorbs it so needs to be completely evaporated
> 
> > **45acp1911\_HD** · [2026-07-18](https://reddit.com/r/resinprinting/comments/1v0286m/comment/oyd0uie/) · 1 points
> > 
> > I did give it a thorough water rinse after cleaning it then let it sit overnight to dry out.
> > 
> > I'll have to give the curing bath a shot in reality interested to see how it goes.

> **Lito\_** · [2026-07-18](https://reddit.com/r/resinprinting/comments/1v0286m/comment/oyccxw6/) · 2 points
> 
> To cure cavities where uv light doesn't reach you need either an UV torch or makeshift a small uv bulb (3-4mm) with an usb cable to stick it in the cavities.
> 
> You probably need something like 5 seconds light off delay for this piece but this is something you'll need to test.
> 
> Realistically you need to find a way to dlnot let resin get trapped in the cavities during printing if you want no blooming, or get lucky with long light off delays.
> 
> At the end of the day this is not a resin print piece. At all. So you'll have a ton of issues with warping, leaks, blooming, etc. You're ecperiencing some already.
> 
> I can't comment on water curing because I don't do it.
> 
> > **45acp1911\_HD** · [2026-07-18](https://reddit.com/r/resinprinting/comments/1v0286m/comment/oyd061j/) · 2 points
> > 
> > Thank you! I'm new to 3d printing and I was thinking also, after the fact, that this would be way better suited for fdm. I initially tried a solid block but it failed 1/4 of the way through because, unknown to me at the time, it was going to take well over 1100g of resin and i didn't keep an eye on the vat level so it just went in it's mary way after it was empty. The small lights make sense but what a pita. Regardless, it got me introduced to tinkercad which was a fun learning experience.
> > 
> > Tldr; just because you CAN doesn't mean you SHOULD 😂