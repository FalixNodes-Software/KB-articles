---
layout: post
title: "Player Details & Commands"
tags: Players
permalink: falix/dashboard/players/player-details
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

To open a player's details, click their card on the [Players](falix/dashboard/players/player-management) page.

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
| **View Ender Chest** | Opens a modal showing the player's 27-slot ender chest contents. You can also clear the ender chest from within this modal. | Any |
| **Give Item** | Give an item to the player -- browse items by category, set quantity (1-64), and choose a target slot | Online |
| **Clear Inventory** | Remove all items from the player's inventory (confirmation required) | Online |

Clicking on a **shulker box** or **bundle** in the inventory will open a modal showing its contents, so you can inspect what's inside without asking the player.

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
| Gravity | Gravitational pull strength |
| Safe Fall Distance | Distance before fall damage starts |
| Fall Damage Multi | Fall damage multiplier |
| Burning Time | Duration of fire damage |
| Explosion Knockback | Knockback resistance from explosions |
| Water Movement | Movement speed in water |
| Oxygen Bonus | Underwater breathing bonus |
| Movement Efficiency | Movement speed on certain blocks |
| Block Interact Range | Reach distance for block interaction |
| Entity Interact Range | Reach distance for entity interaction |
| Attack Knockback | Knockback dealt by melee attacks |
| Block Break Speed | Speed of breaking blocks |
| Underwater Mining | Mining speed while submerged |
| Sneaking Speed | Movement speed while sneaking |
| Flying Speed | Speed while flying |
| Max Absorption | Maximum absorption (golden hearts) |
| Sweeping Damage | Ratio of sweeping attack damage |

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

## Permissions & Moderation

At the top of the actions panel, you'll find quick access buttons for managing the player's permissions and handling moderation:

- **Operator** -- Toggle operator (op) status on or off for the player.
- **Whitelist** -- Add or remove the player from the whitelist.
- **Kick** -- Kick the player from the server (only visible when the player is online).
- **Ban / Unban** -- Ban the player from the server or lift an existing ban.

These are the same actions available on the [Player Management](falix/dashboard/players/player-management) page, but having them here saves you from switching pages when you're already looking at a specific player.

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
| **Teleport to coordinates** | Enter X, Y, Z coordinates to move the player there | Online |
| **Set spawn point** | Set the player's respawn point to their current position | Online |
| **World teleport** | Move the player to the Overworld, Nether, or End, optionally with custom coordinates | Online |

{% endtab %}

{% tab commands Effects %}

Apply or remove potion effects.

**Applying an effect:**
- Select the effect type
- Set duration (in seconds)
- Set amplifier level

Requires the player to be **online**.

{% endtab %}

{% tab commands Messaging %}

Send visual messages to the player. The messaging modal includes:

- **Quick templates** -- Pre-written messages for common situations (Welcome, Warning, Rules, Help) that you can insert with one click.
- **Message text** -- Type your custom message (up to 256 characters).
- **Color codes** -- Pick from all 16 Minecraft color codes to style your text.
- **Formatting** -- Apply bold, italic, underline, strikethrough, or reset formatting.
- **Display type** -- Choose between **Action Bar** (text above the hotbar) or **Title** (large text in the center of the screen).

Requires the player to be **online**.

{% endtab %}

{% tab commands Sounds %}

Play a sound effect for the player. Sounds are organized into four categories:

| Category | Sounds |
|----------|--------|
| **Scary** | Wither, Dragon, Ghast, Guardian |
| **Ambient** | Cave, Thunder, Bell, Pling |
| **Alerts** | Level Up, Challenge, Anvil, XP |
| **Funny** | Villager No, Cat Hiss, Pig, Goat |

Just click any sound button to play it for the player. Requires **online**.

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
| **Burn** | Fire resistance + fills blocks around the player with fire |
| **Rocket** | Gives the player an elytra and 64 firework rockets |
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

## Emergency Actions

When a player is in trouble, emergency action buttons automatically appear to help you respond quickly. These show up contextually based on the player's current status:

| Button | Appears When | Effect |
|--------|-------------|--------|
| **Extinguish Fire** | Player is on fire | Grants fire resistance to put them out |
| **Restore Air** | Player is drowning | Grants water breathing to stop drowning |
| **Clear Fall Damage** | Player is falling | Grants slow falling to prevent fall damage |
| **End Portal Cooldown** | Player is in portal cooldown | Grants resistance to reset portal cooldown |
| **Revive at Death Location** | Player has a recorded death location | Teleports the player back to where they last died |

All emergency actions require the player to be **online**.

## Location

The location card shows where the player is in the world. You'll see:

- **Current coordinates** -- The player's X, Y, Z position along with their current dimension (Overworld, Nether, or End). Click the teleport button to move the player there.
- **Respawn point** -- Where the player will respawn after dying, if one is set. Also has a teleport button.
- **Last death location** -- Where the player most recently died. You can teleport them back to recover their items.

Each location section has a quick-teleport button that sends the player to those coordinates with a single click.

## Statistics

The statistics card gives you a snapshot of the player's in-game activity. At the top you'll see summary stats for **play time** and **distance walked**. Below that, expandable sections break down:

- **Blocks mined** -- Which blocks they've mined and how many of each.
- **Items used** -- Which items they've interacted with.
- **Entities killed** -- Which mobs they've taken down.

Click **View All** to open a full statistics modal with searchable, categorized breakdowns including items crafted, deaths, tools broken, items picked up, items dropped, and custom stats.

{: .info}
> Statistics are only available for Minecraft Java servers. The data comes from the server's built-in statistics tracking.

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
