---
title: Creating a Minecraft Lifesteal Server
tags: Software
permalink: minecraft/modifications/software/lifesteal
description: Learn how to create a lifesteal server where every kill matters.
keywords:
    - keyword: Lifesteal
      matches: ["Create", "setup"]
author:
    - TWIXhunter
toc: true

icon: "https://cdn.modrinth.com/data/KiGjlfaO/71b737e1a9d2ab95a856239e5c1a7f201d40baa7_96.webp"
mod-name: Lifesteal-Plugin
mod-type: Plugin
mod-url: "https://modrinth.com/plugin/twix-lifesteal"
---

## What is LifeSteal?

LifeSteal is an intense Minecraft PvP gamemode where every fight has permanent consequences. When you kill another player, you steal one of their hearts, increasing your maximum health while they lose theirs. Players who lose all their hearts are eliminated from the server (or temporarily banned, depending on configuration).

## Installation:

### Requirements:

Make sure your server is running Spigot or one of its forks (Paper, Purpur, etc).

### Installing the plugin:

Please refer to our [Adding Plugins](/minecraft/modifications/general/adding-plugins) guide.

### Configuring the plugin:

1. Open the [File Manager](https://client.falixnodes.net/server/filemanager).

2. Navigate to the `plugins` directory.

3. Navigate to the `LifeSteal` plugin directory.

4. Open the `config.yml` file. This is the main configuration file where you can customize all available features.

5. Take a look at the options you have there. Some important options you might want to change are:

| Setting                      	| Description                                                                                       |
|-------------------------------|---------------------------------------------------------------------------------------------------|
| enabled-worlds               	| List of worlds where lifesteal mechanics are active                                               |
| elimination-commands         	| Commands executed when a player is eliminated (use %player% placeholder)                          |
| revive.hearts                	| Number of hearts a player gets when revived by an operator                                        |
| revive.commands              	| Commands executed when a player is revived (use %player% placeholder)                             |
| hearts.amount                	| Hearts gained/lost per kill (1 heart = 2 health points)                                           |
| hearts.eliminate-at          	| Heart threshold at or below which a player is eliminated                                          |
| hearts.maximum               	| Maximum number of hearts a player can have                                                        |
| crafting.enabled             	| Enable or disable heart crafting                                                                  |
| crafting.recipe              	| Define the 3x3 crafting grid pattern for heart items                                              |

6. If you want to prevent players from being banned upon elimination, remove or comment out the ban command from `elimination-commands`. Similarly, you can remove the pardon command from `revive.commands` if you're not using bans. 

7. (Re)start the server to apply the config changes.

## Using the Plugin and commands:
### Crafting a heart item:

1. Open a crafting table.

2. Enter the items needed in the crafting recipe defined in the config file. the default crafting recipe can be found below:

![Diamond Gold_ingot Diamond. Redstone Totem Redstone. Diamond Emerald Redstone.](content/assets/images/posts/lifesteal/default-recipe.png)

3. Right-click (consume) the heart item to add it to your health.

### Changing the heart recipe:
1. Open the [File Manager](https://client.falixnodes.net/server/filemanager).

2. Navigate to the `plugins` directory.

3. Navigate to the `LifeSteal` plugin directory and open the `config.yml` file.

4. Scroll down to the `recipe:` option.

5. Edit the item names to change the recipe, make sure to use the official material names (which can be found [here](https://hub.spigotmc.org/javadocs/spigot/org/bukkit/Material.html)) and seperate them with a ",".

```yaml
  recipe:
    row1: "DIAMOND,GOLD_INGOT,DIAMOND"
    row2: "REDSTONE,NETHER_STAR,REDSTONE"
    row3: "DIAMOND,EMERALD,DIAMOND"
```

6. Save the file and (re)start the server to apply the changes.

### Gifting hearts between players:
1. Join the server on Minecraft

2. Open the chat and run `/giftheart <player>` (replace `<player>` with their username).

3. Press enter to execute the command.

### Changing the maximum amount of hearts a player can have.
1. Open the [File Manager](https://client.falixnodes.net/server/filemanager).

2. Navigate to the `plugins` directory.

3. Navigate to the `LifeSteal` plugin directory and open the `config.yml` file.

4. Scroll down to the `maximum:` option inside the "Heart settings" section of the config file.

5. Enter the amount of hearts you want players to have.

6. Save the file and (re)start the server to apply the changes.
