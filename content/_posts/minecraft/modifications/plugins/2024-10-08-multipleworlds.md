---
layout: post
title: Learn how to host multiple worlds at once!
category: Java
tags: plugins
permalink: /minecraft/modifications/plugins/multipleworlds
description: Learn how to use the  Multiverse-core, Multiverse-portals and multiverse-.
author: TheTWIXhunter
toc: true
icon: "content/assets/images/posts/multipleworlds/multiverse-core-logo.png"
mod-name: "Multiverse-core"
mod-software: "Spigot, Paper, Purpur"
mod-url: "https://www.spigotmc.org/resources/multiverse-core.390/"
---

// this is a rough outline, don't correct me on spelling or grammar YET.

# Installing the plugin

Download the multiverse-core plugin [here](https://www.spigotmc.org/resources/multiverse-core.390/)

Open the Filemanenger and go to the /plugins folder

Upload the worldfolder to the File Manager

Go to the worlds page

delete the old worlds and Upload the 'lobby' world of your choise

Press "Make Primary"

(re)start the server

# adding worlds
## uploading a secondary world

Upload the world folder to the (home location of the) File manenger or Upload your world using the Worlds page
(see this )

{: .warning}
> The folder you upload CAN'T have spaces in it's name.

{: .warning}
> Give the folder a clear and easy name, this name will be used as worldname In-game.

Join your server

run this command (you need to have OP rights):

`/mvimport <name> <type>`

replace:
 `<name>` with the name of the folder/world that you uploaded.
 `<type>` with the type of world, possibilities are: `NORMAL`, `NETHER` or `THE_END`

Teleport to the world using `/mvtp <name>`



## Generating a new world

Join your server.

run this command (you need to have OP rights):

`/mvcreate <name> <type> (<-parameters>)`

replace:
 `<name>` with the name of the world.
 `<type>` with the type of world, possibilities are: `NORMAL`, `NETHER` or `THE_END`
 `(-parameters)` with the wanted parameters (optional)(see below)

Optional Parameters:
 `-s <yourseed>` Sets the seed for the world (default: Random)
 `-t <type>` sets the world type, options are: `Flat`, `normal`, `largebiomes`, `Version_1_1` (default: `Normal`)
 `-g <generator>` Uses a custom generator (those need to be installed seperatly)
 `-a <true|false>` Generate structures?

Wait for the world to generate (this can take a while)

Teleport to the world using `/mvtp <name>`

# Create Custom portals between worlds
{: .warning}

> This section needs multiverse-portals installed, download it [here](https://modrinth.com/plugin/multiverse-portals)

## creating a portal

select the blocks that you want to become a portal by left-clicking a wooden_axe to the top-right position and right-clicking the end-position

{: .info}

> the portal can be made out of any blocks of your choise

{: .warning}

> the portal needs to be eather vertical or horizontal

Run this command:
    `/mvp create <name>`

## Linking 2 portals to eachother.

Run this command:
    `/mvp select <portalname>`

once your first portal is selected, run:
    `/mvp modify dest -p <destinationportalname>`

{: .info}

> you need to repead these steps for the destination portal to link it back to the original one

## Linking a portal to a location.

Run this command:
    `/mvp select <portalname>`

Go to the location that you want players teleported to.

Run this command:
    `/mvp modify dest here`