---
layout: post
title: "Viewing & Sharing Server Logs"
tags: Monitoring
permalink: falix/dashboard/monitoring/server-logs
description: "View, filter, analyze, download, and share your server log files."
keywords:
    - keyword: logs
      matches: ["view", "server", "error", "crash", "debug"]
    - keyword: crash
      matches: ["report", "log", "error", "fix"]
    - keyword: error
      matches: ["log", "fix", "debug", "analyze"]
    - keyword: analyze
      matches: ["logs", "issues", "problems", "scan"]
    - keyword: share
      matches: ["logs", "support", "link"]
author: Lily
---

## Introduction
When your server won't start, players are getting disconnected, or a plugin is misbehaving, your log files are the first place to look for answers. Logs record everything your server does — from routine startup messages to critical errors and crash details. They're also the single most useful thing you can share with support when you need help troubleshooting.

The **Logs** page on your dashboard gives you everything you need to view, filter, analyze, and share your server's log files without ever touching an SFTP client.

## Viewing Logs

To get started, head to your server's **Logs** page and pick a log file from the dropdown. The system automatically discovers log files from 14 common directories — including `/logs`, `/crash-reports`, `/minecraft/logs`, and more — so you don't have to hunt for them yourself.

If your server has a `latest.log` file (and it's not empty), it will be selected automatically since that's the one you'll check most often.

Once loaded, the log content appears with syntax highlighting, line numbers, and color-coded severity levels so you can quickly spot what matters.

### Log Display

Each log line is color-coded based on its severity level, making it easy to scan for problems at a glance:

| Severity | Color | Detected Keywords |
|----------|-------|-------------------|
| Error | Red | ERROR, SEVERE, FATAL, EXCEPTION, CRASH |
| Warning | Orange | WARN, WARNING |
| Info | Blue | INFO |
| Debug | Gray | DEBUG |

Timestamps, thread tags, and log level labels also get their own syntax highlighting, so the whole log is much easier to read than a raw text file.

### Crash Reports

If a crash report is detected in the log, the display automatically reformats it so it's actually readable. Crash headers show up in bold red, error descriptions are highlighted, stack traces appear in gray monospace, and section headers, mod lists, and system details each get their own distinct styling.

### Statistics Bar

At the top of the log content, you'll see a live statistics bar showing the total count of **Errors** (red), **Warnings** (orange), and **Lines** overall. This gives you an instant sense of how healthy (or unhealthy) your log looks before you start digging in.

{: .info}
> A high error count doesn't always mean something is seriously wrong — some plugins are just noisy. But if you see errors you don't recognize, it's worth investigating.

## Filtering

### Text Filter

Need to find something specific? Type in the filter input above the log content and the display will update in real-time to show only matching lines. This is great for searching for a specific plugin name, player, or error message. Click the **X** button to clear the filter when you're done.

### Advanced Filters

For more control, click **Advanced Filters** in the More Actions menu to open the full filter panel.

{% tabs filters %}

{% tab filters Log Levels %}

Toggle which severity levels you want to see (all are enabled by default):

- **Errors** — lines containing ERROR, SEVERE, FATAL, EXCEPTION, or CRASH
- **Warnings** — lines containing WARN or WARNING
- **Info** — lines containing INFO
- **Debug** — lines containing DEBUG

This is handy when you want to cut through the noise and focus only on errors and warnings, for example.

{% endtab %}

{% tab filters Log Types (Minecraft) %}

If you're running a Minecraft server, you can also filter by message type (all checked by default):

- **Chat** — player chat messages and [CHAT] tags
- **Commands** — server commands issued by players
- **Players** — join/leave events, advancements, kills, and UUID mentions
- **System** — all other server messages

These filters help you zero in on specific kinds of activity without wading through everything else.

{% endtab %}

{% tab filters Search Options %}

- **Use Regex** — treat the filter text as a regular expression for more powerful pattern matching
- **Match Case** — enable case-sensitive filtering when you need an exact match
- **Invert Results** — flip it around and show only lines that do NOT match the filter

{% endtab %}

{% endtabs %}

## Analyzing Logs

{: .info}
> Log analysis is only available for **Minecraft** servers.

One of the most helpful features on this page is the **Analyze** button. Instead of reading through hundreds of log lines yourself, click Analyze and let the system scan your logs against 200+ known issue categories. It will return results grouped by severity so you can tackle the most important problems first.

{: .info}
> When your server won't start and you're not sure why, the Analyze feature should be your go-to. It can instantly identify common blockers like an unaccepted EULA, wrong Java version, or corrupted server JAR — saving you a lot of guesswork.

### Severity Levels

| Level | Color | Examples |
|-------|-------|---------|
| Critical | Red | EULA not accepted, out of memory, corrupted JAR, port in use, wrong Java version, world corruption |
| High | Orange | Plugin failed to load, missing dependency, mod errors |
| Medium | Blue | Low memory warnings, TPS lag |
| Low | Gray | Minor warnings |

### Analysis Results

For each detected issue, you'll see a severity badge, a clear title, a description of the problem, and relevant details like affected plugins or mods, server version, TPS, memory usage, and affected worlds. The analyzer also shows the specific log lines that triggered the detection, recommended solutions, and how many times the issue occurred.

If nothing turns up, you'll get a green checkmark confirming your logs look clean — always a nice sight.

## Downloading Logs

Click **Download** to save the current log file to your computer. A modal will appear with a download URL — click **Download Directly** to open the file in a new tab, or click **Copy** to grab the URL for sharing.

{: .info}
> Downloads are rate limited to 10 per hour.

## Sharing Logs

Need to share your logs with support or a friend who's helping you troubleshoot? Click **Share** to create a public link for your log file. This is much easier (and more readable) than pasting log text into a chat message.

### Privacy Features

Before your log is shared, the system automatically redacts sensitive information so you don't accidentally leak anything personal:

| Data Type | Replacement |
|-----------|-------------|
| IPv4 addresses | `[REDACTED_IP]` |
| IPv6 addresses | `[REDACTED_IPV6]` |
| Auth tokens, passwords, API keys | `[REDACTED_AUTH_INFO]` |
| Email addresses | `[REDACTED_EMAIL]` |

### Creating a Share Link

1. Click **Share**.
2. Review the privacy features.
3. Click **Create Share Link**.
4. A progress bar will show the redaction and upload process.
5. Once it's done, copy the share URL or click **View** to open it.

### Share Link Details

| Setting | Value |
|---------|-------|
| Expiration | 7 days |
| Rate limit | 10 shares per hour |
| Max size | 10 MB |
| Access | Public via URL |

You can also optionally include metadata with your share like a support ticket ID, server name, server version, and timestamp — useful if you're working with support staff.

## Auto-Refresh

If you're actively watching your server's output (during startup, for example), open the **More Actions** menu and toggle **Auto-Refresh**. This reloads the log content every 10 seconds so you can follow along in near real-time. A visual indicator lets you know when auto-refresh is active.

## Supported Log Files

The system searches 14 directories and recognizes 40+ log file patterns, so it covers just about every server type out there:

| Category | Examples |
|----------|---------|
| Standard logs | `latest.log`, `debug.log`, `server.log` |
| Crash reports | `crash-YYYY-MM-DD-*.log`, `crash_*.txt` |
| JVM crash logs | `hs_err_pid*.log` |
| Mod loader logs | Forge, Fabric, Bukkit, Paper, Spigot logs |
| Rotated logs | `.log.1`, `.log.gz` (compressed) |
| Game-specific | Terraria, Valheim, ARK, Rust, CS:GO, TF2, GMod, and more |

Log files are sorted with `latest.log` first, then `server.log`, followed by crash reports, and compressed files last. Within each group, files are sorted by modification date with the newest first.
