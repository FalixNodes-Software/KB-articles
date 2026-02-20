---
layout: post
title: "Server Properties"
tags: Server
permalink: falix/dashboard/general/server-properties
description: "Edit your server's configuration files including server.properties, bukkit.yml, spigot.yml, paper.yml, and more."
keywords:
    - keyword: properties
      matches: ["server", "config", "settings", "edit"]
    - keyword: motd
      matches: ["message", "server", "description", "edit"]
    - keyword: gamemode
      matches: ["survival", "creative", "adventure", "spectator"]
    - keyword: difficulty
      matches: ["peaceful", "easy", "normal", "hard"]
    - keyword: whitelist
      matches: ["enable", "server", "access", "list"]
    - keyword: online mode
      matches: ["cracked", "premium", "authentication"]
    - keyword: resource pack
      matches: ["texture", "pack", "url", "upload"]
author: Lily
---

## Introduction
Every Minecraft server has a handful of configuration files that control how it behaves -- things like the game mode, difficulty, max players, and whether PvP is on or off. Instead of opening those files by hand and editing raw text, the Server Properties page gives you a visual editor with toggles, dropdowns, and text fields so you can tweak settings quickly and safely.

{: .info}
> Your server needs to be running (or to have been started at least once) before its configuration files exist. If you don't see any properties yet, start your server and come back.

## Configuration File Tabs

Depending on which server software you're running, you may have more than just `server.properties` to configure. The page automatically detects which config files exist and shows each one as its own tab.

| Config File | Server Software |
|-------------|----------------|
| **server.properties** | All Minecraft Java servers |
| **bukkit.yml** | Bukkit, Spigot, Paper |
| **spigot.yml** | Spigot, Paper |
| **paper-global.yml** | Paper 1.19+ |
| **paper-world-defaults.yml** | Paper 1.19+ |
| **purpur.yml** | Purpur |
| **serverconfig.txt** | Terraria |
| **config.json** | Hytale |

Most servers will only ever need to touch **server.properties** -- it covers all the core gameplay and network settings. If you're running Paper, it's worth checking the **paper-global.yml** tab for performance tweaks like async chunk loading and entity tick rates. Spigot users will find similar optimizations in **spigot.yml**.

Each tab loads its settings on demand when you click it, so the page stays fast even if you have several config files.

## Property Categories

The `server.properties` tab organizes its settings into logical groups so you don't have to scroll through a wall of options:

- **Essential** -- The big ones: game mode, difficulty, and other core gameplay settings. Start here.
- **Gameplay** -- Fine-tune game mechanics like PvP, flight, and structure generation.
- **World** -- World generation type, level name, and seed settings.
- **Spawning** -- Control whether monsters, animals, and NPCs spawn, and how many.
- **Performance** -- Entity broadcast range, network compression, tick settings. Helpful if your server feels sluggish.
- **Security** -- Whitelist, online mode, and secure profiles. Important for controlling who can join.
- **Networking** -- Server status, transfer settings, and native transport options.
- **Remote** -- RCON, query, and JMX monitoring for advanced server management.
- **Admin** -- Command block permissions and broadcast settings.
- **Players** -- Max players, view distance, simulation distance, and idle timeout.
- **Resources** -- Resource pack URL, SHA1 hash, and the prompt message players see.
- **Storage** -- Data storage options.
- **Moderation** -- Chat reporting and text filtering settings.
- **Advanced** -- Debug options, code of conduct, and bug report settings. You probably won't need these often.

## Search and Filter

If you know what you're looking for, the search bar is the fastest way to find it -- just start typing a property name or keyword and results filter in real-time. You can also narrow things down by selecting a category from the dropdown.

**Keyboard shortcut**: Press **Ctrl+F** (or **Cmd+F** on Mac) to jump straight to the search bar.

## Editing Properties

### Input Types

Each property uses the input type that makes the most sense for it:

| Type | Used For | Examples |
|------|----------|---------|
| **Toggle** | Boolean on/off settings | PvP, whitelist, hardcore |
| **Dropdown** | Predefined options | Gamemode, difficulty, op level |
| **Text** | Free-form text values | MOTD, level seed, server name |
| **Number** | Numeric values | Max players, view distance, spawn protection |

### Auto-Save

You don't need to hit a save button -- changes are saved automatically 800 milliseconds after you stop editing. You'll see a small indicator letting you know the status:

- **Saving** -- a spinner appears while your change is being written
- **Saved** -- a checkmark confirms success (it fades after 3 seconds)
- **Error** -- something went wrong and the save didn't go through

## Special Editors

A few properties have richer editors built in because plain text fields aren't enough.

### MOTD Editor

Your MOTD (Message of the Day) is what players see in the Minecraft server list, so it's worth making it look good. The dedicated MOTD editor gives you:

- **Live preview** -- see exactly how your MOTD will appear in the server list as you type
- **Color buttons** -- all 16 Minecraft color codes (section-sign 0 through f) at the click of a button
- **Formatting buttons** -- bold, italic, underline, strikethrough, obfuscated, and reset
- **Quick templates** -- pre-made MOTDs for common themes (Welcome, Colorful, Gradient, Survival, Creative, Minigames, Skyblock, Factions, Prison, Christmas, Halloween, and more)
- **Multi-line support** -- Minecraft MOTDs can have up to 2 lines, and the editor supports both

