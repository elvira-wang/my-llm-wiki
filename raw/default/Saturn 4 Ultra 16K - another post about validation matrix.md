---
title: "Saturn 4 Ultra 16K - another post about validation matrix..."
source: "https://www.reddit.com/r/resinprinting/comments/1uze9he/saturn_4_ultra_16k_another_post_about_validation/"
author:
  - "[[dar_mach]]"
published: 2026-07-18
created: 2026-07-24
description: "Hi everyone, truing to calibrate exposure on a brand new Saturn 4 Ultra 16K version, using Anycubics ABS-Line Pro 2 - as I have this left af"
tags:
  - "clippings"
---
Hi everyone, truing to calibrate exposure on a brand new Saturn 4 Ultra 16K version, using Anycubics ABS-Line Pro 2 - as I have this left after a Mono 4.

I have configured "RERF" counterpart of Elegoo, to shoot between 1.6s to 3.6s and... I don't seem to be able to notice much difference between printer validation matrices. They all have 13-14 poles, and 13 holes, but also they all seem kinda... melty? Look on the letters for example on the picture.

I vaguely recall that I've seen some video where the guy claimed that on 16K Saturns the default UV LED power is set too high, and he managed to get proper results after setting git to 75%. Can this be the case?

Sliced with Chitubox, settings screen attached.

