---
layout: help/article
title:  "Registering a Custom IP Address for your Minecraft Server - Falix"
categories: Minecraft
icon: <i class="fa-light fa-sword"></i>
tag: mcgeneral
permalink: /help/minecraft/general/custom-ip.*
gitURL: _posts/minecraft/general/2023-02-10-custom-ip-address.md
description: "Register your own domain for your Minecraft Server at Falix"

author: Korbs
authorGitHub: korbsstudio
---

## Choosing A Domain Provider
There are a lot of places where you can register a domain.
Here are a few popular ones:

* [Namecheap](https://www.namecheap.com/)
* [GoDaddy](https://www.godaddy.com/)
* [bluehost](https://www.bluehost.com/)
* [Google](https://domains.google/)
* [Hover](https://www.hover.com/)


{: .note }
> We're unrelated to the above services and are simply providing examples. Feel free to use any domain provider you want.

## Creating A SRV Record
You are required to use a SRV record to link your domain to your Minecraft server. Some domain providers like Freenom don't provide this, so we recommend that you use Cloudflare.
To create a SRV record, you must first go to your domain's DNS settings. Create a new record, then follow the table below:

| Record Type | Name      | Service      | Priority | Weight | Port   | Target |
| ----------- | --------- | ------------ | -------- | ------ | ------ | ------ |
| SRV         | @         | _minecraft   | 0        | 5      | 000000 | <server_IP> |

Make sure to replace `<server_IP>` with your Minecraft server's IP, for example `game1.falix.cc`.

Make sure to change `port` to your server's port.

{: .note }
> It may take up to 24 hours for your DNS settings to be updated.

You should be able to join your server with your new custom IP.





