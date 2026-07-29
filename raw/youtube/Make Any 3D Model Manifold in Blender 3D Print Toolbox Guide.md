---
title: "Make Any 3D Model Manifold in Blender: 3D Print Toolbox Guide"
source: "https://www.youtube.com/watch?v=beAfWDEdjCc"
author:
  - "[[What Make Art]]"
published: 2025-09-25
created: 2026-07-23
description: "Want reliable, watertight 3D prints? In this quick Blender tutorial, we use the 3D Print Toolbox to check for non-manifold geometry and repair it for clean, ..."
tags:
  - "videos"
---
![](https://www.youtube.com/watch?v=beAfWDEdjCc)

## Transcript

### What “manifold/watertight” means for 3D printing

**0:00** · How do you check if a 3D model is manifold or watertight?

**0:04** · In order to 3D print something successfully, it's a good idea to have a model that doesn't have any holes and is fully watertight and doesn't have any extra pieces on the inside.

**0:15** · There are many ways to do this, but an easy way is to use blender.

### Install and enable the 3D Print Toolbox add-on in Blender

**0:18** · Inside blender, you can install the 3D Print Toolbox add on.

**0:23** · There's a link in the description on how to install the 3D Print Toolbox add on, and that way you can make your 3D mesh manifold for 3D printing inside blender.

### Open panel: N key → 3D Print → Check All

**0:31** · Once you have the add on installed, press N, then click on 3D print.

**0:36** · You can check all and it'll give you a report.

**0:41** · After it's done checking, it'll give you a report on how many non manifold edges add contiguous edges, intersect faces, zero faces, zero edges, non flat faces, thin faces, sharp edges and overhanging faces.

### Why non-manifold edges matter most for 3D printing

**0:55** · The most important one for 3D printing is the non manifold edges.

**0:59** · If you twirl out cleanup simply click Make manifold.

**1:04** · This will go through the process of making the model manifold for 3D printing.

### Make Manifold: automatic cleanup and result overview

**1:09** · It modified 132 vertices, 402 edges, and 261 faces.

**1:15** · Then if I click check all again.

**1:18** · Then we can see that now there are only four non manifold edges.

**1:22** · If you want to track down those last four non manifold edges, you can click your model, then tab in edit mode then select this.

### Find remaining problem edges in Edit Mode (Select → Non-Manifold)

**1:31** · This will highlight the edges.

**1:33** · And then you can go around into the model to find them.

**1:36** · It can sometimes be hard to see.

### Frame and inspect hard-to-see areas

**1:38** · So you can go view frames select it and then it's going to frame where those non manifold edges are.

**1:46** · And they're in here somewhere.

**1:48** · And sometimes what you can do is just press X to delete those edges.

### Delete bad edges, re-check results

**1:54** · And then we can check all again.

**1:56** · now it has five non manifold edges.

**1:58** · That's because we probably created a hole.

**2:00** · So if I click make manifold.

### Fill holes with Make Manifold to fix new gaps

**2:03** · It added one face.

**2:04** · That's exactly what we want it to do.

**2:06** · So now if I click check all again most likely it will have zero non manifold edges.

**2:13** · Now we have zero non manifold edges.

### Confirm zero non-manifold edges

**2:16** · In this particular case deleting the edges was the easiest thing to do.

**2:20** · Sometimes you might see a triangle hanging off the edge and then you can just delete the face.

**2:25** · That's always different depending on your particular model.

**2:28** · Now that I have a clean manifold mesh, I can go ahead and export it as an STL.

**2:33** · Just go to File Export STL.