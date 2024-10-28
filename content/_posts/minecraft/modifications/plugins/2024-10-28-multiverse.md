---
layout: post
title: Adding custom world portals
category: Java
tags: plugins
permalink: /minecraft/modifications/plugins/multiverse
description: Using Multiverse-Core and Multiverse-Portals to add portals to custom worlds
author: 
	- TheTWIXhunter
	- Deka
icon: "content/assets/images/posts/multipleworlds/multiverse-core-logo.png"
mod-name: "Multiverse-Core"
mod-software: "Bukkit, Paper, Spigot"
mod-url: "https://modrinth.com/plugin/multiverse-core"
---

# Installing the Multiverse-Core Plugin

{.info}
> Follow our [plugin installation guide](/minecraft/modifications/general/adding-plugins).

You can get the Multiverse-Core plugin [here](https://modrinth.com/plugin/multiverse-core).

# Adding Worlds

## Uploading a World

1. Upload your world folder to the File Manager or upload your world using the Worlds page.

{: .warning}
> The folder name will be used as the world name in-game; you cannot use spaces for the folder name.

2. Open your server's console.

3. Import the world folder into Multiverse:

   `/mvimport <world> <environment>`

   Replace:
   - `<world>` with the name of the world folder that you uploaded.
   - `<environment>` with a world environment. Some options are: `NORMAL`, `NETHER`, `THE_END`. You can list all available environments by running `/mvenv`.

4. You can teleport to your new world in-game using the `/mvtp <world>` command.

## Generating a New World

1. Open your server's console.

2. Create a new world using Multiverse:

   `/mvcreate <world> <environment> (-parameters)`

   Replace:
   | Option           | Description                                                                                                               |
   |----------------- |---------------------------------------------------------------------------------------------------------------------------|
   | `<world>`        | the name of the world.                                                                                                    |
   | `<environment>`  | a world environment. Some options are: `NORMAL`, `NETHER`, `THE_END`.                                                     |
   | `(-parameters)`  | optional parameters. Refer to [this](https://github.com/Multiverse/Multiverse-Core/wiki/Command-Reference#create-command).|

3. Wait for the world to generate (this can take a while).

4. You can teleport to your new world in-game using the `/mvtp <world>` command.

# Creating Custom Portals Between Worlds

{: .info}
> You will need to install the Multiverse-Portals plugin. You can download it [here](https://modrinth.com/plugin/multiverse-portals).

{: .warning}
> Players without the `multiverse.portal.access.<world>` or `multiverse.portal.access.*` permission will not be able to use the portals.

## Creating a Portal

1. In-game, select the blocks of your portal by left-clicking the start position with a wooden axe and right-clicking the end position.

   {: .info}
   > The portal can be made out of any blocks.

2. Create a portal:
   `/mvp create <name>`.

## Linking Portals

1. Select a portal:
   `/mvp select <portal name>`.

2. Modify it to add a destination portal:
   `/mvp modify dest -p <portal name>`.

   {: .info}
   > Repeat the process if you want the destination portal to link back to the first portal.

## Linking Portals to a Location

1. Select a portal:
   `/mvp select <portalname>`.

2. Go to the location that you want players teleported to.

3. Modify the portal's destination:
   `/mvp modify dest here`.