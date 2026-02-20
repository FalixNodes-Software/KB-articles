---
layout: post
title: "World Settings"
tags: Server
permalink: falix/dashboard/general/world-settings
description: "Configure game rules, time, weather, spawning, world border, and more for individual worlds."
keywords:
    - keyword: game rules
      matches: ["keepinventory", "mobgriefing", "pvp", "daylight"]
    - keyword: world settings
      matches: ["configure", "edit", "world", "rules"]
    - keyword: spawn
      matches: ["point", "location", "coordinates", "protection"]
    - keyword: weather
      matches: ["rain", "thunder", "clear", "toggle"]
    - keyword: time
      matches: ["day", "night", "cycle", "ticks"]
    - keyword: world border
      matches: ["size", "center", "limit", "boundary"]
author: Lily
---

## Introduction
Every world on your server can play by its own rules. Maybe your main survival world has `keepInventory` on and PvP off, while your arena world cranks up the difficulty with hardcore mode. World Settings is where you make that happen — you can fine-tune game rules, weather, time, spawn points, the world border, and a lot more, all on a per-world basis.

To get started, head to the [Worlds](/falix/dashboard/general/worlds) page and click **Settings** on any world card.

## Search and Filter
If you already know the setting you're looking for, use the search bar at the top to find it by name or description. You can also filter by category using the dropdown, which is handy when you just want to browse what's available.

## Setting Categories

### Essential
These are the big three — the settings you'll probably change first on any new world. **Difficulty** lets you pick between Peaceful, Easy, Normal, or Hard. **Game Type** sets the default mode for players joining the world: Survival, Creative, Adventure, or Spectator. And **DataPacks** opens a modal where you can enable or disable any installed datapacks.

### World and Spawn
This category gives you control over where players land and what the world boundaries look like.

| Setting | Type | Description |
|---------|------|-------------|
| **Spawn X, Y, Z** | Number inputs | World spawn coordinates with yaw and pitch rotation |
| **Level Name** | Text | World display name |
| **Border Size** | Number | World border radius in blocks |
| **Border Center X, Z** | Number | World border center position |
| **Border Damage Per Block** | Number | Damage taken outside the border |
| **Hardcore** | Toggle | Hardcore mode (permanent death) |
| **Difficulty Locked** | Toggle | Prevent difficulty changes |
| **Allow Commands** | Toggle | Allow cheats in survival |

{: .info}
> If you run events or minigames, setting a tight **Border Size** with a high **Border Damage Per Block** is a great way to keep players contained without needing plugins.

### Time and Weather
These settings control the current time of day, weather state, and how long until conditions change. All tick-based values display a human-readable time conversion (for example, "2 days, 3 hours, 15 minutes (172,800 ticks)"), so you don't need to do the math yourself.

| Setting | Type | Description |
|---------|------|-------------|
| **Time** | Number | Current world time in ticks (shows in-game hours:minutes) |
| **Day Time** | Number | Time of day for /time query |
| **Rain Time** | Number | Ticks until rain state changes (shows human-readable time) |
| **Thunder Time** | Number | Ticks until thunder state changes |
| **Clear Weather Time** | Number | Guaranteed clear weather in ticks |
| **Raining** | Toggle | Is it currently raining |
| **Thundering** | Toggle | Is there a thunderstorm |

### Technical Info
This section is mostly read-only information about the world file itself. You'll find the Minecraft version the world was created with, the last time it was loaded, how much disk space it uses, and whether it was ever used with mods. There are also a few advanced modals here:

- **Data Version** and **Version** show the NBT data format version and Minecraft version details (read-only).
- **Server Brands** is an editable list of server software names (Vanilla, Spigot, Paper, and so on).
- **Last Played** shows when the world was last loaded, and **Size on Disk** shows the world size in a human-readable format.
- **Was Modded** tells you whether the world has been used with mods.
- **World Gen Settings** opens a modal for viewing the seed, bonus chest toggle, structures toggle, and dimension list.
- **Dragon Fight** shows dragon kill status, times killed, and which end gateways have been activated.
- **Scheduled Events** and **Custom Boss Events** are read-only lists of scheduled game events and custom boss bars, respectively.

{: .info}
> You generally won't need to touch anything here unless you're troubleshooting or migrating a world between server software.

## Game Rules
Click the **Game Rules** button to open the full game rules editor. Rules are searchable and organized by category, so you can quickly jump to whatever you need to change.

### Mobs and Entities
These rules determine how mobs behave in your world — whether they spawn at all, whether they can grief blocks (looking at you, Creepers), and how they interact with players. If you want a peaceful building experience without switching to Peaceful difficulty, turning off `doMobSpawning` is one way to do it while keeping hunger and other survival mechanics intact.

