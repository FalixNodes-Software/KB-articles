---
layout: post
title: How to interact betwene discord and minecraft using DiscordSRV
category: Modifications
tags: Software
permalink: minecraft/modifications/software/discordsrv
description: DiscordSRV is a plugin that allows you to link your Minecraft server and Discord server together.
keywords:
    - keyword: discordSRV
    - keyword: chat
      matches: ["interacteble", "discord"]
author:
    - Twixhunter
toc: true

icon: "https://www.spigotmc.org/data/resource_icons/18/18494.jpg?1455529290"
mod-name: DiscordSRV
mod-type: Plugin
mod-url: "https://www.spigotmc.org/resources/discordsrv.18494/"
---
# What is DiscordSRV
Discord SRV is a plugin that allows you to link your Minecraft server and Discord together.
it allows you to:
- Have an interactive chat between a discord channel and the Minecraft server.
- Forward your Minecraft Console to a Discord text channel.
- Broadcast alerts based on certain events.
- Use Voice Proximity through the Discord Voice Chat.
- Require linking accounts (or certain role/s) to play.

# :hammer_and_wrench: Installation Process:
## installing the plugin:

{% tabs softwareType %}
{% tab softwareType :electric_plug: Plugin %}

We already have a guide on how to install GeyserMC as well as any other plugin in our [Adding Plugins](/minecraft/modifications/general/adding-plugins) guide.

{% endtab %}
{% tab softwareType :gear: Mod %}

We already have a guide on how to install GeyserMC as well as any other mod in our [Adding Mods](/minecraft/modifications/general/adding-mods) guide.

{% endtab %}
{% endtabs %}

## Creating and configuring the discord bot:
1. go to the [Discord developer portal](https://discord.com/developers/applications/)

2. Click on "New application" and enter the name of the Bot that will send messages in your discord server.

3. Open the Installation tab in the left menu, disable the User Install option and set Install Link to `None`.

4. Open the Bot tab, disable the Public Bot option and make sure to enable the Server Members Intent an the Message Content Intent options.

5. Copy the "ApplicationID" from the General Information tab

6. Go to https://scarsz.me/authorize and paste the ApplicationID on the page

7. Select the server that you want the bot to join and press authorize.

8. Click the Reset Token button at the top of the page and copy the token to your clipboard.

## Configuring the Plugin:
{: .warning}
> Make sure to start the server once to generate the needed config file

1. Navigate to the [File Manager](https://client.falixnodes.net/server/filemanager) by hovering over "Manage", then clicking on "File Manager".

2. Open the [Plugins](https://client.falixnodes.net/server/filemanager?dir=/plugins/) folder.

3. Locate and open the [DiscordSRV](https://client.falixnodes.net/server/filemanager?dir=/plugins/DiscordSRV/) configuration folder.

4. Find and open "config.yml". This is the main configuration file where you will be able to customize any feature needed.

5. At line 9, Paste the bot-token in-between the ""

6. 