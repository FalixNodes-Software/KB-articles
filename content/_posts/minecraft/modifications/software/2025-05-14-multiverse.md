---
title: Adding Multiple Worlds and Portals With Multiverse
tags: Software
permalink: /minecraft/modifications/software/multiverse
description: Using Multiverse-Core and Multiverse-Portals to add portals to custom worlds
author:
    - TWIXhunter
    - Deka
    - Mocab
icon: "https://cdn.modrinth.com/data/3wmN97b8/3e3c705351a85c68b78a6131aff23f4674b2f71f_96.webp"
mod-name: "Multiverse-Core"
mod-type: Bukkit, Paper, Spigot
mod-url: "https://modrinth.com/plugin/multiverse-core"
---

## What is Multiverse?

Multiverse is a world management plugin that provides multi-world support, with the ability to set custom seeds, generation, game mode and much more on a per-world basis. You can use both commands and custom portals to teleport between your worlds, with the ability to restrict each world to a set permission.

## Installation:

### Prerequisites:

- Make sure your server is running Spigot or any of its forks (Paper, Purpur, etc).

### Installation:

Please refer to our [Adding Plugins](/minecraft/modifications/general/adding-plugins) guide.

## Adding Worlds:

{% tabs addWorld %}
{% tab addWorld Uploading a World %}

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. Navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

4. Upload your world folder.

    > You may use any name without spaces as the folder name (except for `world`). This will be used as the world name in-game.

5. Navigate back to the [Console](https://client.falixnodes.net/server/console).

6. To import the world into Multiverse, type the command below in the console. Make sure to replace `<world_name>` with the name of the world folder you uploaded, and `<type>` with a world type.

    ```
    /mvimport <world_name> <type>
    ```

    > Some examples of world types are: `NORMAL`, `NETHER`, `THE_END`. To list all available world types, execute `mvenv` in the console.

7. Run the command.

{% endtab %}
{% tab addWorld Generating a New World %}

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. To generate a new world using Multiverse, execute the following command in the [Console](https://client.falixnodes.net/server/console) while replacing all placeholder values by referring to the following table:

    ```
    /mvcreate <world_name> <type> (-parameters)
    ```

    | Placeholder     | Description                                                                                                                                                         |
    | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | `<world_name>`  | The name of the world without any spaces                                                                                                                            |
    | `<type>`        | The world type. Some options are: `NORMAL`, `NETHER`, `THE_END`                                                                                                     |
    | `(-parameters)` | Optional parameters. You may refer to the [official wiki](https://github.com/Multiverse/Multiverse-Core/wiki/Command-Reference#create-command) for more information |

    > To list all available world types, execute `mvenv` in the console.

4. Run the command and allow the world to generate (this can take a while).

{% endtab %}
{% endtabs %}

> To teleport to your world, use the `/mvtp <world_name>` command.

## Creating Custom Portals Between Worlds:

You will need to install the [Multiverse-Portals](https://modrinth.com/plugin/multiverse-portals) plugin. If you want to allow other players to use these portals, you will have to add the `multiverse.portal.access.<world_name>` or `multiverse.portal.access.*` permission.

1. Give yourself operator permissions or use a permission plugin and grant the necessary permissions.

2. Create a portal frame of any size out of any blocks.

3. Select your portal by left-clicking on a corner of the portal with a wooden axe and right-clicking on the corner farthest away.

4. Type the command below in chat while replacing all placeholder values, you may refer to the table for more information.

    ```
    /mvp create <portal_name> <parameter>
    ```

    | Placeholder     | Description                                                                                                                                      |
    | --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
    | `<portal_name>` | The name of the portal without any spaces                                                                                                        |
    | `<parameter>`   | - `w:world_name:se` to link to another world's spawn (replace world_name with the actual world name)                                             |
    |                 | - `e:world_name:X,Y,Z` to link to an exact location in another world (replace world_name and X, Y, Z with the actual world name and coordinates) |
    |                 | - `p:portal_name` to link to another portal (replace portal_name with the actual portal name)                                                    |

5. Run the command to create a portal and automatically select it.

> To modify existing portals you can use `/mvp select <portal_name>` to select the portal, and `/mvp modify dest <parameter>` to change it's destination. The parameters from the previous table will also work for this command.
