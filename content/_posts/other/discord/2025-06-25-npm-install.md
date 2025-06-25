---
layout: post
title: "How To install nodejs packages"
category: discordjs
tags: General
permalink: other/discord/general/npm-install
description: "Learn how to install nodejs packages on your server"
keywords:
    - keyword: discord.js
      matches: ["create", "host"]
author: TWIXhunter
---



1. Navigate to the File Manager and open the `package.json` file. It should look like the following example:

```json
{
  "main": "bot.js",  // Set this to the main file of your bot (like bot.js, main.js or index.js)
  "scripts": {
    "start": "node bot.js"  // Set this to the main file of your bot (like bot.js, main.js or index.js)
  },
  "dependencies": {
    "discord.js": "^14.14.1",
    "ms": "^2.1.3"
  },
  "engines": {
    "node": ">=18.0.0"
  }
}
```

2. Add the following entry inside the dependencies object:

```json
    "packagename": "^version.number.here"
```

3. Ensure each entry (except the last one) ends with a `,` to maintain valid JSON syntax.

4. Save the file and return to the console.

5. Start the server and select option `8` to install the Node.js packages.

6. Wait for the server to install or update all listed packages.
