---
layout: post
title: "How To Set Up Git Integration"
tags: Automation
permalink: falix/dashboard/automation/git-integration
description: "Link a Git repository to your server for automatic or manual deployments."
keywords:
    - keyword: git
      matches: ["connect", "link", "deploy", "integration", "setup"]
    - keyword: github
      matches: ["connect", "link", "deploy", "repository"]
    - keyword: gitlab
      matches: ["connect", "link", "deploy", "repository"]
    - keyword: deploy
      matches: ["automatic", "manual", "webhook", "push"]
    - keyword: repository
      matches: ["link", "connect", "sync"]
author: Lily
---

## Introduction
Imagine pushing a commit to GitHub and having your server automatically pull in the changes -- no manual uploading, no dragging files around, no extra steps. That is exactly what Git integration gives you. Whether you are developing custom plugins, fine-tuning server configs, building a modpack, or collaborating with a team, you can keep everything in version control and deploy straight to your server with a single push (or a single click).

This is perfect for plugin developers who want to test changes quickly, teams managing shared server configurations, or anyone who is tired of manually uploading files every time something changes.

{: .info}
> Git integration is a **premium feature**. Free plan users will need to upgrade to use it.

## Supported Providers
You can connect repositories from any of these providers -- they all support private repos, public repos, and automatic deployments:

| Provider | Private Repos | Public Repos | Auto-Deploy |
|----------|--------------|--------------|-------------|
| GitHub | Yes | Yes | Yes |
| GitLab | Yes | Yes | Yes |
| Bitbucket | Yes | Yes | Yes |
| Codeberg | Yes | Yes | Yes |

## Getting Started

### Step 1: Connect Your Account
If you want to link a private repository, you will need to connect your Git provider account first. This lets Falix see your repos and set up webhooks on your behalf.

1. Navigate to your server and open the **Git** page.
2. Click the badge for your provider (GitHub, GitLab, Bitbucket, or Codeberg).
3. You will be redirected to your provider's authorization page -- go ahead and authorize Falix to access your repositories.
4. Once authorized, you will be sent back to the dashboard with your account connected and ready to go.

{: .info}
> Working with a public repository? You can skip this step entirely. Public repos do not require an account connection.

### Step 2: Link a Repository

{% tabs link %}

{% tab link Private Repository %}

1. On the **Git** page, click **Link Repository**.
2. Select your connected provider from the dropdown.
3. Your repositories will load automatically -- pick the one you want to link.
4. Choose the branch you want to deploy from (the default branch is pre-selected for convenience).
5. Optionally, enable **Auto-Deploy** so that every push to your branch triggers a deployment automatically.
6. Click **Link Repository** to finish up.

A webhook will be created on your repository behind the scenes, which is what makes push-based deployments work.

{% endtab %}

{% tab link Public Repository %}

1. On the **Git** page, click **Link Repository**.
2. Switch to public repository mode.
3. Paste the repository URL, or enter the provider, owner, and repo name manually.
4. The system will check that the repository is public and accessible.
5. Select the branch you want to deploy from.
6. Click **Link Repository** to finish up.

{: .warning}
> Auto-deploy is not available for public repositories since there is no webhook connection. You will need to trigger deployments manually instead.

{% endtab %}

{% endtabs %}

## Deploying
Once your repository is linked, you have two ways to get your code onto your server.

{% tabs deploy %}

{% tab deploy Automatic %}

With auto-deploy enabled, every push to your configured branch automatically triggers a deployment. Your Git provider sends a webhook notification to Falix, which then syncs the latest code to your server -- no manual steps required.

This works with all four supported providers and is set up automatically when you link a private repository. It is the best option if you want a true "push and forget" workflow.

{% endtab %}

{% tab deploy Manual %}

Prefer to deploy on your own schedule? You can trigger a deployment whenever you are ready:

1. Go to the **Git** page on your server.
2. Click the **Trigger Deploy** button.
3. The latest code from your configured branch will be pulled and synced to your server.

This is handy when you want to review changes before they go live, or when you are working with a public repository that does not support auto-deploy.

{% endtab %}

{% endtabs %}

## Deployment Settings
Head over to the **Settings** tab on the Git page to fine-tune how your deployments behave. There are several options here, so let us walk through each one.

### Branch
This controls which branch gets deployed. You can change it at any time -- useful if you want to switch between a development and production branch, for example.

### Auto-Deploy
This toggle controls whether pushes to your branch automatically trigger a deployment. It is only available for private repositories with a connected account, since it relies on webhooks.

### Sync Paths
By default, your entire repository gets synced to the server. But if you only want certain folders or files deployed, you can specify sync paths. This is really useful if your repo contains source code, documentation, and build output but you only want the compiled files on your server.

- Example paths: `src/`, `config/`, `plugins/MyPlugin.jar`
- You can specify up to 20 paths

### Post-Deploy Action
You can tell Falix what to do with your server after a successful deployment. For instance, you might want to automatically restart the server so your changes take effect right away.

| Action | What it does |
|--------|-------------|
| None | Nothing happens after deployment (this is the default) |
| Start | Starts the server |
| Stop | Stops the server |
| Restart | Gracefully restarts the server |
| Kill | Force stops the server immediately |
| Hard restart | Force stops the server and then starts it again |

### Post-Deploy Commands
Need to run specific console commands after a deployment? You can set up to 20 commands that execute automatically. For each command, you can configure:

- **Command** -- the console command to run
- **Delay** -- how long to wait before running it (anywhere from 0 to 300 seconds)
- **Only when** -- whether it should run always, only when the server is online, or only when the server is offline

This is great for things like reloading plugins, broadcasting a maintenance message to players, or running cleanup tasks.

### Post-Deploy Schedules
If you already have schedules set up on your server, you can trigger them automatically after a deployment. Just select the ones you want from your existing schedules -- you can choose up to 10.

## Deployment History
The **Deployments** tab keeps a full history of every deployment, so you can always see what happened and when. Each entry shows:

- **Status** -- whether the deployment is pending, in progress, succeeded, or failed
- **Commit hash and message** -- so you know exactly which code was deployed
- **Branch** -- the branch it was deployed from
- **Author** -- who made the commit
- **Trigger** -- whether it was kicked off manually or by a webhook push
- **Duration** -- how long the deployment took
- **Files changed** -- how many files were affected

This makes it easy to track down issues if something goes wrong after a deploy.

## Unlinking a Repository
If you need to disconnect a repository from your server:

1. Go to the **Git** page on your server.
2. Click the **Unlink** button.
3. Confirm the action in the modal that appears.

{: .info}
> Keep in mind that unlinking a repository does not automatically remove the webhook from your Git provider. If you want to clean things up completely, head over to your repository settings on GitHub, GitLab, Bitbucket, or Codeberg and remove the Falix webhook manually.

## Disconnecting a Provider
If you want to disconnect your Git provider account entirely:

1. Navigate to the **Git** page.
2. Click the X on the provider badge you want to disconnect.
3. If you still have repositories linked from that provider, you will need to unlink them first before you can disconnect.
