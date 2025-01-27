# CIS 099 Independent Study: An Exploration into Augmented Reality Development Tools

This semester, I underwent an independent study teaching myself AR filter development using state-of-the-art AR development toolkits, specifically using Tiktok and Snap Inc.'s proprietary software. I explored the possibilities of AR development in Effect House (by Tiktok) and Lens Studio (Snap Inc.) to learn more about the AR pipeline and the capabilities of these tools for AR content creation. 

**Over the course of few months I developed 6 AR effects total, 3 within each software.**

<img align="center" src=https://github.com/CIIINDYXUU/ARFilters/assets/88256581/9fb8e2cd-abb2-476a-94ca-d840c5192039 >

## Table of Contents

- [Introduction](https://github.com/CIIINDYXUU/ARFilters/blob/main/README.md#introduction)
  - [Objective](https://github.com/CIIINDYXUU/ARFilters/blob/main/README.md#objective)
  - [Timeline](https://github.com/CIIINDYXUU/ARFilters/blob/main/README.md#timeline)
- [Developing in Tiktok's Effect House](https://github.com/CIIINDYXUU/ARFilters/blob/main/README.md#developing-in-tiktoks-effect-house)
  - [Filter #1: Castle Portal Effect](https://github.com/CIIINDYXUU/ARFilters/blob/main/README.md#filter-1-castle-portal-effect)
  - [Filter #2: Ball Bouncer Game](https://github.com/CIIINDYXUU/ARFilters/blob/main/README.md#filter-2-ball-bouncer-game)
  - [Filter #3: Galaxy Face Filter](https://github.com/CIIINDYXUU/ARFilters/blob/main/README.md#filter-3-galaxy-face-effect)
- [Developing in Snap Inc.'s Lens Studio](https://github.com/CIIINDYXUU/ARFilters/blob/main/README.md#developing-in-snap-incs-lens-studio)
  - [Lens #1: Interactive Rain Shader](https://github.com/CIIINDYXUU/ARFilters/blob/main/README.md#lens-1-interactive-rain-shader)
  - [Lens #2: Fish Hand Tracking Effect](https://github.com/CIIINDYXUU/ARFilters/blob/main/README.md#lens-1-interactive-rain-shader)
  - [Lens #3: Volumetric Vortex](https://github.com/CIIINDYXUU/ARFilters/blob/main/README.md#lens-1-interactive-rain-shader)
- [Conclusion](https://github.com/CIIINDYXUU/ARFilters/blob/main/README.md#conclusion)
  
## Introduction

Since its advent in the late 1960s, augmented reality (AR), an immersive technology that allows users to interact with digital objects projected onto the real world, has reshaped the ways in which we consume and interact with digital content. In recent years, interest in AR technology has surged, captivating audiences across various industries with its ability to blend digital with physical. As technological advancements in AR software and hardware, such as Apple's Vision Pro headset, become more mainstream, there exists an exciting opportunity for engineers, researchers, designers, and developers to build AR-based applications and solutions for the masses. AR provides countless affordances in visualization, interaction, and immersion, and presents unique solutions for an array of different industries, particular regarding entertainment and content creation. 

As augmented reality technology continues to gain traction and become increasingly integrated into our daily lives, there is a growing need for individuals with expertise in AR development and design. Over the past decade, more and more tools for AR development have also become more accessible to the public. Two leading players in the AR content creation industry are Tiktok and Snapchat, both platforms that allow their users to create and share original AR filters and effects. From interactive games to beauty filters to new AI and ML-based features, the possibilites for creation are endless.

### Objective
The objective of this independent study is to delve deeper into augmented reality development, gaining a comprehensive understanding of existing state-of-the-art AR toolkits and the AR development pipeline. The projects developed over the course of the semester will be multidisciplinary, requiring a combined foundation of artistic intuition, computer graphics knowledge, and software development skills. 

The initial plan was to learn three different softwares: Tiktok's Effect House, Meta's Spark AR, and Unity's AR Foundation, buildling 2 AR experiences each and 6 total. However, early on in the semester I quickly realized teaching myself 3 new softwares was overambitious and decided to rescope from breadth to depth. I decided to pivot and focus on 2 toolkits: [Tiktok's Effect House](https://effecthouse.tiktok.com/) and [Snap Inc.'s Lens Studio](https://ar.snap.com/lens-studio), with the goal of delving deeper into each software's capabilities. I ended up creating 6 experiences overall, 3 per software. The following list covers the range of AR features and types of effects I was able to explore in the semester:

- Effect House (Tiktok)
  - World AR (projection onto real-world environments)
  - Interactive Gaming
  - Real-time 3D Physics
  - Head Tracking
  - Face Filters
- Lens Studio (Snap Inc.)
  - Interactive Shaders and Post-Processing
  - Volumetric Rendering
  - Hand Tracking
  - VFX

### Timeline

Upon rescoping the project from the initial plan, I restructured my timeline to the following:

![Independent Study (2)](https://github.com/CIIINDYXUU/ARFilters/assets/88256581/d6842852-6917-4cb5-9d6a-c4c73c0df16d)
</details>

## Developing in Tiktok's Effect House

Effect House has a wide array of features for AR development and so I wanted to explore a wide range of AR effects. Each filter, from conceptualization to designing to prototyping, took approximately 2 - 3 weeks. Effect House prioritizes a no-code, node-based visual scripting system and provides pre-made "Objects" allowing users to create different kinds of effects such as head tracking, body tracking, and post-effects. All assets (3D models and materials) were taken directly from Effect House's in-house asset and material libraries, that provide models from [Sketchfab](https://sketchfab.com/). 

### Filter #1: Castle Portal Effect
The first effect I wanted to try making was a portal effect, one where a user could view the portal suspended midair and travel inside to view another world. 

<div align="center">
  <video src= https://github.com/CIIINDYXUU/ARFilters/assets/88256581/50c38b83-80dd-49b4-a634-d3ca960dac12 />
</div>

#### Method
<img align="right" src=https://github.com/CIIINDYXUU/ARFilters/assets/88256581/f8812d45-e4d0-406e-891e-5de972bf7d2e height=200>

This effect relies heavily on Effect House's AR Plane feature, which tracks real-world surfaces and allows for the placement of 3D models in a real environment. Another major component to the filter is occlusion, which are used to mask virtual objects in the scene and hide portions of rendered geometry. The filter comprises mainly of a spherical mesh with a sky material applied to it as well as "The Occluder," another spherical mesh that obscures the outside of the "Sky" object except for the opening of the portal. The screenshot to the left demonstrates how the occluder mesh works to obscure the Sky object inside. Within the Sky object are Castle, Rock, and Cloud assets animated on loop.

### Filter #2: Ball Bouncer Game
Interactive games are one of the most popular filter effects on the TikTok platform and constantly going viral, so I knew that I wanted to attempt making one myself. My goal was to design a straightforward but addictive, interactive game that utilized Effect House's 3D Physics engine. 

Ball Bouncer is an endless runner game where the user tries to keep a ball bouncing for as long as possible, inspired by the popular mobile game Doodle Jump. Instead of platforms already existing for the ball to bounce on top of, the user is responsible for drawing platforms to keep the ball going and must move swiftly to keep the ball from falling. Powerups that launch the ball far up randomly appear as well.

<div align="center">
  <video src= https://github.com/CIIINDYXUU/ARFilters/assets/88256581/78e69e60-dff8-4ef0-b2b4-1e3cf6e21521 />
</div>

#### Method
<img align="right" src=https://github.com/CIIINDYXUU/ARFilters/assets/88256581/f5814975-0a75-4777-a1a7-b0793be7b5c8 height=280>

I implemented the entire game using visual scripting within Effect House, using different types of nodes such as finger touch tracking and collision detection. At a high-level, there are several main features: camera movement, ball movement, platform placement, powerups, and UI elements (i.e. the scoreboard). The screenshot to the right shows the "Hierarchy" of "Render Groups," which determines the order in which groups of objects are rendered in the scene. Here, the General render group contains the major components of the bouncing ball game, like the platforms, powerups, ball, etc. The UI Effects render group contains the score background and text as well a small image prompting users to swipe at the beginning of the game. Finally, the Power Up Post Effects render group creates a chromatic aberration effect when the ball comes in contact with the powerups. This effect took the longest by far (3 - 4 weeks) as I learned that creating games within Effect House's node-based system was incredibly time-intensive with so many different subgraphs and variables to consider.

### Filter #3: Galaxy Face Effect
The final effect I wanted to create in Effect House was a face filter, as AR filters that utilize face tracking to create fun effects are so prevalent and widespread. Inspired by the first portal effect I created, I wanted to create a effect that felt like a three-dimensional portal into the face. Upon seeing TikTok's default assets (the alien) I decided to create a galaxy portal effect where the alien pops out.

<div align="center">
  <video src= https://github.com/CIIINDYXUU/ARFilters/assets/88256581/4ce99c68-691a-4a9c-bde6-3b782dd6665b />
</div>

#### Method

<img align="right" src=https://github.com/CIIINDYXUU/ARFilters/assets/88256581/6071276c-88d3-4758-9376-0205dc7ec892 height=250>

To implement this filter I learned a lot about Effect House's Face Tracking capabilities, specifically from [this documentation on Head Tracking.](https://effecthouse.tiktok.com/learn/3.5.0/guides/technical-guides/objects/ar-tracking/head-tracker) To start I added a Head Tracker object which detects the 3D positions of heads on-screen in virtual space. This tracker allows users to easily track 3D objects to the head and face. To create the portal effect I used an Occluder material once again to mask the onscreen head and create a face-shaped portal. By using Effect House's in-house assets such as the alien, galaxy material, and little UFOs, I parented all these different assets/objects under the Head Tracker which allows all these objects to follow head movement on screen. The final features I implemented was playing the alien animation on loop, a vignette post-process effect, as well as for the filter to activate by tapping the screen.


## Developing in Snap Inc.'s Lens Studio

Compared to Effect House, which released in 2022, Lens Studio has been out since 2017 and as a result felt more robust and developed, especially regarding its graphics capabilities. Unlike Effect House which prioritizes no-code visual scripting, Lens Studio also had more features for custom code and scripts to build out their filters (which are called Lenses in Snapchat). In the second half of the study, I wanted to continue exploring different types of AR effects, specifically post-processing filters, hand tracking, and playing around with the graphics features to make some cool-looking animations. Similarly, each lens took approx. 3 weeks to build and I used assets from either Sketchfab or within Lens Studio.

### Lens #1: Interactive Rain Shader
Upon discovering [this documentation on converting Shadertoy operations to Lens Studio](https://docs.snap.com/lens-studio/references/guides/lens-features/graphics/materials/material-editor/tutorials/shadertoy-to-lens-studio#idate), I was inspired to create a Lens that used GLSL shaders to create an interesting interactive effect. I settled on a rain shader effect, where the user can drag their finger on the screen to temporarily "wipe away" the falling rain.

<div align="center">
  <video src= https://github.com/CIIINDYXUU/ARFilters/assets/88256581/2933b8af-5383-4558-8fbb-ff55d2ac5250/>
</div>

#### Method

<img align="right" src=https://github.com/CIIINDYXUU/ARFilters/assets/88256581/625c4fc4-2635-4ee1-ab64-9a4d24f5077d width=450 height=auto>

The main approach for this filter was using Lens Studio's unique "Custom Code" node which allows for writing custom shaders. Specifically, I found a [Youtube tutorial](https://www.youtube.com/watch?app=desktop&v=1CdKj_kqieY) that outlined how to use [this website](https://codepen.io/2020cv/full/YzaEBgy) to directly convert Shadertoy shaders in GLSL to be compatible within Lens Studio. Then, I scoured the Shadertoy website looking for some interesting rain shaders and decided to go with [this shader with falling rain on glass](https://www.shadertoy.com/view/ltffzl). Following the tutorial, I converted the GLSL code and begun implementing the shader within Lens Studio. 

At a high-level, the implementation behind the filter involves two main parts: a Rain shader material which is applied to the screen as well as a "Brush Controller" that wipes the rain drops clear via masking before fading back to the shader. To implement the "Brush" I implemented a script using [documentation on ScreenTransform](https://docs.snap.com/api/lens-studio/Classes/Components#ScreenTransform), which is a type of class that affects object behavior, in this case allowing a user to draw on screen. A user drawing on the screen is an Overlay effect/material directly affecting the opacity (alpha channel) of the background.

<img src=https://github.com/CIIINDYXUU/ARFilters/assets/88256581/97287d31-b258-4360-a9f8-b921425f0d5d width=500 height=auto>


### Lens #2: Fish Hand Tracking Effect
Since I explored facial/head tracking on Effect House, I wanted to also explore hand tracking which allows for some interesting AR interactive effects. After looking into Snap AR's [documentation on hand tracking](https://docs.snap.com/lens-studio/references/templates/object/hand), I came across an interesting idea combining hand tracking and crowd simulation/VFX. In this filter, users can hold up their hands to control swarms of fish! By holding up their right hand, the fish are attracted to the position of your hand. By holding up your left hand, the fish are repelled away.

<div align="center">
  <video src= https://github.com/CIIINDYXUU/ARFilters/assets/88256581/83776b75-9702-49ea-914e-8b25a9bcd1d9/>
</div>

#### Method
This effect built off of Lens Studio's existing capabilities for hand tracking, which include [3D Hand Tracking components](https://docs.snap.com/lens-studio/references/templates/object/hand/3d-hand-tracking#3dhandtracking) for the right and left hand. The effect also makes use of the VFX Editor, which allows the user to create effects using a node graph. The effect comprises of several main parts -- I created 4 different materials which are assets made up of shaders that define the look and placement of objects. The materials include an underwater effect that creates faint ripples on the screen, sun rays shining into the water, and a distorting/shaking effect on the camera. The screenshots below outline the different node graphs for each material and fish swarm VFX.

<img src=https://github.com/CIIINDYXUU/ARFilters/assets/88256581/f7e4aa06-b548-4e8b-9399-f62ca0f2b5cf height=auto width=480>
<img src=https://github.com/CIIINDYXUU/ARFilters/assets/88256581/032a83f8-0900-454a-8dc8-c1dcca243f35 height=auto width=480>
<img src=https://github.com/CIIINDYXUU/ARFilters/assets/88256581/839df76e-4a79-47d7-be07-773a1f9be989 height=auto width=480>
<img src=https://github.com/CIIINDYXUU/ARFilters/assets/88256581/a65cf1d9-f9dd-4076-9ea7-305d154b7cbf height=auto width=480>


### Lens #3: Volumetric Vortex
The final effect I created explored one of Lens Studio's newest features, Volumetric cloud rendering via raymarching. The filter is a swirling vortex of volumetric clouds along with occasional lightning and 3D particles (cows and dust) flying around. 

<div align="center">
  <video src= https://github.com/CIIINDYXUU/ARFilters/assets/88256581/c75c7daa-471b-41f7-9b26-1fbd14115fae />
</div>

#### Method
The vortex comprises of 2 procedurally drawn cone shapes stacked ontop of one another to make the basic shape of a tornado. The two shapes are then twisted and a noise is applied via a distortion shader node is applied to create the tornado effect. In order to implement the 3D particles swirling around the vortex, I built off existing [documentation on 3D mesh particles](https://docs.snap.com/lens-studio/references/templates/world/particles#3d-mesh-particles), specifically the [GPU Particles object](https://docs.snap.com/lens-studio/references/guides/lens-features/graphics/particles/gpu-particles). Screenshot of the key custom code nodes used (Distortion and Raymarching) and the overall node graph are below:

<img align="center" src=https://github.com/CIIINDYXUU/ARFilters/assets/88256581/cb217a32-e2dd-4a3e-ab07-914ff09c3ecc>  
</br>
<img src=https://github.com/CIIINDYXUU/ARFilters/assets/88256581/f728c821-92e9-4f49-8071-3c381e43d4dc height=242>
<img src=https://github.com/CIIINDYXUU/ARFilters/assets/88256581/f363c2cb-f6ba-4113-ba91-5b9757fc7784 height=242>

## Conclusion
Over the course of the semester, this independent study provided an excellent opportunity to delve deeper into mobile AR development and try out two softwares I've been wanting to learn. The filters developed during the semester got to touch different genres of AR filters as well as try out Effect House and Lens Studio's differnet capabilities/feature. Comparing the two, I ultimately preferred Lens Studio over Effect House for its more fleshed out and powerful graphics abilities. Lens Studio feels more fit for experienced developers who want to utilize graphics to create more advanced and visually-complex effects, while Effect House feels slightly more simple and restricted with its solely node-based scripting system. One feature that I didn't get the chance to explore was both software's AI/ML abilities, which would be an intersting feature to try out in the future. Furthermore, all of the effects created during the study revolved the purpose of entertainment. In the future, I would like to continue buildling on my AR development experience by seeing how Effect House or Lens Studio could be utilized to create different types of AR effects, specifically in the realm of educational technology. Ultimately, this independent study was a great first foray into the world of AR content creation and development, and I look forward to learning more and more about the industry as well as the pipeline for AR.
