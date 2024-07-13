---
layout: help/article
title:  "Configure plugin DiscordSRV - Falix"
categories: Minecraft
icon: <i class='fa-light fa-puzzle'></i>
tags: plugins
permalink: /help/minecraft/plugins/discordsrv.*
gitURL: _posts/minecraft/plugins/2021-08-04-discordsrv.md
description: "Configure plugin DiscordSRV for your Minecraft Server at Falix"

author: Korbs
authorGitHub: korbsstudio
---

<div class="install-plugin">
    <img style="border-radius: 50px;" src="https://www.spigotmc.org/data/resource_icons/18/18494.jpg?1455529290">
    <h2>DiscordSRV</h2>
    <h3>Developer: Scarsz</h3> 
    <a href="https://www.spigotmc.org/resources/discordsrv.18494/">Download this Plugin</a>
</div>

# What is DiscordSRV
Using this plugin, you are able to give players the ability to chat in-game to chat with players on your Discord server as well as having people on the Discord server be able to chat with people on the server- this is useful for the situation of someone not being at their computer and being able to talk in-game.

As well as that, this plugin also has a remote console feature. You can designate a text channel for the plugin to listen on where messages sent to that channel are run as commands by the server console. You should restrict sending this channel to a developer or high ranking role only. Due to how Discord's permissions work, though, you can have some server roles being able to see the console, yet not being able to send messages in that channel, thus creating a read-only console for trusted staff members.

Both the chat and console link are toggleable through the configuration file. Some, but not all, options can be refreshed with /discord reload, by an op. VanishNoPacket permissions like silent join/quit, fake join/quit and join without announcing are checked when sending player join messages in the chat channel.

# Installation Process
Like any other plugin, you'll need to download the <u>.jar</u> file of DiscordSRV, then add it to your plugins folder. Once you've added DiscordSRV to your plugins folder, fully restart the server, and all configuration files will be generated for DiscordSRV.

You can download DiscordSRV by clicking "Download this Plugin" above.

# Creating your Discord Bot
Before continuing, creating a bot on Discord is needed in order to proceed to the next step. 

## Creating
In the Discord Developer dashboard, create a new application. Then, on the application's page, go to the Bot tab, click Add Bot, and confirm. 

Enable the **SERVER MEMBERS INTENT** option under "Privileged Gateway Intents" on the bot tab as well.

## Inviting
Inviting your bot is easy, in the bot's General Information tab, copy the applications' ID. Go [here](https://scarsz.me/authorize), then press Ctrl V to paste the ID. This will redirect you to the bot's invite link. 

Invite the bot to the server you want it in.

# Configuration
## Sync Plugin with Discord Bot
In order for your Minecraft server's chat to send to your Discord server, you'll need to add your bot's token to the plugin's configuration.

To find your bot's token, head back to your Discord Developer dashboard, click on your applications, go to the Bot tab. Click the Copy button under token.

In the <u>config.yml</u> file of DiscordSRV, paste the token where it says BotToken, usually on line 5.

## Setting Channel on your Discord Server
We need to tell DiscordSRV which channel on your Discord server it should send the chat to.

In the <u>config.yml</u> file of DiscordSRV, there is a place to add your channel ID, usually on line 11. Replace "0000000000" with your channel ID. 

To get your channel ID, right click on the channel you want to set for the Minecraft chat, then click on Copy ID. If the Copy ID option is not showing, please enable Developer Mode in your Discord's Advanced settings.

Optionally, you can set a console channel in your Discord server too. This can be used to send commands to your server from Discord, please keep this channel hidden from other members and only visible to admins.