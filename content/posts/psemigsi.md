---
title: How To Build PsemiGSI
description: Build Guide for treblized A-only and AB devices
toc: true
authors: [Gabriel Howard]
tags: [linux, semigsi]
categories: [Linux, Android]
series: []
date: '2018-10-20T10:30:48+01:00'
lastmod: '2018-12-31T10:30:48+01:00'
featuredImage: ''
draft: false
---
### Build Guide for treblized A-only and AB devices

**DOWNLOAD IMAGES FROM:** https://developers.google.com/android/images

## 1. Installing dependencies

```
sudo apt-get update
sudo apt-get install p7zip-full p7zip-rar
sudo apt-get install simg2img
sudo apt-get install git
```

## 2. Extract factory image and get system.img, place on any folder and run:

```
simg2img system.img system.img.raw

mkdir ~/AndroidWorkspace
cd ~/AndroidWorkspace
git clone https://github.com/erfanoabdi/Capire-Le-Treble.git
git clone https://github.com/erfanoabdi/P_semiGSI.git
git clone https://github.com/erfanoabdi/ROM_resigner.git
git clone https://github.com/LineageOS/android_build.git -b lineage-16.0

mkdir system
cd system
```

To mount the image, go to system.img.raw image folder

```
sudo mount -o,noatime system.img.raw ~/AndroidWorkspace/system
```

## 3A. Build for A-Only

```
cd ~/AndroidWorkspace/Capire-Le-Treble/Extra
sudo ./sGSI-ify.sh ~/AndroidWorkspace/system/system 2147483648 ~/AndroidWorkspace/sGSI_A.img
```

Wait until you see: “Press any key to continue”

Open new tab, then:

```
cd ~/AndroidWorkspace/ROM_resigner
sudo python resign.py ~/AndroidWorkspace/Capire-Le-Treble/Extra/tmp/system ~/AndroidWorkspace/android_build/target/product/security
cd ~/AndroidWorkspace/P_semiGSI/systemimgmaker
sudo ./make.sh ~/AndroidWorkspace/Capire-Le-Treble/Extra/tmp/system
```

Back to older and Press any key to exit

## 3B. Build for A-Only

```
cd ~/AndroidWorkspace/Capire-Le-Treble/Extra
sudo ./sGSI-ify_ab.sh ~/AndroidWorkspace/system 2147483648 ~/AndroidWorkspace/sGSI_AB.img
```

Wait until you see: “Press any key to continue”

Open new tab, then:

```
cd ~/AndroidWorkspace/ROM_resigner
sudo python resign.py ~/AndroidWorkspace/Capire-Le-Treble/Extra/tmp/system/system ~/AndroidWorkspace/android_build/target/product/security
cd ~/AndroidWorkspace/P_semiGSI/systemimgmaker
sudo ./makeab.sh ~/AndroidWorkspace/Capire-Le-Treble/Extra/tmp/system
```

Back to older and Press any key to exit

## Fixes
### SELinux folder (by GabrielHoward)

* [Downlaod](http://cloud.educa.madrid.org/index.php/apps/files/?dir=/&fileid=19739779)
* Path: AndroidWorkspace / capire-le-treble / extra / tmp / system / etc

Remove selinux folder and replace with the new one

Give permission to tmp folder:

```
sudo chmod -R 777 tmp
```

### Error unexpected (in building..):
go to: Android WorkSpace / P semiGSI / systemimgmaker / in.sh

put a ! in front of # (should be like this: #!/bin/bash)

Notes made by Gabriel Howard, based on Erfan Abdi’s work
