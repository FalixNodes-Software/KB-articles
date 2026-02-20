---
layout: post
title: "World Settings"
tags: Content
permalink: falix/dashboard/content/world-settings
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

To get started, head to the [Worlds](/falix/dashboard/content/worlds) page and click **Settings** on any world card.

## Search and Filter
If you already know the setting you're looking for, use the search bar at the top to find it by name or description. You can also filter by category using the dropdown, which is handy when you just want to browse what's available.

## Setting Categories

### Essential
These are the settings you'll probably change first on any new world. **Difficulty** lets you pick between Peaceful, Easy, Normal, or Hard. **Game Type** sets the default mode for players joining the world: Survival, Creative, Adventure, or Spectator. **DataPacks** opens a modal where you can enable or disable any installed datapacks. You'll also find quick access to the most popular game rules here — `keepInventory`, `pvp`, `doMobSpawning`, `mobGriefing`, `doDaylightCycle`, and `doWeatherCycle` — so you don't have to hunt through the full list for the things you change most often.

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

- **Data Version** and **Version** show the NBT data format version and Minecraft version details (including name, ID, series, and snapshot status).
- **Server Brands** is an editable list of server software names (Vanilla, Spigot, Paper, Purpur, and so on).
- **Last Played** shows when the world was last loaded, and **Size on Disk** shows the world size in a human-readable format.
- **Was Modded** tells you whether the world has been used with mods or modified server software.
- **Bukkit.Version** and **Forge Data Version** show CraftBukkit/Spigot/Paper version strings and Forge NBT data version numbers respectively, if applicable.
- **World Gen Settings** opens a modal for viewing and editing the seed, bonus chest toggle, structures toggle, and dimension list.
- **Dragon Fight** opens a modal showing dragon kill status (currently dead or alive), total times killed, needs-state-scanning flag, and which of the 20 end gateways have been activated.
- **Scheduled Events** and **Custom Boss Events** are read-only lists of scheduled game events and custom boss bars, respectively.

{: .info}
> You generally won't need to touch anything here unless you're troubleshooting or migrating a world between server software.

## Game Rules
Game rules appear inline alongside the other world settings, organized into the same searchable categories. On some server setups, you may see a **Game Rules** button that opens a dedicated modal editor instead. Either way, rules are searchable and organized by category so you can quickly find whatever you need to change.

### Mobs and Entities
These rules determine how mobs behave in your world — what drops when they die, which special mob types spawn, and whether phantoms bother players who skip sleep. Note that the most popular mob rules (`doMobSpawning` and `mobGriefing`) appear in the Essential category for quick access.

| Rule | Type | Description |
|------|------|-------------|
| **doMobLoot** | Toggle | Mobs drop items, experience orbs, and equipment on death |
| **doPatrolSpawning** | Toggle | Enables pillager patrol spawning |
| **doTraderSpawning** | Toggle | Enables wandering trader spawning |
| **doWardenSpawning** | Toggle | Allows wardens to spawn in deep dark biomes |
| **doInsomnia** | Toggle | Allows phantoms to spawn when players don't sleep |
| **spawnMonsters** | Toggle | Hostile monsters can spawn in monster spawners |

{: .warning}
> Disabling `mobGriefing` (found in the Essential category) prevents Creeper explosions from destroying blocks, but it also stops Endermen from picking up blocks and villagers from farming. Keep that side effect in mind.

### Player and Death
These rules control what happens to players — especially around death. Note that `keepInventory` and `pvp` appear in the Essential category for quick access since they're among the most commonly changed settings on any server.

| Rule | Type | Description |
|------|------|-------------|
| **naturalRegeneration** | Toggle | Players regenerate health naturally when hunger is full |
| **doImmediateRespawn** | Toggle | Players respawn immediately without death screen |
| **playersSleepingPercentage** | Number | Percentage of players who must sleep to skip night (0--100) |
| **spawnRadius** | Number | Radius from spawn where players can randomly spawn (0 = exact spawn) |
| **showDeathMessages** | Toggle | Shows death messages in chat |
| **drowningDamage** | Toggle | Players take damage from drowning |
| **fallDamage** | Toggle | Entities take damage from falling |
| **fireDamage** | Toggle | Entities take damage from fire and lava |
| **freezeDamage** | Toggle | Entities take damage from freezing in powder snow |

