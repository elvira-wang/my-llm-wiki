---
title: "Ring failing to print correctly and I can't figure out why!    环形物无法正确打印，我搞不清楚原因！"
source: "https://www.reddit.com/r/blenderhelp/comments/1uxyb0t/ring_failing_to_print_correctly_and_i_cant_figure/"
author:
  - "[[Low_Alternative8749]]"
published: 2026-07-16
created: 2026-08-03
description: "I have been trying to make an Arsenal ring for my nephew's 18th birthday. I'm very new to CAD, and so incredibly happy with my effort, but f"
tags:
  - "reddit"
---
I have been trying to make an Arsenal ring for my nephew's 18th birthday. I'm very new to CAD, and so incredibly happy with my effort, but for some reason when it comes to print, it keeps failing to print the emblem I've embedded in the base of the ring. It shows up fine in Blender and looks great, but as soon as I load it up in chitubox, it looks like the emblem is not there or something... it's odd.  
我一直在努力为侄子 18 岁的生日制作一枚阿森纳主题的戒指。我对计算机辅助设计非常陌生，所以对我的作品效果相当满意。不过，奇怪的是，在尝试将戒指上的徽章打印出来时，总是出现问题——虽然徽章在 Blender 软件中显示得很不错，但在将戒指导入 Chitubox 软件后，徽章就消失了，或者看起来不太对劲……真是奇怪。

There are 2 components here. 1 is the base of the ring, the second is the arsenal emblem which I've turned into a mesh, Extruded on the Z axis and embedded into the base. As you can see from my screenshots, it looks like how I want it to in Blender, but then on the final print, it looks like the emblem itself isn't printing, but it instead acting almost like I've chucked a boolean modifier on it and it's just cut into the ring face rather than being attached to it.  
这里包含两个部分。第一部分是戒指的基础结构，第二部分则是武器标志的模型。我把这个武器标志模型转化为网格格式，然后在 Z 轴上进行拉伸处理，最后将其嵌入到基础结构之中。从我的截图可以看出，效果确实符合我在 Blender 中的设计意图。不过在实际打印过程中，武器标志似乎并没有被打印出来，而是好像被一个布尔修改器处理了一下，最终只是被切割到了戒指的表面，而没有真正附着在戒指上。

I can't see any holes or gaps in the emblem that would be causing a leak, and I can't figure out for the life of me how to fix this.. Any ideas? Like I said, I'm still very new to this, so if this is a thicky thicky dumb dumb query, please go easy on me, I'm just trying to do something nice for my nephew. I am happy to upload the .blend file if needed. I just want to get this sorted and cast before my sister comes over in August  
我在这个徽章上看不到有任何可能导致泄漏的孔洞或缝隙。但我完全不知道该如何修复这个问题……有没有什么办法吗？就像我说的，我对此还很陌生，所以如果这真是个复杂的难题，请尽量耐心一些吧。我只是想为我的侄子做一件好东西而已。如果需要的话，我很乐意上传那个 Blend 文件。我希望能在 8 月份姐姐来访之前解决这个问题。

---

## Comments

