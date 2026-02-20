---
layout: post
title: "Viewing Shared Logs"
tags: Monitoring
permalink: falix/dashboard/monitoring/shared-logs
description: "How shared log links work and what you can do with them."
keywords:
    - keyword: shared logs
      matches: ["view", "link", "support", "share"]
    - keyword: share
      matches: ["logs", "link", "support", "troubleshoot"]
    - keyword: log link
      matches: ["shared", "view", "open", "support"]
author: Lily
---

## Introduction
Sometimes a friend sends you a link and says "my server keeps crashing, can you take a look?" Other times, a support agent shares a log with you so you can see exactly what went wrong. Either way, when someone [shares a server log](falix/dashboard/monitoring/server-logs), a public link is created that anyone with the URL can open -- no login required.

Shared log URLs follow this format: `https://client.falixnodes.net/shared-logs/<id>`

This article walks you through everything you will see when you open one of those links and how to make the most of the tools available to you.

## What You See

### Header

At the top of the page, you will find the key details about the log you are viewing. The **title** tells you which log file was shared (for example, `latest.log`). Next to that, you will see when the log was **shared** and when the link **expires** -- both of these are automatically converted to your local timezone so there is no guesswork. If the log was attached to a support ticket, you will also see the **Support ID** displayed here so you can cross-reference it.

### Statistics Bar

Just below the header, three counters give you a quick snapshot of the log's health. **Errors** counts every line that contains ERROR, EXCEPTION, FATAL, or SEVERE. **Warnings** counts lines with WARN or WARNING. And **Lines** simply tells you how many total lines are in the log. These counters update in real-time as you filter, so they always reflect what you are currently looking at.

{: .info}
> If the error count is high, jump straight to the Log Analysis section further down -- it will usually tell you exactly what is going on without needing to read through the raw log yourself.

### Log Content

The log itself is displayed in a dark, monospace viewer that is easy on the eyes. Line numbers run down the left side, and syntax highlighting makes timestamps, thread names, and log levels stand out. Error lines are tinted red and warning lines are tinted orange, so problem areas practically jump off the screen. You will also notice some values highlighted in orange like `[REDACTED_IP]` or `[REDACTED_AUTH_INFO]` -- these are pieces of sensitive data that were automatically removed before sharing.

## Filtering

Need to find something specific? Type in the **Filter logs** input at the top of the log viewer to search in real-time. Only matching lines will be shown, and the statistics bar updates to reflect the filtered results.

{: .info}
> Press **Ctrl+F** (or **Cmd+F** on Mac) to jump straight to the filter input instead of triggering the browser's built-in search. This is especially handy when you are looking for a specific plugin name or error message.

To clear your filter and get back to the full log, just click the **X** button.

## Log Analysis

Here is where things get really useful. Shared logs from Minecraft servers are automatically analyzed for known issues, and the results appear in a dedicated section below the log content. If someone sends you their log asking for help, this is the first place you should look -- it does most of the detective work for you.

### What It Detects

The analyzer scans for over 200 issue categories across four severity levels:

| Severity | Examples |
|----------|---------|
| **Critical** | EULA not accepted, out of memory, corrupted JAR, port in use, wrong Java version, world corruption, server crashes |
| **High** | Plugin/mod failed to load, missing dependencies |
| **Medium** | Low memory warnings, TPS lag |
| **Low** | Minor warnings |

### Issue Cards

Each detected issue is presented as a card that gives you everything you need to understand and fix the problem:

- **Severity badge** -- color-coded so you can triage at a glance (red for critical, orange for high, blue for medium, gray for low)
- **Title and description** of the problem in plain language
- **Details** -- affected plugins or mods, server version, TPS, memory usage, and affected worlds
- **Log examples** -- the actual lines that triggered the detection, complete with syntax highlighting so you can see exactly what happened
- **Solutions** -- recommended steps to fix the issue, which you can pass along to the server owner
- **Occurrence count** -- how many times the issue appeared, which helps you gauge how serious it is

If the analyzer does not find any issues, you will see a green checkmark confirming the log looks healthy. That is always a nice sight.

{: .warning}
> When helping someone troubleshoot, start with the critical and high severity cards. These are almost always the root cause, and the suggested solutions will get the server back online faster.

You can collapse or expand the entire analysis section using the **Show/Hide** button if you want to focus on the raw log instead.

## Expiration and Privacy

Shared logs are not permanent. By default, they expire **7 days** after creation, with a maximum lifespan of **30 days**. Once a log expires, it is automatically deleted from the database -- no one can access it after that.

{: .warning}
> If someone sends you a shared log link, do not wait too long to look at it. Once it expires, the link stops working and there is no way to recover it.

### What Gets Redacted

Before a log is ever shared, sensitive data is automatically detected and replaced to protect the server owner's privacy:

| Original | Replaced With |
|----------|--------------|
| IPv4 addresses | `[REDACTED_IP]` |
| IPv6 addresses | `[REDACTED_IPV6]` |
| Auth tokens, passwords, API keys | `[REDACTED_AUTH_INFO]` |
| Email addresses | `[REDACTED_EMAIL]` |

Redacted values are highlighted in orange in the viewer, so you can see exactly where data was removed without worrying about what was there.

### Access Control

Some shared logs may have restricted access. **User-restricted** logs only allow specific users to view them. If you try to open a log you do not have permission for, you will see a permission denied message. In that case, ask the person who shared it to adjust the access settings or share a new link that includes you.

## Discord and Social Embeds

When you paste a shared log link into Discord or any other platform that supports link previews, the embed gives you a quick summary without even clicking through. It shows the log title, the line count, error count, and warning count, along with when it was shared and which server software was running. The embed color also changes based on severity -- red if errors are present, orange if there are only warnings, and green if the log is healthy. This makes it easy to gauge the situation before you even open the link.

## Reporting Content

If you come across anything inappropriate or harmful in a shared log, there is a report link at the bottom of the page. Do not hesitate to use it -- it helps keep the platform safe for everyone.
