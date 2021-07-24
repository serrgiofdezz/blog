---
title: Installing Windows 11 on unsupported machines
description: In this guide I will be installing Windows 11 on a unsupported PC, I will be using a HP Elite 8300 which has an Intel i5 3rd gen, TPM 1.2...
toc: true
authors: [Sergio Fernández]
tags: []
categories: [Windows]
series: []
date: '2021-07-10T10:30:48+08:00'
lastmod: '2021-07-10T10:30:48+08:00'
featuredImage: ''
draft: false
---
<img src="https://cdn.computerhoy.com/sites/navi.axelspringer.es/public/styles/1200/public/media/image/2021/06/windows-11-2372815.jpg" alt="Windows 11 Desktop" >

In this guide I will be installing Windows 11 on a unsupported machine, I will be using a **HP Elite 8300** which has an Intel i5 3rd gen, TPM 1.2...

This Elite 8300 supports UEFI and Secure Boot, also pass the RAM and GHz requirements, you can bypass these ones too but I would recommend to have 8GB or more RAM for Windows 11 (or any machine running in 2021-2022).

## 1. Getting the Insider Preview file

First, you will need to get the ISO file.
Go to [UUP Dump](https://uupdump.net/) webiste and scroll to **Latest Dev Channel Build**

<img src="/posts/images/tut/win11/guides/devchannel.png" alt="Downloading ISO" >

Now select the architecture (x64) and then select the update you will see on the screen.

Once selected that, confirm your ISO language.

You’ll then see a list of Editions screen with a Windows 10 editions checklist. Select the edition you want to install and click next.

<img src="/posts/images/tut/win11/guides/build.png" alt="Downloading ISO" >

On the next screen, select the ‘Download and convert to ISO’ option under Download method section, and under Conversion options leave the default option as is.

<img src="/posts/images/tut/win11/guides/build2.png" alt="Downloading ISO" >

## 2. Building the ISO file

The download package will be downloaded on your PC. It’ll be a ZIP file so extract it in a separate folder (for easier access).

Among the extracted files from the ZIP package, double-click on the uup_download_windows.cmd file.

<img src="/posts/images/tut/win11/guides/filedown.PNG" alt="Downloading ISO" >

A command prompt window will open and it’ll probably ask admin permission to run the scripts to download and generate a Windows 11 Preview ISO. Make sure you give it the permission to do so.

When the script is executed, you can monitor the progress in the CMD window. It might take some time to finish the process.

Once completed, the Windows 11 ISO file will be saved to the same folder where you extracted the package files of the UUP package.

<img src="/posts/images/tut/win11/guides/fileISO.PNG" alt="Downloading ISO" >

Once you have the Windows 11 ISO, you can either create a bootable USB drive with it or mount it on your computer and run the ‘Setup’ file from the Windows 11 ISO to install the update on your system.

## 3. Burn to USB

Now let's burn the ISO into a drivers.

First, get rufus [rufus.ie](https://rufus.ie).

Open the program and once opened, select the Windows 11 ISO file, select GPT scheme, UEFI will be automatically selected in the other panel.

> [!NOTE]
> If your machine doesn't support UEFI, just select MBR instead GPT, it will use the BIOS Mode. **NOTE: I haven't tested Windows 11 in Legacy Mode**

<img src="/posts/images/two.png" alt="rufus" >

Wait until it finishes. Then you can safely close the program.

## 4. Running Setup

If you are attempting to install Windows 11 and receive a message stating, "This PC can't run Windows 11," it is likely that you don't have a TPM 2.0 installed or enabled.

<img src="/posts/images/tut/win11/guides/tpm/1.jpg" alt="unsupported" >

When you see the above message, press Shift+F10 to launch cmd. Now type *regedit* and press enter to launch the Registry Editor.

When the Registry Editor opens, navigate to **HKEY_LOCAL_MACHINE\SYSTEM\Setup**, right-click on the Setup key and select **New > Key**.

When prompted to name the key, enter **LabConfig** and press enter.

Now right-click on the LabConfig key and select **New > DWORD  (32-bit)** value and create a value named **BypassTPMCheck**, set the value to 1. Also create the **BypassRAMCheck** and **BypassSecureBootCheck** values if necessary.

Once you configure the value(s) under **LabConfig**, close the Registry Editor and the Command Prompt.

<img src="/posts/images/tut/win11/guides/tpm/2.jpg" alt="cmd" >

You will now be back at the message stating that the PC can't run Windows 11. Click on the back button in the Windows Setup dialog, as shown below.

<img src="/posts/images/tut/win11/guides/tpm/3.jpg" alt="back" >

Now tap next again and you will go to the next page to install Windows 11. Now continue installation.

## 5. Continue installation

Now you should select the partition and disk to install Windows, same as older Windows version, once selected, wait until it finishes... And enjoy Windows 11!
