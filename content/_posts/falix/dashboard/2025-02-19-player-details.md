---
layout: post
title: "Player Details & Commands"
tags: Server
permalink: falix/dashboard/general/player-details
description: "View player stats, manage inventory, modify abilities, run commands, and edit player data."
keywords:
    - keyword: player
      matches: ["details", "stats", "profile", "view", "info"]
    - keyword: inventory
      matches: ["player", "view", "edit", "clear", "give", "ender chest"]
    - keyword: abilities
      matches: ["fly", "god mode", "invulnerable", "speed", "player"]
    - keyword: gamemode
      matches: ["survival", "creative", "adventure", "spectator", "change"]
    - keyword: teleport
      matches: ["player", "tp", "coordinates", "dimension"]
    - keyword: effects
      matches: ["potion", "player", "apply", "clear"]
author: Lily
---

## Introduction
The player details page gives you full control over an individual player -- right from your dashboard, no commands needed. You can check their health, hunger, experience, inventory, abilities, advancements, and more. Need to heal someone, swap their gamemode, or teleport them across the map? It's all here in one place.

To open a player's details, click their card on the [Players](falix/dashboard/general/player-management) page.

{: .info}
> Most editing features require the player to be **online**. A few actions -- like deleting player data -- actually require the player to be **offline** first.

## Player Profile

At the top of the page, you'll see the player's profile card. This includes a **3D render of their skin**, their **username**, and an **Online/Offline status badge** so you know at a glance whether they're currently on the server. Below that is the player's **UUID** (their unique identifier -- click it to copy), along with timestamps for when they **first joined** and **last logged in**. If the player is currently online, you'll also see their **alive time**, which tracks how long it's been since their last spawn.

### Status Indicators

Active status badges appear when the player is:

- Flying
- On fire
- Drowning
- Falling from height
- Taking damage
- In a portal cooldown
- Sleeping

These update in real time, so you always know what's happening to the player at that moment.

## Health, Hunger & Experience

{% tabs stats %}

{% tab stats Health %}

Displays health as a row of 10 hearts (20 HP total).

| Action | Description | Requires |
|--------|-------------|----------|
| **Heal** | Restore full health | Online |
| **Kill** | Kill the player | Online |

{% endtab %}

{% tab stats Hunger %}

Displays hunger as a row of 10 drumsticks with a saturation bar.

| Action | Description | Requires |
|--------|-------------|----------|
| **Feed** | Restore full hunger and saturation | Online |
| **Starve** | Apply hunger effect | Online |

{% endtab %}

{% tab stats Experience %}

Displays the XP level badge and a progress bar showing percentage to the next level.

| Action | Description | Requires |
|--------|-------------|----------|
| **Give XP Level** | Add 1 XP level | Online |
| **Take XP Level** | Remove 1 XP level | Online |

{% endtab %}

{% endtabs %}

### Hytale Servers

Hytale servers show different stats:

| Stat | Range |
|------|-------|
| Health | 0--100 |
| Mana | 0--100 |
| Stamina | 0--10 |
| Oxygen | 0--100 |

## Inventory

The inventory section displays the player's full Minecraft inventory layout, just like you'd see in-game:

- **4 armor slots** -- head, chest, legs, feet
- **1 offhand slot**
- **27 main inventory slots** (3x9 grid)
- **9 hotbar slots**
- **Trash bin** -- drag items here to drop them (online only)

You can rearrange items by dragging and dropping them between slots, which is a handy way to organize a player's gear without asking them to do it themselves.

### Inventory Actions

| Action | Description | Requires |
|--------|-------------|----------|
| **View Ender Chest** | Opens a modal showing the player's 27-slot ender chest contents | Any |
| **Give Item** | Give an item to the player via a modal | Online |
| **Clear Inventory** | Remove all items from the player's inventory (confirmation required) | Online |

{: .warning}
> Clearing a player's inventory removes everything they're carrying. Double-check before confirming -- there's no undo.

## Abilities

This section lets you toggle individual abilities on or off for a player. It's a quick way to grant (or revoke) special permissions without digging through permission plugins.

- **Flying** -- Whether the player is currently in flight. Turning this off mid-air will cause them to fall, so use it carefully.
- **May Fly** -- Whether the player is *allowed* to fly. This is the permission toggle -- enabling it lets the player double-tap jump to start flying.
- **Invulnerable** -- Makes the player immune to all damage. Useful for events or when you need someone to stand in a dangerous area.
- **Instant Build** -- The player can break blocks instantly, like in creative mode.
- **May Build** -- Controls whether the player can place and break blocks at all. Turning this off effectively locks them out of building.
- **God Mode** -- A convenience toggle that flips multiple protective abilities at once, so you don't have to enable them one by one.

{: .info}
> God Mode is great for temporarily protecting a player during an event or while troubleshooting. Just remember to turn it off when you're done.

### Speed Controls

| Setting | Range | Default |
|---------|-------|---------|
| Walk Speed | 0--1 (step 0.01) | 0.10 |
| Fly Speed | 0--1 (step 0.01) | 0.05 |

A little goes a long way here. Even small changes to walk and fly speed can feel dramatic in-game, so start with minor adjustments and work your way up.

### Advanced Attributes

Click **More Abilities** to open a modal with the full set of player attributes. These give you fine-grained control over how the player interacts with the world:

