---
title: Adding Custom Worlds and Portals With Multiverse
tags: Software
permalink: /minecraft/modifications/software/multiverse
description: Using Multiverse-Core and Multiverse-Portals to add portals to custom worlds
author:
    - Twixhunter
    - Deka
    - Mocab
icon: "https://cdn.modrinth.com/data/3wmN97b8/56e0c8729ad9eee9aa0c74b64560ab5858a7afec_96.webp"
mod-name: "Multiverse-Core"
mod-software: Bukkit, Paper, Spigot
mod-url: "https://modrinth.com/plugin/multiverse-core"
---

## What Is Multiverse?

Multiverse is a world management plugin that provides multi-world support, with the ability to set custom seeds, generation, game mode and much more on a per-world basis. You can use both commands and custom portals to teleport between your worlds, with the ability to restrict each world to a set permission.

## Installation:

### Prerequisites:

-   Ensure your server is running with Spigot or any of its forks (Paper, Purpur, etc).

### Installation:

We already have a guide on how to install Multiverse-core as well as any other plugin in our [Adding Plugins](/minecraft/modifications/general/adding-plugins) guide.

## Adding Worlds:

{% tabs addWrld %}
{% tab addWrld :arrow_up: Uploading a World %}

1. Upload your world folder by following our [World Management Guide](/minecraft/java/general/world-management#arrow_up-uploading-your-world).

    > You may use any name without spaces as the folder name. This will be used as the world name in-game.

2. Navigate back to the [Console](https://client.falixnodes.net/server/console).

3. To import the world into Multiverse, type the command below in the console. Make sure to replace `<world_name>` with the name of the world folder you uploaded, and `<type>` with a world type.

    ```
    /mvimport <world_name> <type>
    ```

    Some examples of world types are: `NORMAL`, `NETHER`, `THE_END`. To find a list of all available world types run `mvenv` in the console.

4. Run the command.

{% endtab %}
{% tab addWrld Generating a New World %}

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). To generate a new world using Multiverse, type the following command in the console while replacing all placeholder values by referring to the table:

    ```
    /mvcreate <world_name> <type> (-parameters)
    ```

    | Placeholder     | Description                                                                                                                                                         |
    | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | `<world_name>`  | The name of the world without any spaces                                                                                                                            |
    | `<type>`        | The world type. Some options are: `NORMAL`, `NETHER`, `THE_END`                                                                                                     |
    | `(-parameters)` | Optional parameters. You may refer to the [official wiki](https://github.com/Multiverse/Multiverse-Core/wiki/Command-Reference#create-command) for more information |

    > To find a list of all available world types run `mvenv` in the console.

4. Run the command and allow the world to generate (this can take a while).

{% endtab %}
{% endtabs%}

> To teleport to your world, use the `/mvtp <world_name>` command.

## Creating Custom Portals Between Worlds:

Before proceeding, you will need to install the [Multiverse-Portals](https://modrinth.com/plugin/multiverse-portals) plugin. You will also need a permission management plugin as only players with the `multiverse.portal.access.<world_name>` or `multiverse.portal.access.*` permission will be able to use these portals.

1.  In-game, give yourself operator permissions or use a permission plugin and give yourself the necessary permissions.

2.  Create a portal frame out of any blocks, this can either be a horizontal portal or vertical.

3.  select your portal by left-clicking on a corner of the portal with a wooden axe and right-clicking on the corner farthest away.

4.  Type the command below in chat while replacing all placeholder values, you may refer to the table for more information.

    ```
    /mvp create <portal_name> <parameter>
    ```

    | Placeholder     | Description                                                                                                                                      |
    | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
    | `<portal_name>` | The name of the portal without any spaces                                                                                                        |
    | `<parameter>`   | - `w:world_name:se` to link to another world's spawn (replace world_name with the actual world name)                                             |
    |                 | - `e:world_name:X,Y,Z` to link to an exact location in another world (replace world_name and X, Y, Z with the actual world name and coordinates) |
    |                 | - `p:portal_name` to link to another portal (replace portal_name with the actual portal name)                                                    |

5.  Run the command to create a portal and automatically select it.

> To modify existing portals simply run `/mvp select <portal_name>` to select the portal, and `/mvp modify dest <parameter>` to change its destination. The parameters from the previous table will also work for this command.