### Resource Pack Prompt Editor

When you require a resource pack, Minecraft shows players a prompt asking them to accept or decline. This editor works just like the MOTD editor with color and formatting buttons, plus its own set of quick templates. The preview shows the prompt with Yes/No buttons exactly as a player would see it.

### Resource Pack Upload

Instead of hosting your resource pack somewhere else and copying URLs around, you can upload a `.zip` file (up to 100 MB) directly through this page. The system handles everything for you:

- Uploads the file to the CDN
- Generates the download URL
- Calculates the SHA1 hash
- Fills in both the `resource-pack` and `resource-pack-sha1` fields automatically

### Server Icon Upload

You can upload an image (up to 5 MB) to use as your server icon. It will be automatically resized to the required 64x64 pixels, and you'll see a preview before confirming the upload.

## Presets

Don't want to tweak every setting by hand? Presets let you apply a batch of settings at once for common play styles. When you apply a preset, you'll see a confirmation dialog listing exactly which properties will change, and the affected settings get briefly highlighted so you can spot them.

{% tabs presets %}

{% tab presets Gameplay %}

| Preset | Description |
|--------|-------------|
| **Vanilla** | Standard Minecraft settings |
| **Creative** | Creative mode, peaceful, no PvP |
| **Hardcore** | Hard difficulty, hardcore mode |
| **PvP** | No spawn protection |
| **Peaceful** | No monsters, no PvP |
| **Skyblock** | No structures, limited world size |
| **Adventure** | Adventure mode, no flight |
| **Minigames** | Command blocks enabled, adventure mode |
| **Roleplay** | Adventure mode, NPCs enabled |
| **Factions** | Hard difficulty, PvP |
| **UltraHardcore** | Extreme hardcore settings |

{% endtab %}

{% tab presets Performance %}

| Preset | Description |
|--------|-------------|
| **Low End** | Reduced view/simulation distance, 50% entity broadcast |
| **Balanced** | Default balanced settings |
| **High End** | 16 view distance, 12 simulation distance |

{% endtab %}

{% tab presets World %}

| Preset | Description |
|--------|-------------|
| **Super Flat** | Flat world generation |
| **Amplified** | Extreme terrain |
| **Large Biomes** | Larger biome sizes |

{% endtab %}

{% tab presets Server Size %}

| Preset | Description |
|--------|-------------|
| **Small Server** | 10 players, whitelist enabled |
| **Large Server** | 100 players, idle timeout, rate limiting |

{% endtab %}

{% endtabs %}

{: .info}
> Presets are a great starting point, but you can always adjust individual settings afterward. They won't lock you into anything.

## Notable Properties

### Online Mode (Cracked Mode)

This is one of the most important settings to understand. By default, **online mode is enabled**, which means your server checks every player's account against Mojang/Microsoft's authentication servers. Only players who own a legitimate copy of Minecraft can join.

Disabling online mode (sometimes called "cracked mode") lets players without a paid account connect. While this might seem appealing if you have friends who haven't bought the game, it comes with serious risks:

- **Inventory and data wipes** -- player data is tied to UUIDs, and cracked accounts get different UUIDs, which can cause data loss when switching between modes
- **Account impersonation** -- anyone can join using any username, including yours, and gain access to that player's inventory and permissions
- **Griefing** -- with no account verification, it's much harder to ban bad actors since they can rejoin with a different name

A warning dialog will appear when you toggle this setting to make sure you understand the trade-offs.

{: .warning}
> The toggle is labeled "Cracked Mode" for clarity, but it works in reverse: enabling Cracked Mode sets `online-mode` to `false` in the actual config file.

### Hardcore Mode

Enabling hardcore mode sets the difficulty to hard and gives players only one life -- when you die, you're put into spectator mode. A warning banner appears when you flip this toggle because once a world is created in hardcore mode, you can't revert it to normal through properties alone. You'd need to edit the `level.dat` file or reset the world.

### RCON

RCON (Remote Console) lets you send commands to your server from external tools. It's powerful but opens a network port that attackers could target, so a security warning appears when you enable it. Make sure you set a strong RCON password if you turn this on.

### Player Idle Timeout

This setting kicks players who have been idle for a set number of minutes, freeing up server slots for active players.

{: .info}
> Player idle timeout is a **premium feature**.

## YAML Configuration Editors

If you're running Bukkit, Spigot, Paper, or Purpur, you'll see additional tabs for their respective YAML config files. These editors work just like the main `server.properties` editor:

- Settings are organized by their top-level key categories
- You get the same input types (toggles, dropdowns, text and number fields)
- Changes auto-save with a 2-second delay
- Each tab has its own independent search and category filter

{: .info}
> The YAML editors use a slightly longer auto-save delay (2 seconds vs. 800 milliseconds) because YAML files tend to be larger and more complex.

## Mobile Features

On mobile devices, a bottom navigation bar keeps everything accessible:

- **Search** -- opens a search sheet
- **Filter** -- opens a category selector
- **Config** -- lets you switch between configuration file tabs
