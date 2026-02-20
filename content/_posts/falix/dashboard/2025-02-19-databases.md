---
layout: post
title: "How To Set Up Databases"
tags: Files
permalink: falix/dashboard/files/databases
description: "Create and manage MySQL, PostgreSQL, and MongoDB databases for your server."
keywords:
    - keyword: database
      matches: ["create", "setup", "mysql", "postgresql", "mongodb"]
    - keyword: mysql
      matches: ["database", "create", "phpmyadmin", "connect"]
    - keyword: postgresql
      matches: ["database", "create", "postgres", "connect"]
    - keyword: mongodb
      matches: ["database", "create", "mongo", "connect"]
    - keyword: phpmyadmin
      matches: ["database", "mysql", "access", "manage"]
author: Lily
---

## Introduction
Many plugins and server applications need a place to store data that sticks around between restarts -- things like player statistics, economy balances, permissions, and ban lists. That's where databases come in. Instead of relying on flat files, a database gives your plugins a fast, reliable way to read and write persistent data.

Falix lets you create and manage MySQL, PostgreSQL, and MongoDB databases right from your dashboard, so there's no need to set up anything externally.

{: .info}
> All plans include databases. Free plan users get up to **5 databases** per server.

## Supported Database Types

| Type | Default Port | Password Length | phpMyAdmin |
|------|-------------|-----------------|------------|
| **MySQL** | 3306 | 24 characters | Yes |
| **PostgreSQL** | 5432 | 32 characters | No |
| **MongoDB** | 27017 | 32 characters | No |

{: .info}
> Most Minecraft plugins use **MySQL**, so if you're not sure which type to pick, go with MySQL -- it has the widest plugin support. PostgreSQL and MongoDB are great choices if a specific application or plugin asks for them.

## Creating a Database

1. Navigate to your server's **Databases** page.
2. Click **Create Database**.
3. Select a database type.
4. Optionally enter a custom database name (or leave it empty and one will be generated for you).
5. For MySQL databases, you can optionally configure remote access.
6. Click **Create Database**.

### Database Name
You can either let Falix auto-generate a random name or provide your own. If you choose a custom name, keep these rules in mind:
- Only letters, numbers, and underscores are allowed.
- The maximum length is 48 characters.
- Your name will automatically be prefixed with your server ID, so a name like `mydb` becomes `s123_mydb`.

### Remote Access (MySQL Only)
Remote access controls which hosts are allowed to connect to your MySQL database. By default, the value is set to `%`, which means connections from anywhere are accepted. You can also lock it down to a specific IP address or hostname if you want tighter security.

{: .info}
> Remote access only applies to MySQL databases. PostgreSQL and MongoDB databases do not show this option.

### Limits
Your plan determines how many databases you can create per server:
- **Free plan** -- up to 5 databases per server.
- **Premium plan** -- up to 20 databases per server. Need more? Contact support to request a higher limit.

A usage bar at the bottom of the page shows how many databases you've used out of your limit.

## Connection Details
Once your database is created, click the **Details** button on it to see everything you need to connect.

You'll find the following fields in the details panel:
- **Database Name** -- the full name of your database (click to copy).
- **Host Address** -- the hostname of the database server.
- **Port** -- the port number to connect on.
- **Username** -- your database username (click to copy).
- **Password** -- your database password. It's hidden by default for security -- click the eye icon to reveal it.

Every field has a handy **copy** button so you can quickly grab values without selecting text manually.

### Connection Strings
If you need a ready-to-use connection URL, click **Connection String** in the details panel. The format depends on your database type:

{% tabs connstring %}

{% tab connstring MySQL %}

```
mysql://username:password@host:port/database
```

{% endtab %}

{% tab connstring PostgreSQL %}

```
postgresql://username:password@host:port/database
```

{% endtab %}

{% tab connstring MongoDB %}

```
mongodb://username:password@host:port/database?authSource=database
```

{% endtab %}

{% endtabs %}

### Copy All
Click **Copy All** to copy every connection field as a formatted text block. This is especially useful when you're pasting credentials into a plugin config file or following a setup guide.

## phpMyAdmin
MySQL databases come with a built-in **phpMyAdmin** button that opens a web-based management interface in a new tab. From there, you can browse tables, run SQL queries, import and export data, and manage your database structure -- all without touching a command line.

To use it:
1. Click the **phpMyAdmin** button on a MySQL database.
2. A secure single sign-on token is generated (it's valid for 60 seconds).
3. phpMyAdmin opens in a new browser tab, already logged in.

{: .info}
> phpMyAdmin is only available for MySQL databases. PostgreSQL and MongoDB databases do not have this option.

## Rotating a Password
If your database password was compromised or you just want a fresh one, you can rotate it in seconds:

1. Click the **Rotate** button on the database.
2. Confirm the action.
3. A new password is generated and applied immediately.

{: .warning}
> The old password stops working right away. Make sure to update any plugins, config files, or scripts that reference the old password, or they'll lose their database connection.

## Deleting a Database
If you no longer need a database, you can remove it from the dashboard. Just be careful -- this action is permanent.

1. Click the **Delete** button on the database.
2. Read the warning carefully. Deletion permanently removes the database itself, all the data stored in it, and all associated users and permissions.
3. Type the exact database name in the confirmation field.
4. Click **Delete Database**.

{: .warning}
> Database deletion is permanent and cannot be undone. If there's any data you want to keep, export it before you delete.

## Connecting from Your Server
Most Minecraft plugins and applications will ask you for a host, port, username, password, and database name. You can grab all of these from the [Connection Details](#connection-details) panel.

Here's what a typical plugin configuration looks like:

{% tabs pluginconfig %}

{% tab pluginconfig MySQL (typical plugin) %}

```yaml
host: db1.example.com
port: 3306
database: s123_mydb
username: u123_user
password: your_password
```

{% endtab %}

{% tab pluginconfig JDBC (Java plugins) %}

```
jdbc:mysql://db1.example.com:3306/s123_mydb
```

{% endtab %}

{% endtabs %}

{: .info}
> If a plugin asks for a "JDBC URL" or "connection string," use the JDBC format shown above. Otherwise, most plugins just need the individual fields filled in separately.

## Wrapping Up
Databases are available on all Falix plans and support MySQL, PostgreSQL, and MongoDB. MySQL is the most common choice for Minecraft servers thanks to its broad plugin compatibility and built-in phpMyAdmin access. No matter which type you choose, you can rotate passwords, manage connections, and delete databases whenever you need to -- all from the dashboard.
