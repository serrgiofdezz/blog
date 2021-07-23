---
title: A problem with the Windows Snipping Tool
description: This program saves the screenshots as “.PNG” instead “.png”, so let's fix it
toc: true
authors: [Sergio Fernández]
tags: []
categories: [Windows]
series: []
date: '2021-04-06T10:30:48+08:00'
lastmod: '2021-04-06T10:30:48+08:00'
featuredImage: ''
draft: false
---
Have you ever used Snipping Tool and realized that this program saves the screenshots as ".PNG" instead ".png"?

This sound a bit dumb but it might be really annoying for some users who uses this every day.

I managed to fix this big problem by editing the SnippingTool.exe

## 1. The Tools
The tool I used to fix this problem was HxD, this program is a fast hex editor. It offers features such as searching and replacing, exporting, checksums/digests...

I also needed a copy of SnippingTool.exe, which is located in C:\Windows\System32

Once I had the copy of SnippingTool.exe in the Desktop. I opened the exe with HxD program. Then I searched for the P, N and G letters.

## 2. Fixing the Problem
<img src="/posts/images/snipping/1.png" alt="Classic VS XPUI Design" >

As you can see there, i found these letters, and they are uppercase.

What I did is to replace these hex numbers in order to set png instead PNG

<img src="/posts/images/snipping/2.png" alt="Classic VS XPUI Design" >

I edited the number, and now as you can see in the decoded text tab, it says png

<img src="/posts/images/snipping/3.png" alt="Classic VS XPUI Design" >

Make sure to find all the PNG

NOTE: You can do this for the other filetypes in the app: (PNG, GIF, JPG)

For JPG just search and replace

<img src="/posts/images/snipping/5.png" alt="Classic VS XPUI Design" >

## 3. Replacing the File
Now it's edited I saved it, so the changes are saved in the Desktop SnippingTool.exe. Now i just moved to C:\Windows\System32

NOTE: If you want to do it, make sure to make a copy of the original Snipping Tool in case you mess it

NOTE 2: Make sure you Take Ownership of the System32 folder, because you won't be able to replace any file from that folder. You can get TakeOwnership for Windows 7 or 10

## 4. Success
<img src="/posts/images/snipping/4.png" alt="Classic VS XPUI Design" >
And now, you don't need to bother changing the PNG to png all the time you use this useful program.
Is funny how this problem is still present in Windows 10, this bug was there from the first time

<img src="/posts/images/snipping/Untitled.png" alt="Classic VS XPUI Design" >

It was also reported in Microsoft Community back in 2009 and the answer was "Delete the PNG and type in png" :/

If you need the modified SnippingTool.exe from Windows 7 Build 7001, i uploaded here, it should work in Windows 8,1 and 10 as I think they didn't even bother in modifying this program
