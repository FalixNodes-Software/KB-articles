---
title: Adding A Custom Domain To your Server
permalink: falix/dashboard/file-management/sftp
tags: General
description: Learn how to add your own domain to your falixnodes server.
keywords:
    - keyword: domain
      matches: ["custom", "own"]
author:
    - TWIXhunter
---

{: .warning }
> This article requires that you already own a domain.

There are many domain registrars you can use to purchase a domain. Here are a few popular options:

- [cloudflare](https://cloudflare.com/en-gb/products/registrar/)
- [Namecheap](https://namecheap.com/)
- [GoDaddy](https://godaddy.com)
- [Bluehost](https://bluehost.com/domains)
- [Squarespace](https://domains.squarespace.com/)
- [Hover](https://www.hover.com/)

> We are not affiliated with any of the services listed above. Feel free to use any domain provider of your choice.

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console) of your server. In the navigation menu, open the "Server Settings" category and navigate to the [Domains](https://client.falixnodes.net/server/subdomains) page. 

4. Click the "+ New domain" button.

5. Select "Custom Domain". and press the "Go to Custom Domain Setup" button.

6. Click the "New Domain" button again.

7. Enter the Domain you want to use (including subdomains like `play.`).

8. Navigate to your domain providers dashboard and enter the given credentials.

    > The exact process of adding the NS record might differ between providers. instructions on how to do this for some popular providers are listed below.

{% tabs providers %}

{% tab providers cloudflare %}

1. Visit [the official Cloudflare site](https://dash.cloudflare.com/login).

2. Log in to your Cloudflare account.

3. Select your domain from the dashboard.

4. Go to the "DNS" tab in the sidebar.

5. Click "Add record".

6. Select the record type (NS).

7. Enter the subdomain you want to use (for example: "play" will redirect "play.example.com"). leave this empty if you don't want any subdomain.

8. Enter the primary and secondary nameservers.

9. leave the TTL at automatic.

10. Click "save"

{% endtab %}


{% tab providers namecheap %}

1. Visit [the official NameCheap site](https://www.namecheap.com/myaccount/login/).

2. Log in to your NameCheap account.

3. Select "Domain List" in the left sidebar or header.

4. Click the "Manage" button next to your domain.

5. Navigate to the "Advanced DNS" tab.

6. Click "ADD NEW RECORD".

7. Select NS Record from the dropdown.

8. Enter the subdomain you want to use (for example: "play" will redirect "play.example.com"). Enter "@" if you don't want any subdomain.

9. Enter the Primary Nameserver.

10. Leave the TTL at "automatic"

11. Click the checkmark to save.

12. repeat the steps above for the secondary Nameserver.

{% endtab %}


{% tab providers GoDaddy %}

1. Visit [the official GoDaddy site](https://dcc.godaddy.com/control/portfolio&prog_id=PROG_ID).

2. Log in to your GoDaddy account.

3. Select your domain.

4. Go to the "DNS" tab.

5. Click the "Add New Record" button.

6. Select "NS" in the type dropdown.

7. Enter the subdomain you want to use (for example: "play" will redirect "play.example.com"). Enter "@" if you don't want any subdomain.

8. Enter the Primary Nameserver domain given in the Falix Domains page into the "Value" field

9. Leave the TTL as "automatic"

10. Click the "Save" button.

11. Repeat the steps above for the secondary nameserver.

{% endtab %}

{% tab providers SquareSpace %}

Steps go here

{% endtab %}

{% endtabs %}

9. Press "I have added the DNS records".

10. Wait for the verification to complete and press "UNKNOWN BUTTON"

{. :success}
> you should now be able to join your Minecraft server using the domain you provided.

