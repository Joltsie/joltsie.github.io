---
# type: docs 
title: Sylvafen Release v1.4.0 has been released! Also what I'm doing next.
date: 2025-06-15T11:34:47+08:00
featured: true
draft: false
comment: true
toc: false
reward: true
pinned: false
carousel: true
series:
  - News
categories: []
tags: []
authors:
  - Joltsie
images: []
---

T-Pose for dominence

<!--more-->

#### Sylvafen 1.4.0

Alright so first order of business, The Sylvafen 1.4 update has finally dropped. It's not super exciting on the surface but there's been a lot of internal changes to improve maintainability and third-party asset compatability. You *will* need to make a new project for this. There's a lot of changes here that will break your existing projects if you try to overwrite things with the new package. Here's a breakdown of the big changes:

##### T-Pose
The Sylvafen, along with all of its officially released outfits and clothing items, have been converted to T-Pose from A-Pose. This was done simply to improve compatability with generic clothing items and accessories that weren't made by me.

As it turns out, the vast majory of VRChat assets are primarily made in T-Pose and it's something I didn't account for when making the Sylvafen. As an artist, A-Pose is very nice for modeling shoulder definition and retopologizing after the sculpt stage and is why I originally stuck with A-Pose.

##### Shaders
The primary shader of choice has been changed from Poiyomi to Standard Toon. This is a new shader introduced with VRChat SDK Version 3.8.1. It's cross-platform compatable, looks great, is highly performant, and has most of the features I'd want out of the box. Using it means that any shadder toggle I introduce works on all platforms and means that both platforms will perform the same under similar lighting conditions. It also means one less dependency that's needed for the avatar to work which is always a good thing in my book.

Poiyomi isn't going anywhere! I'm looking to support it on current and future avatar releases. It is still a cut above in terms of visual fidelity and has a few features that will likely never be supported on official shader options (Namely of interest to me, LTCGI and VRCLightVolumes). I'll still be supporting it as a first-class option with included toggles for the forseeable future and will look for more ways to integrate compatability between the two shaders for people who do go through the trouble to upload and maintain a Quest version of their avatar.

##### Quest Poor Rating
The Sylvafen is now poor rated and under 20,000 triangles with any single official clothing item/outfit! This was a huge undertaking but the release of Avatar Marketplace was a huge motivator to finally get it done. In the future, I'll be making this a target from the start as it's much easier if I keep it in mind throughout the initial creation stages.

Here's the full notes for those interested:

> [!NOTE]-Patch Notes (Click Me)
> 06/10/2025 | 1.4.0
>- Fixed collar weighting - Physbones should work again
>- Massively simplified prefab variant hierarchy. You now only have Sylvafen_PC and its child, Sylvafen_Quest
>    - This was done in the name of increased modularity and making upload/build times faster
>- Moved default outfit into it's own prefab, making it more modular for those that don't want it
>- Greatly optimized Quest/Mobile prefab - Poor rating with any single outfit!
>- Bundled all third-party assets with the Sylvafen package to reduce the need for dependency management
>- Migrated to from Poiyomi to VRChat's new and very excellent Standard Toon shader
>    - Once again, this is to greatly reduce external asset dependency. This also makes shader toggles/settings perfectly synced between     platforms
>- Moved clothes prefab folder into the Sylvafen root folder
>- Removed collar prefab as it's now part of the base
>- Converted base model and all clothing from A-Pose to T-Pose; improving compatibility with third-party assets
>- Added ear fluff toggle
>- Fixed misnamed blendshape (LegChug) on clothing
>- Fixed socks clipping through hand in certain poses when hidden
>- Fixed Harness clipping with certain body shapes
>- Minor Substance file cleanup
>- Created new easier to use Face-Tracking prefab - now packages ADJerry's template into the project without needing an external download

#### I am now unemployed
Yeah so, I've been employed on and off in some capacity for the past few years. It's always been a bit rough for me. I'm a highly creative and self-driven person. Working for people and things I don't particularly care about or feel invested in is always difficult for me to stick with. The regular income is nice of course; I need money to live and survive off of. I have real bills to pay. But I find myself getting progressively more downtrodden and depressed after the initial couple months. I've traditionally worked in the diesel and automotive industry and I've been pretty successful at it but It's just not personally rewarding for me.

Anyways, I found myself at my last job back in November and stuck with it for the past 7 months. In that 7 months, that business took a nosedive and paycheck security was becoming a real concern for me. Things ended up coming to a head financially at the end of May and I took off before the inevitable happened.

So now I'm here, unemployed and actually quite happy about it. I have a couple months of expenses saved up and I'm going to take a bit of a gambit with this whole online 3D artist thing. The Sylvafen is decently successful but nowhere near my real living costs. I think I can make things work though if I play my cards right.

#### So here's the plan for the next 2 months:

##### 1. Continue to support the Sylvafen
- The release of v1.4.0 was the first step of this. I want to make the Sylvafen easier to maintain and make additional content for (both myself and others).
- Update documentation to make current and future avatars easier to use and more approachable.
- Introduce the Sylvafen NSFW DLC. I'm not sure how I want to roll this one out from a publicity standpoint but I'll figure something out. :wink:
- Make a video trailer for both the SFW and NSFW versions! The Sylvafen is still a relatively unknown avatar and could do with another good marketing push. Easily-sharable, short videos could do wonders.
##### 2. Roll out a Patreon
- Surprisingly a lot of people have been asking for this one! Some form of reoccurring support would be a huge boon to my financial situation and smooth out the huge bumps that come from the avatar release cycle.
- Start out as a sort of reoccurring donation platform and introduce additional features from there. Tutorials? Avatar assets? Maybe avatar catalogue access at a certain tier (once I have more than one avatar out, of course). Lots of ways I could go with it.

##### 3. Start a new avatar!
- Obviously can't have an avatar career without making more avatars. I'm thinking something cat-like!

Thanks all for now, thanks for reading!