{: .info}
> `keepInventory` is by far the most popular game rule change on survival servers. If you're running a casual or family-friendly server, turning it on saves a lot of frustration. Setting `playersSleepingPercentage` to 0 means a single player can skip the night without everyone needing to be in a bed.

### Time and Weather
These rules let you freeze or adjust the passage of time, weather cycles, and the speed at which things grow. Note that `doDaylightCycle` and `doWeatherCycle` appear in the Essential category for quick access. If you want a permanent daytime build world, just disable `doDaylightCycle` and set the time to noon. This category also includes block-level environmental behaviors like fire spread, vine growth, snow accumulation, and source block creation.

| Rule | Type | Description |
|------|------|-------------|
| **randomTickSpeed** | Number | Number of random block ticks per chunk section (default: 3, higher = faster growth) |
| **doFireTick** | Toggle | Controls fire spread and extinguishment over time |
| **doVinesSpread** | Toggle | Vines can spread to adjacent blocks |
| **snowAccumulationHeight** | Number | Maximum height snow layers can accumulate (1--8) |
| **lavaSourceConversion** | Toggle | Lava can form new source blocks (infinite lava) |
| **waterSourceConversion** | Toggle | Water can form new source blocks (infinite water) |

{: .info}
> If your server is experiencing lag, try reducing `randomTickSpeed` below the default of 3. Higher values make crops, leaves, and other random-tick blocks update faster, but they also put more load on the server. Conversely, setting it to 0 stops crop growth entirely.

### Blocks and Items
This category controls what drops when blocks are broken or things explode. It's also where you'll find settings for TNT behavior and explosion mechanics.

| Rule | Type | Description |
|------|------|-------------|
| **doTileDrops** | Toggle | Blocks drop items when mined or destroyed |
| **doEntityDrops** | Toggle | Non-mob entities drop items (minecarts, boats, item frames, etc.) |
| **tntExplodes** | Toggle | TNT can explode and destroy blocks |
| **tntExplosionDropDecay** | Toggle | TNT explosions have random chance to destroy item drops |
| **mobExplosionDropDecay** | Toggle | Mob explosions have random chance to destroy item drops |
| **blockExplosionDropDecay** | Toggle | Explosions have random chance to destroy block drops |
| **projectilesCanBreakBlocks** | Toggle | Projectiles (wind charges, etc.) can destroy blocks |

### Commands and Cheats
If you use command blocks on your server or want to control what feedback players see from commands, these are the settings to look at. Most of these can be left at their defaults unless you're building custom maps or minigames with command block logic.

| Rule | Type | Description |
|------|------|-------------|
| **commandBlockOutput** | Toggle | Broadcasts command block command output to server admins |
| **sendCommandFeedback** | Toggle | Shows command results in chat to command executor |
| **logAdminCommands** | Toggle | Logs admin commands to server console |
| **maxCommandChainLength** | Number | Maximum number of commands in a command chain (default: 65,536) |
| **maxCommandForkCount** | Number | Maximum number of forks in command execution (default: 65,536) |
| **commandModificationBlockLimit** | Number | Maximum number of blocks commands can modify (default: 32,768) |
| **commandBlocksEnabled** | Toggle | Allows command blocks to execute commands |

### Advanced Gameplay
These rules cover a mix of features that don't fit neatly into the other categories — things like requiring recipe unlocks, disabling raids, controlling advancement announcements, Nether portal behavior, mob anger mechanics, and movement validation.

