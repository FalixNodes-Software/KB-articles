---
layout: help/article
title:  "Configure server.properties for Your Minecraft Server"
categories: Minecraft
icon: <i class="fa-light fa-sword"></i>
tag: mcgeneral
permalink: /help/minecraft/general/serverproperties.*
gitURL: _posts/minecraft/general/2023-09-29-server-properties.md
description: "Configure your Minecraft server using the server.properties in Falix"

author: Mocab
authorGitHub: mocab
---

## Server Properties (server.properties)

The [server.properties](https://server.properties) file is where your server's configurations are stored, it provides the ability to alter certain settings and mechanics of your server. Furthermore, it can be used to customize your server in any way based on your needs.

## Format

The format of this file is very simple. First comes the "key", which is used to identify the setting/configuration, then an equal sign "=", and last but not least, the "value" of the key. All of them combined on one line is called a "string". One such example is:

```java
online-mode=true
```

"true" is used to signify enabled and "false" is used to signify disabled.
{: .note }
> Make sure to not add any extra spaces as it may cause errors.
> All strings are case-sensitive, so make sure to write them as is.
> If a certain string does not exist, you may simply add it in a new line.

## Configuration

### Remote Console (RCON) Port

Default string:

```java
rcon.port=25575
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Sets the port needed to access your console using RCON.     | An extra port currently not being used by the server.|

#### World seed

Default string:

```java
level-seed=
```

| Description:                                                | Accepted values:                            |
|-------------------------------------------------------------|------------------------------------------------|
| Sets the seed used by the server when generating a new world.| Any value is acceptable and an empty value will cause your server to use a random seed.|

#### Game Mode

Default string:

```java
gamemode=survival
```

| Description:                                                | Accepted values:                            |
|-------------------------------------------------------------|------------------------------------------------|
| Controls the default game mode for the server.              | `survival`, `creative`, `adventure` or `spectator`|

#### Command Block

Default string:

```java
enable-command-block=false
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Controls whether command blocks can be used.                | `true` or `false`                            |

#### Enforce Secure Profile

Default string:

```java
enforce-secure-profile=true
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Controls whether only players with a public signature key can join the server. Setting this to `false` will allow any launcher to connect to your server.| `true` or `false`|

#### Server Message

Default string:

```java
motd=A Minecraft Server
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Sets the message displayed below the server name in the Minecraft client.| Any string under 60 characters is allowed including color and formatting codes, as well as special characters.|

#### Player VS Player

Default string:

```java
pvp=true
```

| Description:                                                | Accepted values:                            |
|-------------------------------------------------------------|------------------------------------------------|
| Controls whether or not players can harm each other.        |  `true` or `false`                             |

#### Generate Structures

Default string:

```java
generate-structures=true
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Controls whether naturally-generated structures, such as villages, can spawn in newly generated chunks in your server's world.| `true` or `false`|

#### Difficulty

Default string:

```java
difficulty=easy
```

| Description:                                                | Accepted values:                            |
|-------------------------------------------------------------|----------------------------------------------|
| Controls the difficulty level of the server.                | `peaceful`, `easy`, `normal`, or `hard`      |

#### Max Tick Time

Default string:

```java
max-tick-time=60000
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Controls the amount of time (in milliseconds) a tick is allowed to take before the server crashes.| Any integer is allowed (`-1` to disable).|

#### Require Resource Pack

Default string:

```java
require-resource-pack=false
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Controls whether the player is required to use the server resource pack. If they fail to do so, they will be disconnected.| `true` or `false`|

#### Online Mode

Default string:

```java
online-mode=true
```

| Description:                                                | Accepted values:                            |
|-------------------------------------------------------------|------------------------------------------------|
| Controls whether or not the server will authenticate players with Mojang's servers. In other words, setting this to false will allow players without a legitimate Minecraft account to join your server.|  `true` or `false`|

#### Flying

Default string:

```java
allow-flight=false
```

| Description:                                                | Accepted values:                            |
|-------------------------------------------------------------|------------------------------------------------|
| Controls whether or not players are allowed to fly using exploits or mods.| `true` or `false`                |

#### Broadcast Remote Console (RCON) to OPs

Default string:

```java
broadcast-rcon-to-ops=true
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Controls whether operators will see commands executed via RCON.| `true` or `false`                         |

#### View Distance

Default string:

```java
view-distance=10
```

| Description:                                                | Accepted values:                            |
|-------------------------------------------------------------|------------------------------------------------|
| Controls the number of chunks (16x16 blocks) that can be seen by the player in each direction.|  Any integer between `3` and `32`.|

#### Resource Pack Prompt

Default string:

```java
resource-pack-prompt=
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Sets a custom resource pack prompt if a server resource pack is defined.| Any message is allowed.          |

#### Allow Nether

Default string:

```java
allow-nether=true
```

| Description:                                                | Accepted values:                            |
|-------------------------------------------------------------|------------------------------------------------|
| Controls whether players can travel to the Nether dimension.|  `true` or `false`                             |

#### Remote Console (RCON)

Default string:

```java
enable-rcon=false
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Controls if RCON is enabled for the server.                 | `true` or `false`                            |

#### Hide Online Players

Default string:

```java
hide-online-players=false
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Controls if the number of players online can be seen from the Minecraft launcher server list.| `true` or `false`|

#### Resource Pack

Default string:

```java
resource-pack=
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Sets the server's resource pack.                            | Any link that can be downloaded by the server.|

#### Simulation Distance

Default string:

```java
simulation-distance=10
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Sets the number of chunks (16x16 blocks) in each direction from each player in which entities will remain loaded.| Any integer between `3` and `32`.|

#### Remote Console (RCON) Password

Default string:

```java
rcon.password=
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Sets a password for RCON.                                   | Any password is valid.                       |

#### Player Idle Timeout

Default string:

```java
player-idle-timeout=0
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Controls when players will be kicked from the server if they are idle (minutes).| Any Integer (`0` to disable).|

#### Force Gamemode

Default string:

```java
force-gamemode=false
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Controls whether or not players should be in the same gamemode as the server every time they join the server.| `true` or `false`|

#### Hardcore

Default string:

```java
hardcore=false
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Controls whether or not hardcode mode is enabled.           | `true` or `false`                            |

#### Whitelist

Default string:

```java
white-list=false
```

| Description:                                                | Accepted values:                            |
|-------------------------------------------------------------|------------------------------------------------|
| Controls whether or not whitelisting is enabled.            |  `true` or `false`                             |

#### Broadcast Console to OPs

Default string:

```java
broadcast-console-to-ops=true
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Controls whether operators will see executed commands of other operators in chat.| `true` or `false`       |

#### Spawn NPCs

Default string:

```java
spawn-npcs=true
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| Controls whether or not villagers and other NPCs spawn.     | `true` or `false`                            |

#### Spawn Animals

Default string:

```hava
spawn-animals=true
```

| Description:                                                | Accepted values:                            |
|-------------------------------------------------------------|------------------------------------------------|
| Controls whether or not animals will spawn.                 |  `true` or `false`                             |

#### Spawn Monsters

Default string:

```java
spawn-monsters=true
```

| Description:                                                | Accepted values:                            |
|-------------------------------------------------------------|------------------------------------------------|
| Controls whether or not monsters or hostile mobs will spawn.|  `true` or `false`                             |

#### Enforce Whitelist

Default string:

```java
enforce-whitelist=false
```

| Description:                                                | Accepted values:                             |
|-------------------------------------------------------------|----------------------------------------------|
| If set to `true`, any online player not in the whitelist will be kicked out of the server.| `true` or `false`|

#### Spawn Protection

Default string:

```java
spawn-protection=16
```

| Description:                                                | Accepted values:                            |
|-------------------------------------------------------------|------------------------------------------------|
| Controls the number of blocks in each direction from your world's spawn block that cannot be interacted with without being a server operator.| Any integer between 0-16 (0 will disable spawn protection)|
