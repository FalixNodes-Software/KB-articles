---
layout: post
title: "How To Set Up Git Integration"
tags: Server
permalink: falix/dashboard/general/git-integration
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
Git integration lets you link a repository to your server and deploy code directly from pushes or with a single click. This is useful for custom server plugins, configurations, modpacks, or any project you manage in Git.

{: .info}
> Git integration is a **premium feature**. Free plan users will need to upgrade to use it.

## Supported Providers

| Provider | Private Repos | Public Repos | Auto-Deploy |
|----------|--------------|--------------|-------------|
| GitHub | Yes | Yes | Yes |
| GitLab | Yes | Yes | Yes |
| Bitbucket | Yes | Yes | Yes |
| Codeberg | Yes | Yes | Yes |

## Getting Started

### Step 1: Connect Your Account

To link a private repository, you first need to connect your Git provider account:

1. Navigate to your server and open the **Git** page.
2. Click the badge for your provider (GitHub, GitLab, Bitbucket, or Codeberg).
3. You will be redirected to your provider's authorization page.
4. Authorize Falix to access your repositories.
5. You will be redirected back to the dashboard with your account connected.

{: .info}
> You can skip this step if you only want to link a public repository. Public repos don't require account connection.

### Step 2: Link a Repository

{% tabs link %}

{% tab link Private Repository %}

1. On the **Git** page, click **Link Repository**.
2. Select your connected provider from the dropdown.
3. Your repositories will be loaded automatically. Select the one you want to link.
4. Choose the branch to deploy from (the default branch is pre-selected).
5. Optionally enable **Auto-Deploy** to deploy automatically when you push.
6. Click **Link Repository**.

A webhook will be automatically created on your repository to enable push-based deployments.

{% endtab %}

{% tab link Public Repository %}

1. On the **Git** page, click **Link Repository**.
2. Switch to the public repository mode.
3. Paste the repository URL or enter the provider, owner, and repo name.
4. The system will validate that the repository is public and accessible.
5. Select the branch to deploy from.
6. Click **Link Repository**.

{: .warning}
> Auto-deploy is not available for public repositories. You will need to trigger deployments manually.

{% endtab %}

{% endtabs %}

## Deploying

{% tabs deploy %}

{% tab deploy Automatic %}

When auto-deploy is enabled, pushing to the configured branch will automatically trigger a deployment via webhook. Your provider sends a notification to Falix, which then syncs the latest code to your server.

This works with all four providers and is set up automatically when you link a private repository.

{% endtab %}

{% tab deploy Manual %}

You can trigger a deployment at any time:

1. Go to the **Git** page on your server.
2. Click the **Trigger Deploy** button.
3. The latest code from your configured branch will be synced to your server.

{% endtab %}

{% endtabs %}

## Deployment Settings

Navigate to the **Settings** tab on the Git page to configure how deployments behave.

### Branch
Choose which branch to deploy from. You can change this at any time.

### Auto-Deploy
Toggle automatic deployments on push. Only available for private repositories with a connected account.

### Sync Paths
By default, the entire repository is synced. To only sync specific folders or files, add sync paths:
- Example: `src/`, `config/`, `plugins/MyPlugin.jar`
- Up to 20 paths can be specified

### Post-Deploy Action
Choose what happens to your server after a successful deployment:

| Action | Description |
|--------|-------------|
| None | No action taken (default) |
| Start | Start the server |
| Stop | Stop the server |
| Restart | Restart the server |
| Kill | Force stop the server |
| Hard restart | Kill and then start the server |

### Post-Deploy Commands
Run console commands on your server after deployment (up to 20 commands):
- **Command** — the console command to execute
- **Delay** — wait 0–300 seconds before executing
- **Only when** — execute always, only when server is online, or only when offline

### Post-Deploy Schedules
Trigger existing server schedules after a deployment. Select from your server's configured schedules (up to 10).

## Deployment History

The **Deployments** tab shows a history of all deployments with:
- Status (pending, in progress, success, or failed)
- Commit hash and message
- Branch deployed from
- How it was triggered (manual or webhook)
- Duration

## Unlinking a Repository

1. Go to the **Git** page on your server.
2. Click the **Unlink** button.
3. Confirm the action in the modal.

{: .info}
> Unlinking a repository does not delete the webhook from your provider. You may want to remove it manually from your repository settings.

## Disconnecting a Provider

1. Navigate to the **Git** page.
2. Click the X on the provider badge you want to disconnect.
3. If you have repositories linked from that provider, you will need to unlink them first.
