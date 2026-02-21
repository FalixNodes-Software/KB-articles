---
layout: post
title: "File Manager"
tags: Files
permalink: falix/dashboard/files/file-manager
description: "Browse, edit, upload, and manage your server files with the built-in file manager."
keywords:
    - keyword: file manager
      matches: ["files", "browse", "upload", "edit"]
    - keyword: upload
      matches: ["file", "folder", "drag", "drop"]
    - keyword: edit
      matches: ["file", "code", "editor", "text"]
    - keyword: download
      matches: ["file", "folder", "save"]
    - keyword: delete
      matches: ["file", "folder", "remove"]
    - keyword: sftp
      matches: ["file", "access", "connect", "upload"]
    - keyword: search
      matches: ["file", "find", "content", "filter"]
    - keyword: archive
      matches: ["zip", "extract", "compress", "tar"]
author: Lily
---

## Introduction
Your server runs on files -- config files, world data, plugins, mods, scripts, and more. The File Manager is where you interact with all of them directly from the dashboard. Whether you need to tweak a setting, upload a new plugin, or dig through logs to troubleshoot an issue, this is your go-to tool.

You can browse directories, edit files in a built-in code editor, upload and download content, manage archives, and even transfer files between servers -- all without leaving your browser.

## File Listing

When you open the File Manager, you will see all the files and folders in your current directory laid out in a list. Each row shows the item's **name** (with a type-specific icon), its **type**, **size**, **last modified date**, and an **actions** dropdown on the right. On mobile, the type, size, and modified columns are hidden to save space, but all the same information is still accessible.

At the left of each row there is a **checkbox** you can use to select files for mass actions (more on that later).

### Special Items

If you are on a premium plan, you will notice two special entries at the top of your root directory. The **Recycle Bin** is where deleted files go instead of being permanently removed -- think of it as a safety net in case you accidentally delete something. The **.backups** folder is a virtual directory that lets you browse and manage your backups right from the File Manager without needing to switch pages.

### Sorting

You can sort your files by clicking any column header. Click once to sort ascending, click again to reverse the direction. You can sort by **name** (alphabetical, which is the default), **size** (largest or smallest first), or **date** (newest or oldest first). On mobile, there is a dedicated sort dropdown that gives you the same options.

## Navigation

### Breadcrumbs

A breadcrumb bar at the top of the page shows your current path. You can click any segment to jump directly to that directory -- handy when you are several folders deep and want to go back a few levels. The home icon takes you straight back to the root `/` directory.

### URL Parameters

The File Manager supports direct links, which is useful for bookmarking specific locations or sharing paths with others:

- `?dir=/path` -- navigate directly to a specific directory
- `?backup=UUID` -- open a specific backup
- `?backupPath=/path` -- navigate to a location within a backup

### Pinned Files

If there are files or folders you access frequently, you can pin them for quick access. Pinned items show up in a collapsible section at the top of the file listing, displaying both the file name and its directory path. Click a pinned item to jump straight to its location.

To pin or unpin something, use the **Pin** / **Unpin** option in the action menu or right-click context menu.

{: .info}
> Pinning is especially useful for config files you edit regularly, like `server.properties` or plugin configs buried several folders deep.

## File Operations

Right-click any file or folder to open the context menu, or use the action dropdown button on the right side of each row. The available actions depend on whether you are working with a file or a folder.

### Available Actions

{% tabs actions %}

{% tab actions Files %}

| Action | Description | Premium Only |
|--------|-------------|:------------:|
| **View Image** | Opens inline image viewer (images only) | -- |
| **Edit NBT** | Opens NBT data editor (Minecraft .nbt files only) | -- |
| **Extract** | Extracts archive contents (archives only) | -- |
| **Edit** | Opens the code editor | -- |
| **History** | View file change history | Yes |
| **Copy** | Copy file to a different path | -- |
| **Download** | Download the file | -- |
| **Transfer** | Send to another server | Yes |
| **Rename** | Change the file name | -- |
| **Move** | Move to a different directory | -- |
| **Permissions** | Change file permissions (chmod) | Yes |
| **Restore** | Restore from a backup | Yes |
| **Pin / Unpin** | Pin for quick access | -- |
| **Delete** | Remove the file | -- |

{% endtab %}

{% tab actions Folders %}

| Action | Description | Premium Only |
|--------|-------------|:------------:|
| **Download** | Downloads the folder as an archive | -- |
| **Transfer** | Send to another server | Yes |
| **Rename** | Change the folder name | -- |
| **Move** | Move to a different directory | -- |
| **Permissions** | Change folder permissions (chmod) | Yes |
| **Restore** | Restore from a backup | Yes |
| **Pin / Unpin** | Pin for quick access | -- |
| **Delete** | Remove the folder and its contents | -- |

{% endtab %}

