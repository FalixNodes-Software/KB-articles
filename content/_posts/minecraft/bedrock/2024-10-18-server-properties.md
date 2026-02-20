---
title: How to Configure Your Minecraft Bedrock Server Properties
tags: Customization
description: Editing and customising common attributes of the server.properties file.
keywords:
    - keyword: server
      matches: ["properties", "configuration", "config", "settings"]
    - keyword: custom
      matches: ["seed", "view distance", "tick distance"]
    - keyword: change
      matches: &change_matches ["seed", "view distance", "tick distance", "gamemode", "game mode", "difficulty", "max players", "maximum players"]
    - keyword: set
      matches: *change_matches
    - keyword: allow
      matches: &allow_matches ["cheats", "cracked"]
    - keyword: enable
      matches: *allow_matches
    - keyword: disable
      matches: *allow_matches
permalink: /minecraft/bedrock/customization/server-properties
author:
    - Kuroi
    - Mocab
---

Understanding the [server.properties](https://server.properties) file is crucial for configuring and customizing your Minecraft server. This guide highlights the essential attributes within the file, enabling you to optimize and alter your server settings for the best gameplay experience.

## Accessing & Configuring server.properties

There are two possible methods to access server.properties, you may either directly alter the file found in the [File Manager](https://client.falixnodes.net/server/filemanager?dir=/), or using our server.properties editor:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console)  of your server. In the navigation menu, open the "Minecraft" category and navigate to [Server Properties](https://client.falixnodes.net/server/properties).

To edit a setting, depending on the type, you may have to select an option from the given dropdown or type in a string of values. Settings that only accept a `true` or `false` value are referred to as booleans, while settings that require a typed value are called strings. In boolean settings, `true` signifies enabled while `false` signifies disabled.

To save your changes, simply click on "**Submit**{: .blue }" at the top of the properties list.

### Configurations:

**server-name**

Possible Values: String  
Default Value: `Dedicated Server`

Specifies the name of the server as it appears in the multiplayer server list.

---

**gamemode**

Possible Values: `survival`, `creative`, `adventure`, `spectator`
Default Value: `survival`

This setting defines the default game mode for players joining the server, such as survival, creative, or adventure mode.

---

**force-gamemode**

Possible Values: Boolean
Default Value: `false`

This setting forces all players to be switched to the default game mode upon (re)joining the server.

---

**difficulty**

Possible Values: `peaceful`, `easy`, `normal`, `hard`
Default Value: `easy`

This setting defines the difficulty level of the server, affecting mob behavior and player damage.

-   If set to `peaceful`, no hostile mobs will spawn and health regenerates quickly.
-   If set to `easy`, hostile mobs will spawn but deal less damage compared to `normal`. Hunger depletes slowly.
-   If set to `normal`, mobs will deal average damage. Some additional behavior is enabled (eg. vindicators can break doors).
-   If set to `hard`, hostile mobs will deal more damage, hunger will deplete faster, and additional behavior is enabled, including the changes from `normal`.

---

**allow-cheats**

Possible Values: Boolean  
Default Value: `false`

Enabling cheats allows server administrators (operators) to use commands that can alter gameplay mechanics, spawn items, teleport players, and more.

{: .warning}

> Enabling this option will disable achievements!

---

**max-players**

Possible Values: Integer between `1` to `65534`
Default Value: `10`

The maximum number of players that can play on the server at the same time.

---

**online-mode**

Possible Values: Boolean
Default Value: `true`

This setting requires players to authenticate with Xbox Live before joining, preventing players with illegitimate accounts from connecting. Disabling this configuration will allow cracked players to join your server.

---

**allow-list**

Possible Values: Boolean  
Default Value: `false`

Enabling this setting ensures that only players listed in the allowlist can join the server, providing control over the players you want to join. This is ideal for private or community servers that limit access to certain players.

{: .warning }

> The allow list is not reliable and can easily be bypassed if `online-mode` is set to `false`.

---

**view-distance**

Possible Values: Integer equal or above `5`  
Default Value: `32`

This setting determines a chunk radius around each player where the server sends information about the world, affecting how much of the world is loaded and visible.

---

**tick-distance**

Possible Values: Integer between `4` to `12`  
Default Value: `4`

Determines the radius in chunks around each player where mobs and certain gameplay mechanics are active and simulated. Directly impacts server performance and gameplay experience.

---

**player-idle-timeout**

Possible Values: Integer (minutes)
Default Value: `30`

This setting determines how long a player can be idle before being kicked from the server, helping to manage active player slots. If set to 0, players can idle indefinitely.

---

**level-name**

Possible Values: String
Default Value: `Bedrock level`

The name given to the world folder.

---

**level-seed**

Possible Values: String
Default Value: ` `

This setting allows specifying a seed for world generation, enabling the creation of specific world layouts or replicating previous worlds. In order for this change to take effect, old worlds must be deleted to allow one with the set seed to be generated. If unspecified, a random value is used.

---

**default-player-permission-level**

Possible Values: `visitor`, `member`, `operator  `
Default Value: `member`

Permission level for new players joining for the first time.

-   If set to `visitor`, players can interact with the world but cannot modify it or use most basic commands.
-   If set to `member`, players can interact with the world, build, mine, and use basic commands.
-   If set to `operator`, players have access to all commands and administrative privileges.

---

**texturepack-required**

Possible Values: Boolean
Default Value: `false`

Forces players to use the server provided resource pack.

---

**content-log-file-enabled**

Possible Values: Boolean
Default Value: `false`

Enables generating a log file.

---

**compression-threshold**

Possible Values: Integers between `0` to `65535`
Default Value: `1`

The maximum size of a packet before it is compressed.

---

**chat-restriction**

Possible Values: `None`, `Dropped`, `Disabled`  
Default Value: `None`

Allows control over the chat functionality.

-   If set to `None`, regular free chat is allowed.
-   If set to `Dropped`, chat messages are dropped and never sent to any client. Players receive a message indicating the feature is disabled.
-   If set to `Disabled`, the chat UI does not appear for non-operator players. No information is displayed to the player.

---

**disable-custom-skins**

Possible Values: Boolean  
Default Value: `false`

If enabled, disables players' custom skins that were customized outside of the Minecraft store assets or in-game assets, preventing potentially offensive custom skins.
