---
layout: post
title: How to Interact Between Discord and Minecraft Using DiscordSRV
category: Modifications
tags: Software
permalink: minecraft/modifications/software/discordsrv
description: DiscordSRV is a plugin that allows you to link your Minecraft server and Discord server together.
keywords:
    - keyword: discordSRV
author:
    - Twixhunter
toc: true

icon: "https://www.spigotmc.org/data/resource_icons/18/18494.jpg?1455529290"
mod-name: DiscordSRV
mod-type: Plugin
mod-url: "https://www.spigotmc.org/resources/discordsrv.18494/"
---
## What is DiscordSRV
DiscordSRV is a plugin that links your Minecraft server and Discord together using a Discord bot hosted on the Minecraft server.
It allows you to:
- Have an interactive chat between a Discord channel and the Minecraft server.
- Forward your Minecraft console to a Discord text channel.
- Broadcast alerts based on certain events.
- Use voice proximity through Discord Voice Chat.
- Require linking accounts (or certain roles) to play.

## Installation Process:

### Installing the Plugin:
We already have a guide on how to install DiscordSRV as well as any other plugin in our [Adding Plugins](/minecraft/modifications/general/adding-plugins) guide, Download DiscordSRV [here](https://get.discordsrv.com)

### Creating and Configuring the Discord Bot:
1. Go to the [Discord Developer Portal](https://discord.com/developers/applications/).

2. Click on "New Application" and enter the name of the bot that will send messages in your Discord server.

3. Open the Installation tab in the left menu, disable the User Install option, and set the Install Link to `None`.

4. Open the Bot tab, disable the Public Bot option, and make sure to enable the Server Members Intent and the Message Content Intent options.

5. Copy the "Application ID" from the General Information tab.

6. Go to https://scarsz.me/authorize and paste the Application ID on the page.

7. Select the server you want the bot to join and press authorize.

8. Click the Reset Token button at the top of the bot's page and copy the token to your clipboard.

### Configuring the Plugin:
{: .warning}
> Make sure to start the server once to generate the needed config file.

1. Navigate to the [File Manager](https://client.falixnodes.net/server/filemanager) by hovering over "Manage," then clicking on "File Manager."

2. Open the [Plugins](https://client.falixnodes.net/server/filemanager?dir=/plugins/) folder.

3. Locate and open the [DiscordSRV](https://client.falixnodes.net/server/filemanager?dir=/plugins/DiscordSRV/) configuration folder.

4. Find and open "config.yml." This is the main configuration file where you will be able to customize any feature needed.

5. At line 9, paste the bot token in between the "".

6. Open Discord and go to your Discord settings by clicking on the User Settings cogwheel at the bottom left of your Discord.

7. Go to the Advanced tab under App Settings and enable Developer Mode.

8. Back in your Discord server, right-click the channel for the interactive chat and click "Copy Channel ID."

{: .error}
> Make sure that the bot has the needed permissions in the channel. You can find more info on how to do this [here](https://docs.discordsrv.com/installation/initial-setup/#give-the-bot-the-discord-permissions-it-needs-to-run).

9. Go back to [the config.yml file](https://client.falixnodes.net/server/edit?path=/plugins/DiscordSRV/config.yml&file=config.yml&mime=text/plain) in [the File Manager](https://client.falixnodes.net/server/filemanager?dir=/plugins/DiscordSRV/).

10. Replace the 000000000000000000 after "global" at line 30 with the Channel ID that you just copied.

> If you use a chat plugin (like HeroChat or TownyChat), then you should read their config on how to set up DiscordSRV.

> <strong>Optional:</strong> Copy the Channel ID of a second staff-only Discord channel to use as console channel, then paste the Channel ID between the "" at line 33.

11. Replace the Discord invite link at line 36 with the invite link to your server; this link will be displayed when players use the /discord command.

12. (Re)start the server.

## Extra Configuration and Features.
### Link to Join Setup.

This feature requires your server members to link their Discord account by sending a DM to the bot when they join the server for the first time. This allows you to use the proximity voice chat feature and whitelist your server to only allow members that joined your Discord server or have a specific role to join your Minecraft server.

1. Make sure "Enabled" is set to "true" in the [linking.yml](https://client.falixnodes.net/server/edit?path=/plugins/DiscordSRV/linking.yml&file=linking.yml&mime=text/plain) config file, then (re)start your server.

2. You can set the message that players get when they try to join on line 32 after "Not linked message:"

3. If you want to force players to be in the Discord server, then you can set "Must be in Discord server:" to "true."

4. If you only want players with a specific role (like subscriber or lvl10) to be able to join, then you can set "Require subscriber role to join:" to "true" at line 52.

5. Paste the role ID(s) of the allowed roles after "Subscriber roles:" at line 53; you can list multiple roles by separating them with a comma.

6. If you have multiple roles whitelisted, choose if you want to require the user to have ALL the roles listed (true) or just needs one of them (false); you can set the message that kicks players that don't meet those criteria at line 55.

Read through the config to get a better understanding of what else you can do with this linking option.

### Proximity Chat Setup.
Lorem ipsum dolor sit amet.

{: .warning}
> Please make sure to go through the "Link to join setup" before proceeding with this setup. You need to link your Discord and Minecraft accounts so that DiscordSRV knows which accounts belong to which player.

1. Make sure "Enabled" is set to "true" in the [linking.yml](https://client.falixnodes.net/server/edit?path=/plugins/DiscordSRV/linking.yml&file=linking.yml&mime=text/plain) config file, then (re)start your server.

2. In your Discord server, create a category (name doesn't matter) where the voice module will create/delete/move voice channels.

3. Right-click on the category and select Copy ID.

4. In the voice.yml config, search for the Voice Category option at line 14 and replace 000000000000000000 with the copied Category ID.

5. Create a channel (name doesn't matter) underneath the voice category you just made; this will be your "Lobby" voice channel.

6. Right-click on the channel after moving it and select Copy ID.

7. In the voice.yml config, search for the Lobby Channel option at line 18 and replace 000000000000000000 with the copied Channel ID.

8. (Re)start your server.

You can configure extra options (like the range of the proximity chat) under the Network option at line 22.