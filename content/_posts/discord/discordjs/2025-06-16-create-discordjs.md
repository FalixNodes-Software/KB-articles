---
layout: post
title: "How To Create A Discord.js Bot"
category: discordjs
tags: General
permalink: discord/discordjs/general/create-discord-js
description: "Learn how to Create and Host A Discord bot using the discord.js package"
keywords:
    - keyword: discord.js
      matches: ["create", "host"]
author: TWIXhunter
---

Creating and hosting a Discord bot using Discord.js allows you to bring custom functionality, automation, and interactive features directly into your Discord server. Whether you're building a moderation tool, music player, or a fun chatbot, Discord.js gives you the flexibility to make it happen with JavaScript.

> Running a Discord bot is only possible on a paid Falixnodes plan.

If you want more information about discord.js or JavaScript then please see the official discord.js [guides](https://discordjs.guide/#before-you-begin) and [documentation](https://discord.js.org/docs/packages/discord.js/14.19.3).

## Creating the server
1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. In the navigation menu, click on [Create Server](https://client.falixnodes.net/create).

3. Scroll down to "Create Server" and input the respective values into each field.

4. Select "Custom Game server" in the "Select Your Game" dropdown.

5. Create the server and open the console.

6. Start the server and enter `5` to select `Discord Bot Hosting`.

7. Enter `1` to select `Bot Hosting`.

## Setting up the discord.js package
1. Navigate to the Filemanager

2. Create a new file called `package.json` (if it doesn't already exists) and enter the following:

```json
{
  "main": "bot.js",  // Set this to the main file of your bot
  "scripts": {
    "start": "node bot.js"  // Set this to the main file of your bot
  },
  "dependencies": {
    "discord.js": "^14.14.1",
    "dotenv": "^16.3.1",
    "ms": "^2.1.3"
  },
  "engines": {
    "node": ">=18.0.0"
  }
}
```

3. create a new file called `.env` and enter the following:
´´´
# discord bot token - DO NOT SHARE WITH ANYONE
TOKEN=Your-discord-bot-token-here
´´´
    {: .warning}
    > Do not share the bot token with anyone, even if they claim to be support, Your bottoken serves as a password for your bot, sharing it will give anyone full access to your bot (and the servers it is in).

    {: .info}
    > If you do not have a discord Aplication/bot set up yet then please read the instructions here.

4. Create or upload your bot.js file (sometimes reffered to as main.js or index.js), this file will contain the code that your bot must run at startup. more info and examples can be found [here](https://discordjs.guide/creating-your-bot/main-file.html#running-your-application)

5. Navigate back to the console and start the server.

6. Select `8` to install all the packages included in package.js

7. Wait for the server to restart and then enter `10` to `Run npm start`.

8. If asked, enter `nodejs24.1.0` to start the latest version of nodejs (at the time of writing).

    > you can skip this step by setting the `NodeJS version` in [the settings page](https://client.falixnodes.net/server/settings).

9. The server should now start your discord bot.