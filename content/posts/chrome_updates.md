---
title: How to block automatic Chrome Updates
description: How to install an old version of Google Chrome and block automatic Updates
toc: true
authors: [Sergio Fernández]
tags: []
categories: [Windows]
series:
date: '2021-10-02T08:12:10+01:00'
lastmod: '2021-10-02T07:12:10+01:00'
featuredImage: ''
draft: false
---
Google Chrome updates are pretty unobtrusive. However, if you've decided you don't want them to run automatically, there's no setting in the browser to turn them off. For people who prefer a more granular level of control over their updates, that's an issue.

In this post I will show how to install an old Google Chrome and then prevent it from update to the latest version.

## 1. Downloading and installing old version

First, go to [Google Chrome Older Versions Download (Windows, Linux & Mac)](https://www.slimjet.com/chrome/google-chrome-old-version.php).

Then, scroll down to Windows and choose your preferred version, I will use Chrome 71, it works perfect.

Once downloaded, launch the setup and wait for Chrome to open.

<img src="/posts/images/gc/intro.png" alt="Version" >

Once is opened, you can now close the browser.

## 2. Blocking updates
Now, navigate to **C:\Program Files (x86)\Google** and select Updates folder.

<img src="/posts/images/gc/2.png" alt="Explorer" >

Tap properties, and navigate to **Security**.

<img src="/posts/images/gc/3.png" alt="Sec" >

Tap Edit, then **Deny** all permissions for all groups or user names.

<img src="/posts/images/gc/4.png" alt="deny" >

Now confirm the changes and exit.

<img src="/posts/images/gc/1.png" alt="deny" >

You can open the broswer and check for updates, as you can see in the image, it can't be updated cause Chrome can't access its Update folder.

Enjoy!