{% endtabs %}

### Renaming

Click **Rename** to open a modal with the current name pre-filled. Edit the name and confirm. Be careful when changing file extensions -- the modal will warn you about this, since changing an extension can make a file unreadable by the software that uses it.

### Moving

Click **Move** to open a directory browser where you can navigate to the destination folder or type a path manually. You can even create a new folder right from the move dialog if you need somewhere new to put the file.

### Copying

Click **Copy** to open a modal where you enter the destination path for the copy. This creates a duplicate of the file at the new location while leaving the original in place.

### Permissions (chmod)

Click **Permissions** to set the file or folder permissions using a 3-digit octal value. Common examples include `755` for directories and `644` for files. A permission guide in the modal explains what each digit means: 4 = read, 2 = write, 1 = execute.

{: .warning}
> Only change permissions if you know what you are doing. Incorrect permissions can prevent your server from reading important files or running scripts.

### Deleting

Click **Delete** to remove a file or folder. A confirmation dialog appears showing the item name so you can double-check before proceeding.

- **Premium users**: Items are moved to the Recycle Bin, so you can recover them if needed
- **Free plan users**: Items are permanently deleted right away

## Creating Files and Folders

### Create File

Use the create file option to make a new empty file in the current directory. Just enter a name, and the file will be created ready for you to open in the code editor. This is great for creating new config files or scripts from scratch.

### Create Folder

Use the create folder option to add a new directory. A tip in the modal reminds you about naming conventions -- stick to lowercase letters, numbers, and hyphens for the most compatible names.

## Uploading

There are several ways to get files onto your server, depending on what is most convenient for you:

- **File Upload** -- Select one or more files from your computer using the file picker
- **Folder Upload** -- Upload an entire folder, including all its subfolders, at once
- **Drag and Drop** -- Simply drag files from your desktop onto the page and a drop overlay will appear
- **Pull from URL** -- Enter a URL and the server will download the file directly, saving you from downloading it to your computer first. You can optionally set a custom filename. This is a **premium feature**
- **Server Importer** -- Import files from another server hosting provider. This is a **premium feature**
- **SFTP** -- Connect with an SFTP client like FileZilla or WinSCP for direct file access and bulk uploads. This is the best option for transferring large numbers of files and is available on all plans

### Upload Limits

| Limit | Value |
|-------|-------|
| **Max file size** | 10 GB |
| **Max total size** | 10 GB |
| **Max files per upload** | 1,000 |

### SFTP Access

Click the **SFTP** button to view your connection details, including the host address and username (both copyable). There is also a button to copy all details at once and a launch button that can open your default SFTP client directly.

{: .info}
> SFTP is available to all users, including those on the free plan. It is the recommended way to upload large files or transfer many files at once.

## Downloading

Click **Download** on any file to download it directly to your computer. For folders, the contents are automatically archived first and then downloaded as a single file.

{: .info}
> Free plan users will see a notice that downloaded archives are automatically deleted from the server after 24 hours. You can check "Don't show again" to dismiss this notice permanently.

## Archive Handling

### Extracting Archives

Click **Extract** on any archive file to decompress it into the current directory. The File Manager supports a wide range of formats: `.zip`, `.rar`, `.7z`, `.tar`, `.gz`, `.tar.gz`, `.tgz`, `.bz2`, and `.xz`.

### Browsing Archives

Here is a handy trick: you can click on an archive file to browse its contents without extracting it first. Navigate through the archive just like you would a regular directory. When you are done looking around, use the go-back button to exit the archive view.

This is useful when you want to check what is inside a zip before extracting it, or when you only need to verify that a specific file is included.

## Code Editor

Click **Edit** on any text or code file to open it in the built-in code editor. The editor provides syntax highlighting for a wide range of file types:

| Category | Extensions |
|----------|-----------|
| **Code** | .js, .jsx, .ts, .tsx, .php, .html, .css, .scss, .java, .py, .c, .cpp, .cs, .rb, .go, .rs, .swift, .kt |
| **Config** | .json, .xml, .yml, .yaml, .ini, .conf, .cfg, .properties, .toml |
| **Scripts** | .sh, .bash, .bat, .ps1, .cmd |
| **Data** | .sql, .csv, .txt, .md, .log |

{: .info}
> The code editor works well for quick edits. For larger changes across many files, consider connecting via SFTP and using a desktop editor like VS Code.

## Search

### Filename Search

{: .info}
> Filename search is a **premium feature**.

Click the search button or press **Ctrl+F** (or **Cmd+F** on Mac) to open the search bar. As you type, files in the current directory are filtered in real-time. A counter shows how many results match (for example, "3 of 12"), making it easy to spot what you are looking for.

## Disk Usage Analysis

