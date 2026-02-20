---
layout: post
title: "Viewing Your Activity Log"
category: Account
tags: Profile
permalink: falix/account/profile/activity-log
description: "Review a history of actions performed on your account."
keywords:
    - keyword: activity
      matches: ["log", "history", "actions", "recent"]
    - keyword: account
      matches: ["history", "log", "actions"]
author: Lily
---

## Introduction
The activity log records actions performed on your account, giving you a timeline of changes and events. This is useful for reviewing your account history and spotting any unauthorized activity.

## Viewing Your Activity Log

1. Navigate to [Activity](https://client.falixnodes.net/profile/activity).
2. Your recent account activity is displayed in chronological order.

## Logged Actions

The activity log tracks both account-level and server-level events.

{% tabs actions %}

{% tab actions Account %}

| Action | Description |
|--------|-------------|
| Login | Logged in (password, Google, Discord, or SSO) |
| Register | Account created (password, Google, or Discord) |
| Password changed | Password updated. All other devices logged out. |
| Password set | Password set for the first time (OAuth-only accounts). |
| Email changed | Email address updated. Verification required. |
| Username changed | Username changed (shows old and new). |
| Git connected | Connected a GitHub or GitLab account. |
| Git disconnected | Disconnected a GitHub or GitLab account. |
| Deletion requested | Account deletion request submitted (14-day cooldown). |
| Deletion cancelled | Deletion cancelled by logging back in. |

{% endtab %}

{% tab actions Server General %}

| Action | Description |
|--------|-------------|
| Server created | A new server was created. |
| Server cloned | A server was cloned from an existing one. |
| Server imported | A server was imported. |
| Server deleted | A server was deleted. |
| Server reinstalled | Server was reinstalled from scratch. |
| Force sync | Server state forcefully synced with the panel. |
| Resource change | CPU, RAM, or disk allocation changed. |
| Server renamed | Server name updated. |
| Server transferred | Server moved to a different node/location. |
| Server migrated | Server migrated between nodes. |
| Inactivity | Server transferred to storage due to inactivity. |
| Application switch | Server game type changed. |
| Docker image changed | Server Docker image updated. |
| EULA accepted | Minecraft EULA was accepted. |
| Startup variable changed | A server startup variable was modified. |
| Java version changed | Server Java version updated. |
| Terraria version changed | Terraria server version was updated. |

{% endtab %}

{% tab actions Server Power %}

| Action | Description |
|--------|-------------|
| Start | Server started. |
| Stop | Server stopped. |
| Restart | Server restarted. |
| Kill | Server process forcefully killed. |
| Console command | A command was sent to the server console. |
| Console viewed | Server console was accessed. |

{% endtab %}

{% tab actions Server Settings %}

| Action | Description |
|--------|-------------|
| Version change | Server software/version changed (Paper, Forge, Bedrock, etc.). |
| Max players changed | Maximum player count updated. |
| Timezone updated | Server timezone changed. |
| Description updated | Server description changed. |
| Server icon changed | Server icon updated. |
| Stop command changed | Custom stop command set. |
| Startup command changed | Custom startup command set. |
| Done message changed | Server "done" detection message updated. |
| Crash config updated | Crash detection settings changed. |
| Properties saved | server.properties file saved. |
| Config saved | A server config file was saved. |

{% endtab %}

{% tab actions Files & SFTP %}

| Action | Description |
|--------|-------------|
| File uploaded | A file was uploaded via file manager. |
| File renamed | A file was renamed. |
| File downloaded | A file was downloaded. |
| File deleted | A file was deleted. |
| File copied | A file was copied. |
| File moved | A file was moved. |
| File permissions changed | File chmod permissions updated. |
| File permissions fixed | File permissions were auto-fixed. |
| File pinned | A file was pinned for quick access. |
| File unpinned | A file was unpinned. |
| Region file edited | A Minecraft region file was modified. |
| Folder created | A new folder was created. |
| File transferred | A file was transferred to another server. |
| File received | A file was received from another server. |
| Folder transferred | A folder was transferred to another server. |
| Folder received | A folder was received from another server. |
| File archived | Files were compressed into an archive. |
| File unarchived | An archive was extracted. |
| Selective extract | Specific files extracted from an archive. |
| Archive downloaded | An archive was downloaded. |
| Logs shared | Server logs shared (with expiration). |
| SFTP file created | A file was created via SFTP. |
| SFTP file written | A file was modified via SFTP. |
| SFTP file renamed | A file was renamed via SFTP. |
| SFTP file deleted | A file was deleted via SFTP. |
| SFTP directory created | A directory was created via SFTP. |

{% endtab %}

{% tab actions Backups %}

| Action | Description |
|--------|-------------|
| Backup created | A new backup was created. |
| Backup deleted | A backup was deleted. |
| Backup restored | A full backup was restored. |
| Backup quick restored | A backup was quick-restored. |
| Selective restore | Specific files restored from a backup. |
| Backup downloaded | A backup was downloaded. |
| Backup locked | A backup was locked (protected from deletion). |
| Backup unlocked | A backup was unlocked. |
| Backup transferred | A backup was transferred to another server. |
| Backup received | A backup was received from another server. |

{% endtab %}

{% tab actions Networking %}

| Action | Description |
|--------|-------------|
| Primary port changed | Primary allocation port switched. |
| Allocation created | A new port allocation was added. |
| Allocation deleted | A port allocation was removed. |
| Allocation note | A note was added to an allocation. |
| Subdomain created | A subdomain was created. |
| Subdomain deleted | A subdomain was deleted. |
| Subdomain edited | A subdomain was modified. |
| Subdomain set as primary | A subdomain was set as the primary. |
| Domain added | A custom domain was added. |
| Domain deleted | A custom domain was removed. |
| Firewall rule added | A firewall rule was created. |
| Firewall rule updated | A firewall rule was modified. |
| Firewall rule deleted | A firewall rule was removed. |
| Firewall toggled | Firewall enabled or disabled. |
| Firewall synced | Firewall rules synced to server. |
| Internal network enabled | Internal networking was enabled. |
| Internal network disabled | Internal networking was disabled. |
| Internal only mode | Server set to internal network only. |
| Proxy created | A proxy was created. |
| Proxy updated | A proxy was modified. |
| Proxy deleted | A proxy was removed. |

{% endtab %}

{% tab actions Databases %}

| Action | Description |
|--------|-------------|
| Database created | A MySQL database was created. |
| Database deleted | A database was deleted. |
| Database password rotated | A database password was regenerated. |
| phpMyAdmin token | A phpMyAdmin access token was generated. |

{% endtab %}

{% tab actions Subusers %}

| Action | Description |
|--------|-------------|
| Subuser added | A sub-user was added to a server. |
| Subuser updated | Sub-user permissions were changed. |
| Subuser removed | A sub-user was removed from a server. |
| Premium subuser | Server marked as premium (subuser benefit sharing). |
| Premium subuser removed | Premium subuser marking removed. |

{% endtab %}

{% tab actions Schedules %}

| Action | Description |
|--------|-------------|
| Schedule created | A scheduled task was created. |
| Schedule updated | A scheduled task was modified. |
| Schedule deleted | A scheduled task was deleted. |
| Schedule executed | A scheduled task was manually triggered. |
| Schedule timezone changed | Schedule timezone was updated. |
| Task created | A task was added to a schedule. |
| Task updated | A schedule task was modified. |
| Task deleted | A schedule task was removed. |
| Task reordered | Schedule tasks were reordered. |
| Trigger created | A schedule trigger was added. |
| Trigger updated | A schedule trigger was modified. |
| Trigger deleted | A schedule trigger was removed. |
| Webhook created | A schedule webhook was added. |
| Webhook deleted | A schedule webhook was removed. |

{% endtab %}

{% tab actions Plugins & Mods %}

| Action | Description |
|--------|-------------|
| Plugin installed | A plugin was installed. |
| Addon installed | An addon was installed. |
| Addon toggled | An addon was enabled or disabled. |
| Modpack installed | A modpack was installed. |

{% endtab %}

{% tab actions Worlds %}

| Action | Description |
|--------|-------------|
| World installed | A world was uploaded/installed. |
| World downloaded | A world was downloaded. |
| World archive downloaded | A world was downloaded as an archive. |
| World config changed | World settings were modified. |
| World NBT edited | World NBT data was modified. |
| World set as primary | A world was set as the primary world. |

{% endtab %}

{% tab actions Git %}

| Action | Description |
|--------|-------------|
| Repo linked | A Git repository was linked to a server. |
| Repo unlinked | A Git repository was unlinked from a server. |
| Deploy triggered | A Git deployment was triggered. |
| Settings changed | Git integration settings were updated. |

{% endtab %}

{% tab actions Players %}

| Action | Description |
|--------|-------------|
| Player command | A player management command was executed. |
| Player files accessed | Player data files were accessed. |
| Player inventory viewed | A player's inventory was viewed. |
| Player NBT edited | Player NBT data was modified. |

{% endtab %}

{% endtabs %}

## Archived Logs

Activity older than 1 year is moved to an archive. You can switch between **Recent** and **Archived** views on the activity page.

## Suspicious Activity

If you notice actions you didn't perform:
1. [Change your password](falix/account/general/change-email-password) immediately.
2. [Review your active sessions](falix/account/general/sessions) and terminate any you don't recognize.
3. [Enable 2FA](falix/account/general/add-2fa) if you haven't already.
