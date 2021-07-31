---
title: Getting Windows Vista Gadgets Style on Windows 7
description: As many users realized, Windows Vista sidebar.exe (most known as Desktop Gadgets), is different from the Windows 7 one, the most noticeable thing is the gradient it has on the desktop
toc: true
authors: [Sergio Fernández]
tags: []
categories: [Windows]
series: []
date: '2020-12-30T10:30:48+01:00'
lastmod: '2021-12-30T10:30:48+01:00'
featuredImage: ''
draft: false
---
<img src="/posts/images/sidebar/main.png" alt="Vista Sidebar" >

As many users realized, Windows Vista sidebar.exe (most known as Desktop Gadgets), is different from the Windows 7 one, the most noticeable thing is the gradient it has on the desktop.

If you want to have the Vista style on Windows 7, you can follow these steps easily.

## 1. Downloading the Tools
First, you will need to download the following ZIP called: Vista Sidebar, it contains the sidebar files from the official build of Vista.

[Download (Google Drive - 9MB)](https://drive.google.com/u/0/uc?export=download&confirm=2Mdg&id=17N3NhrK4zrckT7GeaUxjuWOR2OEkMye7)

## 2. Extracting & Opening
Once downloaded, extract on a safe area of your computer, e.g: Documents. Finally, open the folder, you will see a x64 and x86 folder inside it. Open the folder depending on your Windows Environment, if you're on 64bits, select x64, otherwise select x86.

Once on the folder, you will see a couple of files, click sidebar.exe and instantly you will get the Vista sidebar on the desktop.

## 3. Opening at Startup
Now you have the Vista Style, you may want have the Desktop Sidebar to start at boot, to do it, first create a shortcut of the sidebar.exe and the cut it. (Ctrl - x)

<img src="/posts/images/sidebar/shortcut.png" alt="Vista Sidebar" >

Now, navigate to your startup programs folder

(Its' located in: %appdata%\Microsoft\Windows\StartMenu\Programs\Startup)

Once there, place shortcut there.

> [!NOTE]
> If there is no Startup folder on the path, add it by going one dir up (%appdata%\Microsoft\Windows\StartMenu\Programs) and then create a folder called "Startup". Place it there


### Comparing
**WINDOWS VISTA STYLE**
<img src="/posts/images/sidebar/vista.png" alt="Vista Sidebar" >
**WINDOWS 7 STYLE (ORIGINAL)**
<img src="/posts/images/sidebar/7.png" alt="Vista Sidebar" >

P.D: I know we are on 2021, but Windows 7 is ❤ :D
