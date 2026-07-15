---
title: "6 Blender Hard-Surface Modeling Tricks I Wish I Knew Earlier"
source: "https://www.youtube.com/watch?v=Ml2t8uxPAQU"
author:
  - "[[CG Boost]]"
published: 2024-08-01
created: 2026-07-15
description: "In this video, Louis du Mont (@ldm) walks through 6 hard-surface techniques that can drastically increase modeling speed.⇨ Robotic Planet course: https://cgboost.link/robotic-planet-d6d4df⇨ Download"
tags:
  - "videos"
---
![](https://www.youtube.com/watch?v=Ml2t8uxPAQU)

In this video, Louis du Mont (@ldm) walks through 6 hard-surface techniques that can drastically increase modeling speed.  
⇨ Robotic Planet course: https://cgboost.link/robotic-planet-d6d4df  
⇨ Download Project files: https://www.cgboost.com/resources  
⇨ Blender Secrets E-book (affiliate): https://gumroad.com/a/436106355  
  
CHAPTERS  
00:00 - Intro  
00:22 - Hard Surface Curves  
03:58 - Pin Modifiers  
04:34 - Quick Cables  
05:38 - Right Angle Pipe Join  
06:07 - Mesh Decal  
07:43 - Transfer Normals  
08:54 - Outro  
  
MY SYSTEM  
CPU: AMD Ryzen 5900x  
GPU: GeForce RTX 3090  
RAM: 96 GB  
  
FOLLOW CG BOOST  
⇨ Twitter/X: https://twitter.com/cgboost  
⇨ Instagram: https://www.instagram.com/cg\_boost/  
⇨ Web: https://cgboost.com/

## Transcript

### Intro

**0:00** · In this video we will look at 6 hard surface techniques that changed how I worked.

**0:04** · I have been creating 3D work professionally for 20 years now, that is to say I have come across my fair share of hard surface challenges.

**0:13** · In this video I am going to share some of my top techniques that I wish I had known years earlier and that have saved me hours and hours of frustration.

### Hard Surface Curves

**0:23** · Hard surfaces usually feature a lot of flat surfaces with right angles mainly due to the not overly malleable materials involved.

**0:31** · I am thinking metal, wood and plastic.

**0:34** · However, these things can still be bent, cut and moulded into curved shapes.

**0:39** · Lets take this design for example.

**0:41** · We could start with a very high poly mesh, but what we gain in resolution we lose in control, even with proportional editing.

**0:49** · So lets look at keeping this mesh density super low and controllable while having this high resolution smooth outcome.

**0:56** · So lets move this aside and I am just going to shift and right click to drop the cursor and shift a cylinder.

**1:05** · We only need about 16 vertices here.

**1:07** · Jumping into edit mode lets scale along the Y, something like that looks good.

**1:13** · And in poly select lets do top and bottom, eye to inset and then right click bridge faces.

**1:21** · Lets just move it out the way a little bit.

**1:23** · There we go.

**1:23** · Now we have some larger bevels here, so lets just go into edge mode, select these, bevel, that looks good.

**1:31** · Maybe lets increase it a tad.

**1:33** · And one on the inside here and bevel.

**1:36** · Cool, that looks good.

**1:37** · Now for the front section here we can select these group of polygons, like so.

**1:45** · Hit E to extrude out, scale down along the Y, lets move it back a little bit.

**1:50** · And then assuming you have loop tools enabled, which you may need to do so from the addons menu in the preferences, we can right click, loop tools, circle.

**2:01** · I am just going to scale that down, hit extrude, inset with I and then one more extrude to go in .

**2:07** · Ok, we have roughly the same shape but with very low polys.

**2:11** · Now lets look at how we can make it nice and smooth, but with hard edges.

**2:16** · Firstly, lets add a subd modifier with CTRL and 3.

**2:20** · We have the smooth down, but not the hard edges, so lets go into edit mode and lets select one of the edges in edge mode.

**2:28** · And we can use SHIFT G and then face angles to select edges with the adjacent faces at a certain angle, which we can dial in here, but that looks good to me.

**2:40** · So lets SHIFT E to create the crease, looks good.

**2:44** · We need a few more creases here, so again, lets select that edge, face angle and SHIFT E.

**2:51** · Ok, cool.

**2:52** · Now we also have a couple more edges here that we need to select to match this style and underneath we don't have any sharpness at all, so lets just select that edge loop with ALT, SHIFT E again and reduce to nothing, just make sure that is minus 1.

**3:10** · I'm just going to move this edge up a little bit to match.

**3:13** · Ok, cool, now we have the nice sharp edges, so lets just shade smooth and see what we've got here.

**3:20** · Just going to hide all of the wireframes with ALT SHIFT and Z to switch off the overlays.

**3:26** · Its looking ok, but its not quite as nice and creased as this one, so lets add a bevel as well.

**3:32** · Go into edit mode, select one of the edges with a crease on, and if we SHIFT and G, we can select all of the creases and then CTRL and E, edge bevel, and we'll just add an edge bevel weight of 1.

**3:43** · Now we can add a modifier, search for bevel, limit method to weight, that weight we just created, shading, harden normals.

**3:53** · Now if we switch off our overlays, we have a really nice look with nice sharp edges.

### Pin Modifiers

**3:59** · Lets say you're being a productivity wizard and you're only working on half of your model, knowing you can add a mirror modifier.

**4:05** · If we were to do so now, you can see that we have odd pinching here and its not looking particularly nice, and this is because our mirror modifier is happening after the fact.

**4:17** · Thankfully there is quite a cool way you can remedy this, and that is because as of 4 .2 you can pin modifiers.

**4:23** · So if we select bevel for example, we can pin to last, and likewise on our subdivision.

**4:29** · Now if we add our mirror modifier, it happens before our pinned items in the stack.

### Quick Cables

**4:34** · Really handy.

**4:35** · Now this one took me far too long to realise, I'm sure a lot of you know you can add cables by going into a curve, adding say a bezier curve, going into the curve options and geometry under depth, just cranking things up a little bit like so.

**4:51** · However, I used to then go in and start manipulating these points and try and snap and rotate and arrange things, and it just took a little too long.

**5:00** · And I find it considerably easier to just select all and delete all vertices, jump in to the draw mode and draw from the cursor.

**5:11** · Now if we go into orthographic here, I'm just going to snap the side, lets go to wireframe, we can draw the curve that we want, something like that looks good.

**5:19** · And you can see that the calculation of the bezier handles is already pretty good and only needs a little bit of clean up to finish.

**5:27** · On a side note, you can also go into edit mode and just check surface and now you can draw your cables all over your geometry and it sticks nicely to it like so.

### Right Angle Pipe Join

**5:39** · Right angle joins like this appear quite a lot for me, particularly in hard surface modelling for handles and the like.

**5:45** · Thankfully its quite easy to put together if you have your two cylinders here in place and they are joined into one object, we can select the edges here, right click and then go to bridge edge loops.

**5:58** · And then under number of cuts, you can add say 5 and adjust the smoothness factor to your liking.

### Mesh Decal

**6:07** · And done.

**6:08** · Some things are just painful to add to existing geometry without having to seriously mess up your beautiful underlying base mesh, so why not just stick it on top.

**6:17** · Well, lets look at how to set that up.

**6:20** · Firstly, this is the item we want to stick on the underside of our craft here, just like a pulse engine of sorts.

**6:27** · Firstly, we need to make sure our origin point is snapped to the bottom, so I'm just going to go into edit mode, edge, select the loop with ALT and left click, and then snap our cursor to it with SHIFT and S.

**6:41** · Hitting tab to go back out into object mode, we can go to object, set origin, origin to 3D cursor.

**6:47** · Now under our snap options here, we can make sure we are on face and align rotation to target.

**6:53** · And that affords us the ability to just hit G, hold down control and snap our item on the underside like so.

**7:01** · Now this isn't hugely convincing as a join here, but we're only just getting started, so to make it a little bit more convincing, we can go into edit mode and select these outer polys, go over to our vertex options, create a new vertex group, let's just leave it called group, and click assign.

**7:19** · Now if we jump out into object mode and move over to our modifiers, we can add a new modifier, and search for shrink wrap.

**7:28** · Let's move it to the top of the stack.

**7:30** · Now we can select our target, the main base of the ship here, and restrict this effect by that vertex group we just created.

**7:38** · Now we can duplicate this over the bottom to our hearts content.

### Transfer Normals

**7:44** · Now I'm sure some of you can see that the join here is still quite abrupt, particularly in rendered mode, and it's not really fooling anyone.

**7:52** · Thankfully we can use the normal data from the object which we are stuck to and apply it to this object.

**8:01** · And to do so, with the object selected, we can go add modifier, search for data transfer, select our source object, and go down to face corner data, let's just expand that, and we want the custom normals, and the option we want is nearest face interpolated, and I find this to be the smoothest result.

**8:25** · And as you can see, it looks like it almost doesn't exist at all with some very light shading.

**8:30** · Thankfully we can once again take advantage of our vertex group to isolate the effect, and now you can see, particularly compared to the old method, it looks considerably better.

**8:41** · So let's just shift select all the remaining items, and then the item with the data transfer, and then go to this little dropdown here, and copy to selected.

**8:52** · Excellent.

**8:53** · I hope some of these techniques have helped, now this model was built exclusively to demo most of these techniques, but if you had fun and you'd be interested in learning something a little bit more, then you might like Robotic Planet, a full robot creation course over at CG Boost Academy.

### Outro

**9:13** · We walk through entire robot creations as well as tackling even more tips and tricks.

**9:17** · Enrolling in the course also gives you access to the CG Boost community where you can comment, share ideas, or get help on particular parts of the course.