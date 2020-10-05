---
title: Buffout 4 FAQs
description: 
published: true
date: 2020-10-05T08:32:54.340Z
tags: 
editor: markdown
dateCreated: 2020-10-03T05:50:57.305Z
---

# Basics

## Purpose

Buffout "fixes engine bugs and adds a crash logger to the game." [Here's a list of fixes.](https://github.com/Ryan-rsm-McKenzie/Buffout4/blob/master/Buffout4.toml)

## About the Developer

Buffout was created by Fudgyduff a.k.a. Ryan. It is [available on the Nexus.](https://www.nexusmods.com/fallout4/mods/47359)

## Requirements

- [F4SE](https://f4se.silverlock.org)<br>Extract contents of the `f4se_0_06_21` folder to the folder containing `Fallout4.exe`
- [Address Library](https://www.nexusmods.com/fallout4/mods/47327)<br>Extract contents to `Fallout 4\Data` folder
- [xSE PluginPreloader F4](https://www.nexusmods.com/fallout4/mods/33946)<br>Extract `IpHlpAPI.dll` and `xSE PluginPreloader.xml` to the folder containing `Fallout4.exe`

### Redistributables

- [Intel TBB Redistributable](https://www.nexusmods.com/fallout4/mods/47359?tab=files)<br>Extract `tbbmalloc.dll` to the folder containing `Fallout4.exe`
- [Microsoft Visual C++ Redistributable for Visual Studio 2019](https://support.microsoft.com/en-us/help/2977003/the-latest-supported-visual-c-downloads)<br>Run `vc_redist.x64.exe`

# Questions

## Where do I find the crash logs?

In `%USERPROFILE%\Documents\My Games\Fallout4\F4SE`, you should find `crash`-prefixed `.log` files.

## The game crashed, but I don't have any crash logs.

If the game crashed and no crash log was generated, Buffout could not capture the exception for any number of reasons. There are two relatively easy things you can try instead:

1. Check the System log in the Windows Event Viewer for Error and Critical events whose timestamps coincide with the time the game crashed. If you have such events, these events may provide clues for further investigation.
2. For more technical users, install [DebugDiag](https://www.microsoft.com/en-us/download/details.aspx?id=58210) from Microsoft. Create a crash rule for the `Fallout4.exe` process that logs the stack trace, activate the crash rule, and run the game until you crash. This will produce a detailed log that can be analyzed in DebugDiag and shared.

## How do I read crash logs?

You need a background in programming, debugging, and reverse engineering (RE). Specifically, you need to know assembly, C types, and be familiar with the stack concept. You must also have the tools and skills to load the executable; identify the involved subroutines, logic, and parameters; and statically analyze the stack trace to make your best guess at the error.

There are no easy answers and no easy explanations. There are many gotchas and exceptional cases that require a technical investigator to rule out. Buffout's crash logs are not intended for most users; they are specifically for Ryan and anyone else in the RE community. 

## Should I post my crash log? My game is heavily modded.

Yes. Always post your *entire* crash log. Please use spoiler tags or [Pastebin](https://pastebin.com).

# Configuration Issues

## Couldn't load plugin, or Error 126

This error typically indicates that `tbbmalloc.dll` was not installed or not installed to the correct location. Ensure `tbbmalloc.dll` is present in the folder containing `Fallout4.exe`.

## F4SE failed to inject the DLL

Verify that your preloader config specifies the correct load method.

In `xSE PluginPreloader.xml`, change the load method to `OnThreadAttach` or `ImportAddressHook`.

> Mod Organizer 2 users should change the load method to `OnThreadAttach`.
{.is-info}

To change the load method, edit the `Name` attribute value in the XML file, like so:

```xml
<LoadMethod Name="OnProcessAttach">
...
</LoadMethod>
```

Or:

```xml
<LoadMethod Name="OnThreadAttach">
...
</LoadMethod>
```

# Upstream Issues

## d3d11.dll

ENBSeries, Load Accelerator, and some other mods are distributed with modified versions of `d3d11.dll`. Some `d3d11.dll` crashes are attributable to these mods, which should be fixed by their developers.

For example, in the most recent and only frame of this probable call stack, we see the faulting module is `d3d11.dll` (imagebase: `0x180000000`) at offset `+0128CB0` (address: `0x180128CB0`).

```
PROBABLE CALL STACK:
	[0] 0x7FFE12EE8CB0 d3d11.dll+0128CB0
```

The original assembly exits at `+1FAE0`, leaving us with an address space extending from `0x180001000` to `0x18001FAE0`. Our probable call stack above points to an address far outside the module's address space, which indicates we're dealing with a modified assembly.

If you see `d3d11.dll` in your probable call stack, amend your crash report to point out whether you have ENBSeries, Load Accelerator, or another mod that uses a modified version of `d3d11.dll`.

> **Note:** Load Accelerator users should be using [High FPS Physics Fix](https://www.nexusmods.com/fallout4/mods/44798), which avoids modifying `d3d11.dll`.
{.is-info}


## flexRelease_x64.dll

Fallout 4 implements a defunct version of [NVIDIA FleX](https://developer.nvidia.com/flex) for weapon debris and other particle effects.

Disable FleX entirely by adding the following lines to `fallout4custom.ini`:

```ini
[NVFlex]
bNVFlexEnable=0
bNVFlexInstanceDebris=0
bNVFlexDrawDebris=0
```

> Some crashes not logged by Buffout can be traced to not having FleX disabled.
{.is-info}

## nvwgf2umx.dll

The `nvwgf2umx.dll` assembly belongs to the NVIDIA driver package. Most likely, you recently updated your video drivers, and unfortunately, the `445` driver series appears to cause crashes in many games.

These crashes usually have a probable call stack where `nvwgf2umx.dll` occupies the most recent 20 frames. For example:

```
PROBABLE CALL STACK:
	[ 0] 0x7FFE8A8A8682 nvwgf2umx.dll+0628682  // NVIDIA
	[ 1] 0x7FFE8A8AA487 nvwgf2umx.dll+062A487  // NVIDIA
	[ 2] 0x7FFE8A8AF786 nvwgf2umx.dll+062F786  // NVIDIA
	[ 3] 0x7FFE8A8B2804 nvwgf2umx.dll+0632804  // NVIDIA
	[ 4] 0x7FFE8A8B2C1A nvwgf2umx.dll+0632C1A  // NVIDIA
	[ 5] 0x7FFE8A8B311D nvwgf2umx.dll+063311D  // NVIDIA
	[ 6] 0x7FFE8A97D1C7 nvwgf2umx.dll+06FD1C7  // NVIDIA
	[ 7] 0x7FFE8A7B3F73 nvwgf2umx.dll+0533F73  // NVIDIA
	[ 8] 0x7FFE8A7B43BF nvwgf2umx.dll+05343BF  // NVIDIA
	[ 9] 0x7FFE8A766EEF nvwgf2umx.dll+04E6EEF  // NVIDIA
	[10] 0x7FFE8A7490FA nvwgf2umx.dll+04C90FA  // NVIDIA
	[11] 0x7FFE8A2B7612 nvwgf2umx.dll+0037612  // NVIDIA
	[12] 0x7FFE8A6367F0 nvwgf2umx.dll+03B67F0  // NVIDIA
	[13] 0x7FFE8A3D4B2D nvwgf2umx.dll+0154B2D  // NVIDIA
	[14] 0x7FFE8A38C139 nvwgf2umx.dll+010C139  // NVIDIA
	[15] 0x7FFE8A2FB42D nvwgf2umx.dll+007B42D  // NVIDIA
	[16] 0x7FFE8A615474 nvwgf2umx.dll+0395474  // NVIDIA
	[17] 0x7FFE8A615242 nvwgf2umx.dll+0395242  // NVIDIA
	[18] 0x7FFE8A712D47 nvwgf2umx.dll+0492D47  // NVIDIA
	[19] 0x7FFE8B39FF1C nvwgf2umx.dll+111FF1C  // NVIDIA
	[20] 0x7FFEC66A7BD4  KERNEL32.DLL+0017BD4  // Windows
	[21] 0x7FFEC83ACE51     ntdll.dll+006CE51  // Windows
```

Downgrade to a pre-`445` driver series. You can find links to many older NVIDIA drivers [here.](https://github.com/keylase/nvidia-patch/tree/master/win)
