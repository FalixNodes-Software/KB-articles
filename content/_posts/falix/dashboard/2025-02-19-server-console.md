---
layout: post
title: "Server Console"
tags: Monitoring
permalink: falix/dashboard/monitoring/server-console
description: "Control your server with the real-time console — send commands, monitor resources, view player activity, and manage power state."
keywords:
    - keyword: console
      matches: ["server", "terminal", "command", "output"]
    - keyword: command
      matches: ["send", "console", "type", "execute"]
    - keyword: start
      matches: ["server", "power", "online", "launch"]
    - keyword: stop
      matches: ["server", "power", "offline", "shut"]
    - keyword: restart
      matches: ["server", "power", "reboot"]
    - keyword: kill
      matches: ["server", "force", "stop", "power"]
    - keyword: resource
      matches: ["cpu", "ram", "disk", "usage"]
    - keyword: connect
      matches: ["server", "join", "address", "ip"]
author: Lily
---

## Introduction
If there is one page you will visit more than any other, it is the Console. This is your server's command center -- the place where you can watch logs roll in live, fire off commands, keep an eye on CPU and RAM, see who is online, and start or stop your server with a single click. Everything you need for day-to-day server management lives right here.

## Console Output

The console shows your server's log output in real time, so you always know exactly what is happening. To keep things fast, the console limits the display to roughly 500 messages at a time -- older messages are removed from the view as new ones come in.

### What Makes the Console Smart

The output is not just plain text. The console parses and enriches your logs in several useful ways:

- **Color-coded log levels** -- INFO shows in blue, WARN in yellow, ERROR in red, and DEBUG in purple. You can spot problems at a glance without reading every line.
- **ANSI color codes** are rendered properly, so plugins and mods that use colored output look the way their developers intended.
- **Timestamps are highlighted**, making it easy to correlate events with a specific moment.
- **Player names are clickable** -- click one to open a player card popup with their avatar and quick actions like kick, ban, or op.
- **IP addresses are censored by default** for privacy. Hover over one to reveal it, or click to copy it.
- **UUIDs** are highlighted in purple and clickable to copy.
- **URLs are detected and made clickable**. If a link points to an unknown domain, you will see a trust confirmation before being redirected.
- **Auto-scroll** keeps you pinned to the latest messages. If you scroll up to read older logs, auto-scroll pauses automatically and a "scroll to bottom" button appears so you can jump back down whenever you are ready.

### Console State Overlay

When the console has no messages to show, you will see a state overlay that tells you what is going on with your server and, when possible, gives you an action to take:

| State | What It Means | What You Can Do |
|-------|---------------|-----------------|
| **Offline** | Your server is not running | Click the Start button |
| **Starting** | Your server is booting up | Hang tight -- a spinner is shown |
| **Stopping** | Your server is shutting down | Wait for shutdown to finish |
| **No Software** | No server version is installed (Minecraft/Terraria) | Click Select Software to pick one |
| **Suspended** | Your server has been suspended | Follow the Renew Subscription link |
| **Installing** | The server egg is being installed | A spinner is shown while this completes |
| **Restoring Backup** | A backup restore is in progress | Wait for the restore to finish |
| **Install Failed** | Something went wrong during installation | Click Reinstall to try again |
| **Reinstall Failed** | Reinstallation hit an error | Click Reinstall to try again |

## Console Tabs

{: .info}
> Console tabs are only available for **Minecraft** and **Hytale** servers.

Instead of scrolling through thousands of log lines to find what you need, the console gives you filtered tabs that pull out specific message types:

- **Console** -- the full, unfiltered server output.
- **Chat** -- only player chat messages (Minecraft and Hytale). A badge shows how many chat messages have come in.
- **Players** -- a list of online and offline players (Hytale only). The badge shows the current player count.
- **Errors** -- only error-level log entries (Minecraft only). The badge tells you how many errors have occurred.
- **Warnings** -- only warning-level log entries (Minecraft only). Same idea -- the badge shows the count.

{: .success}
> The Errors and Warnings tabs are a great first place to look when something is not working right. You can see all the problems at a glance without wading through normal log output.

### Tab Controls

On the right side of the tab bar (Minecraft only), you will find a few handy controls:

- **Popup** -- opens the console in a separate popup window so you can monitor your server on a second screen. This is a **premium feature**.
- **Share** -- creates a shareable link of your console logs, perfect for asking for help.
- **View Mode** -- toggles between graph and simple resource views (more on this below).
- **Clear** -- when you are on the main Console tab, this clears all console messages. When you are on the Errors, Warnings, or Chat tab, it clears only that tab's filtered messages.
- **Export** -- appears on the Errors, Warnings, and Chat tabs, letting you download the filtered messages.

