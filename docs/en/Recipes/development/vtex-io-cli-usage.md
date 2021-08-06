---
title: Using VTEX IO's CLI
description: "Any development in VTEX IO begins and ends with the Toolbelt, our CLI (Command Line Interface). Learn all the necessary commands to develop in the platform."
date: "2020-04-04"
tags: ["toolbelt", "cli", "command-line-interface", "commands", "reference"]
version: "0.x"
git: "https://github.com/vtex-apps/io-documentation/blob/master/docs/en/Recipes/development/vtex-io-cli-usage.md"
---

# Using VTEX IO's CLI

## Accessing the list of commands

Start using the VTEX IO CLI by running the following command to access a summary of the CLI's default commands.

```shell
$ vtex help
```

![VTEX command](https://github.com/vtex-apps/io-documentation/blob/master/docs/en/Recipes/development/Media/vtex-io-cli-usage-1.svg?raw=true)

>ℹ️ Check the [Command Reference](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-vtex-io-cli-command-reference) for more details.

## Logging into your VTEX account

Log in to your VTEX account by running the following command.

```shell
$ vtex login {account-name}
```

>⚠️ Replace the value between curly braces according to your scenario.

After you run this command, a new tab will open on your browser, asking you to log in to the desired VTEX account with your email.

Once you log in, the web page will display the following message: *“You may now close this window.”*

Now, when you go back to the computer terminal, you'll have access to a development environment for this VTEX account. You'll see some basic information about your account as in the following.

![Login Screen](https://github.com/vtex-apps/io-documentation/blob/master/docs/en/Recipes/development/Media/vtex-io-cli-usage-2.svg?raw=true)

>ℹ️ If you later decide to work on another account, run `vtex switch {account-name}`, specifying the account name you want to switch to.

## Creating a new workspace

After you log in to a VTEX account, you'll be automatically taken to the `master` workspace, meaning the version publicly available to end-users.

To start customizing your storefront or developing a VTEX IO app, you must switch from the master workspace to a development one.

To switch to an existing development workspace or create a new one, run the following command:

```shell
$ vtex use {workspace-name}
```

Notice that if a workspace with the chosen name already exists, you'll be taken to it.

![Change Workspace](https://github.com/vtex-apps/io-documentation/blob/master/docs/en/Recipes/development/Media/vtex-io-cli-usage-3.svg?raw=true)

Otherwise, you'll be asked if you want to create it.

![New Workspace](https://github.com/vtex-apps/io-documentation/blob/master/docs/en/Recipes/development/Media/vtex-io-cli-usage-4.svg?raw=true)

From now on, every operation performed will happen in the specified workspace.

## Verifying your environment

Confirm the account you're logged into and which workspace you're currently using by running the following command.

```shell
$ vtex whoami
```

## Installing an app

Install an app on your current account and workspace by running the following command.

```shell
$ vtex install {appvendor}.{appname}@{appversion}
```

>⚠️ Replace the value between curly braces according to your scenario.

If you try to install an app that has [Billing Options](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-billing-options), you first need to agree to the app's terms and conditions.

![Billing Options](https://github.com/vtex-apps/io-documentation/blob/master/docs/en/Recipes/development/Media/vtex-io-cli-usage-5.svg?raw=true)

If you agree to the Terms of Service and Charge, press `Y` and `enter` to continue with the installation. Notice that some apps are free and others will have specific methods of charging.

## Starting a new project

Start a new project from pre-defined templates by running the following command.

```shell
$ vtex init
```

![Init command](https://github.com/vtex-apps/io-documentation/blob/master/docs/en/Recipes/development/Media/vtex-io-cli-usage-6.svg?raw=true)

For example, to start developing a store theme app, choose the `store` option. This will clone the [Store Theme](https://github.com/vtex-apps/store) boilerplate app into your local files.

## Developing locally

Change to the directory of the app you're developing and run the following command to sync your local files with the VTEX platform.

```shell
$ vtex link
```

![Link Command](https://github.com/vtex-apps/io-documentation/blob/master/docs/en/Recipes/development/Media/vtex-io-cli-usage-7.svg?raw=true)

VTEX IO's CLI will monitor your files and provide an URL related to that workspace. You'll be able to access it through `https://{workspace}--{account}.myvtex.com`, by replacing the value between curly braces with the name of the workspace previously created and your VTEX account. For example, `https://carolinamenezes--appliancetheme.myvtex.com`.

By accessing this URL, you'll be able to watch for local changes in the linked files.

## Checking the installed apps

List all apps installed on the current account by running the following command.

```shell
$ vtex list
```

Installed apps are classified as in the following:

1. Apps automatically installed by your account's [Edition App](https://developers.vtex.com/vtex-developer-docs/docs/vtex-io-documentation-edition-app).
2. Apps manually installed on the current workspace.
3. Apps linked to the current workspace.

## Authenticating API requests

When developing with VTEX IO, instead of using an `appKey` and `appToken` pair, you must use a `VTEX ID token` to call APIs.

To generate a unique and temporary token for VTEX IO, run the following command:

```shell
$ vtex local token
```

The token will be automatically copied to the clipboard.

## Learning more about a command

Use the `--help` flag as in the following to learn more about a specific command.

```shell
vtex [COMMAND] --help
```

![Help Command](https://github.com/vtex-apps/io-documentation/blob/master/docs/en/Recipes/development/Media/vtex-io-cli-usage-8.svg?raw=true)
