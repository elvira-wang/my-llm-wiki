---
title: "3D Printer Problem: do you know How to Fix Z-Wobble?"
source: "https://www.youtube.com/watch?v=qNCDXdjJb90"
author:
  - "[[Geek Detour]]"
published: 2023-12-16
created: 2026-07-15
description: "Wobbly prints and prints with lines... How you fix it? It can be many things (trust me, every time is a different reason). That's why I loved the Book I showed in this video. It will help you a lot, s"
tags:
  - "videos"
---
![](https://www.youtube.com/watch?v=qNCDXdjJb90)

Wobbly prints and prints with lines... How you fix it? It can be many things (trust me, every time is a different reason). That's why I loved the Book I showed in this video. It will help you a lot, specially if you are just beginning with 3D Printing:  
  
"3D Printing Failures" Book  
by Sean Aranda  
https://geni.us/73Gd (Amazon)  
  
More 3D Printing Books on Amazon:  
https://geni.us/3DPrintingBooks  
  
Grease for 3D Printers Lubrication  
https://geni.us/G3R3V (Amazon)  
  
Sunlu S2 Filament Dryer  
https://geni.us/SunluFilaDryerS2 (Amazon)  
  
Sunlu S1 Filament Dryer  
https://geni.us/SunluFilaDryerS1 (Amazon)  
  
\* Sunlu S4 is not available for sale yet  
my review: https://youtu.be/ZUkEmTvzl2E  
  
  
Elegoo Neptune 3 Pro - 3D Printer  
https://geni.us/Elegoo-Neptune3-Pro (Amazon)  
  
Creality Ender 3 S1 Pro  
https://geni.us/Creality-Ender3-S1-Pro (Amazon)  
  
  
Orange PETG filament from Sunlu:  
https://geni.us/vvmQ5l (Amazon)  
\* this is the filament you saw all the time in the video  
Sunlu has many more colors in this link too  
  
Orange PLA filament from Sunlu:  
https://geni.us/lHGmP (Amazon)  
\* Same orange color, but in PLA  
Sunlu has many more colors in this link too  
  
  
More Gifts for Makers:  
https://www.amazon.com/shop/geekdetour  
  
  
\- I earn commissions from affiliate links.  
\- As an Amazon Associate I earn from qualifying purchases.  
  
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_  
Written, Performed and Produced by Everson Siqueira  
  
I use royalty-free music from Epidemic Sound:  
👉 https://geni.us/IW1NyB  
Sign up with my link to get 10% discount on your first 12 months  
The first 30 days are free  
  
  
How to fix Z-Binding on 3D Printers  
How to fix Z-Wobble on 3D Printers  
My 3D Printer is printing bad  
  
#3DPrinter #3DPrinting #Ender3

## Transcript

**0:01** · These two pieces were printed on two separate 3D Printers: very popular printers, you might have one of them.

**0:08** · One part was perfect and smooth… the other one got these lines, from bottom to top.

**0:14** · You can actually feel the lines with your fingers.

**0:17** · Do you know what happened here?

**0:18** · Do you know how to fix it?

**0:20** · Pause the video right now and write your guess in the comments before we continue… By the way you will see this book a few times during the video I am not the writer, but we will talk about it later.

**0:30** · So, I printed both parts in PETG could be in PLA as well that’s not important.

**0:35** · It is a functional part that I designed in Fusion 360.

**0:39** · They hold these metal rails to the ceiling, where I hang my Studio lights.

**0:43** · They don’t hold any weight, quite the opposite: they are constantly compressed by the nuts.

**0:49** · The actual load is supported by stainless steel rods, chemically anchored to the ceiling.

**0:55** · I needed 4 of these parts, so I used two printers: an Ender 3 S1 Pro and an Elegoo Neptune 3 Pro.

**1:02** · Both printers have been printing perfectly for many months.

**1:05** · So, I got very surprised when one of them got me this ugly part.

**1:10** · That very printer had just printed a perfect piece, just one week before!

**1:16** · So, is it wet filament?

**1:18** · …No!

**1:19** · Why people always say “wet filament”?!

**1:22** · Drying your spools is important, but both printers were using spools that I had recently dried together.

**1:28** · It’s not wet filament.

**1:30** · The layers were so irregular that I had to check for wobbliness… Something might be very loose: like, the bed, the belts, the gantry, the print head… I checked everything: all the wheels were tight as they should, everything was moving smoothly with no play.

**1:52** · Maybe the nozzle temperature is fluctuating a lot… In case you don’t know, if the temperature changes between layers, it doesn’t need to be a lot, when it gets hotter, filament expands and the layer gets wider… So I did a PID tuning It doesn’t matter if your printer runs Klipper or Marlin, you should run a PID calibration both in your nozzle and print bed, so the temperature is constant.

**2:15** · I did the PID tuning and I printed a second part.

**2:18** · The result?

**2:20** · I got the same problem.

**2:23** · But, maybe, the thermistor, the temperature sensor, is failing… it might be showing a constant temperature, when in fact, it could not, who knows?

**2:31** · How can we rule out a faulty sensor?

**2:34** · That is easy: in my hands, now I have not one, but two ugly parts and when I placed them side by side, the line patterns were identical.

**2:44** · Temperature is fine, it needs to be mechanical… and I got pretty convinced it was related to the Z-rods.

**2:51** · Yeah, it was happening on the Ender 3 S1 Pro.

**2:55** · It didn’t have lubricated the rods for a while, so I cleaned the rods, applied some lithium grease lubrication, moved the gantry up and down a few times and started printing the same model for a third time and, sure enough, nothing changed...

**3:10** · The layers were all weird, again.

**3:13** · Do you know the problem already?

**3:15** · I’ll give you a hint: I fixed it with just one tool, an Allen key that came with your printer too.

**3:22** · I noticed the Lead Screw Nuts were a bit tight on both rods… They were quite loose when I started using this printer.

**3:29** · Anyway, I loosened their bolts a few turns and the nuts now were moving sideways much more freely, as they should.

**3:36** · Guess what?

**3:37** · It worked.

**3:39** · The problem was not exactly Z-Wobble it was Z-Binding.

**3:44** · Oddly enough, it is not directly mentioned in the book.

**3:47** · But it is a very well known problem, with many videos on YouTube.

**3:50** · I never though it could make such an ugly print, out of the sudden… As I told you, just one week before, it was printing PERFECTLY, NO SIGNS of it whatsoever… ...or was it?

**4:02** · I had to check that “perfect” part again… and, when I placed them side by side by side even though it was a different model surprise, surprise: it was already there, the lines, the pattern, it was already beginning to happen, discretely but surely.

**4:18** · I am not throwing a rock at the Ender 3 S1 Pro… Z-Binding can happen in ANY printer, even when the Lead Screws seem to be quite straight.

**4:26** · So, let’s do an experiment.

**4:28** · I will put 3 printers side by side: the Ender, the Neptune 3 Pro and a BIQU Hurakan.

**4:36** · They will be printing the same model… By now, everything should be perfect so far… And, without stopping, I will tight their z-nuts.

**4:44** · I’ll let them print a bit more… …and everything printed just fine!...

**4:49** · \<microphone testing> Better! So I'm recording this experiment months after the problem you saw and at the time we just at the time we had just moved I was printing like crazy no time to look at the printers to adjust anything just printing, printing, printing and putting things to work on the house, in the studio and now that I'm trying to reproduce...

**5:12** · ...for the life of me I cannot reproduce the problem!

**5:14** · In my head it was just a matter of tightening the nuts and that thing would happen again and it didn't.

**5:22** · It printed perfectly!

**5:24** · I think that what happened there was the perfect storm of a machine that was too dry no lubrication on the Rods AND on the Nuts so it was starting to bind Dry bind a little bit and then release bind again and adjust again so the layers were so irregular but now that the machines they are well adjusted, lubricated, it doesn't matter I can tight to the nuts I don'teven see the wave patterns I even replaced this the stepper motor

**5:56** · and the rod for a rod that was very bent everything printed just fine!

**6:02** · By the way the nuts must operate loose you should not tight those nuts they are made it to operate lose so they can move sideways and compensate for rods that are not straight.

**6:15** · So, people are now buying the printers that you don't need to do anything they just print fine out of the box all those machines are brand new they will print super nice NOW.

**6:24** · Eventually things happen so people will need to learn how to keep them adjusted how the printers work learn how to troubleshoot your machine sometimes there is lots of trial and error to do that If you just bought a 3D Printer, I recommend you to also buy this book: “3D Printing Failures”, by Sean Aranda Sean might get surprised by my video, I never contacted him.

**6:48** · The book is very nice, it covers so many problems you might encounter on you 3D Printing journey.

**6:53** · Photos are great, fonts are big which I am starting to appreciate.

**6:58** · Of course, no book is complete, it doesn’t mention the binding of the nuts that we just saw in this video… But it mentions Power-loss Recovery Blobs that I also covered in one of my videos Watch my video!

**7:10** · Buy Sean’s book to fix your printing problems… Link in the description I’ll get a small commission Merry Christmas everybody!

**7:17** · And Subscribe!

**7:19** · Thanks for watching.

**7:20** · Hoooo! Hooo! Hooo!