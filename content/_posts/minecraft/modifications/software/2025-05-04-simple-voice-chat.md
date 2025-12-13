---
title: Allow Proximity Chat With Simple Voice Chat
tags: Software
permalink: minecraft/modifications/software/voice-chat
description: How to add a proximity-based voice chat to your server so players can talk to each other in-game.
keywords:
    - keyword: vc
    - keyword: microphone
    - keyword: chat
      matches: ["voice", "proximity"]
author:
    - Naoki
    - Deka
    - Mocab

icon: "https://cdn.modrinth.com/data/9eGKb6K1/icon.png"
mod-name: Simple Voice Chat
mod-type: Plugin, Mod
mod-url: "https://modrinth.com/plugin/simple-voice-chat"
---

## What Is Simple Voice Chat?

Simple Voice Chat is a software that introduces proximity-based voice chat. It allows players to communicate with each other in-game. It also has a variety of addons that offer additional features. Simple Voice Chat requires you to have the mod installed on your client, which is only available on the Java Edition of Minecraft. If you don't have it installed on your client, you can still join the server, but you won't be able to use the voice chat features.

## Installation and Configuration:

### Prerequisites:

{% tabs softwareType %}
{% tab softwareType <i class="type-software plugin"></i> Plugin %}

-   Ensure your server is running with Spigot or any of its forks (Paper, Purpur, etc).
-   Make sure players have the mod installed locally.

{% endtab %}
{% tab softwareType <i class="type-software mod"></i> Mod %}

-   Ensure your server is running with either Fabric or Forge or any of their forks (Quilt & NeoForge respectively).
-   Make sure players have the mod installed locally.

{% endtab %}
{% endtabs %}

### Installation:

{% tabs softwareType %}
{% tab softwareType <i class="type-software plugin"></i> Plugin %}

We already have a guide on how to install Simple Voice Chat as well as any other plugin in our [Adding Plugins](/minecraft/modifications/general/adding-plugins) guide.

{% endtab %}
{% tab softwareType <i class="type-software mod"></i> Mod %}

We already have a guide on how to install Simple Voice Chat as well as any other mod in our [Adding Mods](/minecraft/modifications/general/adding-mods) guide.

{% endtab %}
{% endtabs %}

## Configuration:

{% tabs softwareType %}
{% tab softwareType <i class="type-software plugin"></i> Plugin %}

1. Once again, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

2. Once more, open the [Plugins](https://client.falixnodes.net/server/filemanager?dir=/plugins/) folder.

3. Locate and open the [voicechat](https://client.falixnodes.net/server/filemanager?dir=/plugins/voicechat/) configuration folder.

4. Find and open "voicechat-server.properties". This is the main configuration file where you will be able to customize any feature needed.

5. Look for the `port=` setting and set it to your server's extra port or set it to the main port of your server if it is not possible to create extra ports. This will be the port your voice chat will be hosted on.

    {: .warning}
    > If you are a Free plan user, you may use your server's main port. If your server has plugins that occupy the UDP port (e.g Geyser), this setting will conflict with the other plugin.

    > If you require assistance creating or finding your extra ports, refer to our [extra ports](/falix/dashboard/server/extra-port) guide.

6. Click on "**Save File**{: .green }" to save your changes.

7. (Re)start your server to apply the changes.

{% endtab %}
{% tab softwareType <i class="type-software mod"></i> Mod %}

1. Once again, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

2. Locate and open the [config](https://client.falixnodes.net/server/filemanager?dir=/config/) folder.

3. A new folder called [voicechat](https://client.falixnodes.net/server/filemanager?dir=/config/voicechat/) should have generated. Open it to access the newly generated configuration files.

4. Find and open "voicechat-server.properties". This is the main configuration file where you will be able to customize any feature needed.

5. Look for the `port=` setting and set it to your server's extra port or set it to the main port of your server if it is not possible to create extra ports. This will be the port your voice chat will be hosted on.

    {: .warning}
    > If you are on a free plan then you can use your servers default port. please be aware that this is not possible while running geyser or other plugins that require a UDP port.

6. Click on "**Save File**{: .green }" to save your changes.

7. (Re)start your server to apply the changes.

{% endtab %}
{% endtabs %}
