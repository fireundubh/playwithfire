---
title: How to Fix Scarlett 6i6 2nd Gen Crackling, Popping, Clicking, or Skipping During Playback
description: 
published: true
date: 2020-10-31T05:54:01.760Z
tags: 
editor: markdown
dateCreated: 2020-10-31T05:54:01.760Z
---

> This post is for owners of the [Scarlett 6i6 2nd Gen](https://focusrite.com/usb-audio-interface/scarlett/scarlett-6i6) audio interface.
{.is-info}

If you have Focusrite Control 2.3.4 or 2.4.x installed, you may experience crackling, popping, clicking, or skipping during audio playback in some games and other media software.

> This post was written when Focusrite Control 2.4.x was the latest driver series available. As of October 2020, Focusrite Control 3.6.0 is the latest driver and may not exhibit the same issues.
{.is-warning}

Here's how to solve this problem on Windows 10.

> **BEFORE YOU DO ANYTHING:** Open Focusrite Control and ensure you've set up the device the way you want (e.g., bitrate, routing.) If you follow these instructions, you will not be able to change these settings later unless you revert this whole process and go back to the broken driver.
{.is-warning}

Let's get started.

# Device Manager

1. Open the Windows Device Manager. You can search for "device manager" in the Windows search box and click the resulting link. (See: [Locating the search box in Windows 10](https://support.microsoft.com/en-us/help/4028221/windows-locating-the-search-box-in-windows-10))
2. In _Audio Inputs and Outputs_, right-click each Focusrite endpoint and uninstall. Delete device drivers if prompted. We do this first because these endpoints are controller dependencies. Windows will refuse to uninstall the controller in Step 3 if they remain installed.
3. In _Sound, Video and Game Controllers_, right-click each Focusrite controller and uninstall. Delete device drivers if prompted. You don't want Windows to reinstall them again.

# Programs and Features

1. Open Windows Programs and Features. You can search for "uninstall a program" in the Windows search box and click the resulting link. (See: [Locating the search box in Windows 10](https://support.microsoft.com/en-us/help/4028221/windows-locating-the-search-box-in-windows-10))
2. Uninstall Focusrite or Scarlett software. Use the search bar at the top right of the window to filter the list.

# Scarlett MixControl

Install [Scarlett MixControl 1.8](https://customer.focusrite.com/support/downloads?brand=Focusrite&amp;product_by_type=506&amp;download_type=all) for the Scarlett 6i6 1st Gen. (Yes, despite the fact you have a 2nd gen.)

This version installs Focusrite USB 2.0 Audio Driver 2.5.1, which works on the 2nd gen device.

# Back to the Device Manager

1. Open the Windows Device Manager again.
2. Click the Action dropdown menu and select the "Scan for hardware changes" option.
3. At this point, Windows should automatically install all the devices you need.
4. If all goes well, in _Audio Inputs and Outputs_, you should have the following endpoints:
   - "Microphone (Scarlett 6i6 USB)" and
   - "Speakers (Scarlett 6i6 USB)."
5. In _Sound, Video and Game Controllers_, you should have two "Scarlett 6i6 USB" controllers.
6. In _Other Devices_, you should have "Focusrite Control."
7. One of the controllers and "Focusrite Control" should have warning icons. This is usually bad advice, but in this case, Windows doesn't know what it's talking about, so ignore them!

We're almost finished.

# Services

1. Open Windows Services. You can search for "services" in the Windows search box and click the resulting link. (See: [Locating the search box in Windows 10](https://support.microsoft.com/en-us/help/4028221/windows-locating-the-search-box-in-windows-10))
2. Scroll down to the Windows Audio Endpoint Builder service. Right-click the service and click Restart. Click Yes when prompted to restart the Windows Audio service, too.</li>
3. *Alternatively*, download [HeSuVi](https://sourceforge.net/projects/hesuvi/) and restart the audio service from the Actions menu.

You're good to go.