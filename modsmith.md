---
title: Modsmith
description: 
published: true
date: 2020-11-08T23:18:04.223Z
tags: 
editor: markdown
dateCreated: 2020-01-19T11:04:49.216Z
---

**Modsmith** is a build automation system for *Kingdom Come: Deliverance* mods.

# Benefits

- Allows you to focus on just the changes you want to make
- Improves productivity by eliminating noise in your files and encouraging an organized approach to modding
- Reduces time and effort to update mods after game updates by always patching the latest installed XML files
- Simplifies the work needed to create translations
- Accelerates the process of packaging mods for distribution

# Features

- Isolates mod data and strings from vanilla game data and strings
- Patches mod data into copies of the latest installed versions of vanilla XML tables
- Patches localized strings into copies of the latest installed versions of vanilla XML localization
- Generates zero-byte TBL files as needed for each XML table modified
- Generates distribution-ready ZIP archives of mods,
- Supports packaging arbitrary files that cannot be patched
- Supports patching multiple languages simultaneously

## Future Plans

- Generate actual TBL files as needed for each XML table modified
- Support patching non-table XML files

# Using Modsmith

1. To use Modsmith, you will need to structure your mod project similar to the example below:

Folder Path | Files
:--- | :---
`Data\Libs\Tables\rpg` | `buff.xml`<br>`perk.xml`<br>`perk2perk_exclusivity.xml`<br>`perk_buff.xml`<br>`perk_buff_override.xml`
`Localization\english_xml` | `text_ui_soul.xml`

2. Inside the project folder (e.g., `E:\projects\kingdomcome\More Perks`), there should be a Data folder and/or a Localization folder. Modsmith also supports Data-only mods and Localization-only mods (e.g., translations.)
3. The `mod.manifest` file should be placed in the project root directory.
4. The hierarchy for each folder should imitate the hierarchy needed for your mod (e.g., `Localization\french_xml`.)
5. **Ensure that your XML files contain ONLY the rows your mod adds or changes.** With Modsmith, it is no longer necessary to work on massive XML files to create mods. When your mod is packaged, Modsmith will generate new XML files in the Build folder that combine your merged rows with the rows you didn't alter. This allows you to keep your data isolated, focus on your project, and reduce the time and effort required to update your mod when game patches are released.
6. Run Modsmith with the appropriate command-line arguments.

## Configuration

Before running Modsmith, you will need to edit `modsmith.conf`. Don't worry! There is only one setting.

```
[Game]
Path = C:\Program Files (x86)\Steam\steamapps\common\KingdomComeDeliverance
```

Change the value of `Path` to wherever you installed *Kingdom Come: Deliverance*. It must be the game's root path!

## Arguments

Argument | Required | Description
:--- | :--- | :---
`-p` | Yes | Absolute path to your project root directory (e.g., `E:\projects\kingdomcome\More Perks`)
`-d` | Variable | File name and extension of your data PAK file (e.g., `More Perks.pak`.) Localization-only mods (e.g. translations) do not require this argument, but data mods do.
`-r` | Yes | File name and extension of your redistributable ZIP file (e.g., `More Perks.zip`)
`-l` | No | Absolute path to your project's localization root directory. Use only when storing localization outside the project root.
`--add-arbitrary-files` | No | Allows you to package arbitrary unsupported files
`--debug` | No | Enables debug logging

## Example Usage

### More Perks

```
cd "C:\Modsmith"
modsmith -p "E:\projects\kingdomcome\More Perks" -d "More Perks.pak" -r "More Perks.zip"
```

### Lockpicking Overhaul

```
cd "C:\Modsmith"
modsmith -p "E:\projects\kingdomcome\Lockpicking Overhaul" -d "Lockpicking Overhaul.pak" -r "Lockpicking Overhaul.zip" --add-arbitrary-files
```

# Example Projects

**More Perks** is [a good example of how Modsmith projects are structured and what their XML files contain](https://github.com/fireundubh/kingdomcome/tree/master/More%20Perks) (GitHub). I use **Modsmith** to build and update Lockpicking Overhaul, More Perks, the three versions of Better Trainers, and the two versions of Unleveled Perks.

Other examples:

- [Easy Lockpicking](https://github.com/fireundubh/kingdomcome/tree/master/Easy%20Lockpicking) (GitHub)
- [Better Trainers](https://github.com/fireundubh/kingdomcome/tree/master/Better%20Trainers) (GitHub)
- [Unleveled Perks](https://github.com/fireundubh/kingdomcome/tree/master/Unleveled%20Perks) (GitHub)

# Example Output

**Modsmith** will generate a number of folders and files in the Build folder in your project root directory.

![Example Output](https://i.imgur.com/ySmeFqP.jpg)

## What do you see?

- There is a `Build` folder, and there is a `More Perks` subfolder in the `Build` directory. This subfolder is named after the mod using the file name (without the extension) passed to **Modsmith** with the `-r` argument.
- Inside this folder are the `Data` and `Localization` folders, which replicate the structure of the project.
- There is a PAK file in the `Data` folder using the file name (without the extension) passed to Modsmith with the `-d` argument. This PAK file contains all the files in `Libs\Tables\rpg`.
- In the `Libs\Tables\rpg` folder, there are TBL and XML files. The zero-byte TBL files were generated automatically. Currently, you need these for XML mods to work. These XML files are the product of the packaging process. Compare them with your own in the project `Data` folder and you'll see that while your XML files contain only your modified rows, the XML files in the ZIP contain both your modified rows and all other rows.
- There is a PAK file in the `Localization` folder. Note that **Modsmith** can generate localization XML files and PAKs for multiple languages simultaneously.
- Finally, there is a redistributable ZIP file in the root of the Build path. This ZIP contains only the files necessary for players to install your mod (i.e., folders and PAKs.) You can immediately upload this ZIP to the Nexus, or extract the ZIP to your own Mods folder for testing.

# Contributing/Issues/Source Code

**Modsmith** is available on GitHub at: github.com/fireundubh/modsmith.

If you don't want to run the executable, you can run Modsmith from the Python 3 source code. More details at GitHub.

If you'd like to contribute, pull requests are welcome. Please [submit issues](https://github.com/fireundubh/modsmith/issues) on GitHub only.