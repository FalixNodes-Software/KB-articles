---
layout: post
title: "Reinstalling & Deleting a Server"
tags: Setup
permalink: falix/dashboard/setup/reinstall-delete-server
description: "How to reinstall your server's software or permanently delete a server."
keywords:
    - keyword: reinstall
      matches: ["server", "reset", "fresh", "clean"]
    - keyword: delete
      matches: ["server", "remove", "permanently"]
    - keyword: reset
      matches: ["server", "reinstall", "fresh", "clean"]
author: Lily
---

## Introduction
Sometimes things go sideways. Maybe your server's installation got corrupted after a bad update, your startup files aren't behaving the way they should, or you just want a completely fresh start. Other times, you might be done with a server entirely and want to free up a slot for something new.

That's where the **Danger Zone** tab on your server's **Settings** page comes in. Navigate to your server's **Settings**, then select the **Danger Zone** tab from the tabs at the top. It gives you two powerful options: reinstalling your server's software or permanently deleting the server altogether. Both of these actions are serious, so let's walk through exactly what each one does and when you'd want to use it.

{: .warning}
> Before doing either of these, always create a backup first. Both reinstalling (with file deletion) and deleting a server are irreversible, and there's no way to recover data that wasn't backed up.

## Should I Reinstall or Delete?

It helps to know which option fits your situation:

- **Reinstall** is the right choice when your server itself is fine, but the software installation is broken or misconfigured. It re-runs the installation process without removing your server from the dashboard. Think of it as hitting a "repair" button.
- **Delete** is the right choice when you no longer need the server at all and want to permanently remove it along with all of its data, databases, backups, and configurations. This frees up a server slot on your account.

If you're unsure, reinstalling is the safer option since it can preserve your files while still fixing installation issues.

## Reinstalling a Server

Reinstalling re-runs your server's egg installation script. This is especially helpful if your server won't start due to corrupted or missing startup files, or if you've accidentally modified something that broke the installation.

1. Navigate to your server's **Settings** page.
2. Select the **Danger Zone** tab.
3. Click **Reinstall**.
4. Optionally enable **Delete all files before reinstalling** if you want to wipe everything and start from a completely clean slate.
5. Click **Reinstall** to confirm.

### What Happens During a Reinstall

There are two paths depending on whether you check that "Delete all files" option:

**Without "Delete all files" enabled:**
- The server's egg installation script runs again
- Default configuration files may be overwritten
- Your worlds, plugins, mods, and other custom files are preserved

This is the gentler option. It fixes installation problems while keeping your data intact.

**With "Delete all files" enabled:**
- All server files are permanently deleted — worlds, configs, plugins, mods, everything
- The installation script then runs on a completely empty server

This gives you a true fresh start, as if you just created the server for the first time.

{: .error}
> Enabling "Delete all files" permanently erases everything on your server. This cannot be undone. If there's anything you want to keep, create a backup before you proceed.

## Deleting a Server

Deleting a server is the nuclear option. It permanently removes the server and everything associated with it from your account. Only go this route if you're absolutely sure you're done with the server.

1. Navigate to your server's **Settings** page.
2. Select the **Danger Zone** tab.
3. Click **Delete Server**.
4. Read the warning carefully. Deletion permanently removes:
   - The server and all of its files
   - All databases associated with the server
   - All backups associated with the server
   - All schedules and configurations
5. Type the **exact server name** in the confirmation field.
6. If you have two-factor authentication enabled, enter your **6-digit 2FA code**.
7. Click **Delete Server** to confirm.

{: .error}
> Server deletion is permanent and cannot be reversed. Once you confirm, all data is gone forever. Please make absolutely sure you've backed up anything you might need before going through with this.

{: .info}
> Only the server owner can delete a server. If you're a subuser, you'll need to ask the owner to perform this action.

### What About My Subscription?

If you have a paid subscription tied to the server you're deleting, you may receive a pro-rated credit for the remaining days left on your billing cycle. The exact credit amount is displayed in the deletion confirmation modal before you finalize anything, so you'll know what to expect.