| Rule | Type | Description |
|------|------|-------------|
| **doLimitedCrafting** | Toggle | Requires recipes to be unlocked before crafting |
| **disableRaids** | Toggle | Prevents pillager raids from starting |
| **announceAdvancements** | Toggle | Broadcasts advancement completion to all players |
| **reducedDebugInfo** | Toggle | Limits F3 debug screen information |
| **spectatorsGenerateChunks** | Toggle | Spectators can load/generate new chunks |
| **universalAnger** | Toggle | Angered neutral mobs attack any nearby player |
| **forgiveDeadPlayers** | Toggle | Angered mobs calm down when the player dies |
| **maxEntityCramming** | Number | Maximum entities that can push into a single block (0 = disabled) |
| **enderPearlsVanishOnDeath** | Toggle | Ender pearls disappear when thrower dies mid-flight |
| **globalSoundEvents** | Toggle | Sound events are broadcast globally |
| **playersNetherPortalDefaultDelay** | Number | Ticks before player teleports through Nether portal (default: 80) |
| **playersNetherPortalCreativeDelay** | Number | Ticks before creative player teleports through Nether portal (default: 0) |
| **allowEnteringNetherUsingPortals** | Toggle | Players can use Nether portals to travel |
| **disableElytraMovementCheck** | Toggle | Disables server-side movement check for elytra flight |
| **disablePlayerMovementCheck** | Toggle | Disables server-side movement validation (allows flying) |
| **allowFireTicksAwayFromPlayer** | Toggle | Fire ticks even when far from players |
| **locatorBar** | Toggle | Shows recovery compass locator bar in UI |
| **spawnerBlocksEnabled** | Toggle | Monster spawners can spawn mobs |

### Performance and Safety Indicators
Some game rules display badges next to them to help you make informed decisions:

- **Warning** badges appear on settings like `disablePlayerMovementCheck`, `disableElytraMovementCheck`, `commandBlocksEnabled`, `allowCommands`, `doFireTick`, and `mobGriefing` to flag that changing them carries some risk or has side effects.
- **Performance** badges show up on settings like `randomTickSpeed`, `maxEntityCramming`, `doMobSpawning`, `doWeatherCycle`, `spawnMonsters`, and `maxCommandChainLength` with a note about their impact (for example, "Higher values = faster growth but more lag").

{: .info}
> These indicators are there to help — if you see one, it's worth reading the note before making changes.

## Datapack Manager
The datapack modal gives you a simple dual-list interface. Enabled packs appear on the left and disabled packs on the right. You can move packs between lists by double-clicking them, clicking and holding to drag them, or selecting them and using the Enable/Disable buttons.

{: .warning}
> The `vanilla` datapack cannot be disabled — it's always required.

## Advanced World Settings
These are lower-level settings that most server owners won't need to touch often, but they're useful for fine-tuning world generation and border behavior. They show up in the Advanced Gameplay category in the dashboard.

| Setting | Type | Description |
|---------|------|-------------|
| **Wandering Trader Spawn Chance** | Number | Chance percentage for wandering trader to spawn (0--100, default: 25) |
| **Wandering Trader Spawn Delay** | Number | Game ticks remaining until next wandering trader spawn attempt |
| **Map Features** | Toggle | Whether to generate structures like villages, dungeons, and temples |
| **Generator Name** | Text | World generation type (default, flat, large_biomes, amplified, single_biome_surface, etc.) |
| **Generator Version** | Number | Version number of the world generator algorithm used |
| **Generator Options** | Text | JSON string with custom world generation settings (for superflat, buffet, etc.) |
| **Random Seed** | Number | Numeric seed used to generate the world's terrain and structures |
| **Border Warning Blocks** | Number | Distance in blocks from border where players see red vignette warning |
| **Border Warning Time** | Number | Seconds of warning time before border shrinks to player position |
| **Border Safe Zone** | Number | Buffer zone in blocks inside border that's considered safe |
| **Border Size Lerp Target** | Number | Target diameter in blocks for smooth world border size transition |
| **Border Size Lerp Time** | Number | Milliseconds remaining for world border to reach target size |

## Bedrock Edition Settings
When you're editing a Bedrock world, some additional categories will show up automatically.

### Bedrock Edition
This section includes settings that are specific to how Bedrock Edition handles worlds and won't appear for Java worlds. Here's a sample of what you'll find:

