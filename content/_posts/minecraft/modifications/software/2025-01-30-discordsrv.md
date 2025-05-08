---
title: Bridge Between Discord and Minecraft with DiscordSRV
tags: Software
permalink: minecraft/modifications/software/discordsrv
description: Interact and connect between your Discord and Minecraft servers.
keywords:
    - keyword: discordsrv
    - keyword: discord
      matches: ["minecraft", "chat", "console", "link"]
author:
    - Twixhunter
    - Mocab

icon: "https://cdn.modrinth.com/data/UmLGoGij/icon.png"
mod-name: DiscordSRV
mod-type: Plugin
mod-url: "https://modrinth.com/plugin/discordsrv"
---

## What is DiscordSRV

DiscordSRV is a plugin that allows players to interact between your Minecraft server and Discord through a Discord bot hosted on your Minecraft server. It has features such as:

-   An interactive chat between a Discord channel and the Minecraft server's chat.
-   Forward your Minecraft console to a Discord channel.
-   Send alerts based on specific events.
-   Require linked accounts or specific roles to play.

## Preparing the Discord Bot:

### Creating the Bot:

1. Log in to the [Discord Developer Portal](https://discord.com/developers/applications/).

2. Click on "New Application" and give the bot a name.

3. Make sure to agree to the [Developer Terms of Service](https://support-dev.discord.com/hc/en-us/articles/8562894815383-Discord-Developer-Terms-of-Service) and [Developer Policy](https://support-dev.discord.com/hc/en-us/articles/8563934450327-Discord-Developer-Policy) before clicking "Create".

4. Navigate to the "Installation" tab in the left menu.

5. Under "Installation Contexts" uncheck the "User Install" option.

6. Set the "Install Link" to "None".

7. Click on "**Save Changes**{: .green }" at the bottom of the page.

8. On the left, navigate to the "Bot" tab.

9. Under "Authorization Flow" toggle the "Public Bot" option to off.

10. Under the "Privileged Gateway Intents" section, enable "Server Members Intent" and "Message Content Intent".

### Adding to Your Server:

1.  Navigate back to the "General Information" tab and click on "**Copy**{: .blue }" under "Application ID".

2.  Copy the link below and paste it into your browser, make sure to replace `<application_id>` with the ID you copied.

    ```
    https://discord.com/oauth2/authorize?scope=bot+applications.commands&client_id=<application_id>
    ```

3.  From the dropdown menu, choose your Discord server and click on "**Authorise**{: .blue }".

4.  Give your bot the relevant permissions as explain in the [DiscordSRV guide](https://docs.discordsrv.com/installation/initial-setup/#advanced-information).

### Obtaining the Bot Token

1.  Navigate back to the "Bot" tab and below "Token" click on "**Reset Token**{: .blue }".

2.  Save the token as we will be needing it later on.

## Installation and Configuration:

### Prerequisites:

-   Ensure your server is running with Spigot or any of its forks (Paper, Purpur, etc).

### Installation:

We already have a guide on how to install DiscordSRV as well as any other plugin in our [Adding Plugins](/minecraft/modifications/general/adding-plugins) guide.

### Configuring the Plugin:

1. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

2. Locate and open the [Plugins](https://client.falixnodes.net/server/filemanager?dir=/plugins/) folder.

3. Find and open the [DiscordSRV](https://client.falixnodes.net/server/filemanager?dir=/plugins/DiscordSRV/) folder, this is where all its configuration files are stored.

4. Open "config.yml". This is the main configuration file.

5. Look for the property below and replace `BOTTOKEN` with your bot's token.

    ```
    BotToken: "BOTTOKEN"
    ```

6. Get the ID of the channel you want to connect to the Minecraft chat. A detailed guide by Discord on getting IDs can be found [here](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID).

7. Find and replace `000000000000000000` in the setting below with the channel ID you just copied.

    ```
    Channels: {"global": "000000000000000000"}
    ```

8. Generate a Discord server invite link without an expiry period if it is a public server.

9. Update the setting below to the new server invite. If your server is private leave it as is or change it to `""`.

    ```
    DiscordInviteLink: "https://discord.gg/changethisintheconfig.yml"
    ```

10. Click on "**Save File**{: .green }" to save your changes.

11. (Re)start your server to apply the changes.

### Additional Configuration:

#### Console Channel:

In many cases, you may want to give your admins access to the server console through Discord without needing a Falix account. That is where the console channel feature comes in. It sends all messages from the console to the specified channel, and any commands sent within the channel will be forwarded and run in the actual console.

1. In Discord, copy the ID of the channel you want to use as a console.

2. Navigate and open the main DiscordSRV configuration file.

3. Locate the setting below and set `000000000000000000` the console channel ID.

    ```
    DiscordConsoleChannelId: "000000000000000000"
    ```

4. Click on "**Save File**{: .green }" to save your changes.

5. (Re)start the server.

#### Link Discord To Join:

To safeguard against random and untrusted players joining your server it is advised to enable account linking. This is when a player joins the Minecraft server and is asked to send a code to the Discord bot. Upon sending the code your Discord account will be linked to the Minecraft account and you will gain permission to join the Minecraft server.

1. Once again navigate to the [DiscordSRV configuration Folder](https://client.falixnodes.net/server/filemanager?dir=/plugins/DiscordSRV/).

2. Click to open `linking.yml`.

3. Set `Enabled:` to `true`.

4. Click on "**Save File**{: .green }" to save your changes.

5. (Re)start the server.

#### Subscriber Role:

You may want to further secure the Minecraft server by allowing only Discord users with a specified role to join:

1. In Discord, copy the ID of the subscriber role.

2. In the DiscordSRV configuration folder, open `linking.yml` once more.

3. Set `Require subscriber role to join:` to `true`.\

4. Change the configuration below and set `00000000000000000` to the role ID you copied.

    ```
    Subscriber roles: ["00000000000000000"]
    ```

    > To add multiple roles add `, "00000000000000000"` after `"00000000000000000"`.
    > If you want to require all the listed roles enable `Require all of the listed roles:`.

5. Click on "**Save File**{: .green }" to save your changes.

6. (Re)start the server.