> **AutoModerator** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxuuz73/) · 1 points
> 
> Welcome to [r/blenderhelp](https://www.reddit.com/r/blenderhelp/), [u/Low\_Alternative8749](https://www.reddit.com/user/Low_Alternative8749/)! Please make sure you followed the rules below, so we can help you efficiently (This message is just a reminder, your submission has NOT been deleted):
> 
> - Post full screenshots of your Blender window (more information available for helpers), not cropped, no phone photos (In Blender click Window > Save Screenshot, use Snipping Tool in Windows or Command+Shift+4 on mac).
> - Give background info: Showing the problem is good, but we need to know what you did to get there. Additional information, follow-up questions and screenshots/videos can be added in comments. Keep in mind that nobody knows your project except for yourself.
> - Don't forget to change the flair to "Solved" by including "!Solved" in a comment when your question was answered.
> 
> Thank you for your submission and happy blendering!
> 
> *I am a bot, and this action was performed automatically. Please* [*contact the moderators of this subreddit*](https://www.reddit.com/message/compose/?to=/r/blenderhelp) *if you have any questions or concerns.*

> **igg73** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxuweg9/) · 209 points
> 
> Im pretty new but i always make sure ofa few things: apply scale and rotation. Check to make sure all normals are properly facing. Merge by distance to make sure any weird ovverlapping or duplicate vertexes are merged, and then make sure everything is manifold. Idkif thatl help but i figure id try to give you my first troubleshooting go-tos. Goodluck!  
> 我刚加入这个团队，但我总是会确保做到几件事：应用缩放和旋转操作；检查所有法线是否指向正确的方向；使用距离合并功能来消除任何重叠或重复的顶点；然后确保整个模型是光滑的。不知道这些建议是否对你有帮助，不过我想我会尝试分享一下我的处理经验。祝你好运！
> 
> > **Low\_Alternative8749** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxuzyjr/) · 190 points
> > 
> > OH! YOU ABSOLUTE BEAUTY! This looks like it might have been it! I checked the face orientation and the emblem was red af. I flipped the normals and it now looks right in chitubox! You sir, are a f\*cking don! Thank you so much!  
> > 哦！您真是美丽极了！看来这个就是您说的那个了！我检查了面部的朝向，发现徽章确实是红色的。我把模型翻转了一下，现在在 Chitubox 中看起来很合适了！您真是太棒了！非常感谢您！
> > 
> > ![评论图像](https://preview.redd.it/ring-failing-to-print-correctly-and-i-cant-figure-out-why-v0-ljpk1353kkdh1.jpeg?width=2992&format=pjpg&auto=webp&s=a0d77c60fc98d095afb11daad4d20feee4b37e3b)
> > 
> > > **chicolince** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxvm1hp/) · 32 points
> > > 
> > > I always activate the see normal orientation thing in every project. Imo it should just be active by default. No project would look well if normals arent the proper way  
> > > 我在每个项目中都会启用“显示正常朝向”功能。在我看来，这个功能应该默认是开启状态的。如果正常朝向不是正确的方式，那么任何项目看起来都会很糟糕。
> > > 
> > > > **Psychonaut-n9ne30** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxwmhoh/) · 8 points
> > > > 
> > > > You can change the default startup by using  
> > > > 你可以通过以下方式更改默认启动设置：  
> > > > Files>defaults>save startup file  
> > > > 文件>默认设置>保存启动文件  
> > > > That way you don’t have to set up your preferences every time  
> > > > 这样你就不必每次都重新设置你的偏好设置了。
> > > > 
> > > > > **chicolince** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxwuzpj/) · 2 points
> > > > > 
> > > > > I will thanks
> > > 
> > > > **\-skyrocketeer-** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxwv101/) · 2 points
> > > > 
> > > > This! Turn on Face Orientation in your Viewport Overlay. Then in your 3D Viewport settings in your Theme colours, lower the Alpha value for Face Orientation Front, right down to zero. This will allow your viewport to still look the same, but if you happen to have a face normal that's been flipped, only that face will show in the selected colour (a light red colour by default).
> > > > 
> > > > Don't forget to save these settings to your startup file so they apply every time you start a new project.
> > 
> > > **igg73** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxxji49/) · 5 points
> > > 
> > > Im glad i could help. Im very beginner but thats my checklist for when things arent slicing right before a print. This community is so helpful, im stoked i got to be on the helping side for once. Hope to see the printed product Best wishes
> > > 
> > > > **Low\_Alternative8749** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxyjfgz/) · 11 points
> > > > 
> > > > Here's a side by side of the correct print (left) and failed one (right). It's night and day@ once I've cast it, sanded, polished and got the patina on, i'll send an update of the final product :) thanks so much for the help man. Really made my day
> > > > 
> > > > ![评论图像](https://preview.redd.it/ring-failing-to-print-correctly-and-i-cant-figure-out-why-v0-vjbz7cndgndh1.jpeg?width=2992&format=pjpg&auto=webp&s=a75cc6a8bd512a718dcce89aaef7fba1578e2a4f)
> > > > 
> > > > > **igg73** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxytvco/) · 2 points
> > > > > 
> > > > > Score
> > 
> > > **torlopoff** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxy3va5/) · 5 points
> > > 
> > > Show the final result plz
> > > 
> > > > **Low\_Alternative8749** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxyix9m/) · 6 points
> > > > 
> > > > ![评论图像](https://preview.redd.it/ring-failing-to-print-correctly-and-i-cant-figure-out-why-v0-s2vxs7rzfndh1.jpeg?width=2992&format=pjpg&auto=webp&s=d8f1893e049f068914ac4154b8ac9b8bf680a9de)
> 
> > **Low\_Alternative8749** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxuy13g/) · 15 points
> > 
> > How do you mean check normals are properly facing? Sorry if that's a daft question, but I've not heard that term before
> > 
> > > **Bleiz\_Stirling** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxv09qg/) · 25 points
> > > 
> > > Basically, every face has an outside and an inside. Imagine a cube: you know what is outside and what is inside.
> > > 
> > > Sometimes, you end up with faces orientated the wrong way, which cause various issues. Go into the "Show Overlays" dropdown and check "Face orientation": you model will turn red and blue: the red is supposed to be the inside, and the blue the outside.
> > > 
> > > Also: I think your ring is 2 items, actually? I'm pretty sure it should be one single item, in order to be printed.
> > > 
> > > **dnew** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxwrnk9/) · 4 points
> > > 
> > > What he said. Note that if you go into the themes and turn up the alpha on the "outside" color so it's transparent, you can just leave it turned on all the time and just see red where it's wrong.
> > > 
> > > Also, when asking questions about 3D printing, showing the g-code preview can often help people analyze why you're not getting the results you want. For future questions. :-)
> > > 
> > > Great channels for 3D printing with Blender: Keep Making (especially the Precision Modeling playlist) and Artisans of Vaul (for more artistic stuff like TTWG models).
> > > 
> > > A non-manifold edge is one that doesn't have exactly two faces on it. (Holes, edges sticking out from the model, etc. Mostly caused by holes.) To be manifold, you need all edges to have two faces, all verts to be on an edge, faces not intersecting, and (because it's a modeler and not a math thing) faces all having their normals pointing outwards. The "fix non-manifold" in the 3d print toolbox does a poor job on most problems, because if you could automated it, it would have already been done. :) Faces that aren't flat will also give you a bit of a problem, but not as much; you'll just get weird seams in your print that might not even be visible if the face is small enough. And again, Keep Making has a video specifically on 3d print toolbox and how to use it.
> > > 
> > > > **Low\_Alternative8749** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxyk1pd/) · 2 points
> > > > 
> > > > Thanks for this buddy. That's a really clear and thorough explanation! Much appreciated
> 
> > **\-TheTalkingTree-** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxwh92k/) · 2 points
> > 
> > Well done giving accurate advice as a beginner!
> > 
> > > **igg73** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxxjpcb/) · 2 points
> > > 
> > > Thanks Tree, have a great weekend!

