---
title: How To Add Resource Packs To Your Minecraft Java Server
tags: Configuration
description: Learn how to upload and configure resource packs using the updated FalixNodes panel.
keywords:
  - keyword: pack
    matches: ["resource", "texture", "sound"]
  - keyword: custom
    matches: ["resource", "texture", "sound"]
permalink: /minecraft/java/configuration/resource-pack
author:
  - Cakey
---

Adding a resource pack allows your server to deliver custom textures, sounds, models, and UI elements to players. With the updated FalixNodes panel, resource packs can now be uploaded and configured directly from the dashboard without manually editing `server.properties`.

This guide covers uploading a pack, enabling it for players, enforcing usage, and configuring optional validation settings.

---

## Accessing the Resource Pack Settings

1. Log in to the [FalixNodes Dashboard](https://client.falixnodes.net/).
2. Select your server and open the **Console** page.
3. In the left navigation menu, open **Minecraft → Config**.
4. Scroll to the **Resource Packs** section.

You will see the following options:
- **Require Resource Pack** – force players to use the pack  
- **Resource Pack URL** – direct URL to the pack (auto-filled on upload)  
- **Upload Pack** – upload a `.zip` file  
- **Resource Pack ID** – unique identifier for advanced setups  
- **Resource Pack Prompt** – message shown to players  
- **Resource Pack SHA1** – integrity checksum

---

## Uploading a Resource Pack

FalixNodes now supports **direct ZIP uploading**, making the process simpler and eliminating the need for external hosting.

To upload a pack:

1. Click **Upload Pack**.
2. Select your resource pack as a **`.zip`** file.
3. After uploading, the **Resource Pack URL** field will automatically populate.

Your archive must:
- Be in `.zip` format  
- Contain the `assets/` folder in the **root**, not inside another directory

Once uploaded, the pack can be delivered to players immediately.

---

## Requiring Players to Use the Resource Pack

If your server relies on the pack for gameplay or visual consistency:

1. Enable **Require Resource Pack**.
2. Save your configuration if prompted.

When enabled, any player who does not accept resource packs in their Minecraft client settings will be **unable to join**.

---

## Adding a Custom Download Prompt Message

The **Resource Pack Prompt** field allows you to customize the message shown when players are asked to download the pack.

Example:

> Please download our official resource pack for the best gameplay experience.

This is optional but useful for branding, instructions, or server-specific themes.

---

## Verifying File Integrity (SHA1 Checksum)

To ensure clients download the correct version of your pack, you can specify a **SHA1 checksum**.

1. Generate a SHA1 hash using any checksum tool.
2. Paste the generated string into the **Resource Pack SHA1** field.
3. Save your changes.

If the checksum does not match the file the server distributes, a warning will appear in the console at startup.

---

## Understanding Resource Pack ID (Advanced)

The **Resource Pack ID** is automatically generated when uploading a pack.  
You generally do not need to modify this unless:
- A plugin specifically requires a custom ID  
- You are managing multiple pack layers manually  

Leave it unchanged unless instructed otherwise.

---

## Restarting the Server

After setting up your resource pack:

1. Return to the **Console**.
2. Click **Restart**.

Players will now receive a download prompt when joining.

---

## Troubleshooting

### Players are not receiving the pack
- Confirm the resource pack is a valid `.zip`  
- Ensure `assets/` is in the root of the archive  
- Restart your server after uploading  
- Try re-uploading the file

### Console shows an SHA1 error
- The specified checksum does not match the uploaded pack  
- Regenerate the SHA1 hash and update the field

### Players cannot join the server
- If **Require Resource Pack** is enabled, players must allow server resource packs in their Minecraft client settings

---

This article was rewritten and updated for the new FalixNodes panel by **Cakey**.
