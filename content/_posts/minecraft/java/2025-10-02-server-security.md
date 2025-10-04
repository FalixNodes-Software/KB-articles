---
title: How To Secure Your Minecraft Java Server.
tags: General
permalink: /minecraft/java/general/server-security
description: Learn how to secure your server in 5 simple steps.
keywords:
    - keyword: Griefed
      matches: ["being", "help"]
    - keyword: Griefing
      matches: ["help"]   

    - keyword: hacked
      matches: ["being, help"]
    - keyword: hacking
      matches: ["help"]
author:
    - TWIXhunter
---

In this guide we will explain to you how to make your server even more secure to prevent it from being griefed, hacked and destroyed.

Every step is optional and can be skipped or ignored, however, the more layers of security you have the better so it is recommended to follow as much as them as possible.

If you have a vanilla server then I recommend you to install "PurPur" or "Paper(spigot)" in the versions page, you should then be able to follow the "Plugins" guides without requing any changes on your players sides.

## Step 1: Enable online-mode
Enabling online mode is a crucial part of securing your server, it should be enabled by default but it is great to double check

*What does Online-mode do?*
Online-mode requires all payers to have an active microsoft account and makes sure that everyone that joins your server is actually who they claim to be. Online-mode often gets disabled by server owners because there might be certain players on their server that do not have a legitimate (paid) minecraft account, disabling online-mode allows these players to join because it stops checking if the player that tries to join actually has an account and is who they claim to be.

*I have cracked Players on my server, what do I do*
If you have cracked players (players who did not buy a legitimate copy of the game) on your server and you are not willing to loose them then you are not able to enable online-mode, I encourage you to follow the "Add an authentication plugin." step below so you can make your server secure without having to enable online-mode.

### How to enable-online mode
1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select a server from your server list.

