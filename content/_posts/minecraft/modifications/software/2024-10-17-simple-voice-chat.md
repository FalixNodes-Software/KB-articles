---
layout: post
title: Installing and configuring Simple Voice Chat
category: Modifications
tags: Software
permalink: minecraft/modifications/software/voice-chat
description: Adding a proximity-based voice chat to your server.
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

## :studio_microphone: What Is Simple Voice Chat?

Simple Voice Chat is a software that introduces proximity-based voice chat. It allows players to communicate with each other in-game. It also has a variety of addons that offer additional features. Simple Voice Chat requires you to have the mod installed on your client, which is only available on the Java Edition of Minecraft. If you don't have it installed on your client, you can still join the server, but you won't be able to use the voice chat features.

## :hammer_and_wrench: Installation and Configuration:

### Prerequisites:

{% tabs softwareType %}
{% tab softwareType :electric_plug: Plugin %}

-   Ensure your server is running with Spigot or any of its forks (Paper, Purpur, etc).
-   Your server must have at least one **unused** extra port or in other words, a forwarded port. If you wish to allocate an extra port, please follow our [extra ports](/falix/dashboard/server/extra-port) guide.
-   Make sure players have the mod installed locally.

{% endtab %}
{% tab softwareType :gear: Mod %}

-   Ensure your server is running with either Fabric or Forge or any of their forks (Quilt & NeoForge respectively).
-   Your server must have at least one **unused** extra port or in other words, a forwarded port. If you wish to allocate an extra port, please follow our [extra ports](/falix/dashboard/server/extra-port) guide.
-   Make sure players have the mod installed locally.

{% endtab %}
{% endtabs %}

### Installation:

{% tabs softwareType %}
{% tab softwareType :electric_plug: Plugin %}

We already have a guide on how to install Simple Voice Chat as well as any other plugin in our [Adding Plugins](/minecraft/modifications/general/adding-plugins) guide.

{% endtab %}
{% tab softwareType :gear: Mod %}

We already have a guide on how to install Simple Voice Chat as well as any other mod in our [Adding Mods](/minecraft/modifications/general/adding-mods) guide.

{% endtab %}
{% endtabs %}

## Configuration:

{% tabs softwareType %}
{% tab softwareType :electric_plug: Plugin %}

1. Once again, navigate back to the [File Manager](https://client.falixnodes.net/server/filemanager) by hovering over "Manage", then clicking on "File Manager".

2. Once more, open the [Plugins](https://client.falixnodes.net/server/filemanager?dir=/plugins/) folder.

3. Locate and open the [voicechat](https://client.falixnodes.net/server/filemanager?dir=/plugins/voicechat/) configuration folder.

4. Find and open "voicechat-server.properties". This is the main configuration file where you will be able to customize any feature needed.

5. Look for the `port=` setting and set it to your server's **unused** extra port. This will be the port your voice chat will be hosted on.

    > If you require assistance creating or finding your extra ports, refer to our [extra ports](/falix/dashboard/server/extra-port) guide.

6. Click on "**Save File**{: .green }" to save your changes.

7. (Re)start your server to apply the changes.

{% endtab %}
{% tab softwareType :gear: Mod %}

1. Once again, navigate back to the [File Manager](https://client.falixnodes.net/server/filemanager) by hovering over "Manage", then clicking on "File Manager".

2. Locate and open the [config](https://client.falixnodes.net/server/filemanager?dir=/config/) folder.

3. A new folder called [voicechat](https://client.falixnodes.net/server/filemanager?dir=/config/voicechat/) should have generated. Open it to access the newly generated configuration files.

4. Find and open "voicechat-server.properties". This is the main configuration file where you will be able to customize any feature needed.

5. Look for the `port=` setting and set it to your server's **unused** extra port. This will be the port your voice chat will be hosted on.

    > If you require assistance creating or finding your extra ports, refer to our [extra ports](/falix/dashboard/server/extra-port) guide.

6. Click on "**Save File**{: .green }" to save your changes.

7. (Re)start your server to apply the changes.

{% endtab %}
{% endtabs %}
