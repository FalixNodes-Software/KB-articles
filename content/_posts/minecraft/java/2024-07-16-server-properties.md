---
layout: post
title: Configuring server.properties
category: Java
tags: Server
description: Editing the commonly used attributes of the server.properties file to configure your Java server.
permalink: /minecraft/java/server/server-properties
author:
    - Kuroi
    - Mocab
---

## :scroll: Introduction:

Understanding the [server.properties](https://server.properties) file is crucial for configuring and customizing your Minecraft server. This guide highlights the essential attributes within the file, enabling you to optimize and alter your server settings for the best gameplay experience.

## :pencil2: Accessing & Configuring server.properties

There are two possible methods to access server.properties, you may either directly alter the file found in the [File Manager](https://client.falixnodes.net/server/filemanager?dir=/), or using our server.properties editor:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Scroll down and choose a server, then click on "Play".

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). On the top navigation bar, hover over "Manage" then click on [Server Properties](https://client.falixnodes.net/server/properties).

To edit a setting, depending on the type, you may have to select an option from the given dropdown or type in a string of values. Settings that only accept a `true` or `false` value are referred to as booleans, while settings that require a typed value are called strings. In boolean settings, `true` signifies enabled while `false` signifies disabled.

To save your changes, simply click on "Submit" at the top of the properties list.

### :wrench: Configurations:

**accepts-transfers**

Possible Values: Boolean
Default Value: `false`

This setting determines if the server accepts player transfers from other servers in a network.
It's often used in server networks to facilitate smooth transitions between different server instances using the `/transfer` command.

---

**allow-flight**

Possible Values: Boolean
Default Value: `false`

This option determines whether or not the server checks if players are flying. It's useful for servers with plugins that don't override this check and allow flight in Survival mode.

> Most cheat clients bypass this check easily, making it essentially useless and making trouble with false positives. If you want to protect from hackers, you should use an Anti Cheat.

---

**allow-nether**

Possible Values: Boolean
Default Value: `true`

This setting controls whether players can travel to the Nether dimension. Disabling it prevents players from accessing the Nether, which can be useful for servers with specific gameplay rules.

---

**broadcast-console-to-ops**

Possible Values: Boolean
Default Value: `true`

This property controls whether console command outputs are shown to online operators.

---

**broadcast-rcon-to-ops**

Possible Values: Boolean
Default Value: `true`

This property controls whether RCON command outputs are shown to online operators.

---

**bug-report-link**

Possible Values: URL
Default Value: ` `

A URL where players are able to report bugs and issues in the server. This can be accessed within the client's menu by navigating to "Server Links..." and then "Report Server Bug". Players will then be prompted with a warning message with the URL of the website provided.

---

**debug**

Possible Values: Boolean
Default Value: `false`

Enabling this option will cause the server to display additional information relating to its inner functions and processes in the console. As is clear from it's name, it is very useful for server owner's looking to fix bugs and other issues in their server.

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

**enable-command-block**

Possible Values: Boolean
Default Value: `false`

Command blocks allow for automation and complex commands within the game. Enabling them can enhance server functionality if used, but may pose security risks if not properly managed. They are often used in custom maps and some datapacks.

---

**enable-rcon**

Possible Values: Boolean
Default Value: `false`

Remote Control (RCON) is an alternate way to access the server console through an RCON client such as [MCRCON](https://github.com/Tiiffi/mcrcon/).

---

**enable-status**

Possible Values: Boolean
Default Value: `true`

When disabled, your server will appear as if it is offline in the server list without any additional information being shared. However, players will still be able to join the server.

---

**enforce-secure-profile**

Possible Values: Boolean
Default Value: `true`

This setting ensures that players without a Mojang-signed public key will not be able to connect to the server. And therefore, players without a legitimate copy of the game or those with mods that alter their messages or public keys will be prevented from joining your server.

---

**enforce-whitelist**

Possible Values: Boolean
Default Value: `false`

Enabling this setting ensures that only players listed in the whitelist can join the server, providing control over the players you want to join. This is ideal for private or community servers that limit access to certain players.

{: .warning }

> The whitelist is not reliable and can easily be bypassed if `online-mode` is set to `false`.

---

**entity-broadcast-range-percentage**

Possible Values: Between `10` to `1000` percent
Default Value: `100`

Controls how close entities are sent to the client; at higher values, players will be able to see entities (such as mobs) at a farther distance at the cost of performance.

---

**force-gamemode**

Possible Values: Boolean
Default Value: `false`

This setting forces all players to be switched to the default game mode upon (re)joining the server.

---

**function-permission-level**

Possible Values: Integer between `1` to `4`
Default Value: `2`

Sets the default required permission level to run `/function`, with 1 being the least power and 4 being operator level. Functions are provided by datapacks as a way to run certain features provided by the datapack itself.

---

**gamemode**

Possible Values: `survival`, `creative`, `adventure`, `spectator`
Default Value: `survival`

This setting defines the default game mode for players joining the server, such as survival, creative, or adventur mode.

---

**generate-structures**

Possible Values: Boolean
Default Value: `true`

This setting controls whether structures like villages and desert temples generate in the world.

---

**generator-settings**

Possible Values: String
Default Value: `{}`

Highly customizable arguments used to generate your world file, allowing you to alter world generation. You may either use online generators or refer to the guide provided by the [Minecraft Wiki](https://minecraft.wiki/w/Java_Edition_level_format#generatorOptions_tag_format).

---

**hardcore**

Possible Values: Boolean
Default Value: `false`

Enabling this will change the server difficulty to hard while giving the player a single life, once this life is lost, the player will only be allowed to spectate their world.

---

**hide-online-players**

Possible Values: Boolean
Default Value: `false`

Allows you to hide the names of players online when viewed in the server list.

---

**level-name**

Possible Values: String
Default Value: `world`

The name given to the world folder.

---

**level-seed**

Possible Values: String
Default Value: ` `

This setting allows specifying a seed for world generation, enabling the creation of specific world layouts or replicating previous worlds. In order for this change to take effect, old worlds must be deleted to allow one with the set seed to be generated.

---

**level-type**

Possible Values: `minecraft:normal`, `minecraft:flat`, `minecraft:large_biomes`, `minecraft:amplified`, `minecraft:single_biome_surface`
Default Value: `minecraft:normal`

Alters the type of world generation, allowing different styles, such as flat and amplified to be generated. As such, previous worlds must be deleted to allow a new world with the set settings to be created.

-   `normal` Generates a normal world with all standard features, such as hills and rivers.
-   `flat` Generates a flat plains world with no land features.
-   `large_biomes` Same as normal, but with larger and bigger biomes.
-   `amplified` Same as normal, but world generation height is increased, resulting in more mountains and taller biomes.
-   `single_biome_surface` Generates the entire overworld as a single biome.

---

**log-ips**

Possible Values: Boolean
Default Value: `true`

Determines if player IP addresses are logged upon connection, which can be useful for monitoring and security purposes. Set this to `false` if you prefer the server to be privacy-friendly.

---

**max-players**

Possible Values: Integer
Default Value: `20`

This setting specifies the maximum number of players allowed on the server simultaneously, impacting server load and community size.

---

**max-tick-time**

Possible Values: Integer (milliseconds) or `-1`
Default Value: `60000`

This setting defines the maximum time in milliseconds a single tick may take before the server watchdog stops the server, causing the server to be shutdown resulting in a crash. A value of `-1` will result in it being disabled.

---

**max-world-size**

Possible Values: Integer
Default Value: `29999984`

The maximum allowed size of the world radius, in blocks. This only affects the chunks that are generated when the world is initially created, and not the world border.

---

**motd**

Possible Values: String
Default Value: `A Minecraft Server`

The message of the day (MOTD) is displayed in the server list and provides a brief description or welcome message for players.

> Refer to the [MOTD](https://kb.falixnodes.net/minecraft/java/server/motd) article for instructions on how to create one!

---

**network-compression-threshold**

Possible Values: Integer (bytes) or `-1`
Default Value: `512`

The maximum number of bytes of a packet before it is compressed. A value of `-1` disables this setting.

---

**online-mode**

Possible Values: Boolean
Default Value: `true`

This setting requires players to authenticate with Minecraft's account database before joining, preventing players with illegitimate accounts from connecting. Disabling this configuration will allow cracked players to join your server.

---

**op-permission-level**

Possible Values: Integer between `1` to `4`
Default Value: `4`

The permission level to grant to server operators by default. With `1` being the least powerful and `4` being the highest permissions.

---

**player-idle-timeout**

Possible Values: Integer (minutes)
Default Value: `0`

This setting determines how long a player can be idle before being kicked from the server, helping to manage active player slots.

---

**pvp**

Possible Values: Boolean
Default Value: `true`

Controls whether players can engage in player-versus-player combat, or in other words fight each other with weapons.

---

**rate-limit**

Possible Values: Integer
Default Value: `0`

Limits the maximum amount of packets that can be sent before being kicked. Leaving this value as `0` disables it.

---

**rcon-password**

Possible Values: String
Default Value: ` `

Sets the password used to authenticate when connecting with RCON.

---

**rcon-port**

Possible Values: Integer
Default Value: `25575`

Sets the port used to connect when using RCON. This will only work when set to an extra port.

---

**require-resource-pack**

Possible Values: Boolean
Default Value: `false`

Forces players to use the server provided resource pack otherwise kicking them out.

---

**resource-pack**

Possible Values: URL
Default Value: ` `

This setting specifies a direct download URL of the server's resource pack, prompting users to use the provided resource pack when joining.

---

**resource-pack-id**

Possible Values: String
Default Value: ` `

This setting provides the UUID of the resource pack, used to identify and verify the correct pack version.

---

**resource-pack-prompt**

Possible Values: String
Default Value: ` `

This setting displays a custom message when players are prompted to download the resource pack, providing additional information or instructions.

---

**resource-pack-sha1**

Possible Values: String
Default Value: ` `

This setting provides a hash of the resource pack for verification, ensuring players download the correct and unmodified pack.

---

**simulation-distance**

Possible Values: Integer
Default Value: `10`

Controls the chunk radius around each player where chunks are ticked, meaning mobs and gameplay mechanics are active, affecting server performance and gameplay experience.

---

**spawn-animals**

Possible Values: Boolean
Default Value: `true`

Affects whether animals can spawn naturally in the world.

---

**spawn-monsters**

Possible Values: Boolean
Default Value: `true`

This setting controls whether monsters can spawn naturally in the world.

---

**spawn-npcs**

Possible Values: Boolean
Default Value: `true`

This setting controls whether villagers and other NPCs can spawn naturally in the world.

---

**spawn-protection**

Possible Values: Integer
Default Value: `16`

This setting defines a protected area of blocks around the spawn point where players cannot build or destroy blocks, helping to preserve the spawn environment.

---

**view-distance**

Possible Values: Integer
Default Value: `10`

This setting determines a chunk radius around each player where the server sends information about the world, affecting how much of the world is loaded and visible.

---

**white-list**

Possible Values: Boolean
Default Value: `false`

This setting enables a whitelist on the server, allowing only selected users to connect and providing controlled access to the server. Which is ideal for private servers or community servers where certain servers requires only limited access of players.

{: .warning }

> The whitelist is not reliable and can easily be bypassed if `online-mode` is set to `false`.
