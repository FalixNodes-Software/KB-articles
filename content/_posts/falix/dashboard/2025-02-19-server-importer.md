---
layout: post
title: "How To Import a Server"
tags: Setup
permalink: falix/dashboard/setup/server-importer
description: "Import files from another server or host via SFTP or FTP."
keywords:
    - keyword: import
      matches: ["server", "files", "transfer", "migrate"]
    - keyword: migrate
      matches: ["server", "host", "transfer", "move"]
    - keyword: sftp
      matches: ["import", "transfer", "connect", "files"]
    - keyword: ftp
      matches: ["import", "transfer", "connect", "files"]
    - keyword: transfer
      matches: ["files", "server", "import", "move"]
author: Lily
---

## Introduction
Switching hosting providers? Moving a world from a friend's server? Maybe you have a remote backup sitting on another machine and you want to pull it into Falix. Whatever the reason, the Server Importer makes it easy to bring files over from any remote server using SFTP or FTP -- no manual downloading and re-uploading required.

Instead of going through the hassle of downloading your server files to your computer and then uploading them again, the importer connects directly to the remote server and transfers everything in the background. It is especially handy when you are migrating an entire server from another host, since you can pull over all your worlds, plugins, configs, and data in one shot.

## How It Works

Here is the general flow of an import:

1. You provide SFTP or FTP connection details for the remote server (the one you are pulling files from).
2. Falix temporarily stops your server to avoid file conflicts during the transfer.
3. Files are transferred directly from the remote server to your Falix server in the background.
4. Once the import finishes, your server restarts automatically.

{: .info}
> The whole process happens server-to-server, so you do not need to keep your browser open while it runs. Feel free to check back later or watch the progress from the console.

## Importing Files

Navigate to your server's **Importer** page under Advanced to get started.

### Step 1: Connection Settings

First, choose your connection type and enter the credentials for the remote server you want to import from. If you are migrating from another hosting provider, you can usually find these details in their control panel or dashboard.

{% tabs connection %}

{% tab connection SFTP %}

SFTP (SSH File Transfer Protocol) is the recommended option. It encrypts the connection, so your credentials and files are protected during transfer.

| Field | Description |
|-------|-------------|
| Host Address | Hostname or IP address of the remote server (e.g. `example.com` or `192.168.1.1`) |
| Port | Default: **22** |
| Username | Your SFTP username |
| Password | Your SFTP password |

{% endtab %}

{% tab connection FTP %}

FTP (File Transfer Protocol) sends data without encryption. Only use this if the remote server does not support SFTP.

| Field | Description |
|-------|-------------|
| Host Address | Hostname or IP address of the remote server |
| Port | Default: **21** |
| Username | Your FTP username |
| Password | Your FTP password |

{: .warning}
> FTP transmits your credentials in plain text. If you have the option, always prefer SFTP for a secure transfer.

{% endtab %}

{% endtabs %}

You can toggle between SFTP and FTP using the connection type buttons at the top of the page. The port number automatically adjusts when you switch.

{: .info}
> Not sure which to pick? Go with SFTP. Most modern hosts support it, and it is more secure than FTP.

### Step 2: Import Paths

Next, tell Falix where to pull files from and where to put them.

- **Source Directory** -- The path on the remote server to import from. Defaults to `/` (the root), which grabs everything.
- **Destination Directory** -- The path on your Falix server where the imported files will land. Defaults to `/` (the root).
- **Delete existing files** -- When enabled, this removes all files in the destination directory before the import starts. This is off by default.

{: .warning}
> Enabling **Delete existing files** will permanently remove all files in the destination directory before the import begins. This cannot be undone. Only enable this if you want a completely clean slate.

### Step 3: Start Import

When everything looks good, click **Import** to begin. The button will show a loading spinner while the request is processed.

Once the import starts successfully, a modal appears with two options:
- **Stay Here** -- remain on the importer page
- **Go to Console** -- open the server console to watch the import progress in real time