### Exporting Tab Messages

When you are viewing the Errors, Warnings, or Chat tab, an **Export** button appears alongside the Clear button. Clicking it downloads the filtered messages as a `.txt` file with a filename like `server-errors-{id}-{date}.txt`, `server-warnings-{id}-{date}.txt`, or `server-chat-{id}-{date}.txt` depending on the active tab. This is useful when you want to save a record of issues or share them with someone helping you troubleshoot.

### Players Panel

The Players tab (Hytale only) gives you a quick look at who is connected:

- **Online Players** -- currently connected players, shown with a green status dot.
- **Offline Players** -- players who were seen recently but are no longer online, shown with a gray dot.

Click any player name to open their player card popup.

## Command Input

At the bottom of the console, you will find the command input field. Type your command and press **Enter** (or click the send button) to execute it.

Here are a few things that make the command input especially handy:

- **Command history** -- your last 10 commands are saved. Use the **Up** and **Down** arrow keys to cycle through them, so you do not have to retype commands you use often.
- **Auto-slash removal** -- if you are running a Minecraft server and you type a leading `/`, it is automatically stripped before the command is sent. The server does not need the slash, so this saves you from a common mistake.
- **The `clear` command** -- typing `clear` wipes all console messages locally, giving you a fresh view without affecting the actual server.
- **Autocomplete** -- as you type, plugin commands are detected and suggested in a dropdown. Use the arrow keys to navigate suggestions and **Enter** to confirm your selection.

## Power Controls

The console header gives you quick access to your server's power state:

- **Start** -- boots your server when it is offline.
- **Restart** -- gracefully restarts a running server. Use this after making configuration changes that require a restart.
- **Stop** -- sends a graceful shutdown signal, giving your server time to save and clean up.
- **Kill** -- force-stops the server immediately. This replaces the Stop button once you have already clicked Stop, in case the graceful shutdown gets stuck.
- **Connect** -- opens the connection modal with your server address and instructions for joining.

{: .warning}
> Only use **Kill** if your server is not responding to a normal Stop. Force-stopping can occasionally cause data loss if the server has not finished saving.

For non-Minecraft servers, the Popup, Share, and View Mode controls are tucked under a dropdown menu (**...**) in the header instead of appearing in the tab bar.

### Startup Queue

If the node your server is on is at capacity, your server will be placed in a startup queue. When this happens, you will see a queue alert with:

- A message explaining that your server is waiting in line.
- An **Upgrade to Premium** button to skip the queue entirely.
- A **Watch Ad** button to bypass the queue on the free plan.

The system automatically retries starting your server every 60 seconds, for up to 30 attempts, so you do not need to keep clicking Start.

### Transfer Queue

If your server is being transferred to another node, you will see a transfer alert with a countdown timer. Console interaction is blocked during the transfer -- just wait for it to complete.

## Resource Monitoring

Below the console, three resource cards give you a real-time picture of how your server is performing. This is where you check if your server is running out of RAM, burning through CPU, or filling up disk space.

### Graph View (Default)

Each resource displays a live line chart that updates in real time with a 10-point rolling window:

- **CPU** (blue) -- shown as a percentage of your limit (e.g., 25% / 400%).
- **RAM** (green) -- shown in GB used vs. total (e.g., 1.5 GB / 8 GB).
- **Disk** (orange) -- shown in GB used vs. total (e.g., 45.2 GB / 100 GB), or an infinity symbol for unlimited plans.

{: .info}
> If you notice RAM usage climbing steadily over time without dropping, your server might have a memory leak from a plugin or mod. A restart can help in the short term, but you will want to investigate which addon is causing it.

### Simple View

Prefer something more compact? Toggle to simple view to see progress bars instead of charts. When combined view is enabled, server info cards appear alongside the resource bars in a single, compact layout.

### Mobile Resources

On mobile, you will see a compact resource card showing CPU, RAM, and Disk with inline progress bars and limits. Tap it to open a full resource modal with more detail.

## Server Information Sidebar

The right sidebar displays compact info cards that give you quick access to important server details. Here is what you will find:

- **Uptime** -- how long since your server last started. Hidden when the server is offline.
- **Address** -- your server's domain or IP:port. Click to copy it, or click the edit button to jump to the Subdomains page.
- **Port** -- your server's port number (only shown for non-Minecraft/non-Hytale servers). Click to copy.
- **CPU** -- the CPU model running your server. Premium users see it directly; free users see a prompt to upgrade.
- **Location** -- the physical location of your node, with a country flag. Click to open the transfer modal (premium) or see the upgrade prompt (free).
- **Server Version** -- your installed software and version (Minecraft only). Click to open the version changer. If no version is installed, this card pulses with a warning glow to get your attention.
- **Max Players** -- shows current / max player count (Minecraft only). Click to edit.
- **Modpack** -- the installed modpack name and version, if you have one. Click to go to the Modpacks page.
- **Server Type** -- your Terraria server variant (Terraria only). Click to change it.
- **Support Info** -- your server's UUID and support details. Click to view -- this is what support staff will ask for if you open a ticket.

