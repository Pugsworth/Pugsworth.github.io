---
layout: project
type: project
image: images/garrysmod-logo.png
image-spawnmenu: images/spawnmenu.png
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

Source: [Wikipedia exerpt](https://en.wikipedia.org/wiki/Garry%27s_Mod);

&nbsp;

At the time, I was a part of a community server called MetaConstruct that acted as a kind of hub for developers and players.
This provided a really great place to test new ideas and interact with other developers and players alike. Lots of collaboration took place throughout the years.

<hr>

&nbsp;

Here's a couple of the things I developed:

#### dropweapon.lua
One of my first bigger scripts that allowed the player to "throw" their active weapon onto the ground.
After an amount of time, the weapon used an effect that took inspiration from Borderlands 1 -- They would shrink over time until they would pop out of existance.

*Takeaway:* I learned to combine user input with delayed execution.

#### quickspawnmenu.lua
Garry's Mod uses something called a SpawnMenu. The SpawnMenu is a menu that allowed the player to spawn props/entities/npcs and select various tools. This is a script that creates a mini sort of "favorites" menu replication of the spawnmenu.

*Takeaway:* Learned about UI development and organization.


#### fohud.lua
One of my next bigger scripts. This was an attempt to fully recreate the HUD from Fallout 3. It featured a fully functional compass along with health/armor/stamina. This was a drop-in replacement for the default HUD.

*Takeaway:* Code clarity and organization is important with UX. I also learned about working with images and some vector math.


#### dhook.lua
dhook was a simple developer utility script to manage hooks. A hook in Garry's Mod is a event callback for various things in the game. *e.g. you would add a hook to detect when a player died or spawned.*

*Takeaway:* I didn't know it at the time, but this was my introduction into writing something akin to an API.


#### hurtreactions.lua
A system for relaying what kind of damage a player took that involved custom sounds based on the playermodel.
Using hooks, the system would detect where the player was hit and dynamically react with a random sound based on a configuration format of location -> sound(s).

*Takeaway:* I learned a lot about dynamic code and creating a configuration format that is easy for anyone to edit.


#### crosshair.lua
A simple dynamic crosshair that showed a representation of spread for the currently active weapon

*Takeaway:* There was a little dynamic code.


#### quickinfo.lua
Half-Life 2 features a unique kind of HUD element that can show the player their health and ammo counts at a glance. Due to a bug, the engine's quickinfo wasn't functional. I recreated it to the best of my abilities. Using C++ engine source code, I was able to recreate the functionality in Lua.

*Takeaway:* At the time, Lua was the only language I really knew. I used the C++ source code to learn about how the original worked and replicated it.


#### addons/luadev
Development environment for executing and debugging Lua code clientside and serverside.

*Takeaway:* I learned about networking and compression of code in order to minimize the demand on the server. I also learned about sandboxing through a kind of 'eval' system of Lua executing Lua.


#### crate.lua
This is a silly script that allowed a player to turn their character model into a crate. It took inspiration from Metal Gear Solid with the box disguise. The original script was made by Cake!, another developer on the MetaConstruct server The player took control of a box that could be nudged in any direction and jump. If the player clicked their mouse, a random voice sound was played. To the unsuspecting player, you couldn't tell if it was a box prop or a player. If the box was broken, the player would emerge with a scream.

*Takeaway:* Programming isn't always supposed to be serious.


#### addons/teleporter
An entity that took inspiration from many games that used similar teleportation mechanics. This was an entity that upon spawning would register itself to a "pool" of teleporters. The player could select either a location in the world or another teleporter as the target. When the player approached the entity, it would open and show a bubble with various particle effects. Inside the bubble was a realtime preview of where they would be going to. This used identical effects as was used in the video game Portal and Portal 2. Garry's Mod doesn't have shader access, but there was a system for **stencils**. Stencils  allowed essentially cutting of textures that were drawn to the screen to isolate which part of the camera render target was to be drawn for the portal effect. Now, this effect is so well known that you can find many tutorials and examples on Youtube.

*Takeaway:* This project involved lots of vector math and shader-style code.


#### metachat.lua
I used websockets to develop a clientside/singleplayer addon to link the chat of the server MetaConstruct with the local chat.
This allowed communication across singleplayer.

*Takeaway:* I learned about websockets networking and how to organize data for it. Synchronization and error correction proved
challenging, but not impossible.


#### MetaConstruct maps
At the same time I was learning to write code, I was interested in level design. A couple level designers and I collaborated on improving the server's levels.

*Takeaway:* Remote teamwork. Since the level editor had no collaborative editing, we split the levels into sections and worked on those. When it was time to compile and test, there was a system to combine everything together and spit out a single map. There was lots of communication and voting on what was to be added and scrapped based on feedback.

### Garry's Mod contributions
I have made a couple contributions to Garry's Mod in my time with the game.
One was during a huge revamp of the game, the creator asked the community to collaborate on recreating the icon map **gm_construct**.  
During this collaboration, I helped fix some bugs in the map and helped create some of the areas. 
I have also helped push changes to add some minor features and fix various bugs in the codebase.

*Takeaway:* Collaboration and communication on an organizational level.

