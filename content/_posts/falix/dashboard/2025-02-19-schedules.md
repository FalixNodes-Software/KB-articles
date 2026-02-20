---
layout: post
title: "How To Set Up Schedules"
tags: Automation
permalink: falix/dashboard/automation/schedules
description: "Automate server tasks like backups, restarts, and commands with scheduled tasks."
keywords:
    - keyword: schedule
      matches: ["create", "setup", "automate", "cron", "task"]
    - keyword: automate
      matches: ["restart", "backup", "command", "task"]
    - keyword: cron
      matches: ["job", "schedule", "task", "expression"]
    - keyword: task
      matches: ["schedule", "automate", "add", "create"]
    - keyword: webhook
      matches: ["discord", "notification", "schedule"]
author: Lily
---

## Introduction
Ever forget to back up your world before a big update? Or wish your server would restart itself every night to stay fresh without you having to lift a finger? That's exactly what schedules are for. They let you automate the routine stuff -- backups, restarts, console commands, file cleanup -- so your server takes care of itself even while you're away. You can run tasks on a timer, fire them off when something happens on your server (like a crash or a player joining), or just trigger them manually whenever you need to.

## Setting Your Timezone

Before you create any schedules, take a moment to set your timezone so everything displays in times that actually make sense to you:

1. Navigate to your server's **Schedules** page.
2. Click the timezone dropdown in the top right.
3. Search for and select your timezone.

{: .info}
> All schedule times are displayed in your selected timezone. Behind the scenes, the server stores everything in UTC.

## Creating a Schedule

1. Navigate to your server's **Schedules** page.
2. Click **Create Schedule**.
3. Give your schedule a descriptive **name** -- something like "Daily Backup" or "Hourly Restart" so you can tell at a glance what it does.
4. Select a **schedule type** based on how often (or why) you want it to run.

### Schedule Types

{% tabs type %}

{% tab type Interval %}

Repeats every X minutes or hours.

**Quick presets:** 5 min, 15 min, 30 min, 1 hr, 2 hr, 6 hr, 12 hr

Or enter a custom value with a unit (minutes or hours).

**Example cron:** `*/30 * * * *` (every 30 minutes)

{% endtab %}

{% tab type Daily %}

Runs once per day at a specific time.

**Quick presets:** Midnight, 6 AM, Noon, 6 PM

Or set a custom time using the time picker.

**Example cron:** `0 14 * * *` (daily at 2:00 PM)

{% endtab %}

{% tab type Weekly %}

Runs on selected days of the week at a specific time.

1. Select one or more weekdays (Sun--Sat).
2. Set the time using the time picker.

**Example cron:** `0 14 * * 1,3,5` (Mon, Wed, Fri at 2:00 PM)

{% endtab %}

{% tab type Monthly %}

Runs on a specific day of the month at a specific time.

1. Select the day of the month (1st--31st).
2. Set the time using the time picker.

**Example cron:** `0 14 15 * *` (15th of every month at 2:00 PM)

{% endtab %}

{% tab type Event %}

Triggered by server events instead of (or in addition to) a timer.

