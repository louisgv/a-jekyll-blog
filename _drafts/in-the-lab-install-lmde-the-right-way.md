---
layout: post
title: 'In the lab: install LMDE'
tagline: v0.0.9
date: '2015-08-16 17:35'
tags:
  - lmde
  - tutorial
categories:
  - linux
---

A tutorial on installing LMDE the way we have done it in our lab.

# Preparation

This tutorial requires a spare PC (spare means you are allowed to make a `Will it blend` video with it). Wise guy should try first with a virtual machine (VM). Recommended setup for a VM is a simple Linux VDI with 1GB of RAM and 10GB of memory.

Get the LMDE disc [here](http://www.linuxmint.com/download_lmde.php).

+ If **using VM**, search for a tutorial on how to setup the iso.
+ If **using a real machine**, make a bootable USB.
  + On Linux, use `dd`
  + On Windows, make sure you use `Universal USB Booting`, not `YUME` since YUME is designed to test the distro, not to install.

# Path Definition

In the lab, tons of data are separated from the main operating system (OS), such that even when the OS is down, the data is still safe and sound. Drive partitioning the right way will allow future recovery, backup and upgrade session pain-less.

Partitioning works only when one are aware of the following `important path`:

```
  --- BASIC
  '/' : The $ROOT path. This path contains everything.
  '/home' : The $HOME path where all your data, node_modules, go, etc... should reside.
  '/tmp' : The $TMP path where all temporary files should reside.

  --- BOOT
  '/boot' : The $BOOT path comprise your boot images (vid and img)
  '/boot/efi' : The $EFI path contains software that take care of dealing with your UEFI system.

  --- EXECUTABLE
  '/usr' : The $USER path. Any configuration and packages installed for all user resides here
  '/bin' : The $BIN path contains only binary program that can be called.
  '/usr/sbin' : The $SBIN path contains program that only super user (sudo) can call
  '/usr/bin' : The $UBIN path contains programs that all user can call
  '/opt' : The $OPT path contains optional programs installed by the user. Programs resides here is not depended by the OS and are generally stand-alone.

  --- CONFIG
  '/etc' : The $ETC path contains system-wise setting for devices, programs, booting, etc...

```

# Partition Schema

In the lab, we use GPT partition table as it offers more than just 4 primary



+ For ease of use, make your $HOME double the size of your $ROOT.

+ Installing software packages outside library in your $ROOT only when it's related to the system, and you would be safe and sound. The best thing about this setup, is that all your work-related software are safe and sound even if the main system suddenly die because you tried to install glib and it outright kill your system right in front of your eye.

+ Installing rEFInd
+ Copy rEFInd to /boot

# Customization