Wondering where all your storage went? Open the disk usage modal to get a visual breakdown with a pie chart and a table of the largest files and folders. You can navigate through directories within the modal or enter a custom path to analyze a specific area of your server.

The modal shows your **total size**, **file count**, and **folder count** -- very helpful for tracking down that one plugin that is generating massive log files.

## Mass Actions

When you need to do the same thing to multiple files at once, select them using the checkboxes. A floating panel appears at the bottom of the screen showing how many items you have selected and what you can do with them.

| Action | Description | Premium Only |
|--------|-------------|:------------:|
| **Download** | Archives selected items into a zip and downloads | -- |
| **Archive** | Creates a `.tar` or `.tar.gz` archive of selected items | Yes |
| **Move** | Move all selected items to a different directory | Yes |
| **Transfer** | Send selected items to another server | Yes |
| **Permissions** | Apply chmod to all selected items | Yes |
| **Restore** | Open quick restore to restore selected files from a backup | Yes |
| **Delete** | Remove all selected items | -- |

Use the **Select All** checkbox in the table header to quickly select or deselect everything in the current directory.

## Transferring Files Between Servers

{: .info}
> Transfer is a **premium feature**.

If you run multiple servers, you can send files directly from one to another without downloading and re-uploading. Click **Transfer** on a file, folder, or use the mass action transfer option.

1. Select the target server from a list of your other servers.
2. Choose the destination directory using the directory browser.
3. Confirm the transfer.

A progress modal keeps you updated on the transfer status. When you transfer a folder, it is automatically archived, sent to the destination, and extracted there -- all handled behind the scenes.

## Backup Integration

The File Manager and the backup system are tightly connected, so you can manage your backups without switching pages.

### Browsing Backups

Navigate to the `.backups` virtual folder in the root directory to see all your backups. Each one shows its name, creation date, type (manual or scheduled), and whether it is locked.

### Backup Actions

| Action | Description |
|--------|-------------|
| **Browse** | View the backup's file structure |
| **Restore** | Restore the entire backup or select specific files |
| **Download** | Download the backup file |
| **Lock / Unlock** | Prevent or allow accidental deletion |
| **Delete** | Remove the backup (locked backups cannot be deleted) |

### Creating Backups from File Manager

You can create a backup directly from the File Manager without switching to the Backups page:

1. Enter a backup name.
2. Optionally toggle **Selective Backup** to choose specific files and folders to include.
3. Optionally enable **Lock Backup** to prevent accidental deletion.
4. Click **Create Backup**.

### Quick Restore

If you realize a file has been changed or broken and you want to restore it from a backup, select the file (or multiple files) and click **Restore** in the mass actions panel:

1. Select which backup to restore from.
2. Confirm the files to restore.

You can also copy individual files from a backup to a specific directory using the backup copy modal, which gives you more control over where the restored files end up.

## File History

{: .info}
> File history is a **premium feature**.

Click **History** on any file to see how it has changed over time. This is especially valuable for config files -- if a change breaks something, you can see exactly what was modified and when.

## Integrated Console

{: .info}
> The integrated console is a **premium feature**.

Premium users get a console panel at the bottom of the File Manager, so you can edit files and interact with your server at the same time. The console shows real-time server output, lets you type commands, and includes power controls (start, stop, restart, kill) along with a server status indicator. You can minimize or close it when you do not need it.

## Floating Navigation Bar

{: .info}
> The floating navigation bar is a **premium feature**.

Premium users also get a floating bar at the bottom of the screen for quick access to common actions:

- **Create** -- new file or new folder
- **Upload** -- files, folder, pull from URL, or SFTP
- **Quick Actions** -- refresh directory, scroll to top

## Keyboard Shortcuts

If you prefer keeping your hands on the keyboard, the File Manager has you covered with these shortcuts:

| Shortcut | Action |
|----------|--------|
| **Ctrl+F / Cmd+F** | Open filename search (premium only) |
| **Ctrl+A / Cmd+A** | Select all files |
| **Ctrl+U / Cmd+U** | Upload files |
| **Ctrl+N / Cmd+N** | Create new folder |
| **Ctrl+R / Cmd+R** | Refresh directory |
| **Delete** | Delete selected files (when files are selected) |
| **Backspace** | Navigate to parent directory |
| **Arrow Up / Down** | Navigate between files |
| **Enter** | Open selected file or folder |
| **Escape** | Close search bar, dropdowns, or modals |

## World Viewer

For Minecraft Java servers, when you navigate into a world's `region` folder, a **World View** button appears in the toolbar. Click it to visualize your Minecraft world data right in the browser -- see a top-down map of the entire world, zoom into regions with actual block textures, inspect chunks in 3D with X-Ray mode, and bulk-delete unused chunks to reduce world size.

For full details, see the dedicated [World Viewer](/falix/dashboard/files/world-viewer) article.