| Setting | Description |
|---------|-------------|
| **Spawn Location** | Player spawn position, rotation, and dimension |
| **Biome Override** | Override the default biome for the world |
| **World Generator** | World generation type |
| **LAN Broadcast** | Enable LAN world broadcasting |
| **Commands Enabled** | Whether commands are allowed |
| **Bonus Chest** | Enable bonus chest on world creation |
| **Multiplayer Game** | Enable multiplayer mode |
| **Texture Packs Required** | Force texture pack usage |
| **Start with Map** | Give players a map on spawn |
| **Immutable World** | Prevent world modifications |
| **Force Game Type** | Force all players into the default game mode on join |
| **Education Features** | Enable Education Edition features |
| **Chunk Tick Range** | Radius of chunks to tick around players |

### Experimental Features
Bedrock Edition has a set of experimental toggles for features that are still in development. Enable these if you want to test cutting-edge functionality, but keep in mind they may change or break between updates. The exact list of toggles depends on which experiments your world has encountered, but here are the ones the dashboard recognizes:

| Feature | Description |
|---------|-------------|
| **Beta APIs** | Enable Beta scripting APIs for add-on development |
| **Upcoming Creator Features** | Preview upcoming creator and modding features |
| **Villager Trade Rebalance** | Enable rebalanced villager trading mechanics |
| **Data-Driven Biomes** | Enable custom biome definitions via behavior packs |
| **Data-Driven Items** | Enable custom item definitions via behavior packs |
| **Experimental Molang** | Enable experimental Molang animation features |
| **Experimental Cameras** | Enable experimental camera features |
| **Creator Cameras** | Enable creator camera features for add-ons |
| **Jigsaw Structures** | Enable jigsaw structure generation features |
| **Deferred Rendering** | Enable Render Dragon deferred rendering (Preview only) |
| **2025 Drop 3** | Enable features from 2025 Drop 3 update |
| **Experiments Ever Used** | Tracks if experiments have ever been enabled on this world |
| **Saved With Experiments** | Tracks if the world was saved with experiments toggled |

{: .warning}
> Experimental features can cause world corruption in rare cases. Back up your world before enabling any of these.

## Hytale Settings
When editing a Hytale world, two specific categories appear in place of the standard Minecraft settings.

### World Settings

| Setting | Type | Description |
|---------|------|-------------|
| **World Ticking** | Toggle | Enable world tick updates |
| **Block Ticking** | Toggle | Enable block tick updates (crops, etc.) |
| **PvP Enabled** | Toggle | Allow players to damage each other |
| **Fall Damage** | Toggle | Players take damage from falling |
| **Pause Game Time** | Toggle | Stop the day/night cycle |
| **NPC Spawning** | Toggle | Allow NPCs to spawn naturally |
| **Freeze All NPCs** | Toggle | Prevent all NPC movement and AI |
| **Spawn Markers** | Toggle | Show spawn point markers |
| **Compass Updates** | Toggle | Update compass direction |
| **Save Players** | Toggle | Save player data to disk |
| **Save Chunks** | Toggle | Save chunk data to disk |
| **Save New Chunks** | Toggle | Save newly generated chunks |
| **Unload Chunks** | Toggle | Unload distant chunks from memory |
| **Objective Markers** | Toggle | Show objective markers on screen |
| **Delete On Start** | Toggle | Delete this world when universe starts |
| **Delete On Remove** | Toggle | Delete world data when removed |

### Visual Effects
Hytale gives you fine-grained control over lighting and visual effects. These are great for building cinematic scenes or adjusting the mood of your world.

| Setting | Type | Description |
|---------|------|-------------|
| **Sun Height** | Number | Height of the sun in the sky (0--100) |
| **Sun Angle** | Number | Rotation angle of the sun |
| **Bloom Intensity** | Number | Intensity of bloom lighting effect |
| **Bloom Power** | Number | Power/strength of bloom effect |
| **Sun Intensity** | Number | Brightness of sunlight |
| **Sunshaft Intensity** | Number | Intensity of god ray effects |
| **Sunshaft Scale** | Number | Scale factor for god rays |

## Auto-Save
You don't need to worry about hitting a save button. All settings auto-save 800 milliseconds after you make a change. Each setting card shows a small indicator so you know what's happening:

- **Saving** -- a spinner appears while the change is being saved.
- **Saved** -- a checkmark confirms the change went through.
- **Error** -- something went wrong with the save. Try refreshing the page and making the change again.
