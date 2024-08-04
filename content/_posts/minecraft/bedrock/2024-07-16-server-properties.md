---
layout: post
title: Configuring the server.properties file
category: Bedrock
tags: Server
description: Editing the commonly used attributes of the server.properties file to configure your Bedrock server.
permalink: /minecraft/bedrock/server/server-properties
author: Kuroi Jigoku
toc: false
---

## Introduction

Understanding the server.properties file is crucial for configuring and customizing your Minecraft server. This guide highlights the essential attributes within the file, enabling you to optimize your server settings for the best gameplay experience.

## server.properties

### server-name

Possible Values: String  
Default Value: Dedicated Server  

Specifies the name of the server as it appears in the multiplayer server list.

- Helps players identify and connect to the server easily.

---

### gamemode

Possible Values: survival, creative, adventure  
Default Value: survival  

Defines the mode of gameplay.

---

### force-gamemode

Possible Values: Boolean  
Default Value: false  

This can help enforce server rules or create consistent gameplay experiences, especially in controlled environments like minigames or events.

- Setting this to `true` ensures that all players joining the server are immediately switched to the game mode specified by `gamemode` in server.properties.

---

### difficulty

Possible Values: peaceful, easy, normal, hard  
Default Value: easy  

Defines the difficulty of the server.

- If set to `peaceful`, no hostile mobs will spawn and health regenerates quickly.
- If set to `easy`, hostile mobs will spawn but deal less damage compared to `normal`. Hunger depletes slowly.
- If set to `normal`, mobs will deal average damage. Some additional behaviour is enabled (eg. pillagers can break doors).
- If set to `hard`, hostile mobs will deal more damage, hunger will deplete faster, and additional behavior is enabled, including the changes from `normal` (eg. zombies can also break doors).

---

### allow-cheats

Possible Values: Boolean  
Default Value: false  

Enabling cheats allows server administrators (operators) to use commands that can alter gameplay mechanics, spawn items, teleport players, and more.
{: .warning}

> Enabling this option will disable achievements!

---

### max-players

Possible Values: Integer (1 to 65534)  
Default Value: 10  

The maximum number of players that can play on the server at the same time.

---

### online-mode

Possible Values: Boolean  
Default Value: true  
Enhances security by ensuring only authenticated players can join, protecting against unauthorized access.

- Sets whether the server checks if joining players are authenticated to Xbox Live.
- Recommended to leave on true to protect the server from fake and unsafe accounts.

---

### allow-list

Possible Values: Boolean  
Default Value: false

Enabling this setting ensures that only players listed in the allowlist can join the server, providing control over the players you want to join. This is ideal for private or community servers that limit access to certain players.

- Works similarly to Java Edition's Whitelist.

---

### view-distance

Possible Values: Integer (>=5)  
Default Value: 32  

Sets the distance in chunks around each player that the server shows.

- Directly affects how much of the world is loaded and visible to players.

---

### tick-distance

Possible Values: Integer (4-12)  
Default Value: 4  

Determines the radius in chunks around each player where mobs and certain gameplay mechanics are active and simulated.
Directly impacts server performance and gameplay experience.

---

### player-idle-timeout

Possible Values: Integer (>=0)  
Default Value: 30  

This setting determines how long a player can be idle before being kicked from the server, helping to manage active player slots. Value is measured in minutes.

- If set to 0, players can idle indefinitely.

---

### level-seed

Possible Values: String  
Default Value: (empty)

This setting allows specifying a seed for world generation, enabling the creation of specific world layouts or replicating previous worlds.

- The seed used to generate the world.
- Leave blank to default to random.

---

### default-player-permission-level

Possible Values: visitor, member, operator  
Default Value: member  

Permission level for new players joining for the first time.

- If set to `visitor`, players can interact with the world but cannot modify it significantly or use most basic commands.
- If set to `member`, players can interact with the world, build, mine, and use basic commands.
- If set to `operator`, players have access to all commands and administrative privileges.

---

### chat-restriction

Possible Values: None, Dropped, Disabled  
Default Value: None  

Allows control over chat functionality.

- If set to `None`, regular free chat is allowed.
- If set to `Dropped`, chat messages are dropped and never sent to any client. Players receive a message indicating the feature is disabled.
- If set to `Disabled`, the chat UI does not appear for non-operator players. No information is displayed to the player.

---

### disable-custom-skins

Possible Values: Boolean  
Default Value: false  

Helps maintain a controlled visual environment and prevents potentially offensive custom skins.

- If set to `true`, disables players' custom skins that were customized outside of the Minecraft store assets or in-game assets.

---