> **MrVishwamitra** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxv3isq/) · 33 points
> 
> try manchester once
> 
> > **Icy\_Back2726** · [2026-07-18](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oy7szie/) · 1 points
> > 
> > you mean united right? right? 🙏 🙏 🙏 I need someone else to like united too

> **AshKetchumYO** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxuwi1m/) · 20 points
> 
> Theres a plugin built into blender called 3d toolkit. Activate it and check if your geometry is manifold. Otherwise also check if normals are flipped
> 
> > **Low\_Alternative8749** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxuxxcq/) · 4 points
> > 
> > So This was one of the things I tried. When I run a check, it says there are 45 non-manifold edges. When I run a clean up to make manifold, this drops to 20... but it also causes weird, visible gaps and distortions, which I then can't fix.. Not sure why that's happening as there's nothing there to begin with other than a lot of edges that are maybe overlapping?
> > 
> > ![评论图像](https://preview.redd.it/ring-failing-to-print-correctly-and-i-cant-figure-out-why-v0-q6gjkpc9hkdh1.png?width=2560&format=png&auto=webp&s=d01f522982111058d3941d6a12763a321e54cece)
> > 
> > > **Salty\_Salad\_5061** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxvg2st/) · 2 points
> > > 
> > > You can go to select in the menu bar and there is a select all the non manifold edges option. Sometimes they are just loose geometry and you can delete them. It wil at least show you where the non manifold parts are.

> **The\_RealAnim8me2** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxvpis3/) · 10 points
> 
> Probably because it’s Arsenal. Always chokes at the end. /s
> 
> Sorry, I’m also a gunner.

> **Curis** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxv0i9t/) · 2 points
> 
> The text isn't properly connected with the face below it. If you upload the .blend I can fix that for you easily.

> **Green\_Device3131** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxvtn5h/) · 2 points
> 
> bro thats face oreientation issue, or the part isnt one mesh or it has non manifold regions. inbox me i will help you deal with this.

> **bigleroy24** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxvtpe8/) · 2 points
> 
> Coyg!

> **Low\_Alternative8749** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxuwjzx/) · 1 points
> 
> ![评论图像](https://preview.redd.it/ring-failing-to-print-correctly-and-i-cant-figure-out-why-v0-0we1ytsefkdh1.png?width=2560&format=png&auto=webp&s=362edf7c78959b53ef0a543075e32980ca3fddd6)
> 
> I cannot add pictures to my post, and apparently my screenshots did not follow the rules :S Sorry. I'll re-post them in full here and hope that helps
> 
> > **Low\_Alternative8749** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxuwkv3/) · 1 points
> > 
> > ![评论图像](https://preview.redd.it/ring-failing-to-print-correctly-and-i-cant-figure-out-why-v0-sdysvrhkfkdh1.png?width=2560&format=png&auto=webp&s=2d1b6858302c2b54a1f2aad151ff9df88beb7125)

> **Aenieweddien** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxvy3n8/) · 1 points
> 
> I'm pretty much noob also, but every time when I model something for 3d print from curves(and then maybe even use boolean modifier on resulting mesh) its a huge pain in the ass. What I found working for me. Extrude curve, turn it into mesh, then apply voxel remesh modifier. Your face count skyrockets, but don't think it matters for 3d print. Voxel remesh is super useful in case of 3d print, cause it generates manifold mesh

> **marmeden** · [2026-07-17](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oy04qbd/) · 1 points
> 
> Which filament you plan to use for the final version?

> **RobHood19** · [2026-07-16](https://reddit.com/r/blenderhelp/comments/1uxyb0t/comment/oxwrwxh/) · \-1 points
> 
> Wrong logo.