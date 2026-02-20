---
layout: post
title: "How To Set Up Schedules"
tags: Server
permalink: falix/dashboard/general/schedules
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
Schedules let you automate server tasks like backups, restarts, and console commands. You can run them on a timer, trigger them from server events, or execute them manually.

## Setting Your Timezone

Before creating schedules, set your timezone so all times display correctly:

1. Navigate to your server's **Schedules** page.
2. Click the timezone dropdown in the top right.
3. Search for and select your timezone.

{: .info}
> All schedule times are displayed in your selected timezone. The server stores everything in UTC internally.

## Creating a Schedule

1. Navigate to your server's **Schedules** page.
2. Click **Create Schedule**.
3. Enter a **name** for your schedule (e.g. "Daily Backup", "Hourly Restart").
4. Select a **schedule type**.

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

1. Select one or more weekdays (Sun–Sat).
2. Set the time using the time picker.

**Example cron:** `0 14 * * 1,3,5` (Mon, Wed, Fri at 2:00 PM)

{% endtab %}

{% tab type Monthly %}

Runs on a specific day of the month at a specific time.

1. Select the day of the month (1st–31st).
2. Set the time using the time picker.

**Example cron:** `0 14 15 * *` (15th of every month at 2:00 PM)

{% endtab %}

{% tab type Event %}

Triggered by server events instead of (or in addition to) a timer.

See the [Event Triggers](#event-triggers) section below for all available events.

You can optionally enable **"Also run on a time schedule"** to combine event triggers with a time-based backup schedule (interval, daily, weekly, or monthly).

{% endtab %}

{% tab type Manual %}

Only runs when you click the **Run Now** button or when triggered by a Git deployment.

No timer or event configuration needed.

{% endtab %}

{% endtabs %}

### Additional Options

- **Run When Offline** — allows the schedule to execute even when the server is stopped (premium only)
- **Advanced: Custom Cron** — expand Advanced Options to enter a raw cron expression (format: `minute hour day_of_month month day_of_week`)

A live **schedule preview** shows a human-readable description of when your schedule will run (e.g. "Runs every Monday, Wednesday, Friday at 3:00 PM").

5. Click **Create Schedule**.

## Adding Tasks

After creating a schedule, you'll be taken to the task page to add actions. Tasks run sequentially in the order they appear.

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
- Optionally set a label for the backup
- Backup limits are enforced — if you've reached your server's backup limit, the oldest unlocked backup is automatically deleted

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
Enable a warning command that runs before the server shuts down. Template variables:
- `{time}` — formatted countdown (e.g. "30 seconds")
- `{seconds}` — raw seconds value

**Built-in warning templates:**
- Minecraft: `say Server shutting down in {time}!`
- Tellraw: `tellraw @a {"text":"Shutting down in {time}!","color":"red"}`
- Essentials: `broadcast &c[Server] &fShutting down in {time}!`

{% endtab %}

{% tab tasks Delete Files %}

Delete specified files or folders from your server.

**Availability:** Premium only

**Configuration:**
- Enter file paths to delete, one per line
- Paths are relative to the server root
- Examples: `logs/`, `crash-reports/`, `*.log`

{: .warning}
> Dangerous paths like `/`, `*`, `**`, `..` are blocked to prevent accidental deletion of your entire server.

{% endtab %}

{% tab tasks Git Sync %}

Trigger a deployment from your linked Git repository.

**Availability:** Premium only

**Configuration:**
- No additional settings — uses your existing Git integration configuration (branch, sync paths, post-deploy action)
- A Git repository must be linked to your server

{% endtab %}

{% endtabs %}

### Task Options

Every task has these additional options:

| Option | Description |
|--------|-------------|
| Time offset | Delay before this task runs (0 seconds to 6 hours). Presets: 0s, 30s, 1m, 5m, 10m, 15m, 30m, 1h, 2h, 4h, 6h |
| Continue on failure | If enabled, the next task runs even if this one fails. Otherwise the schedule stops. |

### Reordering Tasks
Drag and drop tasks to change the execution order.

## Event Triggers

Event-based schedules trigger automatically when server conditions are met.

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
| Server idle | Triggers after no players for X minutes | Idle duration: 1–1440 minutes (default: 5) |

### Threshold Events

| Event | Description | Configuration |
|-------|-------------|---------------|
| CPU usage | Triggers when CPU crosses a threshold | Operator (>=, >, <=, <) + percentage (1–100%, default: 80%) |
| Memory usage | Triggers when memory crosses a threshold | Operator + percentage (default: 90%) |
| Disk usage | Triggers when disk crosses a threshold | Operator + percentage (default: 95%) |

### Integration Events

| Event | Description | Configuration |
|-------|-------------|---------------|
| Git deployment completed | Triggers when a Git deployment finishes | None |

### Event Trigger Options

- **Cooldown** — minimum seconds between triggers to prevent rapid re-triggering (default: 60 seconds, range: 0–86400)
- **Rate limit** — maximum 60 triggers per server per hour (hard limit)
- Threshold events include **hysteresis** to prevent flapping around the boundary

## Running a Schedule

{% tabs run %}

{% tab run Automatic %}

Time-based schedules run automatically according to their configured interval. The next run time is displayed on the schedule row.

Event-based schedules trigger automatically when the configured event occurs.

{% endtab %}

{% tab run Manual %}

Click the **Run Now** button (play icon) on any schedule to execute it immediately. All tasks in the schedule will run in order.

{: .warning}
> A schedule that is already running cannot be triggered again until it finishes.

{% endtab %}

{% endtabs %}

## Webhooks

Get notified when your schedules run by setting up webhooks:

1. Click the **webhook button** on a schedule row.
2. Click **Add Webhook**.
3. Enter the webhook URL (must be HTTPS) and select the type.
4. Select which events to notify on.
5. Save and optionally click **Test** to verify the webhook works.

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
- Click the **delete button** (trash icon) to remove a schedule and all its tasks.

## Viewing Logs

Click the **logs button** on a schedule to view execution history. Each log entry shows:

| Field | Description |
|-------|-------------|
| Event | What happened (started, completed, failed) |
| Status | Success, failed, or skipped |
| Action | Which task action ran |
| Execution time | How long it took |
| Error message | Details if the task failed |

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
