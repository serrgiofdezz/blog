---
title: Installing and Setting Up Windows 7 (2021 Edition)
description: Installing and configuring Windows 7 in 2021. It it worth it?
toc: true
authors: [Sergio Fernández]
tags: []
categories: [Windows]
series: []
date: '2021-01-01T10:30:48+08:00'
lastmod: '2021-01-01T10:30:48+08:00'
featuredImage: ''
draft: false
---
In this med-long blog I will be setting up Windows 7 in 2021. Have you got tired of Windows 10? Follow me and get rid of that version with full of telemetry

## 1. Downloading necessary files

The first thing we need is to download the Windows 7 ISO file. To do it, I highly recommend [Microsoft Windows and Office ISO Download Tool](https://www.heidoc.net/joomla/technology-science/microsoft/67-microsoft-windows-and-office-iso-download-tool). With this tool we will be able to download any Windows Version, including Windows 7, 8.1 and 10.

Once the program has been downloaded, open it and navigate to ***Windows 7 (Aug 2018)*** tab

> [NOTE]
> You can also download the original SP1 Windows 7 file. However I strongly recommend the Aug 2018 build as it contains the latest drivers and updates from Microsoft (like IE11 & .NET 4.7.2).

Select your preferred version (I recommend Professional) and then download it.

<img src="/posts/images/one.png" alt="Downloading ISO" >

Once downloaded, now we will burn the ISO into a USB.

First, get rufus [rufus.ie](https://rufus.ie).

Open the program and once opened, select the Windows 7 ISO file you downloaded, select GPT scheme, UEFI will be automatically selected in the other panel.

> [NOTE]
> If your machine doesn't support UEFI, just select MBR instead GPT, it will use the BIOS Mode.

> [WARNING]
> If you are going to proceed with UEFI mode (like me), you should know that Windows 7 doesn't natively support UEFI, make sure you have the CSM (Compatbility Support Mode) enabled in the BIOS.

> [NOTE]
> If your UEFI computer BIOS settings doesn't have the CSM option, you should find for "Legacy Boot", enable it. This applies for some HP computers like the ***Hp Elite 8xxx*** series. Enabling the legacy boot it will enable CSM when installing as UEFI.

<img src="/posts/images/two.png" alt="rufus" >

Wait until it finishes. Then you can safely close the program.

##### Optional but important too, looking for drivers

Before I start to install Windows 7, I recommend searching for Windows 7 drivers for my computer. I own a ***HP Elite 8300*** so finding the drivers is very easy.

<img src="/posts/images/three.png" alt="drivers 1" >

I downloaded just the important drivers, like the Ethernet Driver and the audio drivers.

> [!NOTE]
> You can search for Windows 10 drivers if your computer is really new.

##### Important
If you have a Nvidia Graphics Card, make sure to download the drivers too. Download it from [NVIDIA Driver Downloads](https://www.nvidia.com/Download/index.aspx)

Select the graphics card series and product, and then select the operating system version: Windows 7 64-bit

Grab the drivers and copy them on a USB. You can copy them on the same USB, just create a folder inside the root usb dir.

## 2. Installing Windows 7

Now, shut down the computer.

When turned off, turn on the PC and access the Boot Menu. Common keys for accessing the Boot Menu are Esc, F2, F10 or F12, depending on the manufacturer of the computer or motherboard., select boot options and select the USB device.

Now follow the installation until you get to "Type of Installation", select the second option: "Custom: Install Windows Only (advanced)".

<img src="/posts/images/inst1.png" alt="inst 1" >


In the following screen, it will show you all the partitions of the different disks you have in your computer.

<img src="/posts/images/inst2.png" alt="inst 2" >

Make sure you know where do you want to install Windows 7, if you only have one disk, then just delete all partitions from the disk and continue the installation. Otherwise be careful what you are deleting.

Wait until the installation finishes. Your computer may reboot while the process

### 2.1. Continuing installation

Once the files are placed into the disk, you will need to set up some quick things before you can start using Windows 7.

<img src="https://petri.com/wp-content/uploads/sites/3/install_win7_9-533x400.png" alt="inst 3" >

First, set up your name and desktop name

<img src="https://petri.com/wp-content/uploads/sites/3/install_win7_10-533x400.png" alt="inst 4" >

Create a password for your account.

You're almost there, Windows will ask for a key, you can skip this step if you don't have a product key. Then it will ask some final things like clock and Internet.

**DONE!**

<img src="/posts/images/initial.png" alt="Desktop" >

## 3. Installing drivers
As you can see in my image, there is no internet, no Aero Glass theme...

Now get the downloaded drivers you copied into an USB, and install them. Once you download them, you will have Internet access and the Nvidia drivers properly installed in Windows 7.

### 3.1. Checking for updates
The second thing you should do before starting enjoying Windows 7 is to check for all updates via Windows Update.

<img src="/posts/images/upd.png" alt="Updates" >

Select the updates you want to install and install them. It usually contains some missing drivers for computers.

### 3.2. Some final drivers
Windows 7 Compatibility is not as good as Windows 10, so you may have some problems with USB ports or devices, so let's check for missing drivers with [Snappy Driver Installer Origin](https://www.snappy-driver-installer.org/download/).

This tool searches for missing drivers and will install automatically for us. Extract the ZIP folder and open SDIO_x64_R729.exe inside the folder.

Once opened accept the license, then it will ask to download some drivers. Select the third option called "**Download Indexes Only**".

<img src="/posts/images/snappy1.png" alt="Updates" >

After the indexes are downloaded, the program will show all the drivers ready to update, you can check the drivers you want to update & install, or just select all from the left panel. Click ***Install*** and wait.

Reboot your machine once the drivers got updated.

## 4. Customizing Windows 7

### 4.1. Enabling Aero Glass Theme

On the desktop, right-click and select ***Personalize***

<img src="/posts/images/aero.png" alt="Aero Glass" >

Select Windows 7 from the Aero Section.

### 4.2 Installing Useful Programs for a Better Experience
#### Check [Guide - Useful Programs for a Better Windows 7 Experience](/posts/programs7/)

And you're done, you successfully installed Windows 7 in your computer.

In my opinion Windows 7 looks better than Windows 10 with the transparency, called Aero Theme. Or maybe is just me who got tired of the clean Windows 10 look.

I hope you find this tutorial easy to follow, if you have any questions just ping me at [sergio@bbjprojek.org](mailto:sergio@bbjprojek.org) and I'll answer any doubts and questions :D

Happy 2021!

-----------

### External Tools you may need

1. [Windows & Office Enabler](https://wiki.bbjprojek.org/#/more/windows?id=office)
2. [ADB & Fastboot](https://wiki.bbjprojek.org/#//more/windows?id=adb-amp-fastboot)
3. [More Tools](https://wiki.bbjprojek.org/#//more/windows?id=more-useful-programs)
4. [WinRAR](https://wiki.bbjprojek.org/#//more/windows?id=winrar)
5. [Programs for Windows 7](/posts/programs7/)
