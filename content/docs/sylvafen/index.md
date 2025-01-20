---
date: 2022-09-06T22:42:23+08:00
title: Introduction
navWeight: 1000 # Upper weight gets higher precedence, optional.
linkTitleIcon: <i class="fas fa-fw fa-book"></i> # The icon of the link title, optional.
series:
  - Guide
---

Sylvafen v1.3 Release

Thank you so much for purchasing The Sylvafen! This is my very first avatar release and I've put a lot of love and care into them. Your support really means a lot to me. <3
Don't hesitate to bother me in the Discord if you have any questions, issues setting up, or just want to show off your Sylvafen, I don't bite <3

---

BASIC AVATAR SETUP INSTRUCTIONS

1. Install VRC Creator Companion (https://www.youtube.com/watch?v=0u1g0TYoJsU) and the appropriate Unity version using it
2. Make a new Unity project using VRChat's Creator Companion
3. Add the Avatars SDK (Built-In), VRCFury (https://vrcfury.com/download/) and Poiyomi (https://github.com/poiyomi/PoiyomiToonShader) VCC packages to your newly created project using the creator companion
4. Open your newly created Unity Project
5. Unzip the avatar zip into a new folder and drag the .unitypackage file into your Unity
6. Open the provided Unity scene
7. Open the VRChat SDK in Unity, log in, and then upload

---

PREFAB VARIANTS

This avatar uses a prefab for the PC version with the Quest version being a Prefab Variant of Sylvafen_PC_Base. This means that if you edit the prefab directly instead of editing the scene, you can have your avatar edits effect your Quest version and all other versions as well. Highly recommend using this workflow if you intend on extensively modifying your Fen while wanting to keep the avatar cross-platform

The 'Standard' prefabs are the default without color/texture swaps for better VRAM usage.
The 'Public' prefabs are mostly indentical save for the inclusion of the advertisement and additional color sliders/texture toggles found in the public one.
The 'Face-Tracking' prefabs are face-tracked, being integrated with ADJerry's FT template and utilizing the 'Ulimited Params' component from VRCFury to cram it all in there.

---

FACE TRACKING
The face-tracking prefabs rely on ADJerry91's face tracking template. Add it to your project via VRChat's Creator Companion by using this URL and adding the repository and sebsequently adding it to your project (https://adjerry91.github.io/VRCFaceTracking-Templates/).

Then simply add one of the face-tracking prefabs to your scene and upload!

---

TEXTURES

If you make your own custom textures, I would recommend copying the texture settings of the existing textures (or overwriting the originals). There's various settings in there meant to fix rendering artifacts ingame (like around the eyes, for example) and to optimize the Quest textures for upload (very important with the limited upload size of 10mb).

---

PC/QUEST INTEROPERABILITY

The PC and Quest versions are nearly identical in function but they have a few differences

1. The hue shift options are only work on PC. Quest users will see the non-shifted version of your texture.
2. The blushing present on certain gestures is only visible on PC
3. No toe, whisker, nose, or butt physics on quest
4. Lighting options are PC only

---

VRCFURY/TOGGLES/PARAMETER BITS

Parameter space is very limited in VRChat and as such, this project makes heavy use of VRCFury for implementation of much of the avatar's customization functionality. Most things can be added or deleted just by deleting the associated game objects in the Avatar's hierarchy (Including GoGo Loco).

Objects that are safe to delete have the number of parameter bits they used listed next to their name. Much if this functionality can be done through editing the Body's blendshapes manually and is unnessesary if you don't need to modify these while in-game.

This makes it easy to make more paramater space for things you want to add!

---

BLENDER/SUBSTANCE EXPORT SETTINGS FOR BASE EDITORS

For advanced users. Refer to "Docs/FBXExportSettingsUnity.png" and "FBXExportSettingsSubstance.png"

Unity FBX export settings. Overwrite the existing FBX in your Unity assets. Make sure not to accidentally include the Substance Painter mesh.

The exploded model for Substance is in the .blend file. Export that and the base mesh using the settings above.

---

TROUBLESHOOTING

"I see a bunch of scripts that say 'None (Mono Script)'"
This happens if you don't have VRCFury added in your Unity Project. Also make sure you're using the most recent Avatars SDK

"My upload size is too large for Quest"
If you're adding your own textures, make sure you copy the texture settings (specifically the overrides for Android) from the existing textures to make them smaller and compress more to fit the strict avatar size limit that the Quest has.

"My custom body texture seems to be lower quality than the originals"
In your custom texture's settings, make sure your Max Size is set to 4096 (i.e. 4k) (PC Only, keep your Android Max Size at 2k or lower). Be default, Unity sets the max to 2048.

"My eyes don't change color when I apply my custom texture"
The Bits texture is applied in two different places in the Bits material. You need to change the one in the 'Decals' section as well.

"My unpacked avatar size seems unusually large"
This is a symptom of all the texture options on the avatar. If you are happy with just one of the texture options, just deleting the 'Texture Swap (6 Bits)' and 'Clothes Texture Swaps (PC/Quest)' objects in your avatar components and setting the texture you want manually in the material before uploading will bring this size down by over half.

"I'd like to hide my hair and use my own"
The easiest way to accomplish this would be to shrink the HairRoot bone and then move it inside the head. Then attach your own preferred hair mesh.

"My eye texure isn't applying correctly"
There's two slots you need to replace the 'Bits' texture in the Bits Material. One is the main texture and then there's another slot under the decals.

"My face tracking prefab is missing components or isn't uploading"
Make sure you have AdJerry91's face tracking template installed via VCC (https://adjerry91.github.io/VRCFaceTracking-Templates/)

---

CHANGELOG

01/08/2025 | v1.3.3
- Fixed boob bone weights clipping through clothes
- Re-ordered body customization blendshapes
- Fixed floor collider toggle not working
- Fixed extra face animation toggles not saving between worlds
- Organized 'Default' outfit into it's own menu folder, reducing menu clutter for those using DLC outfits
- Remade the toggle functionality of the Default outfit, allowing it to completely disable rendering if none of the pieces are being shown
- Fixed an issue with Quest Sylvafen package size being too large to upload by default

10/29/2024 | v1.3.2
Hotfix
- Cleaned up weight painting around hands

10/28/2024 | v1.3.1
Hotfix
- Fixed boob blendshape clipping
- Fixed potential issue for those using Gesture Manager by clearing out the 'Controller' field on the prefab animators

10/28/2024 | v1.3.0
Face Tracking, Performance Improvements, VTubing, and Polish
- Updated ToS to allow cloneable/public uploads on VRChat
- Improved Boobs blendshape
- Added floof-pressing blendshape for hoodie
- Improved normal blending around base of ear floofs
- Fixed tail collider toggle
- Fixed shoulder floof not hiding at correct times with harness asset equipped
- Cleaned up 'Red Fox' texture in substance file
- Defaulted 'Flatten Lighting' toggle to 'On'
- Improved face-tracking shapes across the board
- Added various face-tracking animations for tongue, ears, and tail
- Added face-tracking prefabs
- Added VRM 0.X prefab for VTubing (with additional support for ARKit shapes!)
- Updated hand muscle settings to fix clipping issues with Steam Input 2.0 (Thanks Blu!)
- Removed texture swap options from the 'Standard' Sylvafen prefab save on VRAM usage
- Reduced body mesh poly count by a few thousand (Mostly in the floofs). Should let you put a few clothing items on now without going over the 'Very Poor' threshold.
- Changed rest pose of toes to be closed by default, increasing compatibility with other programs
- Created parent/root bones for similar Physbones in order to optimize Phybone component counts
- Created a default 'Optimized' prefab, removed Butt and Toe Physbones from it to achieve a 'Good' rating by default. Fully-featured Fen can still be found under the 'Base' Prefabs
- Changed texture filtering on 'Bits' textures
- Reduced VRAM usage via compression settings
- Added constraints to tongue physbones
- Made separate 'Collar-Only' and 'Sock-Only' prefabs for those who want to further optimize their poly count and add overhead for other clothing items
- Improved blink viseme
- Updated documentation

7/30/2024 | v1.2.2
MMD Hotfix
- Fixed MMD Blendshapes getting optimized out of avatar uploads
- Updated ReadMe

7/26/2024 | v1.2.1
Minor Update

- Improved weight painting around legs and groin area / improved various clothes clipping situations
- Lowered glossiness of beans
- Lowered unpacked filesize
- Fixed collar clipping into chest when laying down
- Reduced physbone jiggle on toes
- Added butt bones with jiggle; by popular request~


7/23/2024 | v1.2.0
MMD Support

- Full MMD support with japanese blendshapes - Get out there and dance!
- Fixed eye shader producing a white outline around iris
- Fixed body color masking making the mouth change color with the hue slider
- Reworked customization and puppet menus to be more modular and easier to individually delete
- Added GoGo Loco by default on all prefab variants
- Various clothes clipping fixes
- Added nose boop physbone
- PoV Snoot now saves properly
- Added better constraints to tail movement
- Fixed ear animation not looping on the smug gesture
- Updated ReadMe


7/16/2024 | v1.1.0
Minor Update

- Separated public packages out to their own prefab variants
- Improved sleep blend
- Renamed Snoot menu option to 'PoV Snoot'
- Changed base textures to color sliding for better customizability without requiring a custom re-texture
- Improved collar texture
- Made head and nose contacts larger
- Improved underwear and sock weights/deforms
- Added bulge blendshape to panties
- Improved texture density on clothes
- Shader improvements to the eyes
- Embedded texture files in .blend
- Restored default camera in the Unity Scene file
- Fixed a typo on the piercings toggle
- Swapped piercings and skirt order in the clothing menu
- Lowered gravity on the tail


7/14/2024 | v1.0.0
Initial Release!