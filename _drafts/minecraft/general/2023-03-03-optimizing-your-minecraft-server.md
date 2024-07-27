---
layout: help/article
title:  "Optimizing Your Minecraft Server - Falix"
categories: Minecraft
icon: <i class="fa-light fa-sword"></i>
tags: mcgeneral
permalink: /help/minecraft/general/optimizing-your-minecraft-server.*
gitURL: _posts/minecraft/general/2023-03-03-optimizing-your-minecraft-server.md
description: "Tricks and tips to optimize your Minecraft Server at Falix"

author: Grace
authorGitHub: AgentDeath253
---

## Why Optimize Your Server

Optimizing your Minecraft server is a great way to help it run better and to get the best performance from your server. It's also a very good way to prevent your server from lagging and will allow your server to run better with more players. Optimizing your server can be hard, but we will try to make it as easy as possible. Spigot and Paper offer settings that greatly improve performance. This guide breaks down suggested values that get the most out of your server without compromising gameplay.

## Bukkit.yml

spawn-limits
Default: monsters:70, animals:10, water-animals:15, water-ambient:20, ambient:15
Optimized: monsters:50, animals:8, water-animals:7, water-ambient:10, ambient:1
Performance Impact: Heavy

 While there is more to this than "mobs per player" (explained here), lower values mean less mobs. Avoid going too low or the mob shortages will be noticeable. Subsequent values in the guide will make the reduction less noticeable.

chunk-gc.period-in-ticks
Def: 600
Opt: 400
Impact: Medium

 This unloads vacant chunks faster. Ticking fewer chunks means less TPS consumption.

ticks-per.(type)-spawns
Def: monster:1, water:1, water-ambient:1, ambient:1
Opt: monster:5, water:11, water-ambient:21, ambient:31
Impact: Medium

 This sets how often (in ticks) the server attempts to spawn entities. Increasing the time between spawn attempts should not impact gameplay. Offsetting the tick rates spreads them out more.

{: .note }
 Only go higher if you have significant tick loss to the mobSpawn task.

autosave
Def: 6000 (usually)
Opt: 6000
Impact: N/A

 This enables Bukkit's world saving and how often it runs (in ticks). It should be 6000 by default, just double check it is not 0 (disabled).

{: .note }
 If you use your server or a plugin to run saves, STOP! They just run the very obsolete /save-all command.

Worldsave Lag: Lag spikes from Worldsave? You might want to consider Paper's lag-free saving.

## Spigot.yml

