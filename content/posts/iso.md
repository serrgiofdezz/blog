---
title: Create an ISO File from a Folder in Windows
description:
toc: true
authors: [Sergio Fernández]
tags: []
categories: [Windows]
series: []
date: '2019-01-14T10:30:48+08:00'
lastmod: '2019-01-14T10:30:48+08:00'
featuredImage: ''
draft: false
---
An ISO file is a container that can hold a number of files. It’s usually used to create backups of your CD and DVD discs. However, you can create an ISO from the folders on your Windows PC as well.

## 1. Download the required software

I personally recommend the program "Folder2ISO". Download from [https://www.trustfm.net/software/utilities/Folder2Iso.php?page=Download](https://www.trustfm.net/software/utilities/Folder2Iso.php?page=Download)

Folder2Iso it’s a free and portable tool that helps quickly create ISOs. It works on many versions of Windows including Windows 7, 8, 10, and Linux.

## 2. Selecting the folder

<img src="/posts/images/tut/iso/folder2iso1.png" alt="app" >

When you open the app, you need to select the folder you want to convert to an ISO Image.

Once selected, select output and choose the folder where you’d like to save your ISO file

<img src="/posts/images/tut/iso/folder2iso2.png" alt="app 2" >

Click on the Generate ISO button to make an ISO out of your chosen folders.

<img src="/posts/images/tut/iso/iso.png" alt="Generated ISO" >

And it's done, you can open it and you will see all the files and sub-folder of the folder you selected before, but as an ISO file.

## Customizing ISO properties

Do you know you can customize your ISO file? You can set a ISO icon when mounted and to auto-run a executable file

First you will need to create a file called "autorun.inf" in the root directory of the folder that you will generate the ISO

<img src="/posts/images/tut/iso/root.png" alt="autorun" >

Open it in your preferred text editor and type:

```
[autorun]
OPEN=$PATH\TO\EXEC
ICON=$PATH\TO\ICON
```

If you want for example run a executable called Drivers.exe:

```
[autorun]
OPEN=Drivers.exe
ICON=Drivers.exe
```

> [!NOTE]
> If the file is on a subfolder, just add a `\`. For example: `OPEN=Folder\Drivers.exe`

<img src="/posts/images/tut/iso/root2.png" alt="drivers" >

Now convert to an ISO file with the tool. Mount it

<img src="/posts/images/tut/iso/iso_drive.png" alt="drivers" >

As you can see, it shows the icon of the executable, it will also auto-lunch the selected exec file we defined in the autorun file.
