---
layout: post
title: How to Interact Between Discord and Minecraft Using DiscordSRV
category: Modifications
tags: Software
permalink: minecraft/modifications/software/discordsrv
description: DiscordSRV is a plugin that allows you to connect your Minecraft server to your Discord server together.
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
DiscordSRV is a plugin that connects your Minecraft server and Discord using a Discord bot hosted on the Minecraft server.
It allows you to
- Have an interactive chat between a Discord channel and the Minecraft server.
- Forward your Minecraft console to a Discord text channel.
- Send alerts based on specific events.
- Use voice proximity through Discord voice chat.
- Require linked accounts (or specific roles) to play.

## Installation Process:

### Installing the Plugin:
We already have a guide on how to install DiscordSRV as well as any other plugin in our [Adding Plugins](/minecraft/modifications/general/adding-plugins) guide, Download DiscordSRV [here](https://get.discordsrv.com)

### Creating and configuring the Discord bot:
1. Go to the [Discord Developer Portal](https://discord.com/developers/applications/).

2. Click on "New Application" and enter the name of the bot that will post to your Discord server.

3. Go to the Installation tab in the left menu, uncheck the User Install option and set the Install Link to 'None'.

4. Open the Bot tab, uncheck the Public Bot option, and make sure the Server Members Intent and Message Content Intent options are checked.

5. Copy the Application ID from the General Information tab.

6. Go to https://scarsz.me/authorize and paste the Application ID into the page.

### Configuring the Plugin:
{: .warning}
> Make sure to start the server once to generate the needed config file.

1. Navigate to the [File Manager](https://client.falixnodes.net/server/filemanager) by hovering over "Manage," then clicking on "File Manager."

2. Open the [Plugins](https://client.falixnodes.net/server/filemanager?dir=/plugins/) folder.

3. Locate and open the [DiscordSRV](https://client.falixnodes.net/server/filemanager?dir=/plugins/DiscordSRV/) configuration folder.

4. Locate and open "config.yml". This is the main configuration file where you will be able to customise all the features you need.

5. On line 9, paste the bot token between the "".

6. Open Discord and go to your Discord settings by clicking on the User Settings cogwheel at the bottom left of your Discord.

7. Under App Settings, go to the Advanced tab and enable Developer Mode.

8. Back on your Discord server, right-click on the channel for the interactive chat and click 'Copy Channel ID'.

{: .error}
> Make sure that the bot has the needed permissions in the channel. You can find more info on how to do this [here](https://docs.discordsrv.com/installation/initial-setup/#give-the-bot-the-discord-permissions-it-needs-to-run).

9. Go back to [the config.yml file](https://client.falixnodes.net/server/edit?path=/plugins/DiscordSRV/config.yml&file=config.yml&mime=text/plain) in [the File Manager](https://client.falixnodes.net/server/filemanager?dir=/plugins/DiscordSRV/).

10. Replace the 000000000000000000 after "global" at line 30 with the Channel ID that you just copied.

> If you use a chat plugin (like HeroChat or TownyChat), then you should read their config on how to set up DiscordSRV.

> <strong>Optional:</strong> Copy the Channel ID of a second staff-only Discord channel to use as console channel, then paste the Channel ID between the "" at line 33.

11. Replace the discord invite link on line 36 with the invite link to your server; this will be displayed when players use the /discord command.

12. (Re-)start the server.

## Additional configuration and features.
### Link to Join Setup.

This feature requires members of your server to link their Discord account by sending a DM to the bot when they first join the server. This allows you to use the proximity voice chat feature and whitelist your server to only allow members who have joined your Discord server or have a specific role to join your Minecraft server.

1. Make sure "Enabled" is set to "true" in the [linking.yml](https://client.falixnodes.net/server/edit?path=/plugins/DiscordSRV/linking.yml&file=linking.yml&mime=text/plain) config file, then (re)start your server.

2. You can set the message that players get when they try to join on line 32 after "Not linked message:".

3. If you want to force players to be on the Discord server, you can set "Must be on Discord server:" to "true".

4. If you only want players with a certain role (like subscriber or lvl10) to be able to join, you can set "Require subscriber role to join:" to "true" on line 52.

5. Add the role ID(s) of the allowed roles after "Subscriber roles:" on line 53; you can list multiple roles by separating them with a comma.

6. If you have multiple roles whitelisted, choose whether you want to require the user to have ALL of the roles listed (true) or just one of them (false); you can set the message that kicks players who don't meet these criteria on line 55.

Read through the config to get a better understanding of what else you can do with this linking option.

### Proximity Chat Setup.

{: .warning}
> Please be sure to read the "Link to join setup" before proceeding with this setup. You will need to link your Discord and Minecraft accounts so that DiscordSRV knows which account belongs to which player.

1. Make sure "Enabled" is set to "true" in the [linking.yml](https://client.falixnodes.net/server/edit?path=/plugins/DiscordSRV/linking.yml&file=linking.yml&mime=text/plain) config file, then (re)start your server.

2. In your Discord server, create a category (name doesn't matter) where the voice module will create/delete/move voice channels.

3. Right-click on the category and select Copy ID.

4. In the voice.yml config, look for the Voice Category option on line 14 and replace 000000000000000000 with the copied category ID.

5. Create a channel (name doesn't matter) under the voice category you just created; this will be your "Lobby" voice channel.

6. After moving the channel, right-click on it and select Copy ID.

7. In the voice.yml config, look for the Lobby Channel option on line 18 and replace 000000000000000000 with the copied channel ID.

8. (Re-)start your server.

You can configure additional options (such as proximity chat range) under the Network option on line 22.