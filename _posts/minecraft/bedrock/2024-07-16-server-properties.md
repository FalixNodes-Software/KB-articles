---
layout: post
title:  "Configuring Minecraft Server: Server Properties"
category: 
    - Bedrock
    - Getting-started
tags: Server
description: "Explore the commonly used attributes of the server.properties file to effectively configure your Bedrock Minecraft server"
permalink: /minecraft/bedrock/server/server-properties
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

- If set to `survival`, players must gather resources, build structures, and survive against hostile mobs.
- If set to `creative`, players have unlimited resources, can fly, and are not attacked by hostile mobs.
- If set to `adventure`, players can interact with objects like levers and buttons but cannot break blocks.

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
- If set to `easy`, hostile mobs spawn but deal less damage, and hunger depletes slowly.
- If set to `normal`, standard difficulty with mobs dealing normal damage and hunger depletion.
- If set to `hard`, hostile mobs deal more damage and hunger depletes faster.

---

### allow-cheats

Possible Values: Boolean  
Default Value: false  

Enabling cheats allows server administrators (operators) to use commands that can alter gameplay mechanics, spawn items, teleport players, and more.

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

Ideal for private or community servers that require limited access to only certain players.

- If `true`, all connected players must be listed in the separate allowlist.json file.
- Works similarly to Java Edition's Whitelist.

---

### view-distance

Possible Values: Integer (>=5)  
Default Value: 32  

Determines the radius (in chunks) around each player where the server sends information about the game world.

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

This setting determines how long a player can be idle before being kicked from the server, helping to manage active player slots. value is measured in minutes.

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

Allows control over chat functionality, enhancing server moderation and player experience.

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