save-user-cache-on-stop-only
Default: false
Optimized: true
Performance Impact: Medium

 Should the server constantly save user data (false) or delay that task until a stop/restart (true)? This is nice TPS savings on Spigot (less on Paper since it's more efficient).

Note: Take regular backups to avoid data loss in the rare event of a fatal crash.

max-tick-time
Def: tile:50, entity:50
Opt: tile:1000, entity:1000
Impact: N/A

 1000 disables this feature. The small TPS savings is not worth the potential damage. Damage? (click here)

mob-spawn-range
Def: 8
Opt: 6
Impact: N/A

 This sets the max mob spawning distance (in chunks) from players. After limiting spawns in Bukkit, this will condense mobs to mimic the appearance of normal rates.

Warning: If your view-distance is 6 or smaller, set a spawn range 1 below that value (ex. If view-distance is 5, set mob-spawn-range to 4)

entity-activation-range
Def: animals:32, monsters:32, raiders: 48, misc:16
Opt: animals:16, monsters:24, raiders: 48, misc:8
Impact: Medium

 Entities past this range will be ticked less often. Avoid setting this too low or you might break mob behavior (mob aggro, raids, etc).

Note: Villagers should be left alone (if possible) to protect mechanics.

tick-inactive-villagers
Def: true
Opt: false
Impact: Medium

 Enabling this prevents the server from ticking villagers outside the activation range.

{: .note }
 Vanilla behavior ticks all villagers in loaded chunks. Enable villagers-active-for-panic to save some iron farms from breaking.

merge-radius
Def: item:2.5, exp:3.0
Opt: item:4.0, exp:6.0
Impact: Medium

 Merging items means less ground item ticking. Higher values allow more items to be swept into piles.

 {: .note }
 Merging will lead to the illusion of items disappearing as they merge together. A minor annoyance.

nerf-spawner-mobs
Def: false
Opt: true
Impact: Medium

 When enabled, mobs from spawners will not have AI (will not swim/attack/move). This is big TPS savings for massive mob farms, but also messes with behavior. A farm limiter plugin might be a better solution.

{: .note }
 Paper has an option to force nerfed mobs to jump/swim. This fixes water push farms.

item-despawn-rate
Def: 6000 (5 minutes)
Opt: less?
Impact: Situational

 The time (in ticks) before a ground item is removed. While the TPS savings can be significant if reduced, it also impacts gameplay on servers where returning to dropped items is critical.

{: .note }
 See Paper's alt-item-despawn-rate so you can target trash items (cobblestone) without clearing valuable items.

arrow-despawn-rate
Def: 1200
Opt: 300
Impact: Minor

 Similar to item-despawn-rate, but for arrows. Some servers may want to keep arrows on the ground longer, but most will have no complaints if removed faster.

 {: .note }
 Paper has settings to reduce the gameplay impact of arrow removal. Leave this near default if you use Paper's arrow options.

## Paper.yml

max-auto-save-chunks-per-tick
Default: 24
Optimized: 6
Performance Impact: Heavy

 This slows down incremental chunk saving during the world save task. This is incredibly important for modern servers (world saving sucks).

 Setting this too low might result in unsaved chunks, so avoid going lower.

optimize-explosions
Default: false
Optimized: true
Impact: Minor

 Paper has a very efficient algorithm for explosions with no impact to gameplay.

mob-spawner-tick-rate
Def: 1
Opt: 2
Impact: Minor

 This is the delay (in ticks) before an active spawner attempts spawns. Doubling the delay will not impact spawn rates. Only go higher if you have significant tick loss from ticking spawners.

disable-chest-cat-detection
Def: false
Opt: true
Impact: Minor

 Chests scan for a cat on top of it when opened by a player. While enabling this eliminates vanilla behavior (cats block chests), do you really need this mechanic?

container-update-tick-rate
Def: 1
Opt: 3
Impact: Minor

 This changes how often (in ticks) inventories are refreshed while open. Do not exceed 4 to avoid visual issues.

max-entity-collisions (in Spigot.yml in some builds)
Def: 8
Opt: 2
Impact: Medium

 Crammed entities (grinders, farms, etc.) will collide less and consume less TPS in the process.

grass-spread-tick-rate
Def: 1
Opt: 4
Impact: Medium

 The time (in ticks) before the server tries to spread grass in chunks. This will have no gameplay impact on most game types.

despawn-ranges
Def: soft: 32, hard: 128
Opt: soft: 28, hard: 96
Impact: Minor

Soft = The distance (in blocks) from a player where mobs will be periodically removed.
Hard = Distance where mobs are removed instantly.

 Lower ranges clear background mobs and allow more to be spawned in areas with player traffic. This further reduces the gameplay impact of reduced spawning (bukkit.yml).

hopper.disable-move-event
Def: false
Opt: true
Impact: Heavy

 This will significantly reduce hopper lag by preventing InventoryMoveItemEvent being called for EVERY slot in a container.

Warning: Plugins that listen for InventoryMoveItemEvent will break.

non-player-arrow-despawn-rate
Def: -1 (uses Spigot arrow-despawn-rate)
Opt: 60 (3 seconds)
Impact: Minor

 Similar to Spigot's arrow-despawn-rate, but targets skeleton-fired arrows. Since players cannot retrieve mob arrows, this is only a cosmetic change.

creative-arrow-despawn-rate
Def: -1 (Spigot arrow-despawn-rate)
Opt: 60 (3 seconds)
Impact: Minor

 Like the setting above, but for player-fired arrows that cannot be retrieved (infinity bows).

prevent-moving-into-unloaded-chunks
Def: false
Opt: true
Impact: Medium

 Prevents players from entering an unloaded chunk (due to lag), which causes more lag. The true setting will set them back to a safe location instead.

Note: If you did not pre-generate your world (what's wrong with you?!) this setting is critical.

use-faster-eigencraft-redstone
Def: false
Opt: true
Impact: Heavy

 This setting reduces redundant redstone updates by as much as 95% without breaking vanilla devices. Empirical testing shows a speedup by as much as 10x!

{: .note } If you use a plugin to change redstone algorithms, consider replacing them with this option as plugins tend to break redstone behavior.

armor-stands-tick
Def: true
Opt: false
Impact: Minor

 Some items are viewed as entities (require ticking) since they interact with the world. Unticked armor stands will not get pushed by water (do you care?)

Note: Paper also offsets item frame ticking instead of ticking all frames at once. This is not configurable, just enjoy the TPS savings with no gameplay impact.

per-player-mob-spawns
Def: false
Opt: true
Impact: Minor

 This implements singleplayer spawning behavior instead of Bukkit's random algorithms. This prevents the actions of others (i.e. Massive farms) from impacting the server's spawn rates.

{: .note }
 If you lowered spawn-limits in Bukkit and notice shortages of animals and monsters, consider bumping those back up until you find a happy place.

alt-item-despawn-rate
Def: false
Opt: true
Impact: Medium

 Remove certain item drops faster (or slower) than the item-despawn-rate set in Spigot. This lets you avoid ticking massive piles of garbage.

Example of despawning cobblestone and netherrack in 15 seconds:
    ```
      enabled: true
      items:
        COBBLESTONE: 300
        NETHERRACK: 300 ```
{: .note }
 Use the Spigot material list when adding items.

no-tick-view-distance
Def: -1
Opt: # > view-distance setting
Impact: N/A

 This is the distance at which chunks are loaded, but will still not be ticked outside your view-distance.

Note: If you had to set your view-distance really low (like 3 or 4), you might set this at 5 or 6 to improve your gameplay experience.

anti-xray.enabled
Def: false
Opt: true
Impact: N/A

{: .note }
 Anti-Xray is not needed for small private servers; it is only needed in public servers.

 While this setting will actually cost TPS, Paper's anti-xray is the most efficient in existence! Engine 1 might be less heavy (mainly for clients), but mode 2 is by far more effective.

## Server.Properties

view-distance
Def: 10
Opt: 6-8
Impact: Heavy

 This is the most impactful setting in all your files as it caps the chunk render distance. Open world servers (like Survival) should strive to use 6+, but others on shared hosts, low specs, or huge player counts might consider 4-5 if chunk gen causes lag.

Warning: See note in mob-spawn-range (spigot.yml) if you set your view distance lower than 7.

network-compression-threshold
Default: 256
Optimized: Standalone(512) BungeeCord(-1)
Impact: Minor

This option caps the size of a packet before the server attempts to compress it. Setting it higher can save some resources at the cost of bandwidth, setting it to -1 disables it.
