---
layout: post
title: "How To Create A discord.js Bot"
category: discordjs
tags: General
permalink: other/discord/general/create-discordjs
description: "Learn how to create and host A Discord bot using the discord.js package"
keywords:
    - keyword: discord.js
      matches: ["create", "host"]
author: TWIXhunter
---

Using [discord.js](https://discord.js.org) to create and host a Discord bot allows you to bring custom functionality, automation and interactive features directly to your Discord server. Whether you're building a moderation tool, a music player or a fun chatbot, discord.js gives you the flexibility to do so using JavaScript and Node.js.

{: .warning}
> Running a Discord bot is only possible on a paid FalixNodes plan.

For more information about discord.js or JavaScript, please refer to the official discord.js [guides](https://discordjs.guide/#before-you-begin) and [documentation](https://discord.js.org/docs/packages/discord.js/14.19.3).


## Creating the server
1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. In the navigation menu, click on Create Server.

3. Select a plan and enter a name and domain for your server.

4. Go to the "Applications" tab and select "Node.JS"

5. Click continue and choose the desired resources and location.

6. Complete the Billing steps (if needed) or press "Create My Server".

7. Select the server to go open the console and wait for Node.js to be installed.

## Setting up the Discord Bot

1. In the navigation menu, open the "Server Settings" category and navigate to [Settings](https://client.falixnodes.net/server/settings).

2. Go to the "Startup" tab and select the correct NodeJS version in the "Docker Image" Dropdown.

2. Go to the "Environment" tab and find the "Additional Node packages" variable.

3. Enter `discord.js` and other packages if desired.

4. Scroll down to the "Main File" option and enter the name of the file your server should run at startup. For example `index.js` or `bot.js`.

5. Navigate to [the File Manager](https://client.falixnodes.net/server/filemanager?dir=%2F) and upload or your bot files.

6. Navigate to [the console page](https://client.falixnodes.net/server/console) and start the server.