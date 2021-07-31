---
title: Install Windows 8.1 alongside Windows 10
description: Installing Windows 10 and windows 8.1 version of the Microsoft Operating system via UEFI.
toc: true
authors: [Sergio Fernández]
tags: []
categories: [Windows]
series: []
date: '2020-10-20T10:30:48+01:00'
lastmod: '2020-10-20T10:30:48+01:00'
featuredImage: ''
draft: false
---
<img src="/posts/images/tut/W10.png" alt="windows 10" >
<img src="/posts/images/tut/W8.png" alt="windows 8.1" >

Installing Windows 10 and windows 8.1 version of the Microsoft Operating system is really easy as they both support Windows Boot Manager via UEFI.

In this post I'll show you how to install both versions of Windows in your PC (UEFI).

## 1. Prerequisites:
* At least 1 USB device (2 recommended).
* A Windows system.
* An UEFI PC (for the installation).
* A disk drive (2 recommended).

## 2. Downloading necessary files
First, we're going to download Windows 10 and Windows 8.1 ISO files.

For Windows 10, [Download Windows 10 ISO](https://www.microsoft.com/software-download/windows10ISO), if you can't download directly the ISO file, in your browser press F12 and tap mobile version, refresh the page. You should be able to download the ISO file of Windows 10.

<img src="/posts/images/tut/downloadiso.png" alt="windows 10 webpage" >

For Windows 8.1, just [Download it from here](https://www.microsoft.com/software-download/windows8ISO)

Once downloaded both versions, you will need a program called Rufus, download it from [rufus.ie](https://rufus.ie).

## 3. Burning the ISO File
Download and install it, once opened, select the Windows 10 ISO file you downloaded, select GPT scheme, UEFI will be automatically selected in the other panel.

<img src="/posts/images/tut/rufus10.png" alt="rufus windows 10" >

> [!NOTE]
> Make sure "Standard Windows installation" is selected.

Tap Start and wait until it finishes.

If you have another USB device, disconnect the Windows 10 installation USB and connect the other USB, now select Windows 8.1 ISO file instead, same options goes for this USB.

<img src="/posts/images/tut/rufus8.png" alt="rufus windows 10" >

Tap "Start".

Once you have both USB devices, let's check the disk you have in the computer you're going to install both Windows version.

If your computer have windows:
Go to Windows > Search > Create and forma hard disk partitions.

Take a look at your disks:

<img src="/posts/images/tut/partitionsfinal.png" alt="partitions" >

**For Ubuntu instead**:

Open the Disks program

<img src="/posts/images/tut/partitionsU.png" alt="partitions" >

## 4. Checking computer disks
If you're installing Windows 10 and Windows 8.1 in the same disk, you'll need to shrink your disk (or create the new partitions if the disk drive is unallocated):

**Shrinking**: If you're in Windows: select the disk and select shrink, write the kB you want for the partition, I recommend setting the half of your disk so if you have a 480GB disk, you'll have 240GB for Windows 10 and another 240GB for 8.1.

<img src="/posts/images/tut/shrinking.png" alt="partitions" >

> [!NOTE]
> If you don't have windows in that PC, you can use **diskpart** to shrink the disk later at the installation. See [Shrink a basic volume](https://docs.microsoft.com/en-us/windows-server/storage/disk-management/shrink-a-basic-volume)

> [!TIP]
> You can open command prompt on a Windows Installation by pressing SHIFT + F10"

If you're installing in different disks, just note the disks you'll have been installing.

## 5. Installing Windows 10
Time to boot a USB drive (Windows 10).

When turned off, turn on the pc and access the Boot Menu. Common keys for accessing the Boot Menu are Esc, F2, F10 or F12, depending on the manufacturer of the computer or motherboard., select boot options and select the USB device.

Now follow the installation until you get to "Type of Installation", select the second option: "Custom: Install Windows Only (advanced)".

> [!TIP]
> You can open command prompt on a Windows Installation by pressing SHIFT + F10".

<img src="/posts/images/tut/inst1.png" alt="setup 1" >

In this screen, it will show you all the partitions of the different disks you have in your computer.

### 5.1 Selecting disk for installation
Select the partition you want:

> [!NOTE]
> In the case you are installing on your shrinked disk, select that partition, it should be called Disk 0, Partition 1,make sure that disk have another partition with similar size, as I explained earlier (the partition we created for Windows 8.1).


<img src="/posts/images/tut/diskssetup.png" alt="setup 2" >

> [!WARNING]
> If you're installing in different disk, make sure to remove any other partitions on that disk. [UEFI partition will be auto created].

Continue the installation.
### 5.2 Setting up Windows 10

Once you are in Windows 10, you can set up some things with this tutorial. [Windows Configuration](/more/windows.md).

If you burned Windows 8.1 ISO, now continue to [Installing Windows 8.1](guides/windows8?id=_7-installing-windows-81), if don't, now it's time to burn it in the USB you burned Windows 10, to do: download Rufus and the Windows 8.1 iso. [Seen here](guides/windows8?id=_3-burning-the-iso-file).

On Windows 10, open disk and partitions tool, and note the disk and partition for the Windows 8.1 installation.

## 6. Installing Windows 8.1
Power on the pc and access Boot Menu, select your Windows 8.1 installation USB. Follow the instructions until you get to "Type of Installation"

### 6.1 Selecting disk for installation
Select "Custom: Install Windows Only" and select your partition

In case you're installing in the same disk, select the second partition of the disk that you installed Windows 10

If installing in different disk, remove all the partition of that disk (if applicable), and install

Continue to installation.

On the first reboot of the installation, Windows Boot Manager should have added both entries (10 and 8.1) on the menu list.
Select Windows 8.1 to finish the installation.

<img src="/posts/images/tut/wbmc.png" alt="Windows Boot Manager" >


Once you finish the Windows 8.1, you're ready to go.

## 7. Customizing the Windows Boot Manager options

You can customize the Windows boot options by opening msconfig (Win + R) then type msconfig.

<img src="/posts/images/tut/msconfig.png" alt="msconfig" >

You can set the default OS to boot and the timeout for it to start.

## F.A.Q
### Avoiding a computer restart when selecting non-default operating system
You may notice if you select windows 8.1 while Windows 10 is your default system, the computer will restart after selecting it, then it will boot.

The reason for two reboots is that the Windows 8 bootloader boots into a pre-boot environment which is like a mini operating system, before it shows the boot menu. When you choose Windows 7, your PC needs to be rebooted to unload this preboot OS environment of Windows 8 and then load Windows 7. Well, now you know how to improve your dual boot experience.

##### Step 1. Enable Legacy Mode
<img src="https://winaero.com/blog/wp-content/uploads/2013/11/Legacy-Boot-Loader.png" alt="legacy bootloader" >

The first option is to enable the legacy boot menu mode. Instead of the graphical bootloader, you can enable the classic text-based boot loader which shows a list of bootable OSes.

```cmd
bcdedit /set "{current}" bootmenupolicy legacy
bcdedit /set "{default}" bootmenupolicy legacy
```

To return to the default bootloader:

```cmd
bcdedit /set {default} bootmenupolicy standard
```

**Source:** https://winaero.com/how-to-avoid-two-reboots-with-windows-8-1-and-windows-7-dual-boot/

##### Step 2. Disable Fast-Startup
If you don't disable the fast-startup, the PC will be anyways booted to the pre-environment Windows Boot Loader from the last system you used, and will require a restart if you select the other operating system.

Go to Control Panel, select "Hardware and Sound" and then "Power Options". In the left panel, select "Choose what the power buttons do". Once there.

<img src="/posts/images/tut/fast.png" alt="Fast Startup" >

Click "Change settings that are currently unavailable"

Now disable "Turn on fast startup (recommended)".

<img src="/posts/images/tut/fast3.png" alt="Fast Startup" >

Click Save changes and you're done.

##### What does Fast Startup does?
Check this video.

<iframe src="https://www.youtube.com/embed/C1ecCjj0KWc?start=292" </iframe>
