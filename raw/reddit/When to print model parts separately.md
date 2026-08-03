---
title: When to print model parts separately?
source: https://www.reddit.com/r/3Dprinting/comments/w01lho/when_to_print_model_parts_separately/
author:
  - "[[Sociologer]]"
published: 2022-07-16
created: 2026-07-15
description: Hello folks! I'm getting my first 3D printer, a resin Anycubic Photon M3 if it's important. I've done a lot of research and learned quite a
tags:
  - reddit
---
Hello folks! I'm getting my first 3D printer, a resin Anycubic Photon M3 if it's important. I've done a lot of research and learned quite a bit, but I'm still unsure about one thing. When is it required, or at least advisable, to print a single model in multiple parts to be assembled after printing? The most obvious is simply printing a model too large for the printer in one go. The only reason I've come up with is to make the supports easier to place. I've seen some pretty large, intricate models printed as a single piece and others split into 6-12 parts and assembled afterward. Not having to assemble post-print seems ideal to me, but I feel like I'm missing something as to when I can do that and when it is not wise to do so. Your collective wisdom would be greatly appreciated!

---

## Comments

> **\[已删除\]** · [2022-07-15](https://reddit.com/r/3Dprinting/comments/w01lho/comment/igbrz70/) · 3 points
> 
> The trick is to determine what *can* be printed as one piece, and what is better printed as separate parts and assembled.
> 
> I think this comes down to experience.
> 
> The best advice I can offer is this. Bring the body into the slicer, and look at it, and see what the slicer will do, and imagine the printer trying to build it.
> 
> If you can avoid supports and such by splitting the model into two or more pieces, then that's what you do.
> 
> I print enclosures for electronics. The assemblies are designed in Fusion360. I always have separate front and back panels, because those parts have holes and slots for controls, LEDs and such, and they print better just being flat on the bed. The base can be a tray with two sides. Then print a separate top piece. Screw it together with self-tapping screws. Make sure to leave holes in the parts for the screw bodies and heads.

> **krichek** · [2022-07-16](https://reddit.com/r/3Dprinting/comments/w01lho/comment/igc4kp4/) · 2 points
> 
> I own both an FDM printer and a Resin printer and there is a large difference in what can be print unsupported when comparing them. Specifically flat to the bed with the object scaling up is almost always the best way to orient a print on an FDM printer in my experience. Just about any print will need at least some support when printed using Resin. I and a lot of other Resin printers tend to flip a print 45 degrees to the bed to 1. give it lots of support and 2. to lessen lines that can occur on some models at certain angles.
> 
> I generally see models split when any one of the following occurs:
> 
> 1: It's to big for the print area or some of the support bases/rafts will overhang even if the  
> model itself fits.
> 
> 2\. Pieces are going to be interchangeable, such as arms, heads, hands, weapons etc..
> 
> 3\. Separating pieces will make it easier in some way to post process. A good example of this  
> is bases are almost always separate from a miniature so that they can be painted  
> separately.
> 
> 4\. The person who created the file was limited by #1 and split the file to print themselves and  
> didn't create one for people that have a larger print area (this one is pretty rare now days)
> 
> 5\. The print changes in a way at some point that splitting it into multiple pieces makes it  
> easier to orient each piece for optimal printing.

> **jmdbcool** · [2022-07-15](https://reddit.com/r/3Dprinting/comments/w01lho/comment/igbujcl/) · 1 points
> 
> Resin is more forgiving than FFF, in terms of what details and features you can print in one piece. Some shapes in FFF will be a MUCH easier print in a a different orientation (i.e. flat against the bed). So if part A would be easier flat, but so would part B, and those are both part of the same solid object 90° perpendicular to each other, it may be time to divide and conquer. Then you can print with fewer supports, or maybe no supports at all. This gets easier with experience.
> 
> If I can choose to print one piece with many supports, or many pieces with little to no support, I will choose less support every time. I don't mind assembly, the easier print wins.