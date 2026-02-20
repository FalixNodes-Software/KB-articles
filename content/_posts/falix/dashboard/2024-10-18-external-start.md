---
title: How To Start Your Server Externally
tags: Automation
permalink: falix/dashboard/automation/external-start
description: Use the external start feature to turn on your server without accessing the console.
keywords:
    - keyword: turn on
      matches: &start_matches ["without", "external", "friend", "friends"]
    - keyword: start
      matches: *start_matches
author:
    - TWIXhunter
    - Mocab
---

The external start feature is a great way to allow players or users to start your server when needed without needing access to your server's console. This is especially handy when you want to let your community start the server on their own whenever they want to play.

## Toggling the External Start Feature

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Navigate to your [Profile Settings](https://client.falixnodes.net/profile/settings) by clicking "Settings" in the "Account" section of the navigation menu.

3. Look for the **External Server Start** toggle.

4. Flip the toggle to enable or disable the feature across all your servers. The change is saved automatically.

{: .info}
> This is an account-wide setting. When enabled, it applies to all servers you own.

## Starting a Server Using External Start

{: .warning}
> Server owners and admins are **not** allowed to use this feature, please use the console instead.

1. Go to the [External Start page](https://falixnodes.net/startserver).

2. Enter the subdomain of the server you want to start; it should resemble this format: `xxxxx.falixsrv.me`.

    > You can prefill the subdomain by adding `?ip=xxxxx.falixsrv.me` to the end of the page URL. Make sure to replace `xxxxx.falixsrv.me` with your actual subdomain.

3. Click on the "**Start Server**" button to initiate a server start.

{: .success}
> If successful, you should see "Server `xxxxx.falixsrv.me` has been started".

> You may have to wait a few minutes for the server to finish starting.