See the [Event Triggers](#event-triggers) section below for all available events.

You can optionally enable **"Also run on a time schedule"** to combine event triggers with a time-based schedule (interval, daily, weekly, or monthly). This is great when you want a backup to run both every night and whenever the server crashes.

{% endtab %}

{% tab type Manual %}

Only runs when you click the **Run Now** button or when triggered by a Git deployment.

No timer or event configuration needed -- this is perfect for tasks you only want to run on demand.

{% endtab %}

{% endtabs %}

### Additional Options

- **Run When Offline** -- lets the schedule execute even when your server is stopped. This is a premium-only feature, and it's handy for things like Git syncs or file cleanup that don't need the server running.
- **Advanced: Custom Cron** -- expand Advanced Options to enter a raw cron expression if you're comfortable with that format: `minute hour day_of_month month day_of_week`.

A live **schedule preview** appears as you configure things, showing a plain-English description of when your schedule will fire (for example, "Runs every Monday, Wednesday, Friday at 3:00 PM"). It's a quick sanity check before you save.

5. Click **Create Schedule**.

## Adding Tasks

After creating a schedule, you'll land on the task page where you add the actual actions you want to happen. Tasks run one after another in the order you set them, so think of it like writing a to-do list for your server.

### Task Actions

{% tabs tasks %}

{% tab tasks Console Command %}

Send a command to the server console.

**Availability:** All plans

**Configuration:**
- Enter the command text in the input field

{% endtab %}

{% tab tasks Backup %}

Create a server backup.

**Availability:** All plans (free users limited to daily or less frequent schedules)

**Configuration:**
- No additional configuration needed -- a backup is created automatically when this task runs
- If you've reached your server's backup limit, the oldest unlocked backup is automatically deleted to make room

{: .info}
> A great starting point: set up a daily backup at 3 AM so your world is always protected, even if you forget to do it manually.

{% endtab %}

{% tab tasks Power Action %}

Start, restart, stop, or kill the server.

**Availability:** Premium only

**Options:**

| Action | Description |
|--------|-------------|
| Start | Start the server |
| Restart | Restart the server |
| Stop | Gracefully stop the server |
| Kill | Force stop the server process |

**Shutdown Warning (for stop and kill):**
You can enable a warning command that runs before the server shuts down, giving your players a heads-up. Use these template variables in your warning message:
- `{time}` -- formatted countdown (e.g. "30 seconds")
- `{seconds}` -- raw seconds value

**Built-in warning templates:**
- Minecraft: `say Server shutting down in {time}!`
- Tellraw: `tellraw @a {"text":"Shutting down in {time}!","color":"red"}`
- Essentials: `broadcast &c[Server] &fShutting down in {time}!`

{: .info}
> Use a shutdown warning template so your players aren't caught off-guard by restarts. Nobody likes getting kicked mid-build without notice.

{% endtab %}

{% tab tasks Delete Files %}

Delete specified files or folders from your server.

**Availability:** Premium only

**Configuration:**
- Enter file paths to delete, one per line
- Paths are relative to the server root
- Examples: `logs/`, `crash-reports/`, `*.log`

{: .warning}
> Dangerous paths like `/`, `*`, `**`, and `..` are blocked to prevent accidental deletion of your entire server.

{% endtab %}

{% tab tasks Git Sync %}

Trigger a deployment from your linked Git repository.

**Availability:** Premium only

**Configuration:**
- No additional settings needed -- it uses your existing Git integration configuration (branch, sync paths, post-deploy action)
- A Git repository must already be linked to your server

{% endtab %}

{% endtabs %}

### Task Options

Every task has an extra setting you can tweak:

- **Time offset** -- adds a delay before this task runs, anywhere from 0 seconds up to 6 hours. Presets are available (0s, 30s, 1m, 5m, 10m, 15m, 30m, 1h, 2h, 4h, 6h), or you can enter a custom value. This is useful when you want to stagger actions -- for example, sending a warning message and then waiting 30 seconds before actually stopping the server.

### Reordering Tasks
You can drag and drop tasks to change the order they run in. Since tasks execute sequentially, the order matters -- put your warning messages before your restarts, and your save commands before your backups.

## Event Triggers

Event-based schedules fire automatically when certain conditions are met on your server. This is a premium feature and it's incredibly useful for things like running a backup whenever the server crashes, or shutting down when the server goes idle.

### Server Events

| Event | Description | Configuration |
|-------|-------------|---------------|
| Server started | Triggers when the server starts | None |
| Server stopped | Triggers when the server stops | None |
| Server crashed | Triggers when the server crashes | None |
| Backup completed | Triggers when a backup finishes | None |

### Player Events

| Event | Description | Configuration |
|-------|-------------|---------------|
| Player joined | Triggers when a player joins | None |
| Player left | Triggers when a player leaves | None |
| Server idle | Triggers after no players for X minutes | Idle duration: 1--1440 minutes (default: 5) |

### Threshold Events

| Event | Description | Configuration |
|-------|-------------|---------------|
| CPU usage | Triggers when CPU crosses a threshold | Operator (>=, >, <=, <) + percentage (1--100%, default: 80%) |
| Memory usage | Triggers when memory crosses a threshold | Operator + percentage (default: 90%) |
| Disk usage | Triggers when disk crosses a threshold | Operator + percentage (default: 95%) |

### Integration Events

| Event | Description | Configuration |
|-------|-------------|---------------|
| Git deployment completed | Triggers when a Git deployment finishes | None |

### Event Trigger Options

- **Cooldown** -- the minimum number of seconds between triggers, preventing the same event from firing over and over in rapid succession. The default is 60 seconds, and you can set it anywhere from 0 to 86,400 (a full day).
- **Rate limit** -- there's a hard cap of 60 triggers per server per hour, so even a misconfigured schedule can't run away on you.
- Threshold events include **hysteresis** to prevent flapping -- this means the value has to move meaningfully past the boundary before it can trigger again, so you won't get spammed with notifications when CPU usage hovers right around 80%.

## Running a Schedule

{% tabs run %}

{% tab run Automatic %}

Time-based schedules run automatically according to their configured interval. You can see when each schedule will next run on the schedule row.

Event-based schedules trigger automatically whenever the configured event occurs.

{% endtab %}

{% tab run Manual %}

Click the **Run Now** button (play icon) on any schedule to execute it immediately. All tasks in the schedule will run in order.

{: .warning}
> A schedule that is already running cannot be triggered again until it finishes.

{% endtab %}

{% endtabs %}

## Webhooks

Want to know when your schedules actually run? Webhooks let you get real-time notifications -- sent straight to a Discord channel or to any external tool you use.

1. Click the **webhook button** on a schedule row.
2. Click **Add Webhook**.
3. Enter the webhook URL (must be HTTPS) and select the type.
4. Choose which events you want to be notified about.
5. Save, and optionally click **Test** to verify the webhook is working.

### Webhook Types

{% tabs webhook %}

{% tab webhook Discord %}

Sends color-coded embeds to a Discord channel. Paste your Discord channel webhook URL.

**Embed colors:**

| Event | Color |
|-------|-------|
| Schedule started | Blue |
| Task completed | Green |
| Task failed | Red |
| Schedule completed | Green |

**Embed fields included per event:**

| Event | Fields |
|-------|--------|
| Schedule started | Server name, Schedule name, Task count |
| Task completed | Server name, Schedule name, Task action, Step number, Command/Details |
| Task failed | Server name, Schedule name, Task action, Step number, Command/Details, Error message |
| Schedule completed | Server name, Schedule name, Total tasks completed, Duration |

{% endtab %}

{% tab webhook Generic %}

Sends a JSON POST request with `Content-Type: application/json`. Useful for integrating with external automation tools or custom scripts.

**Payload format:**

```json
{
  "event": "schedule_started",
  "timestamp": "2025-02-19T14:30:00+00:00",
  "data": {
    "server_name": "My Server",
    "schedule_name": "Daily Backup",
    "task_count": 3
  }
}
```

**Data fields per event:**

| Event | Data Fields |
|-------|------------|
| `schedule_started` | `server_name`, `schedule_name`, `task_count` |
| `task_completed` | `server_name`, `schedule_name`, `task_action`, `task_sequence`, `task_payload` |
| `task_failed` | `server_name`, `schedule_name`, `task_action`, `task_sequence`, `task_payload`, `error_message` |
| `schedule_completed` | `server_name`, `schedule_name`, `total_tasks`, `duration` (in seconds) |

{% endtab %}

{% endtabs %}

### Webhook Events

| Event | Description |
|-------|-------------|
| Schedule started | Fires when the schedule begins execution |
| Task completed | Fires after each individual task finishes successfully |
| Task failed | Fires when a task fails |
| Schedule completed | Fires when all tasks in the schedule are done |

{: .info}
> Webhook URLs must be HTTPS. Private/internal IPs and localhost URLs are blocked for security.

## Editing and Deleting

- Click the **edit button** (pencil icon) on a schedule to modify its name, timing, or settings.
- Click the **delete button** (trash icon) to remove a schedule along with all its tasks. This can't be undone, so make sure you really don't need it anymore.

## Viewing Logs

Click the **logs button** on a schedule to see its execution history. This is the first place to look when something isn't working the way you expect. Each log entry shows:

- **Event** -- what happened (started, completed, or failed)
- **Status** -- whether it succeeded, failed, or was skipped
- **Action** -- which task action ran
- **Execution time** -- how long it took
- **Error message** -- details about what went wrong, if the task failed

## Free vs Premium

| Feature | Free | Premium |
|---------|------|---------|
| Console command tasks | Yes | Yes |
| Backup tasks | Daily or less frequent | Hourly or less frequent |
| Power action tasks | No | Yes |
| Delete files tasks | No | Yes |
| Git sync tasks | No | Yes |
| Run when offline | No | Yes |
| Event-based triggers | No | Yes |
| Time-based schedules | Yes | Yes |
| Webhooks | Yes | Yes |
