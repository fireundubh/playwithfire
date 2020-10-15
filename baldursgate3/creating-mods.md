---
title: Creating Mods
description: A step-by-step guide
published: true
date: 2020-10-15T00:02:54.369Z
tags: 
editor: markdown
dateCreated: 2020-10-15T00:02:54.369Z
---

# First steps

1. Create a folder outside the game directory. We'll call this our Workspace Root.
2. Create a folder in the Workspace Root named after your mod. This is your Project Dir.
3. Extract `Gustav.pak` into `Gustav_Data` in your Workspace Root. 
4. Extract `Shared.pak` into `Shared_Data` in your Workspace Root.

> These destination folder names remind us these folders contain files from the Gustav and Shared modules, and these folders are akin to the game's `Data` folder.
{.is-info}

# Making changes

5. Use [Agent Ransack](https://www.mythicsoft.com/agentransack/) to search these folders for files that contain data you want to modify. When you find those files, copy them to your Project Dir, creating intermediate folders as needed.

> When creating intermediate folders, treat your Project Dir as akin to the game's `Data` folder. For example, `ProjectDir\Stats` would be correct, not `ProjectDir\Public\Shared\Stats`.
{.is-info}

6. Modify those files as desired.

# Building and testing

7. Create metadata (`meta.lsx`) for your project in the Project Dir.
8. Use lslib's ConverterApp to create a PAK from your Project Dir.
9. Enable your mod in `modsettings.lsx`.

Play the game and verify your changes.