---
layout: post
title: Learn how to host multiple worlds at once!!
category: Java
tags: plugins
permalink: /minecraft/modifications/plugins/multipleworlds
description: Learn how to host multiple worlds at once on one server.
author: TheTWIXhunter
toc: true
icon: "https://media.forgecdn.net/avatars/65/506/636163025316086566.png"
mod-name: "Multiverse"
mod-software: "Spigot, Paper, Purpur"
mod-url: "https://dev.bukkit.org/projects/multiverse-core"
---

// this is a rough outline, don't correct me on spelling or grammar YET.

# Installing the plugin and a lobby world

Download the multiverse-core plugin [here](https://www.spigotmc.org/resources/multiverse-core.390/)

Open the Filemanenger and go to the /plugins folder

Upload the file to the folder

Go to the worlds page

delete the old worlds and Upload the 'lobby' world of your choise

Press "Make Primary"

(re)start the server

## uploading a secondary world

Upload the world folder to the (home location of the) File manenger or Upload your world using the Worlds page
(see this )

{: .warning}
> The folder you upload CAN'T have spaces in it's name.

{: .warning}
> Give the folder a clear and easy name, this name will be used as worldname In-game.

Join your server

run the command (you need to have OP rights):

`/mv import <name> <type>`

replace:
 `<name>` with the name of the folder/world that you uploaded.
 `<type>` with the type of world, possibilities are: `NORMAL`, `NETHER` or `THE_END`

Teleport to the world using `/mvtp <name>`