| Rule | Type | Description |
|------|------|-------------|
| **doMobSpawning** | Toggle | Mob spawning |
| **mobGriefing** | Toggle | Mobs can destroy blocks |
| **doMobLoot** | Toggle | Mobs drop items on death |
| **doPatrolSpawning** | Toggle | Pillager patrols |
| **doTraderSpawning** | Toggle | Wandering traders |
| **doWardenSpawning** | Toggle | Wardens in the deep dark |
| **doInsomnia** | Toggle | Phantoms spawn when players skip sleep |
| **maxEntityCramming** | Number | Entity push limit (0 = disabled) |
| **universalAnger** | Toggle | Angered mobs attack any player |
| **forgiveDeadPlayers** | Toggle | Mobs calm when a player dies |

{: .warning}
> Disabling `mobGriefing` prevents Creeper explosions from destroying blocks, but it also stops Endermen from picking up blocks and villagers from farming. Keep that side effect in mind.

### Player and Death
These rules control what happens to players — especially around death. Whether players keep their inventory on death is one of the most commonly changed settings on any server, and you'll find it right here.

| Rule | Type | Description |
|------|------|-------------|
| **keepInventory** | Toggle | Keep items on death |
| **pvp** | Toggle | Player-versus-player damage |
| **naturalRegeneration** | Toggle | Health regeneration from food |
| **doImmediateRespawn** | Toggle | Skip the death screen |
| **playersSleepingPercentage** | Number | Percentage of players needed to skip night (0--100) |
| **spawnRadius** | Number | Spawn point spread in blocks |
| **showDeathMessages** | Toggle | Display death messages in chat |
| **drowningDamage** | Toggle | Drowning causes damage |
| **fallDamage** | Toggle | Fall damage |
| **fireDamage** | Toggle | Fire and lava damage |
| **freezeDamage** | Toggle | Powder snow freezing damage |

{: .info}
> `keepInventory` is by far the most popular game rule change on survival servers. If you're running a casual or family-friendly server, turning it on saves a lot of frustration. Setting `playersSleepingPercentage` to 0 means a single player can skip the night without everyone needing to be in a bed.

### Time and Weather
These rules let you freeze or adjust the passage of time, weather cycles, and the speed at which things grow. If you want a permanent daytime build world, just disable `doDaylightCycle` and set the time to noon.

| Rule | Type | Description |
|------|------|-------------|
| **doDaylightCycle** | Toggle | Day/night cycle progression |
| **doWeatherCycle** | Toggle | Weather changes |
| **randomTickSpeed** | Number | Block tick speed (default: 3, higher = faster crop growth) |
| **doFireTick** | Toggle | Fire spreads |
| **doVinesSpread** | Toggle | Vine growth |

{: .info}
> If your server is experiencing lag, try reducing `randomTickSpeed` below the default of 3. Higher values make crops, leaves, and other random-tick blocks update faster, but they also put more load on the server. Conversely, setting it to 0 stops crop growth entirely.

### Blocks and Items
This category controls what drops when blocks are broken or things explode. It's also where you'll find settings for TNT behavior, snow accumulation, and infinite source block creation.

| Rule | Type | Description |
|------|------|-------------|
| **doTileDrops** | Toggle | Blocks drop items when mined |
| **doEntityDrops** | Toggle | Non-mob entities drop items |
| **tntExplodes** | Toggle | TNT can explode |
| **tntExplosionDropDecay** | Toggle | Random drop destruction from TNT |
| **mobExplosionDropDecay** | Toggle | Mob explosion drops |
| **blockExplosionDropDecay** | Toggle | Block explosion drops |
| **projectilesCanBreakBlocks** | Toggle | Projectiles can break blocks |
| **snowAccumulationHeight** | Number | Max snow layers (1--8) |
| **lavaSourceConversion** | Toggle | Infinite lava source creation |
| **waterSourceConversion** | Toggle | Infinite water source creation |

### Commands and Cheats
If you use command blocks on your server or want to control what feedback players see from commands, these are the settings to look at. Most of these can be left at their defaults unless you're building custom maps or minigames with command block logic.

| Rule | Type | Description |
|------|------|-------------|
| **commandBlockOutput** | Toggle | Broadcast command block output |
| **sendCommandFeedback** | Toggle | Show command results to players |
| **logAdminCommands** | Toggle | Log admin commands to console |
| **maxCommandChainLength** | Number | Max command chain length (default: 65,536) |
| **maxCommandForkCount** | Number | Max command forks (default: 65,536) |
| **commandModificationBlockLimit** | Number | Max blocks modified by commands (default: 32,768) |
| **commandBlocksEnabled** | Toggle | Allow command blocks |

### Advanced Gameplay
These rules cover a mix of features that don't fit neatly into the other categories — things like requiring recipe unlocks, disabling raids, controlling advancement announcements, and adjusting Nether portal delays.

| Rule | Type | Description |
|------|------|-------------|
| **doLimitedCrafting** | Toggle | Require recipe unlock before crafting |
| **disableRaids** | Toggle | Prevent pillager raids |
| **announceAdvancements** | Toggle | Broadcast advancement completion |
| **reducedDebugInfo** | Toggle | Limit F3 debug info |
| **spectatorsGenerateChunks** | Toggle | Spectators load new chunks |
| **enderPearlsVanishOnDeath** | Toggle | Ender pearls vanish when thrower dies |
| **globalSoundEvents** | Toggle | Broadcast sound events server-wide |
| **playersNetherPortalDefaultDelay** | Number | Nether portal teleport delay in ticks (default: 80) |