### Editing Max Players

Want to change how many players can join at once?

1. Click the **Max Players** card in the sidebar.
2. Enter a value between 0 and 1000.
3. Click **Save Changes**.

{: .info}
> You will need to restart your server for the new max player count to take effect.

## Connection Modal

Click the **Connect** button to see exactly how players can join your server.

{% tabs connect %}

{% tab connect Minecraft %}

The Minecraft connection modal has **Java Edition** and **Bedrock Edition** tabs.

**Java Edition** shows:
1. Step-by-step instructions for adding the server to your Minecraft client.
2. Your domain address (click to copy).
3. Your direct IP:port (click to copy).

**Bedrock Edition** shows:
1. A Quick Join button that uses the `minecraft://` protocol to launch the game and add the server directly.
2. A share link you can send to friends so they can easily join.
3. Direct IP and Port fields (click to copy).

A **Verify DNS** button checks whether your domain is resolving correctly and reports success, warning, or error status. This is handy if players are having trouble connecting using your domain.

The connection modal also includes a **Remote Startup** section at the bottom, where you can create a public link that allows friends to start your server remotely even when you are not online.

{: .warning}
> If your server is Java-only, the Bedrock tab will show a warning suggesting you install Geyser to enable cross-play. If it is Bedrock-only, the Java tab shows a corresponding note.

{% endtab %}

{% tab connect Non-Minecraft %}

For non-Minecraft servers, the modal is simpler:

- Domain address with port (click to copy)
- Direct IP:port connection (click to copy)
- Separate IP and Port fields (click to copy) -- not shown for Hytale servers

{% endtab %}

{% endtabs %}

## Sharing Console Logs

When you need help troubleshooting, the **Share** button is your best friend. Click it to create a shareable link of your console logs. Here is what happens behind the scenes:

1. HTML formatting is stripped from the log output.
2. Sensitive information like IP addresses, auth tokens, and email addresses is automatically redacted.
3. A header with your server name is added for context.
4. A link is generated with a 7-day expiration.

Copy the resulting URL and share it with others -- in a support ticket, a Discord server, or wherever you need help.

{: .success}
> Because sensitive data is redacted automatically, you can share your logs without worrying about accidentally leaking private information.

## Popup Console

{: .info}
> The popup console is a **premium feature**.

Click the **Popup** button to open the console in a separate browser window. This is particularly useful if you have a second monitor -- you can keep the console visible while working in the file manager, editing configurations, or managing plugins on your main screen.

## Alerts and Notifications

The console displays alerts when something important needs your attention. Here is what you might see:

- **Connection Error** -- the WebSocket connection to your server failed. This usually resolves on its own, but check your internet connection if it persists.
- **Disk Full** -- your disk usage has exceeded 90%. Free up space before your server runs into problems.
- **Inactivity** -- your server has been moved to inactivity storage. You will need to bring it back before it can run.
- **RCON Warning** -- RCON is enabled, which is a security risk. You can dismiss this alert, and it includes a link to your server properties where you can disable RCON.
- **Auto-Update** -- your server was automatically updated. The alert shows both the old and new version so you know what changed.
- **Heavy Usage** -- sustained high resource usage has been detected. This appears on free plans with a prompt to upgrade.
- **Ad Blocker** -- an ad blocker was detected. Disabling it helps keep Falix free for everyone.
- **File Permissions** -- file permission issues were detected. If you imported a world, a quick fix option is available to correct the permissions automatically.

## Player Name Detection

The console automatically recognizes player names in your log output and makes them clickable. This works across several common log patterns:

- Chat messages: `<username> message`
- Join/leave events: `username joined the game`
- Commands: `username issued server command`
- IP connections: `username[/IP]` (the IP is censored for privacy)
- Operator changes: `Made username a server operator`
- Bans: `Banned username`
- Hytale-specific patterns

Clicking any detected player name opens a popup card showing their avatar, online status, and quick action buttons for copying their username, kicking, banning, or granting operator status.

## Keyboard Shortcuts

These shortcuts help you work faster without reaching for the mouse:

| Shortcut | What It Does |
|----------|--------------|
| **Enter** | Send the command you have typed |
| **Up/Down arrows** (in command input) | Cycle through your command history |
| **Up/Down arrows** (when autocomplete is open) | Navigate autocomplete suggestions |
| **Enter** (when autocomplete is open) | Confirm the selected autocomplete suggestion |
