---
title: Starfield
description: 
published: true
date: 2023-10-29T20:00:33.795Z
tags: 
editor: markdown
dateCreated: 2023-10-28T22:14:13.093Z
---

# Common User Errors

## Bad Ideas

- installed a mod that patched `Starfield.exe` directly (e.g., a non-SFSE achievement enabler), rendering the game incompatible or partially incompatible with SFSE plugins that employ signature or byte array searches
- continuing to use ESPs, ESLs, and Overlay-flagged plugins [despite *far more* technical people telling you to stop](https://github.com/TES5Edit/TES5Edit/blob/dev-4.1.5/whatsnew.md)


## Bad User

- posted a comment on Plugins.txt Enabler that the mod is useless or doesn't work
- posted a comment on any ESM mod that the mod is useless or doesn't work


## Bad Setup

- did not install [SFSE](https://sfse.silverlock.org) correctly or otherwise
- did not configure Steam to launch the game with the SFSE loader (`sfse_loader.exe`) (whenever you launch the game, you have to do so with this loader)
- did not launch the game with the SFSE loader (`sfse_loader.exe`) (whenever you launch the game, you have to do so with this loader)
- did not install [Plugins.txt Enabler](https://www.nexusmods.com/starfield/mods/4157) (required; fixes a **game engine bug** - deliberately chosen words! - that prevents the game from reading `plugins.txt`)
- did not install [Visual C++ Redistributable for Visual Studio 2015-2022](https://learn.microsoft.com/en-US/cpp/windows/latest-supported-vc-redist), if encountering error 126 (0x7E) when starting the game
- did not install [Baka Disable My Games Folder](https://www.nexusmods.com/starfield/mods/1599) (not a requirement but makes life easier)
- did not install [Baka Achievement Enabler](https://www.nexusmods.com/starfield/mods/658) (not a requirement but addresses the "mods disable achievements?" questions)
- did not install the MO2 v2.5.0 Beta with Starfield support (required for MO2 users; not a requirement for everyone else but makes life easier)
- did not enable Archive Invalidation in `StarfieldCustom.ini`

```ini
[Archive]
bInvalidateOlderFiles=1
sResourceDataDirsFinal=
```

## Bad MO2 Configuration

- if using the MO2 v2.5.0 Beta, did not set `enable_plugin_management` to `true` in the Starfield Support plugin options
- if Baka Disable My Games Folder is installed, did not enable MO2 Compatibility Mode in that plugin's configuration file
- disabled Archive Invalidation


## Bad File Names

> If you have not already done so, disable the "[Hide extensions for known file types](https://i.imgur.com/Fq011VV.jpg)" filter in File Explorer.
{.is-warning}

- created a `plugin.txt` file (the correct file name is `plugins.txt`)
- created a `plugin.txt.txt` file (the correct file name is `plugins.txt`)
- created a `plugins.txt.txt` file (the correct file name is `plugins.txt`)
- created a `plugins..txt` file (the correct file name is `plugins.txt`)
- entered the incorrect file names of plugins on disk in the `plugins.txt` file (the game cannot guess what you mean; the file names must be exact)


## Bad File Paths

- created or moved the `plugins.txt` file to a location where the game cannot find the file
- created or moved the `plugins.txt` file to a location outside `%LOCALAPPDATA%\Starfield`


## Bad Data

- entered console commands in the `plugins.txt` file
- entered `sTestFile` entries with the `sTestFile` key in the `plugins.txt` file


## Bad Syntax

- did not prefix correct file names of plugins on disk with an asterisk to enable those plugins
- copied a `sStartingCjavascript-event-strippedbat` line into `StarfieldCustom.ini` (the correct key is `sStartingConsoleCommand` but a Nexus bug obfuscates the key in comments)


## Using sTestFile

>  [Plugins.txt Enabler](https://www.nexusmods.com/starfield/mods/4157) and use of `sTestFile` are mutually exclusive! `plugins.txt` is used by all BGS games. `sTestFile` is not for end users to load mods and will break the game.
{.is-danger}

- did not remove the `sTestFile*` keys from `StarfieldCustom.ini`
- did not remove the `sTestFile*` keys from INI files distributed by some mods


## Bad Plugin Management

- did not install mod requirements
- did not update any SFSE plugins that needed to be updated
- did not wait for SFSE plugins to be updated that needed to be updated following a new game version


# Common Non-Errors

These are NOT errors, although some people confidently (and wrongly) say otherwise:

- not having a `#` symbol at the top of the `plugins.txt` file (the `#` symbol denotes a comment, which is skipped by the parser; this line does nothing)
- defining `sStartingConsoleCommand` in `StarfieldCustom.ini` (the game works with both `plugins.txt` and console commands)