3. Navigate to the [Properties](https://client.falixnodes.net/server/properties) page (under the minecraft category).

4. Scroll down to find the "Online Mode" property (it should be under the "Security Settings" section).

5. Enable the toggle.

> if it is already enabled then you don't have to do anything, great work!

## Step 2: Add a whitelist
Adding a whitelist means that only players that you know are able to join this server, however, this is easily bypassable whenever your server is still in offline-mode but it is a great method to prevent bots flooding your server.

### How to enable the whitelist
1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select a server from your server list.

3. Navigate to the [Properties](https://client.falixnodes.net/server/properties) page (under the minecraft category).

4. Scroll down to find the "White List" property (it should be under the "Security Settings" section).

5. Enable the toggle.

6. Scroll up to the "Enforce Whitelist" property and enable it as well.

### How to manage my whitelist
There are a few basic command you will want to learn to manage your whitelist.

| Command                     	| description                                      	|
|-----------------------------	|--------------------------------------------------	|
| /whitelist add <player>     	| Adds the specified player to the whitelist.      	|
| /whitelist remove <player>  	| Removes the specified player from the whitelist. 	|
| /whitelist list             	| List all players on the whitelist.               	|
| /whitelist on               	| Enables the whitelist.                           	|
| /whitelist off              	| Disables the whitelist.                          	|

You can also add and remove players from the whitelist by pressing their username in the console (when it appears blue) and using the "+ whitelist" and "Unwhitelist" buttons.

## Step 3: Add an authentication plugin.
authmereloaded is a plugin that requires everyone to set a password when they first join the server and give it again every time they join from a new device. This makes sure that everyone is who they actually claim to be without requiring a microsoft account.

> This step is only useful for servers that do not have "online-mode" enabled. if you have it enabled then you can just skip this step.


### How to install and configure authmereloaded
1. Make sure that you have a plugin loader (like Bukkit, Spigot, Paper or PurPur) installed, if you are not sure then you can just install it again in [the versions page](https://client.falixnodes.net/server/versions).

2. Add the [authmereloaded](https://modrinth.com/plugin/authmereloaded) plugin to your server, more information about the installment process of plugins can be found [here](https://kb.falixnodes.net/minecraft/modifications/general/adding-plugins).

3. Restart the server.

4. Open the File Manager and navigate to the [/plugins/authme/config.yml file (click me)](https://client.falixnodes.net/server/edit?path=%2Fplugins%2FAuthMe%2Fconfig.yml&mime=text%2Fplain).

5. Scroll down to the "enabled" option at Line 107 and set it to `true`.

6. Scroll down to the Timeout setting at line 110 and set it to the desired number, the higher the less likely it is for people to have to login again when on the same device as before.

the default is `10` (minutes), you are able to set it to whatever value you want (like `60` for 1 hour or `1440` for a complete day)

7. Scroll down to the `maxRegPerIp` option at line 145, this option restricts how many people can join from 1 wifi network, this is great to prevent alting but might be triggered when multiple players are playing together in the same location (like family members), I personally like to set this to `3` but that's up to you, setting it to 0 disables the feature.

8. Save the file and go back to the server console.

9. Restart the server

## Step 4: Add anti-grief plugins.
This step is useful for all servers, even just when playing with friends.
Coreprotect registers who placed/broke what block and who took what out of the chests (etc).

{: .warning}
> Coreportect is not able to recover damage done before it got added as a plugin

### How to install coreprotect.
1. Make sure that you have a plugin loader (like Bukkit, Spigot, Paper or PurPur) installed, if you are not sure then you can just install it again in [the versions page](https://client.falixnodes.net/server/versions).

2. Add the [Coreprotect](https://modrinth.com/plugin/coreprotect) plugin to your server, more information about the installment process of plugins can be found [here](https://kb.falixnodes.net/minecraft/modifications/general/adding-plugins).

3. Restart the server.

### How to use Coreprotect

**Checking who did something**
You can check for actions like a block being placed or broken, items being put into or picked out of a chest, etc.. by running the `/co inspect` command, this will enable the inspector mode, trying to break a block shows everything that happened in that position.

**Rolling back damage**
You can rollback changes using the `/co rollback` command, there are a few extra arguments you have to add:

| argument   	| description                                          	| Special notes                                                                                       	|
|------------	|------------------------------------------------------	|-----------------------------------------------------------------------------------------------------	|
| u:<user>   	| specifies the user who's actions you want to resore  	| use a , between names to specifie multiple users, use # (like #tnt) to specify netural events.      	|
| t:<time>   	| specifies the time you want to roll back             	| valid options look like: 2w (2 weeks), 5d (5days), 7h (7 hours) 2m (2minutes) and 10s (10 seconds). 	|
| r:<radius> 	| The radius (in blocks) of the area you want to edit. 	| Use #global to rollback the entire server, use #worldname to rollback a specific world.             	|

For example:
`/co rollback u:TestUser r:10 t:1h`
Rolls all the actions TestUser did in a radius of 10 blocks back to how they were 1h ago.

`/co rollback r:#global t:1d`
rolls the entire server back to how it was 1 day ago.

## Step 5: Take regular backups
taking regular backups (for example weekly, twice-a-week or even daily) allows you to recover your server when everything else fails, taking backups regularly allows you to always have a restore point without having to go back too far into the past.

### How to take a backup
1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select a server from your server list.

3. Navigate to the [Backups](https://client.falixnodes.net/server/backups) page.

4. Click on the "+ New Backup" button in the top-right corner.

5. Enter a name (optional).

6. Click the "+ Create Backup" button.

### How to delete old backups
1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select a server from your server list.

3. Navigate to the [Backups](https://client.falixnodes.net/server/backups) page.

4. Scroll to the desired backup and press "delete".

### How to automate backups
1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select a server from your server list.

3. Navigate to the [Schedules](https://client.falixnodes.net/server/schedules) page (under the Server Settings category).

4. Select your timezone in the dropdown.

5. Press the "+ New schedule" button.

6. Give your backup a clear name (eg. Daily Backup).

7. Select the Time you want to run the schedule at (eg. Daily at 12PM, Weekly on sunday at 9PM, every 48 hours).

8. Click the "Create schedule" button

9. Click on the "Tasks" button.

10. Add your first task by pressing the "New Task" button.

11. Select command and enter "save-all"

12. Click the "Create Task" button.

13. Create another task.

14. Select the "Backup" Option.

15. Select a 30 seconds Execution delay to make sure that the save-all command finishes in time.

16. Click the "Create Task" button.