![r/resinprinting - Saturn 4 Ultra 16K - another post about validation matrix...](https://preview.redd.it/saturn-4-ultra-16k-another-post-about-validation-matrix-v0-sde3zgbp9vdh1.png?width=545&format=png&auto=webp&s=70625f864ce3798b0d19ebb1857ce24b57ccee23)

![r/resinprinting - Saturn 4 Ultra 16K - another post about validation matrix...](https://preview.redd.it/saturn-4-ultra-16k-another-post-about-validation-matrix-v0-lgu93rs99vdh1.png?width=1080&crop=smart&auto=webp&s=fdfc46a91f23ced0a0b8a0f1cbc836c6d2fbc714)

---

## Comments

> **HammeredDog** · [2026-07-17](https://reddit.com/r/resinprinting/comments/1uze9he/comment/oy6q8it/) · 1 points
> 
> Can't speak to this model, but I just went through calibration on the same printer, but with different resin and cones of calibration. There wasn't a lot of difference on most of the tests, but the cones themselves led me where I needed to be. I didn't need to adjust uv strength.

> **awyeahmuffins** · [2026-07-17](https://reddit.com/r/resinprinting/comments/1uze9he/comment/oy6r3xl/) · 1 points
> 
> I don't have the slicer in front of me, but [confirming some info online](https://www.reddit.com/r/3Dprinting/comments/191liet/you_need_to_adjust_your_printing_profile_for_the/) the validation matrix part of the print starts at 0.20mm, meaning at 0.03mm it's starting around layer ~7. Which means you have 10 transition layers of 'overexposure' at the start of the matrix, probably causing that "blurring" you're seeing.
> 
> Pretty sure for the flat validation matrices you want 0 transition layers, and stick to 4-5 bottom layers to keep it below where the matrix starts.
> 
> For what it's worth my settings for the 16k for Anycubic ABS-like Pro 2 are 0.04mm layer height, 15s base, 1.9s normal, 225 PWM for both bottom and normal.
> 
> I also run with 40-second Wait Before Cure (Rest Time after retract) on bottom layers -> 3s normal. This is fairly conservative for the 16k, you could also try 20s -> 1s. This will help combat some of the z-compression issues from viscous resins and the auto-level system.
> 
> > **dar\_mach** · [2026-07-17](https://reddit.com/r/resinprinting/comments/1uze9he/comment/oy6sw9i/) · 1 points
> > 
> > Oh, so you lowered power of the lamp too? I'll give your suggestions a try tomorrow!
> > 
> > > **awyeahmuffins** · [2026-07-17](https://reddit.com/r/resinprinting/comments/1uze9he/comment/oy70rua/) · 1 points
> > > 
> > > Yeah typically speaking resins will behave (especially with support tips) a bit more predictably around the ~2s exposure mark.
> > > 
> > > I tend to lower the lamp PWM for anything below 1.8s.
> > > 
> > > I will say I've gotten some reports that perhaps PWM adjustment doesn't work in .GOO file-type. I haven't tried confirming it myself, I know for sure it works for .CTB.
> > > 
> > > > **dar\_mach** · [2026-07-18](https://reddit.com/r/resinprinting/comments/1uze9he/comment/oy8t7js/) · 1 points
> > > > 
> > > > Hmm, I don't seem to be able to find rest time after retract for bottom layers, am I missing something?
> > > > 
> > > > I have FDM experience, but new to resin printing. Had Mono 4 Ultra but returned due to QC issues.
> > > > 
> > > > How would you sum up your experiences with layer height? I know miniatures are more willing to hide layer lines, but I expect to be printing mostly functional pieces - so aesthetic will be on flat surfaces which are merciless...
> > > > 
> > > > Trying for now 30um - I see you're using 40?
> > > > 
> > > > > **awyeahmuffins** · [2026-07-18](https://reddit.com/r/resinprinting/comments/1uze9he/comment/oy8wc7u/) · 1 points
> > > > > 
> > > > > I think that is a limitation of Chitubox unfortunately - can only set a single wait time.
> > > > > 
> > > > > You can run the file in UVTools after slicing to set the Wait Before Cure time, this has the advantage of being able to set a gradient separate from the bottom/normal layers.
> > > > > 
> > > > > Example: [https://www.reddit.com/r/resinprinting/comments/1kvbtvi/first\_print\_not\_sticking\_saturn\_4\_ultra\_16k/mu9a61k/](https://www.reddit.com/r/resinprinting/comments/1kvbtvi/first_print_not_sticking_saturn_4_ultra_16k/mu9a61k/)
> > > > > 
> > > > > Personally I use 40um for everything, but I mostly use it for DnD items and cosplay items, so sanding, priming, painting workflows means the layer height is less important. Perfectly flat surfaces should be fine at larger layer heights, it's *almost* flat (ie some curve to them) surfaces that tend to be the issue.
> > > > > 
> > > > > AA does work on the 16k to a limited extent, but you have to use .CTB file type, unfortunately it's disabled on .GOO but that's not obvious unless you know that.
> > > > > 
> > > > > > **dar\_mach** · [2026-07-18](https://reddit.com/r/resinprinting/comments/1uze9he/comment/oyb5skq/) · 2 points
> > > > > > 
> > > > > > Conducted few tests, did not manage to get validation matris to look any decent - still looks like its bloated, like melting. Switched to cones of calibration just to test, an dI do have \*some\* results.
> > > > > > 
> > > > > > May I bother you some more? :)
> > > > > > 
> > > > > > > **awyeahmuffins** · [2026-07-18](https://reddit.com/r/resinprinting/comments/1uze9he/comment/oyb74rh/) · 1 points
> > > > > > > 
> > > > > > > Sure go ahead!
> > > > > > > 
> > > > > > > > **dar\_mach** · [2026-07-18](https://reddit.com/r/resinprinting/comments/1uze9he/comment/oyc1v1o/) · 1 points
> > > > > > > > 
> > > > > > > > Settings for the test - 6 pieces of Cones:
> > > > > > > > 
> > > > > > > > ![评论图像](https://preview.redd.it/saturn-4-ultra-16k-another-post-about-validation-matrix-v0-7j1e482mu0eh1.png?width=482&format=png&auto=webp&s=23abd1b305157ea8af989326be929afe8fe1977a)
> > > > > > > > 
> > > > > > > > Results:  
> > > > > > > > All were roughly 6mm within 0.02mm, the best (~2.1-2.1) were spot on.
> > > > > > > > 
> > > > > > > > Exposure - cup result - sword result - support result.
> > > > > > > > 
> > > > > > > > 1.7s - cup falls out - sword fits the tight hole - all supports ok  
> > > > > > > > 1.9s - cup loose too - sword ok - first (+) support failed  
> > > > > > > > 2.1s - cup gets in easy, a tiny bit loose - sword ok - supports ok.  
> > > > > > > > 2.3 - cup fits have to hit hard to get it out - sword ok - supports ok, hard to get stuff off supports (skull, sword)  
> > > > > > > > 2,5 - cup fits unable to pull out - sword perfect - all supports
> > > > > > > > 
> > > > > > > > All Z height 5.75 on the 6mm block. I assume layer compression - would using thicker paper during manual leveling help? (I might calibrate different Z height for tension sensor trigger)
> > > > > > > > 
> > > > > > > > Judging from the above I would say 2.4 might be the sweet spot - could I bring back some UV light power (that one was 75%) and shorten the times?
> > > > > > > > 
> > > > > > > > > **awyeahmuffins** · [2026-07-18](https://reddit.com/r/resinprinting/comments/1uze9he/comment/oyc6cbu/) · 2 points
> > > > > > > > > 
> > > > > > > > > Personally I value getting supports off easier than I do 100% dimensional accuracy (in general the cones are not a great dimensional accuracy test, but they do give a ballpark). So I would trend towards 2.1-2.2s, but that's more of a personal preference - depends on what you are printing and how accurate you're looking for. Seems like 2.1 - 2.4s should all be viable.
> > > > > > > > > 
> > > > > > > > > You could re-level, but before you do I'd recommend trying a calibration with 40s Rest Time After Retract / Wait Before Cure. That's usually the best way to combat z-compression on the 16k, although typically the compression issues end up with thicker rafts. I don't think using thicker paper during manual leveling would help (and would probably cause issues with first layer failures) - it uses the force sensor during printing, but the issue with more viscous resin is that there has not been enough time for the resin to flow out from underneath the build plate so you end up curing too soon. This becomes more of an issue at lower layer heights.
> > > > > > > > > 
> > > > > > > > > Luckily PWM and time is communicative so if you have 2.4s at 75% you could make it 1.8s at 100%, or 2s at 90%, etc.
> > > > > > > > > 
> > > > > > > > > > **dar\_mach** · [2026-07-19](https://reddit.com/r/resinprinting/comments/1uze9he/comment/oyffari/) · 1 points
> > > > > > > > > > 
> > > > > > > > > > Hmm, how about these supports. That's the thing I never sorted out on Mono 4, switched to ball supports (allegedly better?) and tinkered with sizes, but never for to the point where they looked decent. Or maybe my expectations are unrealistic. This is what I was getting on the top (bottom?!) layers - the ones on the build plate side. Flowy-like resin and support holes on ball supports.
> > > > > > > > > > 
> > > > > > > > > > ![评论图像](https://preview.redd.it/saturn-4-ultra-16k-another-post-about-validation-matrix-v0-7ez6idg5m4eh1.png?width=1224&format=png&auto=webp&s=dcb68a8e55642811f777ec652a41dfc27991ab3d)
> > > > > > > > > > 
> > > > > > > > > > Maybe shortening bottom exposure time would help to remove that "flowy / gooey" look on the bottom surface? I have to give this a try on the saturn yet.

> **thedisliked23** · [2026-07-18](https://reddit.com/r/resinprinting/comments/1uze9he/comment/oy7uw92/) · 1 points
> 
> Cones of calibration.
> 
> The sword never lies. Perfect calibration on all my printers and requires no eyeballing of anything.