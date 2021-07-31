---
title: Enable Windows 7 Style on Windows 8.1
description:
toc: true
authors: [Sergio Fernández]
tags: []
categories: [Windows]
series: []
date: '2020-12-30T10:30:48+01:00'
lastmod: '2020-12-30T10:30:48+01:00'
featuredImage: ''
draft: false
---
## Screenshots
<img src="/posts/images/tut/7style/preview.png" alt="windows 8.1" >

## Guide
### Step 1. Downloading files

[Download ZIP File (373MB)](https://drive.google.com/file/d/1-lbkJ1P9Tnkc89STRlJ76oBIioLzhl67/view?usp=sharing) // [Mirror](http://cloud.educa.madrid.org/index.php/s/GP1h0AXabO6AtRl/download)

> [!NOTE]
> Extract the zip in a safe folder like Documents, don't delete the folder or you'll break some things later

<img src="/posts/images/tut/7style/files.png" alt="Explorer" >

### Step 2. Running the Aero Glass Setup File
**Path: Aero Glass Setup\setup-w8.1-1.2.5.exe**

In installation uncheck "Install Theme"

### Step 3. Installing Required Files from "Windows Aero 8.1.1v2.3" folder
##### Step 3.1. Install UxStyle
**Path: Windows Aero 8.1.1v2.3\Required\UxStyle\UxStyle_sep23_x86_x64_Windows8.1.exe**

##### Step 3.2. Add AeroGlass Registry File
**Path: Windows Aero 8.1.1v2.3\Required\AeroGlass_Settings.reg**

##### Step 3.3. Install Aero W7 Themes
First go to Themes Folder (Windows Aero 8.1.1v2.3\Themes)
Then select the "Recommended Ones Only (Commandbar ui based)" folder

Copy all files inside that folder and paste them on **"C:\Windows\Resources\Themes"**

Open Personalize > Select Windows 7 theme, apply it

### Step 4. Installing Windows 7-like Explorer
##### Step 4.1 Open OldNewExplorer
**Path: OldNewExplorer\OldNewExplorerCfg.exe**

Select all except "Use Alternate navigation buttons style" and "Show Status Bar"

<img src="/posts/images/tut/7style/explorer.png" alt="Explorer" >

Apply it, close all Explorer Windows, and re-open it

### Step 5. Opening CustomizerGod
##### Step 5.1 Change Some Icons (like: Ethernet Icons, Windows Drive Icon and ! and ? icons) These files to replace are on Windows 7 Pack folder

> [!WARNING]
> If your Windows 8.1 is suddenly unlicensed after this, open CustomizerGod, then Tab the three lines icon at the bottom, and then tap Restore Backup > All System Files. Once completed, reboot the computer
>
> Some people reported that is "Branding Logo" file that causes Windows 8 to be unlicensed, try not to replace that image

### Step 6. Install ClasicShell (Disable IE installation)
##### Step 6.1 Adding Windows 7 Start Icon
Open Classic Start Menu Settings. Then Enable Show All Settings. Go to **Start Button** tab > Replace Start Button > Select Start Button icon in Windows 7 Pack Folder

##### Step 6.2 Get Windows 7 Start Menu Appearance
Get WIN7LIKE\WIN7LIKE.skin7 from the downloaded file. Open Classic Start Menu Settings. Go to **Skin** tab and copy to C:\Program Files\Classic Shell\Skins

**Classic Start Menu Settings**
##### Step 6.2.1 WIN7LIKE

Get WIN7LIKE\ **WIN7LIKE.skin7** file Skin and copy to C:\Program Files\Classic Shell\Skins

Then Restart ClassicShell and go to Settings > Skin > WIN7LIKE. Set the Glass Color to High

**More Start Menu Config**
- Menu Look > Main Menu Animation=NO / Enable Aero Glass=YES
- Windows 8.1 Settings > Skip Metro screen=YES // Disable active corners=ALL
- Taskbar > Taskbar Look=OPAQUE
- Main Menu > Max Recent Programs=6 (As your wish)
- Search Box > Search The System Path=NO // Match parts of words=NO

**Classic Explorer Settings**
Open Settings For Explorer and select Show All Settings:

- Status Bar > Show Status Bar=NO
- Toolbar Options > Drag all into the right panel except "SEPARATOR"

### Step 7. Setting up Custom Blur
#####  Step 7.1 Install AGBlurTweaker
**Path: AGBlurTweaker.exe**

Apply the following settings:
```
Blur Deviation Amount > 15
Radius of Windows Corners > 12 (DEFAULT)
Active Color Balance > 40
Inactive Color Balanca > 0 (null)
Active Blur Balance > 50
Inactive Blur Balance > 0 (null)
Glass Reflection Intensity > 100
Theme Resource > DONT TOUCH IT // 0 (null)
```

### Credits
**VIDEO:** https://www.youtube.com/watch?v=SISUMjSrLJM&t=2114s
