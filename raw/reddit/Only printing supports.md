---
title: "Only printing supports??"
source: "https://www.reddit.com/r/ElegooMars/comments/1va970p/only_printing_supports/"
author:
  - "[[Financial-Pilot5166]]"
published: 2026-07-30
created: 2026-08-05
description: "I have been trying to print this ring 4 times now and the result is always the same. I take my stl file from blender fix the issues on formw"
tags:
  - "reddit"
---
I have been trying to print this ring 4 times now and the result is always the same. I take my stl file from blender fix the issues on formware.co and then upload that STL to chitubox where i add supports and slice the file.

Then i send the file to my elegoo mars 5 ultra via network sending and the second photo is what i get. I am so annoyed and i know im doing something wrong but i cannot get to what is causing this. Any help is MUCH appreciated!

---

## Comments

> **AutoModerator** · [2026-07-29](https://reddit.com/r/ElegooMars/comments/1va970p/comment/p0jqozg/) · 1 points
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

> **cambriencassell14** · [2026-07-29](https://reddit.com/r/ElegooMars/comments/1va970p/comment/p0js59w/) · 12 points
> 
> Your lowest point is an Island. It's not starting the model because the first part is being left behind. (I am still new to Resin Printing, so someone correct me if im wrong)
> 
> > **Financial-Pilot5166** · [2026-07-29](https://reddit.com/r/ElegooMars/comments/1va970p/comment/p0jsmko/) · 2 points
> > 
> > Oh my gosh this actually might be it. The bottom of the sprue is an island so i added a support there and deleted all other islands. This might actually be the issue though. I will trouble shoot and see if that is the cause. Thank you
> > 
> > **Just-League-9847** · [2026-07-30](https://reddit.com/r/ElegooMars/comments/1va970p/comment/p0lxor4/) · 1 points
> > 
> > This is likely the correct answer

> **Common\_Development95** · [2026-07-29](https://reddit.com/r/ElegooMars/comments/1va970p/comment/p0jvkhr/) · 3 points
> 
> Are you using auto add supports or are you making the supports yourself manually? I've found the latest auto add supports to be pretty good.
> 
> > **Financial-Pilot5166** · [2026-07-29](https://reddit.com/r/ElegooMars/comments/1va970p/comment/p0jx7iy/) · 0 points
> > 
> > Im adding them manually, i dont want to add supports to the ring because then ill have to sand it down later and i would like the ring to remain as neat as possible, so im only adding supports to the sprue. However, ive printed this model before with the same supports and it printed fine

> **Paulrik** · [2026-07-29](https://reddit.com/r/ElegooMars/comments/1va970p/comment/p0k4w66/) · 2 points
> 
> Many of Sirayatech's resins are a little finicky with printing temperatures, it looks like Cast recommends printing at 25 - 35 Celsius. It also recommends using medium supports.
> 
> Here what their website says: A must read before printing with wax-based resin! Very important!!
> 
> 1. Make sure the printing temperature is above 25C (About 77F).
> 2. Wax-based resin prints are very soft, and it is recommended that small printers be used for printing.
> 3. Support is important for wax-based resins, please use at least medium support for small printers, and at least heavy supports for slightly larger printers. The specific settings depend on the 3D printer type.
> 
> Siraya Tech Castable Resin for jewelry | Elegoo Castable Resin [https://siraya.tech/products/cast-castable-resin?srsltid=AfmBOorNME7sZvv7-QgGcXebuUOvdF3s7zJ3yXa1r09Q0\_uP8CEAPCXv](https://siraya.tech/products/cast-castable-resin?srsltid=AfmBOorNME7sZvv7-QgGcXebuUOvdF3s7zJ3yXa1r09Q0_uP8CEAPCXv)

> **flameswithin** · [2026-07-29](https://reddit.com/r/ElegooMars/comments/1va970p/comment/p0kngmh/) · 2 points
> 
> Is there anything on your fep? If not, double check the orientation of your normals in the model itself. If your normals are flipped, could be the culprit. I’m not sure about the M5U, but my old Phrozen Shuffle would often have difficulty rendering files if I screwed up the normals on some part of a ring.

> **unverz06** · [2026-07-30](https://reddit.com/r/ElegooMars/comments/1va970p/comment/p0mkvo1/) · 2 points
> 
> You need more support !

> **theonlybaker** · [2026-07-30](https://reddit.com/r/ElegooMars/comments/1va970p/comment/p0mx0pw/) · 2 points
> 
> I would say you need way more support for that. try using the light supports and almost filling it up

> **undisclosed-identity** · [2026-07-30](https://reddit.com/r/ElegooMars/comments/1va970p/comment/p0o9r90/) · 2 points
> 
> I use lychee, not chitubox, but when i see what you're seeing, usually there is a glob of resin on the bottom of the vat. I get this because the supports aren't strong enough to hold the print, especially with the soft sirayatech resin. But as others mentioned, your lowest point being an island could likely be the culprit as well.

> **MountyC** · [2026-08-01](https://reddit.com/r/ElegooMars/comments/1va970p/comment/p11ahm9/) · 1 points
> 
> Repair should fix it.. but it could be inverted normals. Set it to show normals in blender see if it has any issues.

> **CalendarOk4561** · [2026-08-02](https://reddit.com/r/ElegooMars/comments/1va970p/comment/p1bn02j/) · 1 points
> 
> I’ve had models that are non manifold or have a deeper glitch in the modeling that the printer won’t print them. Try adding a known model that works as a check

> **Financial-Pilot5166** · [2026-07-29](https://reddit.com/r/ElegooMars/comments/1va970p/comment/p0jqw13/) · 0 points
> 
> Printer model: Elegoo Mars 5 Ultra, resin: siraya tech cast purple, slicer: chitubox