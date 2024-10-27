---
layout: post  
title: Learn How to Host Multiple Worlds at Once!  
category: Java  
tags: plugins  
permalink: /minecraft/modifications/plugins/multipleworlds  
description: Learn how to use the Multiverse-Core, Multiverse-Portals, and Multiverse-.  
author: TheTWIXhunter  
toc: true  
icon: "content/assets/images/posts/multipleworlds/multiverse-core-logo.png"  
mod-name: "Multiverse-Core"  
mod-software: "Spigot, Paper, Purpur"  
mod-url: "https://modrinth.com/plugin/multiverse-core"  
---

# Installing the Plugin

1. Download the Multiverse-Core plugin [here](https://modrinth.com/plugin/multiverse-core).

2. Open the File Manager and go to the /plugins folder.

3. Upload the world folder to the File Manager.

4. Go to the worlds page.

5. Delete the old worlds (except the one that you want as default world)

6. (Re)start the server.

# Adding Worlds
## Uploading a Secondary World

1. Upload the world folder to the (home location of the) File Manager or upload your world using the Worlds page (see this).

   {: .warning}
   > The folder you upload can't have spaces in its name.

   {: .warning}
   > Give the folder a clear and easy name; this name will be used as the world name in-game.

2. Join your server or open your server's console.

3. Run this command (you need to have OP rights):

   `/mvimport <name> <type>`

   Replace:
   - `<name>` with the name of the folder/world that you uploaded.
   - `<type>` with the type of world, possibilities are: `NORMAL`, `NETHER`, or `THE_END`.

4. Teleport to the world using `/mvtp <name>`.

## Generating a New World

1. Join your server or open your server's console.

2. Run this command (you need to have OP rights):

   `/mvcreate <name> <type> (-parameters)`

   Replace:
   | `<name>`         | the name of the world.                                                                          |
   |----------------- |-------------------------------------------------------------------------------------------------|
   | `<type>`         | the world type; options are: `Flat`, `normal`, `largebiomes`, `Version_1_1` (default: `Normal`) |
   | `(-parameters)`  | the wanted parameters (optional) (see below)                                                    |

   **Optional Parameters:**
   | Parameter          | explanation                                                                      | default   |
   |--------------------|----------------------------------------------------------------------------------|-----------|
   | `-s <yourseed>`    | Sets the seed for the world                                                      | Random    |
   | `-t <worldtype>`   | Sets the world type; options are: `Flat`, `normal`, `largebiomes`, `Version_1_1` | `normal`  |
   | `-g <generator>`   | Sets a custom generator to be used                                               | `vanilla` |
   | `-a <true/false>`  | Whether or not to generate structures                                            | `true`    |

3. Wait for the world to generate (this can take a while).

4. Teleport to the world using `/mvtp <name>`.


# Create Custom Portals Between Worlds

{: .warning}
> This section needs Multiverse-Portals te be installed, download it [here](https://modrinth.com/plugin/multiverse-portals).

{: .error}
> only players having the `multiverse.portal.access.*` (or the `multiverse.portal.access.<portalname>`) permission can use portals.
> Give these permissions to your players using your permission plugin (like: luckperms).

## Creating a Portal

1. Select the blocks that you want to become a portal by left-clicking a wooden axe to the top-right position and right-clicking the end position.

   {: .info}
   > The portal can be made out of any blocks of your choice.

   {: .warning}
   > The portal needs to be either vertical or horizontal.

2. Run this command:
   `/mvp create <name>`.

## Linking 2 Portals to Each Other

1. Run this command:
   `/mvp select <portalname>`.

2. Once your first portal is selected, run:
   `/mvp modify dest -p <destinationportalname>`.

   {: .info}
   > You need to repeat these steps for the destination portal to link it back to the original one.

## Linking a Portal to a Location

1. Run this command:
   `/mvp select <portalname>`.

2. Go to the location that you want players teleported to.

3. Run this command:
   `/mvp modify dest here`.