### Performance and Safety Indicators
Some game rules display badges next to them to help you make informed decisions:

- **Warning** badges appear on settings like `disablePlayerMovementCheck` and `commandBlocksEnabled` to flag that enabling them carries some risk.
- **Performance** badges show up on settings like `randomTickSpeed` and `maxEntityCramming` with a note about their impact (for example, "Higher values = faster growth but more lag").

{: .info}
> These indicators are there to help — if you see one, it's worth reading the note before making changes.

## Datapack Manager
The datapack modal gives you a simple dual-list interface. Enabled packs appear on the left and disabled packs on the right. Double-click a pack or use the arrow buttons to move it between the two lists.

{: .warning}
> The `vanilla` datapack cannot be disabled — it's always required.

## Advanced World Settings
These are lower-level settings that most server owners won't need to touch often, but they're useful for fine-tuning world generation and border behavior.

| Setting | Type | Description |
|---------|------|-------------|
| **Wandering Trader Spawn Chance** | Number | 0--100 percentage |
| **Wandering Trader Spawn Delay** | Number | Ticks between spawn attempts |
| **Map Features** | Toggle | Structure generation |
| **Generator Name** | Text | World type (default, flat, large_biomes, amplified) |
| **Random Seed** | Number | World generation seed |
| **Border Warning Blocks** | Number | Distance from border for warning vignette |
| **Border Warning Time** | Number | Seconds before border shrinks |
| **Border Safe Zone** | Number | Safe zone buffer in blocks |

## Bedrock Edition Settings
When you're editing a Bedrock world, some additional categories will show up automatically.

### Bedrock Edition
This section includes settings for spawn location, biome override, generator type, LAN broadcast, commands, bonus chest, multiplayer mode, and texture pack requirement. These are specific to how Bedrock Edition handles worlds and won't appear for Java worlds.

### Experimental Features
Bedrock Edition has a set of experimental toggles for features that are still in development. Enable these if you want to test cutting-edge functionality, but keep in mind they may change or break between updates.

| Feature | Description |
|---------|-------------|
| **Beta APIs** | Beta scripting APIs |
| **Creator Features** | Preview modding features |
| **Villager Trades Rebalance** | Rebalanced villager trades |
| **Data Driven Biomes** | Custom biomes via behavior packs |
| **Data Driven Items** | Custom items via behavior packs |
| **Jigsaw Structures** | Jigsaw structure generation |
| **Deferred Rendering** | Render Dragon deferred rendering |

{: .warning}
> Experimental features can cause world corruption in rare cases. Back up your world before enabling any of these.

## Hytale Settings
When editing a Hytale world, two specific categories appear in place of the standard Minecraft settings.

### World Settings

| Setting | Type | Description |
|---------|------|-------------|
| **Is Ticking** | Toggle | World tick updates |
| **Is Block Ticking** | Toggle | Block ticks (crop growth, etc.) |
| **Is PvP Enabled** | Toggle | Player damage |
| **Is Fall Damage Enabled** | Toggle | Fall damage |
| **Is Game Time Paused** | Toggle | Pause the day/night cycle |
| **Is Spawning NPC** | Toggle | NPC spawning |
| **Is All NPC Frozen** | Toggle | Freeze all NPC movement |
| **Is Spawn Markers Enabled** | Toggle | Show spawn point markers |
| **Is Compass Updating** | Toggle | Update compass direction |
| **Is Saving Players** | Toggle | Save player data |
| **Is Saving Chunks** | Toggle | Save chunk data |
| **Save New Chunks** | Toggle | Save newly generated chunks |
| **Is Unloading Chunks** | Toggle | Unload distant chunks |
| **Is Objective Markers Enabled** | Toggle | Show objective markers on screen |
| **Delete On Universe Start** | Toggle | Delete world when universe starts |
| **Delete On Remove** | Toggle | Delete world data when removed |

### Visual Effects
Hytale gives you fine-grained control over lighting and visual effects. These are great for building cinematic scenes or adjusting the mood of your world.

| Setting | Type | Description |
|---------|------|-------------|
| **Sun Height Percent** | Number | Sun position (0--100) |
| **Sun Angle Degrees** | Number | Sun rotation |
| **Bloom Intensity** | Number | Bloom lighting intensity |
| **Bloom Power** | Number | Bloom effect strength |
| **Sun Intensity** | Number | Sunlight brightness |
| **Sunshaft Intensity** | Number | God ray intensity |
| **Sunshaft Scale Factor** | Number | God ray scale |

## Auto-Save
You don't need to worry about hitting a save button. All settings auto-save 800 milliseconds after you make a change. Each setting card shows a small indicator so you know what's happening:

- **Saving** -- a spinner appears while the change is being saved.
- **Saved** -- a checkmark confirms the change went through.
- **Error** -- something went wrong with the save. Try refreshing the page and making the change again.
