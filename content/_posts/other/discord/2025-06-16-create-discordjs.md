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

3. Enter a name and domain for your server.

4. Select `Custom Game Server` from the `Select Your Game` dropdown menu.

5. Choose the desired resources and location and accept the EULA.

5. Create the server and open the console.

6. Start the server and enter 5 to select 'Discord Bot Hosting'.

7. Enter 1 to select 'Bot Hosting'.

## Setting up the discord.js package

1. Navigate to the File Manager.

2. Create a new file called 'package.json' (if it doesn't already exist) and enter the following:

```json
{
  "main": "bot.js",  // Set this to the main file of your bot (like bot.js, main.js or index.js).
  "scripts": {
    "start": "node bot.js"  // Set this to the main file of your bot (like bot.js, main.js or index.js).
  },
  "dependencies": {
    "discord.js": "^14.14.1", //some older bots might be build for older versions of discordjs, double check it before you proceed!
    "ms": "^2.1.3"
// add more dependencies here if needed, install them using the "Install NodeJS packages from package.json" option in the console.
  },
  "engines": {
    "node": ">=18.0.0"
  }
}
```

3. Upload or create your `bot.js file`. This is the main file that your bot runs at startup. Depending on your setup, it may also be named `main.js` or `index.js` (make sure that it matches the name set in `package.json`). You can find examples and more information [here](https://discordjs.guide/creating-your-bot/main-file.html#running-your-application).

4. Navigate back to the console and start the server.

5. Select `8` to install all the packages included in package.json.

6. Wait for the server to restart.

7. Navigate to the server settings page.

8. Find the "Main bot file" option and set it to the name of your main bot file (this file will be ran at startup)

9. Find the "NodeJS version" option and set it to the version of nodeJS required for your bot (most bots will be compatible with the latest version (nodejs24.1.0, at the time of writing) but doubble check it to be sure)

10. Navigate back to the console and start the server.

11. Select `1` to run the file set in the settings.

> More information about creating a custom discord.js bot can be found [here](https://discordjs.guide/creating-your-bot/).
