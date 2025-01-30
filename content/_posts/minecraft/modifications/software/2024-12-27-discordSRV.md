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
## What is DiscordSRV?

DiscordSRV is a plugin that connects your Minecraft server and Discord using a Discord bot hosted on the Minecraft server.
It allows you to:
- Have an interactive chat between a Discord channel and the Minecraft server.
- Forward your Minecraft console to a Discord text channel.
- Send alerts based on specific events.
- Use voice proximity through Discord voice chat.
- Require linked accounts (or specific roles) to play.

## Installation Process:

### Installing the Plugin:
You can refer to our guide on how to add plugins here: [Adding Plugins](/minecraft/modifications/general/adding-plugins).

### Creating and configuring the Discord bot:
1. Go to the [Discord Developer Portal](https://discord.com/developers/applications/).

2. Click on "New Application" and make a name for the bot that will be used on your Discord server.

3. Go to the Installation tab, uncheck the User Install option and set the Install Link to 'None'.

4. Open the Bot tab, uncheck the Public Bot option, and make sure the Server Members Intent and Message Content Intent options are checked.

5. Copy the Application ID from the General Information tab.

6. Go to the [Discord bot authorization URL generator](https://scarsz.me/authorize) and paste the Application ID into the page.

### Configuring the Plugin:

{: .warning}
> Make sure you start your server at least once after adding the plugin to generate required configuration files.

1. Navigate to the [File Manager](https://client.falixnodes.net/server/filemanager?dir=/plugins/DiscordSRV/) and open the `plugins/DiscordSRV` folder.

2. Open the `config.yml` file. This is the main configuration file.

3. In the file, paste your bot token between the quotes after `BotToken:`.

4. Open Discord and go to your Discord settings.

5. On desktop, go to the Advanced tab and enable Developer Mode.

6. On your Discord server, right-click on the channel for the interactive chat and click 'Copy Channel ID'.

{: .warning}
> Make sure that your bot has the required permissions to see the channel.

7. Replace the `000000000000000000` after `global` at line 30 with the Channel ID that you copied.

> If you use a chat plugin (like HeroChat or TownyChat), then you should read their config on how to set up DiscordSRV.

> <strong>Optional:</strong> Copy the Channel ID of a second staff-only Discord channel to use as a console channel, then paste the Channel ID between the quotes at line 33.

8. Replace the discord invite link on line 36 with the invite link to your server; this will be displayed when players use the `/discord` command.

9. (Re-)start the server.

## Additional configuration and features

### Link to Join Setup

This feature requires players to link their Discord account by sending a DM to the bot when they first join the Minecraft server. This allows you to whitelist your server to members who have joined your Discord server or have a specific role in it to join your Minecraft server.

1. Make sure `Enabled:` is set to `true` in the `linking.yml` config file, then (re)start your server to apply changes.

2. You can set the message that players get when they try to join on line 32 after `Not linked message:`.

3. If you want to force players to be on the Discord server, you can set `Must be on Discord server:` to `true`.

4. If you want players only with a certain role to be able to join, you can set `Require subscriber role to join:` to `true` on line 52.

5. Add the role ID(s) of the allowed roles after `Subscriber roles:` on line 53; you can list multiple roles by separating them with a comma.

6. If you have multiple roles whitelisted, choose whether you want to require the user to have ALL of the roles listed (true) or just one of them (false); you can set the message that kicks players who don't meet these criteria on line 55.

### Proximity Chat Setup

{: .warning}
> Make sure to read the "Link to Join Setup" section before proceeding. You will need to link your Discord and Minecraft accounts so that DiscordSRV knows which account belongs to which player.

1. In your Discord server, create a category where the voice module will create/delete/move voice channels.

2. Right-click on the category and select Copy ID.

3. In the `voice.yml` config file, look for the Voice Category option on line 14 and replace `000000000000000000` with the copied category ID.

5. Create a channel (name doesn't matter) under the voice category you just created; this will be your "Lobby" voice channel.

6. After moving the channel, right-click on it and select Copy ID.

7. Look for the Lobby Channel option on line 18 and replace `000000000000000000` with the copied channel ID.

8. (Re-)start your server to apply changes.

You can configure additional options (such as proximity chat range) under the Network option on line 22.