| Attribute | Description |
|-----------|-------------|
| Walk Speed | Base movement speed |
| Max Health | Maximum health points |
| Attack Damage | Base melee damage |
| Attack Speed | Attack cooldown speed |
| Jump Strength | Jump height |
| Luck | Affects loot table rolls |
| Armor | Damage reduction from armor |
| Armor Toughness | Reduces effectiveness of strong attacks |
| Knockback Resist | Resistance to knockback |
| Follow Range | Mob detection range |
| Step Height | Maximum block height the player can step up |
| Scale | Player model scale |
| Safe Fall Distance | Distance before fall damage starts |
| Fall Damage Multi | Fall damage multiplier |
| Burning Time | Duration of fire damage |
| Explosion Knockback | Knockback resistance from explosions |
| Water Movement | Movement speed in water |
| Oxygen Bonus | Underwater breathing bonus |
| Movement Efficiency | Movement speed on certain blocks |
| Block Interact Range | Reach distance for block interaction |

{: .info}
> Most of the time you won't need to touch advanced attributes, but they're incredibly useful for custom game modes, events, or debugging weird player behavior.

## Advancements & Recipes

{% tabs progress %}

{% tab progress Advancements %}

Shows the player's advancement completion with a progress bar and percentage badge (e.g. "45/123 advancements"). Click to open a modal listing all advancements and their completion status.

{% endtab %}

{% tab progress Recipes %}

Shows unlocked recipe count with a progress bar. Displays the number of new recipes available. Click to open a modal listing all recipes.

{% endtab %}

{% endtabs %}

## Commands

One of the most powerful parts of the player details page is the ability to run commands directly on a player -- no need to type anything in the server console. Some commands require the player to be online.

{% tabs commands %}

{% tab commands Gamemode %}

Change the player's game mode.

| Mode | Description |
|------|-------------|
| Survival | Normal gameplay |
| Creative | Unlimited resources, flying, no damage |
| Adventure | Can interact but not break/place blocks |
| Spectator | Invisible, can fly through blocks |

Requires the player to be **online**.

{% endtab %}

{% tab commands Teleportation %}

| Command | Description | Requires |
|---------|-------------|----------|
| **Teleport to coordinates** | Enter X, Y, Z coordinates | Online |
| **Set spawn point** | Set the player's spawn to specific coordinates | Any |
| **Teleport to dimension** | Move to Overworld, Nether, or End | Online |

{% endtab %}

{% tab commands Effects %}

Apply or remove potion effects.

**Applying an effect:**
- Select the effect type
- Set duration (in seconds)
- Set amplifier level

**Quick effects:**

| Button | Effect |
|--------|--------|
| **Extinguish** | Fire resistance (removes fire) |
| **Restore Air** | Water breathing (stops drowning) |
| **Clear Fall** | Slow falling (prevents fall damage) |
| **End Portal Cooldown** | Resets portal cooldown timer |

You can also clear a specific active effect by clicking the remove button next to it.

All effect commands require the player to be **online**.

{% endtab %}

{% tab commands Messaging %}

Send visual messages to the player.

| Type | Description |
|------|-------------|
| **Title** | Large text in the center of the screen |
| **Action Bar** | Text above the hotbar |

Enter the message text and select the display type. Requires **online**.

{% endtab %}

{% tab commands Sounds %}

Play a sound effect for the player. Select from available Minecraft sounds. Requires **online**.

{% endtab %}

{% tab commands Fun Commands %}

Chaos commands for fun interactions with online players.

| Command | Effect |
|---------|--------|
| **Smite** | Lightning strike at the player's location |
| **Launch** | Levitation effect |
| **Spin** | Nausea effect |
| **Freeze** | Slowness + Mining Fatigue |
| **Blind** | Blindness effect |
| **Bounce** | Jump boost |
| **Burn** | Fire + fire blocks around the player |
| **Rocket** | Elytra + firework boost |
| **Drunk** | Nausea + Slowness |
| **Glow** | Glowing outline effect |
| **Invisible** | Invisibility effect |
| **Poison** | Poison effect |
| **Wither** | Wither effect |
| **Explode** | Summon TNT at the player |
| **Zombie** | Summon 3 zombies at the player |
| **Rain** | Summon 10 diamond items above the player |

All fun commands require the player to be **online**.

{% endtab %}

{% endtabs %}

{: .info}
> The fun commands are a great way to interact with your community during events or livestreams. Just be mindful that some of them (like Explode and Burn) can destroy blocks or kill the player, so use them wisely.

## Player Data Files

Sometimes you need to wipe a player's data and give them a fresh start -- maybe their playerdata file is corrupted, or they want to reset their progress. You can manage the player's stored data files from here. All of these actions require the player to be **offline**.

| Action | Description |
|--------|-------------|
| **Delete Playerdata** | Removes the player's DAT file (resets position, inventory, health, etc.) |
| **Delete Stats** | Removes the player's statistics file |
| **Delete Advancements** | Removes the player's advancement progress |

{: .warning}
> Deleting player data is permanent and cannot be undone. The player will start fresh for whichever data type you delete. Always consider creating a backup before wiping any player data.

## Hytale Commands

Hytale servers have a different command set tailored to the Hytale engine. These cover the essentials -- operator management, whitelist control, bans, and movement.

| Command | Description |
|---------|-------------|
| **Op** | Grant operator status |
| **Deop** | Remove operator status |
| **Whitelist add** | Add to whitelist |
| **Whitelist remove** | Remove from whitelist |
| **Ban** | Ban with optional reason |
| **Unban** | Remove ban |
| **Kick** | Kick from server |
| **Gamemode** | Set to Creative or Adventure |
| **Teleport** | Teleport to coordinates, top of world, home, or a specific world |
