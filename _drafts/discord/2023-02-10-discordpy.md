---
layout: help/article
title:  "Setting Up Discord bot in Python - Falix"
categories: Discord
tags: discordPY
icon: <i class='fa-brands fa-python'></i>
permalink: /help/discord/python-discord-bot.*
gitURL: _posts/discord/2023-02-10-discordpy.md
description: "Find out how to create your own Discord Bot with python in Falix"

author: Juoum
authorGitHub: itsjuoum
---

# Creating And Hosting a Discord Bot Using Discord.py

{: .note }
> We do not recommend the use of Discord.py as it has been discontinued and will not be updated anymore. For further information, read this [official announcement](https://gist.github.com/Rapptz/4a2f62751b9600a31a0d3c78100287f1) from the owner of Discord.py.
Please find a new package for Python Discord bots as soon as possible.

## Creating a Bot
First, simply go to [Discord's Developers Portal](https://discord.com/developers/applications) and login. Then, click on "New Application" in the top right corner of the screen, give it a name and click on "Create". After that, click on bot on the side menu, press "add bot" and confirm it.
You've successfully created the bot account!

## Coding a Bot
To start coding your Discord bot, please refer to the official [Discord.py guide](https://discordpy.readthedocs.io) for a detailed step-by-step guide with further information and examples.

## Hosting The Bot
{: .note }
> Discord Bot hosting is only available on our [Premium plans](https://falixnodes.net/minecraft-server-hosting).

To host your bot in our service, you need a server. To create one, follow [this article](https://help.falixnodes.net/falix/general/getting-started/#creating-a-server). Head over to the [Game Panel](https://panel.falixnodes.net), log in and select the server you've just created. Once you're there, go to your server's file manager. A button for it can be found on the top bar. 
Now, simply upload your project files. Wait for the upload to complete and navigate back to your server's console, then start your server. 
You will now see 2 options, one for Discord bot hosting, and the other for SinusBot hosting. Type `1`, for Discord bot hosting. You'll now be shown a new menu with a bunch of options. If not, start the server manually. 
This is a Python Discord bot guide, so we're going to choose option `2`, to start a Python server, then choose the Python version (If you downloaded the latest Python version or you're running a version that is not listed, choose `custom`, and type the version you want). Wait for it to download and install.
Your server should've crashed. Wait for it to start again. Now, we're going to install discord.py. For that, you'll need to choose option `4`, then type `discord.py`, and once more, pick a Python version. Once the installation process of discord.py has finished, start the Python server (option 2), type the name of the project's main file (usually `index.py` or `main.py`) and choose a Python version.

{: .note }
> You can change the Python version under the startup tab so that it is set automatically.
