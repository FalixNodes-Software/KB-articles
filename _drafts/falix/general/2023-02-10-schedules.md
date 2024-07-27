---
layout: help/article
title:  "Make Schedules for your Minecraft server commands - Falix"
categories: Falix
icon: <i class='fa-light fa-memo'></i></span>
tags: fxgeneral
permalink: /help/falix/general/schedules.*
gitURL: _posts/falix/general/2023-02-10-schedules.md
description: "Find out on how to make schedules for your Minecraft server in Falix"

author: Mocab
authorGitHub: mocab
---

{: .note#warning }
> This guide is currently outdated. The schedules feature has not yet been released for the new dashboard.

## A Guide to Using Schedules

## What are Schedules?

Schedules are used to run commands or functions at a specified date or time.

## What are Schedules Used for?

Schedules run certain tasks at a specified time or date. One example might be turning off a server after 4 hours or turning it on every day at 10 AM.

## What Functions Can Schedules Perform?

They can:

+ Run a power action
+ Create a backup
+ Run any command in the console

## Getting Started

## Step 1: Creating a Schedule

1. Log in to the [Game Panel](https://dev-panel.falixnodes.net), then choose a server.
2. Navigate to the "Schedules" tab at the top of the page.
3. Click on "Create Schedule", a popup should appear.
4. Give it a name, make sure it is clear and it explains what the schedule is for.
5. Use the information provided below to fill in the rest of the fields.

|Field Name         |Allowed Values     |Allowed special Characters                     |
|-------------------|-------------------|-----------------------------------------------|
|Minute             |0-59               | ,  -  *  /                                    |
|-------------------|-------------------|-----------------------------------------------|
|Hour               |0-23               | ,  -  *  /                                    |
|-------------------|-------------------|-----------------------------------------------|
|Day of the month   |1-31               | ,  -  *  /                                    |
|-------------------|-------------------|-----------------------------------------------|
|Month              |1-12 OR JAN-DEC    | ,  -  *  /                                    |
|-------------------|-------------------|-----------------------------------------------|
|Day of the Week    |1-7  OR SUN-SAT    | ,  -  *  /                                    |

**The table below explains what each special character means and what it is used for.**

|Character          |Purpose                                        |Example                                                           |
|-------------------|-----------------------------------------------|------------------------------------------------------------------|
| *                 |Specifies all possible values                  |Inserting * into the "Minute field" refers to every minute        |
|-------------------|-----------------------------------------------|------------------------------------------------------------------|
| -                 |Specifies a range of values                    |1-5 is equivalent to 1,2,3,4,5                                    |
|-------------------|-----------------------------------------------|------------------------------------------------------------------|
| ,                 |Specifies a list of values or multiple values  |1,3,4,6,9                                                         |
|-------------------|-----------------------------------------------|------------------------------------------------------------------|
| /                 |Skips a given number of values                 |*/3 in the minute time field is equivalent to 0,3,6,9,12,15,18,21... The asterisk (* ) specifies “every hour”, but the /3 means only the first, fourth, seventh. You can also use numbers instead of *         |

> + The names of months and days of the week are not case sensitive. MON is the same as mon.
> + You must use the `*` character in either the day-of-week or day-of-month fields. Specifying both fields in the same schedule is not supported.
> + Schedules do not support mixing `/` and `-` special characters in the same expression.

## Step 2: Assigning Tasks

1. Click on the schedule you just made.
2. Click on "New Task" at the top right of the page.
3. Click on "Actions", then select whichever action you want the schedule to perform (Refer to the sections below if you aren't sure which to use or how to use it).

### Send command

{: .note }
> You are unable to send the "restart" command.

To run a console command, use "Send Command". Any command that can run through the console can be used here!

"Time Offset" is the amount of time to wait after the previous task executes before running this one. If this is the first task on a schedule, this will not be applied.

"Payload" is where you will type in your commands. If you're using multiple commands, type each one on a separate line.

### Send power action

{: .note }
> Sending power actions is only available with our [Premium plan](https://falixnodes.net/minecraft-server-hosting).
"Send power action" either shuts down your server, restarts it, or terminates it.

"Time offset" is the amount of time to wait after the previous task executes before running this one. If this is the first task on a schedule, this will not be applied.

"Payload" is where you will select the action you want the schedule to perform.

{: .note }
> The "Start" and "Restart" power actions only work on premium servers.

### Create backup

"Create backup" creates a clone or copy of all your server files and stores them for you to use in the future.

"Time offset" is the amount of time to wait after the previous task executes before running this one. If this is the first task on a schedule, this will not be applied.

Under "Ignored Files", you can exclude any files or folders you do not want backed up. If you want the schedule to ignore multiple files, then type each file's path on a different line.
