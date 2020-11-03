# Ragdoll

Real-time physics for Autodesk® Maya 2020

<a class="button" href="download">Download v{{site.ragdoll_version}}</a>

Ragdoll enables **animators** to work directly with **live physics** in their character rigs, at a 0-5 ms/frame performance impact.

- [Real-time full body dynamics](#fbd)
- [Real-time hair](#hair)
- [Real-time cloth](#cloth)
- [Real-time muscles](#muscle)

The results can either plug straight into final render or give technical animators a physically realistic starting point for e.g. high-resolution folds in clothing, volumetric fascia simulation and skin sliding.

<br>

<!-- <h2 class=usp id=fbd>RFBD<img src=https://user-images.githubusercontent.com/47274066/97966499-d41db400-1db3-11eb-946a-9cac61feddf0.png></h2> -->
<h2 class=usp id=fbd>RFBD <img src=https://user-images.githubusercontent.com/47274066/97966499-d41db400-1db3-11eb-946a-9cac61feddf0.png></h2>

Animate like it's 1999, or leverage *Full Body Dynamics* to automate the vast majority of secondary animation, that respond to changes in environment and interacts with other characters. Your choice.

![ragdollfbd](https://user-images.githubusercontent.com/47274066/97965511-63c26300-1db2-11eb-94bf-0a197b3bca95.gif)

<h2 class=usp id=muscle>Muscle <img src=https://user-images.githubusercontent.com/47274066/95461832-983b2e80-096e-11eb-9b9e-b2eb90bc66bd.png></h2>

Suffer the performance impact of corrective blendshapes and pray that the subsequent muscle simulation won't mess up the silhouette of your finished animation. Or, work with muscles directly as you animate. Your choice.

![ragdollstrongman2](https://user-images.githubusercontent.com/2152766/95451419-a6ce1980-095f-11eb-85cc-1a8c52ceb179.gif)

<h2 class=usp id=hair>Hair <img src=https://user-images.githubusercontent.com/47274066/95461849-9cffe280-096e-11eb-8a7a-f2152a4ea30e.png></h2>

Animate each individual strand, respond to the overall motion of the body and take care not to intersect. Or, animate with physically accurate hair in real-time. Your choice.

![ragdollhair3](https://user-images.githubusercontent.com/2152766/95451343-8f8f2c00-095f-11eb-9f43-9880e5871d59.gif)
 
<h2 class=usp id=cloth>Cloth <img src=https://user-images.githubusercontent.com/47274066/95461823-95d8d480-096e-11eb-96d8-04daf71690dc.png></h2>

Imagine what cloth will eventually look like weeks after you're finished animating, or work with it directly as you animate. Your choice.

![ragdollskirtwind3](https://user-images.githubusercontent.com/2152766/95451361-94ec7680-095f-11eb-8656-a47232c64bdd.gif)
 
<br>
<br>

## Features

- **Performance** 0-5 ms/frame, from a single box to a full character with skeleton, hair, cloth and muscles running in parallel with native and interactive forwards and backwards caching, with additional support for Cached Playback in Maya 2020+
- **Stability** Simulate anything from anatomically correct skeletons to complex mechanical contraptions
- **Collision Detection** Exactly what would would expect from any self-respecting physics solver
- **Constraints** Point, Orient and Parent constraints; just like regular Maya constraints, except physical!
- **Natural Forces** Push, Pull and Turbulence for perfect integration into any environment
- **Rewind and Continue** Play forwards and backwards without ever having to worry about returning to frame 1. Suck on that, nCloth!
- **Active Control** Balance animation and physics with life-like control over "virtual muscles"
- **Anatomical Limits** Precise control over the angle each limb or chain can attain
- **Determinsm** Trust that every playthrough is identical to the last, even on different machines and operating systems.
- **Python API** Precise integration into your pipeline with this first-class API, built with the fast and flexible [cmdx](https://github.com/mottosso/cmdx)

<br>

## Tutorials

[![image](https://user-images.githubusercontent.com/47274066/95450416-2c50ca00-095e-11eb-90c9-a3c671f99c58.png)](https://youtu.be/mJFRmRGthMw)

[![image](https://user-images.githubusercontent.com/47274066/95450438-3377d800-095e-11eb-856c-94b6d634fbdb.png)](https://youtu.be/HsyCGfuim0k)

[![image](https://user-images.githubusercontent.com/47274066/95450452-383c8c00-095e-11eb-82b0-09954e2c706c.png)](https://youtu.be/sKESMr5lyz0)

<a class="button" href="howto">More</a>

<br>

##### Legal

> - "Just a Girl" modeled by [腱鞘炎の人](https://sketchfab.com/3d-models/just-a-girl-b2359160a4f54e76b5ae427a55d9594d), modified
> - "Super Human" modeled by [Davyd Vidiger](https://sketchfab.com/3d-models/super-human-7aa58e978b9f4357b8e73d8e0440c896), modified
> - "mGirl" modeled by [鈴木 一平](https://github.com/mgear-dev/Data-centric_rigging_sample_data), modified
