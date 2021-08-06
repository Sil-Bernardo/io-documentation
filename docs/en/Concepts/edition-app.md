---
title: Edition App
description: "Edition app concept"
date: "2020-03-17"
tags: ["edition", "edition-app", "sponsor"]
version: "0.x"
git: "https://github.com/vtex-apps/io-documentation/blob/docs/en/Concepts/edition-app.md"
---

# Edition App

An Edition App consists of a bundle of settings, policies, back-end and front-end apps encapsulated and exported by a [Sponsor Account](https://vtex.io/docs/concepts/sponsor-account/).

Its main objective is to facilitate the installation of numerous apps that might be considered as essential to set up one specific environment. 

![EditionApp](https://user-images.githubusercontent.com/60782333/91470034-927c0480-e86a-11ea-866e-54575f3c0975.png)

For example, consider the two Edition Apps developed by the `vtex` account:

- The Edition Business (`vtex.edition-business@0.x`) - installs all the necessary apps to build a store with our legacy [CMS](https://help.vtex.com/en/tracks/cms--2YcpgIljVaLVQYMzxQbc3z/6OCY6S9tqBXPD5mgpbBInC).

- The Edition Store (`vtex.edition-store@2.x`) - installs all the necessary apps to develop a store with the [Store Framework](https://vtex.io/docs/getting-started/build-stores-with-store-framework/1/).

In fact, any VTEX account that meets the [requirements needed to be a Sponsor Account](https://vtex.io/docs/recipes/development/becoming-a-sponsor-account/) can develop and release their own Edition Apps.

Notice that this can be especially useful for complex account families, such as the ones under the same brand or holding.

That's because, besides the fundamental development environment set up by a `vtex` native Edition App, a Sponsor Account can extend an Edition App by creating a new and customized one that meets its account family needs. 

>ℹ️ To change the Edition App installed in an account, you must <a href ="https://help-tickets.vtex.com/smartlink/sso/login/zendesk">open a support ticket</a>. This is required to avoid critical issues that could be caused by its misconfiguration.
Note that all Edition apps must depend, directly or indirectly, on either `vtex.edition-business` or `vtex.edition-store`.

The apps that are part of the Edition App included as a dependency are considered inherited apps.

Despite these, all apps of an Edition App must have the same vendor as the Edition App that bundles them.

Keep in mind that Sponsored Accounts cannot change the apps and configurations installed through an Edition App. Only the Sponsor Account is authorized to do that, by releasing a new version of its Edition App and requiring it to be reinstalled.

To sum it up, by encapsulating all the necessary settings, policies, back-, and front-end apps, an Edition App provides all the essential functionalities to set up one desired environment.
