---
layout: post
title:  "Configuring Minecraft Server: Server Properties"
category: Java
tags: Server
description: "Explore the commonly used attributes of the server.properties file to effectively configure your Java Minecraft server"
permalink: /minecraft/java/server/server-properties
author: "Kuroi Jigoku"
toc: false
---

## Introduction

Understanding the server.properties file is crucial for configuring and customizing your Minecraft server. This guide highlights the essential attributes within the file, enabling you to optimize your server settings for the best gameplay experience.

## server.properties

### accepts-transfers

Possible Values: Boolean
Default Value: false

This setting determines if the server accepts player transfers from other servers in a network.
It's often used in server networks to facilitate smooth transitions between different game modes or server instances.

---

### allow-flight

Possible Values: Boolean
Default Value: false

This option allows players to fly in Survival mode. It's useful for servers that want to enable flight for players, often for building purposes or to accommodate specific server plugins.

- Setting this to true will also allow hackers to fly around the world.

---

### allow-nether

Possible Values: Boolean
Default Value: false

This setting controls whether players can build Nether portals and travel to the Nether dimension. Disabling it can prevent players from accessing the Nether, which can be useful for servers with specific gameplay rules.

---
  
### difficulty

Possible Values: easy, normal, hard
Default Value: easy

This setting defines the difficulty level of the server, affecting mob behavior and player damage.

- If set to `peaceful`, No hostile mobs will spawn and health regenerate quickly.
- If set to `easy`, Hostile mobs will spawn but they deal less damage. hunger depletes slowly.
- If set to `normal`, Standard difficulty with mobs dealing normal damage and hunger depletion.
- If set to `hard`, Hostile mobs deals more damage, hunger depletes faster, zombie breaks down doors and some game mechanics are little more challenging.

---
  
### enable-command-block

Possible Values: Boolean
Default Value: false

Command blocks allow for automation and complex commands within the game. Enabling them can enhance server functionality but may pose security risks if not properly managed.

- Usually they are used in custom maps.

---

### enforce-secure-profile

Possible Values: Boolean
Default Value: true

This setting ensures that Players without a Mojang-signed public key will not be able to connect to the server.

- You should set this to `false` if you want to allow players with cracked clients to join the server.

---

### enforce-whitelist

Possible Values: Boolean
Default Value: false

Enabling this setting ensures that only players listed in the whitelist can join the server, providing controlled access, This is ideal for private or community servers that require limited access to only certain players.

---
  
### force-gamemode

Possible Values: Boolean
Default Value: false

This setting forces all players to be switched to a specific game mode upon joining the server.

---

### gamemode

Possible Values: survival, creative, adventure, spectator
Default Value: survival

This setting defines the default game mode for players joining the server, such as survival, creative, or adventure.

- If set to `survival`, Players must gather resources, build structures, and survive against hostile mobs.
- If set to `creative`, Players have unlimited access to the resources, They can fly, hostile mobs do not attack them.
- If set to `adventure`, Players can interact with objects like levers and buttons, but they are unable to break the blocks.
- If set to `spectator`, Players can fly, phase through blocks, see through blocks. They cannot interact with the world and are invisible to other players.

---

### generate-structures

Possible Values: Boolean
Default Value: true

This setting controls whether structures like villages and temples generate in the world, which can impact gameplay and exploration.

---

### hardcore

Possible Values: Boolean
Default Value: false

Setting this to `true` will change the server difficulty to hard and sets gamemode to spectator upon death if they choose to respawn, adding an extra layer of challenge.

---

### level-seed

Possible Values: String
Default Value: *blank*

This setting allows specifying a seed for world generation, enabling the creation of specific world layouts or replicating previous worlds.

---

### log-ips

Possible Values: Boolean
Default Value: true

This setting determines if player IP addresses are logged upon connection, which can be useful for monitoring and security purposes. Set this to `false` if you prefer the server to be privacy-friendly.

---

### max-players

Possible Values: Integer
Default Value: 20

This setting specifies the maximum number of players allowed on the server simultaneously, impacting server load and community size.

---

### max-tick-time

Possible Values: Integer (in milliseconds) or -1
Default Value: 60000

This setting defines the maximum time in milliseconds a single tick may take before the server watchdog stops the server, helping to prevent severe performance issues.

- If a single server tick took 60 seconds, the watchdog will consider it as a crash and forcibly shut downs the server.
- Set to `-1` to disable the watchdog.

---

### max-world-size

Possible Values: Integer
Default Value: 29999984

The maximum allowed size of the world radius, in blocks. This only affects the chunks that are generated when the world is initially created, and not the world border.

---

### motd

Possible Values: String
Default Value: A Minecraft Server

The message of the day (MOTD) is displayed in the server list and provides a brief description or welcome message for players.

---

### online-mode

Possible Values: Boolean
Default Value: true

This setting requires players to authenticate with Minecraft's account database before joining, preventing players with cracked clients from connecting.

- Set to `false` to allow cracked players to join the server.

---

### player-idle-timeout

Possible Values: Integer (in minutes)
Default Value: 0

This setting determines how long a player can be idle before being kicked from the server, helping to manage active player slots.
The following packets resets this timer:

- "Click Window"
- "Enchant Item"
- "Update Sign"
- "Player Digging"
- "Player Block Placement"
- "Held Item Change"
- "Animation (swing arm)"
- "Entity Action"
- "Client Status"
- "Chat Message"
- "Use Entity"

---

### pvp

Possible Values: Boolean
Default Value: true

This setting controls whether players can engage in player-versus-player combat, impacting gameplay dynamics and server rules.

---

### require-resource-pack

Possible Values: Boolean
Default Value: false

This setting forces players to download and use a specified resource pack to join the server, ensuring a consistent visual experience.

---

### resource-pack

Possible Values: String
Default Value: *blank*

This setting specifies the URL of the server's resource pack, allowing players to download custom textures and assets.

---

### resource-pack-id

Possible Values: String
Default Value: *blank*

This setting provides the UUID of the resource pack, used to identify and verify the correct pack version.

---

### resource-pack-prompt

Possible Values: String
Default Value: *blank*

This setting displays a custom message when players are prompted to download the resource pack, providing additional information or instructions.

---

### resource-pack-sha1

Possible Values: String
Default Value: *blank*

This setting provides a hash of the resource pack for verification, ensuring players download the correct and unmodified pack.

---

### simulation-distance

Possible Values: Integer
Default Value: 10

This setting controls the radius around each player where mobs and gameplay mechanics are active, impacting server performance and gameplay experience.

---

### spawn-animals

Possible Values: Boolean
Default Value: true

This setting controls whether animals can spawn naturally in the world, affecting gameplay and resource availability.

---

### spawn-monsters

Possible Values: Boolean
Default Value: true

This setting controls whether monsters can spawn naturally in the world, affecting gameplay and resource availability.

---

### spawn-npcs

Possible Values: Boolean
Default Value: true

This setting controls whether villagers and other NPCs can spawn naturally in the world, affecting gameplay and resource availability.

---

### spawn-protection

Possible Values: Integer
Default Value: 16

This setting defines a protected area around the spawn point where players cannot build or destroy blocks, helping to preserve the spawn environment.

---

### view-distance

Possible Values: Integer
Default Value: 10

This setting determines the radius around each player where the server sends information about the world, affecting how much of the world is loaded and visible.

---

### white-list

Possible Values: Boolean
Default Value: false

This setting enables a whitelist on the server, allowing only selected users to connect and providing controlled access to the server. Which is ideal for private servers or community servers where certain servers requires only limited access of players.

---
