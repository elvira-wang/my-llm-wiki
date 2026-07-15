---
title: "3D resin print supports [EASY GUIDE]"
source: "https://www.youtube.com/watch?v=MU0Cq_bjhy4"
author:
  - "[[VogMan]]"
published: 2020-11-20
created: 2026-07-14
description: "Supporting 3D resin prints to get GREAT prints every time is easy! Just orientate to avoid islands and overhangs, raft, anchor, support and print. If that sounds confusing, it really isn't. In this si"
tags:
  - "videos"
---
![](https://www.youtube.com/watch?v=MU0Cq_bjhy4)

Supporting 3D resin prints to get GREAT prints every time is easy! Just orientate to avoid islands and overhangs, raft, anchor, support and print. If that sounds confusing, it really isn't. In this simple guide I'll show you how - and hopefully answer many of the popular questions I receive about 3D printing problems.  
So if you want to know how to support your 3D prints, how to overcome common printing problems, how to get the most from ChiTuBox and similar slicers, this video is for you.  
  
\*SUBSCRIBE for more tips, guides and fun projects\*  
https://youtube.com/@vogman?sub\_confirmation=1  
  
💚💚💚 PLEASE SUPPORT THIS CHANNEL 💚💚💚  
The price of a cup of coffee can really help me grow my channel. If, and only IF, you can spare a little, please consider becoming one of my Patrons. You can read more about this here:  
🟢 https://www.patreon.com/vegoilguy 😃  
Or if you prefer to make a PayPal donation, you can do that here  
🟢 www.vegoilguy.co.uk/donations 😁  
  
\*\*\* ARCHVILLAIN GAMES \*\*\*  
Fantastic miniatures, great giveaways and competitions...  
http://bit.ly/AVGVOG  
  
\*\*\* ETSY STORE \*\*\*  
I sell a few castings on Etsy. Proceeds help me maintain my channel.  
https://www.etsy.com/uk/shop/VegOilGuy  
  
🔹 \_\*MY LINKS\*\_ 🔹  
▶ http://vogman.co.uk  
▶ https://www.facebook.com/thevogman  
▶ https://instagram.com/the\_vogman  
▶ https://rumble.com/c/c-2100620  
▶ https://vogsmerch.myspreadshop.co.uk  
▶ https://etsy.com/uk/shop/VegOilGuy  
▶ https://patreon.com/vegoilguy  
  
#3dprinting  
#3dresinprinting  
#vogman  
#vegoilguy  
#vog

## Transcript

### Intro

**0:00** · Hey guys, I never claim to be an expert on anything, but I’m getting so many print related questions lately, I thought I’d do a quick, simple guide to help answer many of these questions. It’s aimed mainly at beginners, but it might be useful to even experienced printers. Hopefully what follows will help you get resin prints that stick to the plate and, importantly, print well.

**0:29** · For me, resin printing is all about supports. Let’s start with something simple – a sphere. Resin prints typically occur upside down, forming layer upon layer from a build plate, suspended in the air. Gravity is doing it’s best to stop us from doing this, so if we want our print to stick to the build plate, we generally need to add supports. So let’s add some supports to our sphere.

**1:01** · That will stick well to the built plate, but will it print?

**1:06** · With this supported sphere in ChiTuBox, we can see that ChiTuBox has coloured this area red because it’s telling us this area needs supporting.

**1:17** · Let’s ignore it for a moment and use these slide tools.

**1:23** · We can see the layers being added one at a time. But look here – at the bottom of the sphere. It’s unsupported and trying to print in mid-air. There’s no connection to the plate and it certainly can’t stick to fresh air, so it’s got no choice but to form an ugly blob on the FEP. It’s a failed print. So it’s critical that the lowest point of the print needs to be supported. In fact, with just one good support, this sphere may potentially print perfectly.

**1:56** · This is because it’s well anchored to the build plate, and each layer can adhere to the one before it. Unfortunately, most things we print are not as simple as a sphere. Look at this model from Archvillain Games. For the moment, let’s imagine that I’ll try to print this model as it is, which isn’t ideal, but I’ll come back to orientation in a moment. This guy’s got two perfectly good feet and I could start with these on the build plate, right?

### Example

**2:29** · That looks like plenty of support there and the model should print. Or so you might think.

**2:40** · Using these slide tools again, we see the two feet appear to be doing a great job. But hang on, what’s this…? You can see the bottom of his cape is trying to print in mid-air. Again it’s an unsupported floating section. It’s not connected to the plate and it can’t print on fresh air. The print will drop away here if we let it.

### Islands

**3:06** · So this point must be supported otherwise the print will fail.

**3:11** · Now areas like this are called Islands and they’re surprisingly common. If you want to produce good prints, you’ll need to start looking for them.

**3:22** · Here’s one… and another… actually there’s loads here.

**3:29** · Changing the camera angle and moving around will allow us to see even more Islands and if we want a good print, this is time well spent.

**3:39** · Now to be fair, I’m using version 1.7.0 of ChiTuBox and enabling this little Eye icon reveals these lines. These are the way ChiTuBox tells us we have a problem area that needs supporting. And sure, we could use the Auto-Support feature and let ChiTuBox do the work. The problem there is no Auto Support is perfect, so having a good understanding of WHY we need these supports will help us do a better job than AutoSupport.

### Auto support

**4:16** · If we come back to the feet, we can also see support-suggesting indicators there too, and that’s because, despite initial appearances, those feet aren’t actually flat against the plate, and like it or not, feet themselves aren’t actually all that flat. And this shows that maybe choosing a different orientation for the model would have been a better idea.

**4:41** · Not only that, a large cluster of islands like this would mean our model would be littered with supports, and that mean lots of clipping and lots and sanding, which is time consuming and can damage your print. To make printing easier, slicers like ChiTuBox let us change the angle of our prints and vary the orientation.

**5:04** · Let’s take this strange shape as an example. It can’t lie flat and generally unless you want a flat face to touch the build plate, it’s best to raise the print above the platform by about 5mm or so. Now we could add supports to this flat area here and this could work. But this can lead the sagging between the supports which misshapes and ruins the print. So avoid flat edges adjacent to the build plate.

### Flat support

**5:37** · Doing this is easy enough. We can adjust angle of the print a few degrees.

**5:45** · But notice the colour. It’s still dark red. ChiTuBox is warning us we’ll need lots of supports to make that work and at such a shallow angle, we could still get sagging.

**5:58** · But if we tilt the angle a little further, watch the colour now. It’s blue - with just the tiniest hint of red on the lowest edge. ChiTuBox is happy with us because our print is now at an angle that each layer can safely print on top of the previous layer without need of support. This angle is generally around 45 degrees and depends a lot on the printer and the resin being used. It’s possible to print steeper angles, but these overhangs are weak points and can sag or even break. So it’s best to keep 45 degrees and under.

### Angle support

### No islands

**6:41** · However, if we spin around this side, we’ve still got a who lot of red.

**6:48** · So this time, let’s go back and change the Y axis by 45 degrees.

**6:55** · Look now, there’s no red at all. By simply changing the orientation of our model on two axis, we’ve made sure there are no islands and each layer can safely print on the previous layer without the need for support and really, that’s the goal here… no islands and minimal supports. Just like with the sphere, in theory one good support in this corner and the whole thing should print. But several thin supports would probably work better.

**7:27** · So, adjusting the orientation of the print will minimise islands and the number of supports required. It just takes a little patience to spin the print and spot and ideal position, and remember, there’s potentially dozens of good positions so look for those that suit your model best.

**7:49** · Let’s just pretend this model would print great from this angle – which is clearly wouldn’t – but if we pretend it did, the supports will be going into the models head and no matter how careful we are with clipping and sanding, that’s going to spoil our finished print, so look for a combination of the best orientation and good support points.

**8:14** · Now I’m cheating here to save time… this model came pre-supported from Archvillain Games and they already went to the trouble of getting the orientation right – or at least as good as possible, as perfection isn’t always an option.

### Presupported

### Support options

**8:33** · So all we need to do now is add supports… but there’s so many options… Light, Medium, Heavy, Rafts, depths, and more. So what’s the best options?

**8:44** · Now here you’ll get lots of differing opinions, but for the absolute beginner, here’s my advice. Firstly, always use a raft. It’s a nice, large area that really helps the print stick to the plate. I tend to increase the size of my raft up to 150% to really help the resin stick firmly.

### Beginner tips

**9:11** · For supports, keep the settings standard, at least until your experience grows. If you’ve already fiddled, just reset to take everything back to factory settings.

### Light supports

**9:24** · Try to use Light supports wherever possible. These have a much smaller contact with the print and consequently damage the surface least. But long Light supports go bendy when printing, so Medium to Heavy are better over distances, and the weight of the print is important. A large print will need a lot of Light supports or a fewer heavy ones.

**9:53** · A tip I will share with you is the lowest point. I try to make sure that the lowest point always has at least one Heavy support. Remember, as the print grows, most of the weight will fall upon this first support, particularly if the other supports aren’t yet fully printed. So a good first support will save you many a lost print. And for that reason, try to make sure the lowest point is an unimportant spot, such as the bottom of a foot.

### Heavy supports

**10:25** · Then look for a few boring spots on the print, nice flat areas with little detail. Add some heavy supports here as well because this will really help your print stay fixed and firm on the plate. The size of the print will determine how many you need, but on something small like this, a couple is fine.

**10:51** · Next, look for your Islands. Use the slicer tool carefully to home in on the lowest point and make sure you support these. Then look for those pink areas. These may not be islands, but a little support will help. Make sure there’s a good gap between the print and the support. If they’re too close, they can get meshed together. Remember, you can reposition your supports and ChiTuBox doesn’t always choose the best spot.

**11:32** · A favourite trick of mine is to manually bond two, three or even more supports together.

**11:39** · That way I can combine Light supports and make a heavy support that will stand up over a distance. This gives me a thicker, stronger trunk but a lighter tip, which means plenty of support area with fewer downward supports. I also tend to over-support. Many criticise

**12:15** · me for this, but I don’t get many mis-prints so I don’t care. Adding one or two supports even in an area that ChiTuBox doesn’t recommend can’t really do any harm.

**12:26** · In fact, I even support my supports sometimes, especially tall supports on a large print.

**12:34** · Yes, fewer supports is good, but a successful print with a little extra clean up is better than a failed print, lost time and wasted resin.

**12:45** · So there you go… that’s about as much as I can think to say on the subject of Supports.

**12:52** · If you have a good level plate and you’ve dialled your resin setting in correctly, then these simple tips should make sure your prints work every time. And through this video, I hope I’ve answered most of the questions folks have been asking me lately.

### Outro

**13:11** · Of course I’ve been talking about ChiTuBox throughout this video and Slicing software can make a massive difference. ChiTuBox is good, but I think I’ve found a much better and much simpler Slicer. But for that, you’ll have to tune in to my next video.

**13:30** · So if you have any questions or comments, as always, drop me a line.

**13:37** · Happy printing guys. Take care, and thanks for watching.