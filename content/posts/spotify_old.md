---
title: Get Old Spotify UI back (Permanent)
description:
toc: true
authors: [Sergio Fernández]
tags: []
categories: [Windows, Spotify]
series: []
date: '2021-07-14T10:30:48+08:00'
lastmod: '2021-07-14T10:30:48+08:00'
featuredImage: ''
draft: false
---
The new Spotify look is nice, but everything is shifted around. This makes navigating Spotify awful. Fortunately, there is a way to get the old Spotify back.

<img src="/posts/images/spotify/classicVSxpui.png" alt="Classic VS XPUI Design" >

*Classic VS XPUI Design*

## Step 1. Downloading and Installing Old Spotify Version
First, you will need to install and old Windows Spotify version of Spotify, 1.1.51.380 works for the new and the old design.

* [Download Spotify 1.1.51.380 (Uptodown)](https://spotify.en.uptodown.com/windows/download/3173791) / [Google Drive Mirror](https://drive.google.com/file/d/1Le-xGlZvI9ZN9we46QSSU4mWgReXyBnm/view?usp=sharing)

Once download, install the program. When Spotify opens, close the window.

## Step 2. Block Automatic Updates

Go to your AppData folder, by opening Windows Explorer. Then navigate to **C:\Users\YOURUSERNAME\AppData\Local\Spotify**

<img src="/posts/images/spotify/local.png" alt="Spotify Local Folder" >

Once there, create a new folder called **Update**. Now open the new folder properties and navigate to **Security** tab.

<img src="/posts/images/spotify/props.png" alt="Properties" >

Tap **Edit** and then deny full control for all users and administration, including **SYSTEM**, click Apply and exit.

<img src="/posts/images/spotify/denying.png" alt="Deny permissions" >

Now Spotify won't able to update the Spotify App and you will never get newest Spotify versions which removed old UI

### Step 3. Enabling Classic UI

This version have the XPUI design as default, but still have the old UI resources, so just need to enable it.

Navigate to **C:\Users\YOURUSERNAME\AppData\Roaming\Spotify**

Find the file called **prefs**

<img src="/posts/images/spotify/roaming_folder.png" alt="prefs file in Roaming folder" >

Open the file (with notepad or any other text editor).

You will see some properties, just go the end of the file, and create a new line with the following text:

```prefs
ui.experience_override="classic"
```

<img src="/posts/images/spotify/prefs.png" alt="prefs file in Roaming folder" >

Save the file and exit.

Now open Spotify, sign in, and done! You now have the old Spotify UI, with better tools, key shortcuts, and in my opinion, a better design

-------
