---
layout: help/article
title:  "Setting Up Discord Bot in NodeJS - Falix"
categories: Discord
tags: discordJS
icon: <i class='fa-brands fa-js-square'></i>
permalink: /help/discord/nodejs-discord-bot.*
gitURL: _posts/discord/2023-02-10-discordjs.md
description: "Find out how to create your own Discord Bot with nodejs in Falix"

author: Juoum
authorGitHub: itsjuoum
---

# Creating And Hosting a Discord Bot Using Discord.js

## Creating a Bot

First, simply go to [Discord's Developers Portal](https://discord.com/developers/applications) and login.
Then, click on "New Application" in the top right corner of the screen, give it a name and click on "Create".
After that, click on bot on the side menu, press "add bot" and confirm it.
You've successfully created the bot account!

## Coding a Bot

To start coding your Discord bot, please refer to the official [Discord.js guide](https://discordjs.guide) for a detailed step-by-step guide with further information and examples.

## Hosting The Bot

{: .note }
> Discord Bot hosting is only available on our [Premium plans](https://falixnodes.net/minecraft-server-hosting).

To host your bot on our service, you need a server.
To create one, follow [this article](https://help.falixnodes.net/falix/general/getting-started/#creating-a-server).
Head over to the [Game Panel](https://panel.falixnodes.net), log in and select the server you've just created.
Once you're there, go to your server's file manager. A button for it can be found on the top nav bar.
Now, simply upload your project files, make sure to include the `package.json`, `package-lock.json`, and your main/start file. Wait for the upload to be complete and navigate back to your server's console, then start your server.
You'll be shown a bunch of options including Bot hosting. Since we're hosting a Discord bot, type `5` and press enter.
You will now see 2 options, one for Discord bot hosting, and other for SinusBot hosting. Type `1`, for Discord bot hosting.
Your server will restart and you'll now be shown a new menu with a bunch of options. If not, start the server manually. Now that that's done, let's install the discord.js package. To do this, select number `5` (Install NodeJS package), and type `discord.js`. Afterwards, choose a NodeJS version and wait for the package to be installed. The server will shut down after the installation, so start it again once it's finished installing. Following on, choose option `1` to start the NodeJS server. Then, type the name of your bot's main/start file, (usually `index.js`).
You'll then be asked for a NodeJS version, it's recommended to use the latest stable version.
Enter the version you'd like, then wait a bit, and your server should be ready, and your bot online!

{: .note }
> You can change the NodeJS version under the startup tab so that it is set automatically.
