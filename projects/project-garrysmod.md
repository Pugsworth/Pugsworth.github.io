---
layout: project
type: project
image: images/projects/garrysmod-logo.png
image-spawnmenu: images/projects/spawnmenu.png
title: Garry's Mod scripts
permalink: projects/gmod
# All dates must be YYYY-MM-DD format!
date: 2021-06-19
labels:
  - Lua
  - Garry's Mod
  - Source Engine
summary: Various code I have written in my time playing Garry's Mod and on the server Metastruct.
---


# Garry's Mod


The bulk of my entry into programming happened in a game called Garry's Mod.

Garry's Mod is a modification to the Source Engine, and principally, Half-Life 2.
It is a large sandbox game with massive amounts of user created content.

> Garry's Mod (abbreviated GMod) is a 2006 sandbox game developed by Facepunch Studios and published by Valve. The base game mode of Garry's Mod has no set objectives and provides the player with a world in which to freely manipulate objects. Other game modes, notably Trouble in Terrorist Town, are created by other developers as mods and are installed separately, by means such as the Steam Workshop. Garry's Mod was created by Garry Newman as a mod for Valve's Source game engine and released in December 2004, before being expanded into a standalone release that was published by Valve in November 2006. (...)

Source: [Wikipedia excerpt](https://en.wikipedia.org/wiki/Garry%27s_Mod);

&nbsp;

At the time, I was a part of a community server called MetaConstruct that acted like a hub for developers and players.
This provided a great place to test new ideas and interact with other developers and players alike. Within here, a lot of collaboration took place throughout the years.

<hr>

&nbsp;

The following are some of the projects I have developed.

#### dropweapon.lua
One of my first scripts I wrote allowed the player to "throw" their active weapon onto the ground.
Inspired by Borderlands 1, I recreated a similar effect in which, after a timeout, the weapons would shrink over time until they would pop out of existence.

*Takeaway:* Learned to combine user input with delayed execution.

#### quickspawnmenu.lua
Garry's Mod has a feature for creating entities called a Spawn Menu. The Spawn Menu is a menu that allowed the player to create props, entities, npcs, and select various tools.
This is a script that replicates a spawn menu in the form of a mini "favorites" menu. The player can add items to the menu that they often interact with.
This takes away some of the inconvenient inputs needed for frequently used items.

*Takeaway:* Learned about UI development and organization.


#### fohud.lua
This script replicated the HUD from Fallout 3. It featured a fully functional compass along with health, armor, and stamina display. This was a drop-in replacement for the default HUD.

*Takeaway:* Learned about working with images and vector math as well as code clarity and organization, which is important for UI.


#### dhook.lua
dhook is a developer utility script to manage hooks. A hook in Garry's Mod is a event callback for various things in the game. *e.g. you would add a hook to detect when a player died or spawned.*

*Takeaway:* I didn't know it at the time, but this was my introduction into writing something akin to an API.


#### hurtreactions.lua
A system for relaying what kind of damage a player took that involved custom sounds based on the playermodel.
Using hooks, the system would detect where the player was hit and dynamically react with a random sound based on a configuration format of location -> sound(s).

*Takeaway:* Learned considerably about dynamic code and creating a configuration format that is easy for anyone to edit.


#### crosshair.lua
A dynamic crosshair that showed a representation of spread for the currently active weapon

*Takeaway:* Past knowledge allowed me to create this fun project.


#### quickinfo.lua
Half-Life 2 features a unique kind of HUD element that can show the player their health and ammo counts at a glance. Due to a bug, the engine's quickinfo wasn't functional.
By reading the C++ engine source code, I was able to recreate the functionality in Lua.

*Takeaway:* At the time, I was only familiar with Lua. I read the C++ source code was able to learn about how the original worked and replicated it.


#### addons/luadev
This is a Development environment for executing and debugging Lua code clientside and serverside.

*Takeaway:* Learned about networking and compression of code in order to minimize the demand on the server. I also learned about sandboxing through an 'eval' system of Lua executing Lua.


#### crate.lua
This is a silly script that allowed a player to turn their character model into a crate. It took inspiration from Metal Gear Solid with the box disguise.
The original script was made by Cake!, another developer on the MetaConstruct server. The player took control of a box that could jump or be nudged in any direction.
If the player clicked their mouse, a random voice sound was played. To the unsuspecting player, you couldn't tell if it was a box prop or a player. If the box was broken, the player would emerge with a scream.

*Takeaway:* Programming can lend itself to ridiculous features that end up being some of the most fun.


#### addons/teleporter
An entity that took inspiration from many games that used similar teleportation mechanics. This was an entity that, upon spawning would register itself to a "pool" of teleporters.
The player could select either a location in the world or another teleporter as the target. When the player approached the entity, it would open and show a bubble with various particle effects.
Inside the bubble was a real-time preview of where they would be going to. This mimicked the effects of a portal that was used in the video game Portal and Portal 2.
Garry's Mod doesn't have shader access, but there was a system for **stencils**.
Stencils allowed essentially cutting of textures that were drawn to the screen to isolate which part of the camera render target was to be drawn for the portal effect.
Now, this effect is so well known that you can find many tutorials and examples on Youtube.

*Takeaway:* Learned a great deal more vector math as well as shader style code.


#### metachat.lua
I used websockets to develop a clientside/singleplayer addon to link the chat of the server MetaConstruct with the local chat.
This enabled communication across singleplayer.

*Takeaway:* Learned about websocket networking and how to organize data for it. Synchronization and error correction has proven a good challenge that I was able to overcome.


#### MetaConstruct maps
At the same time I was learning to write code, I was interested in level design. A couple level designers and I participated on improving the server's levels.
Since the level editor had no collaborative editing, we split the levels into sections and worked on those. When it was time to compile and test, there was a system to combine everything together and spit out a single map.
There was constant communication and collaboration on what was to be added and scrapped based on feedback.

*Takeaway:* Learned about many facets of level design and remote collaboration. 


### Garry's Mod contributions
I have made several contributions to Garry's Mod while engrossed in the game.
A meaningful contribution was during a major overhaul of the game; the creator asked the community to collaborate on recreating the iconic map **gm_construct**.  
During this collaboration, I helped fix some bugs in the map and helped create some of the areas. 
I have also helped push changes to add some features and fix various bugs in the codebase.

*Takeaway:* Learned collaboration and communication on an organizational level.