{: .info}
> Your server will stop during the import and restart automatically when it finishes. You can monitor progress from the console at any time.

## Path Rules

Source and destination paths need to follow a few simple rules:

- Must start with `/`
- Allowed characters: letters, numbers, forward slash, underscore, hyphen, dot, and spaces
- Path traversal (`..`) is automatically stripped for security

**Examples:**

| Source | Destination | Result |
|--------|-------------|--------|
| `/` | `/` | Imports everything to server root |
| `/plugins` | `/plugins` | Imports only the plugins folder |
| `/world` | `/world` | Imports only the world folder |
| `/` | `/imported` | Imports everything into a subfolder |

{: .info}
> Importing into a subfolder like `/imported` is a great way to review the files before merging them into your live server. You can move things around afterward using the File Manager.

## Limits

There are a couple of limits to keep in mind:

- **Rate limit** -- You can run a maximum of 5 imports per 5 minutes. If you hit the limit, just wait a few minutes before trying again.
- **One at a time** -- Only one import can run per server at a time. You will need to wait for the current import to finish before starting another.

## Common Use Cases

{% tabs usecases %}

{% tab usecases Migrate from Another Host %}

This is the most common reason to use the importer. If you are moving your server from another hosting provider to Falix, here is how to do it:

1. Get the SFTP or FTP credentials from your current host. Check their control panel, dashboard, or support docs -- most providers list these somewhere accessible.
2. Set the **Source Directory** to `/` to import everything.
3. Set the **Destination Directory** to `/`.
4. Enable **Delete existing files** if you want a clean start with no leftover default files.
5. Click **Import** and let it run.

{: .info}
> Before you start, it is a good idea to make sure your current host's server is stopped. This avoids any issues with files being written to during the transfer.

{% endtab %}

{% tab usecases Import Specific Folders %}

Sometimes you do not need everything -- maybe you just want to pull over a world from a friend's server, or grab a plugins folder from a backup. You can import individual folders instead of the whole server:

1. Set the **Source Directory** to the folder path you want (e.g. `/plugins` or `/world`).
2. Set the **Destination Directory** to the matching path on your Falix server.
3. Click **Import**.

If you need multiple folders, just repeat the process for each one. Since the importer only transfers what you specify, this is much faster than importing everything.

{% endtab %}

{% endtabs %}

## Migration Tips

Here are a few practical tips to make your migration as smooth as possible:

- **Back up first.** If your Falix server already has files you care about, create a backup before importing. The importer can overwrite existing files, and it is better to be safe.
- **Check your server software.** Make sure your Falix server is running the same server software (e.g. Paper, Forge, Fabric) and a compatible version as the server you are importing from. Mismatched versions can cause crashes or world corruption.
- **Test after importing.** Once the import completes, start your server and check that everything loaded correctly. Look at the console for errors, join the server and verify your worlds, and spot-check that plugins or mods are working.
- **Import selectively when possible.** If you only need specific folders (like worlds or plugins), import just those instead of everything. It is faster and reduces the chance of overwriting something unintended.

## Troubleshooting

If something goes wrong during or after an import, here are the most common issues and how to fix them:

| Issue | What to Do |
|-------|------------|
| Connection failed | Double-check that the host address, port, username, and password are all correct. Also confirm that the remote server allows SFTP or FTP connections -- some hosts require you to enable this in their panel first. |
| Rate limit exceeded | You have hit the 5-imports-per-5-minutes limit. Wait a few minutes and try again. |
| Import already in progress | Only one import can run at a time per server. Wait for the current one to finish -- you can check progress in the console. |
| Files not appearing | Verify that your source and destination paths are correct. Check the server console for any error messages that appeared during the import. |
| Server not starting after import | The imported files may be incompatible with your server software or version. Check the console for errors, and make sure the server type and version match what the imported files expect. |
