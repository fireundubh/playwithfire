---
title: Turning a release build into a debug build
description: 
published: true
date: 2021-08-13T04:34:11.222Z
tags: 
editor: markdown
dateCreated: 2020-01-19T11:08:11.523Z
---

# Requirements

Type | Name | Developer | Price | License | Website
:--- | :--- | :--- | :--- | :--- | :---
Decompiler | dotPeek | JetBrains | Free | Commercial |  [Official Website](https://www.jetbrains.com/decompiler/)
Deobfuscator | de4dot | 0xd4d | Open source | GPL v3 | [GitHub Fork](https://github.com/fireundubh/de4dot/tree/pdbgen)

You will also need to install the correct Unity Editor from the [official Unity download archive](https://unity3d.com/get-unity/download/archive).

# Preflight

## Set Up Debug Binaries

**For Unity 2017.2 and above.** For older versions, see [0xd4d's guide to debugging Unity games](https://github.com/dnSpy/dnSpy/wiki/Debugging-Unity-Games).

Before you do anything, backup the game's player `.exe`, `UnityPlayer.dll`, and the `Managed` folder.

1. Download and install the correct version of Unity from the [official Unity download archive](https://unity3d.com/get-unity/download/archive).
2. In the Unity installation directory, go to the `Editor\Data\PlaybackEngines\windowsstandalonesupport\Variations` folder.
3. Determine whether the game is 32-bit or 64-bit, and go to either `win32_development_mono` or `win64_development_mono`.
4. In the game's root directory, delete the game's `.exe` and `UnityPlayer.dll`.
5. Copy the debug `WindowsPlayer.exe` and `UnityPlayer.dll` to the game's root directory.
6. Rename the game's new `WindowsPlayer.exe` appropriately.
7. From the folder selected in #3, copy the contents of `Data\Managed` to the game's respective folder, overwriting all files when prompted.
8. Create a new plain text file in the game's Data folder named `boot.config`.
9. Edit `boot.config`, add the line `player-connection-debug=1`, and save.
10. Replace `mono-2.0-bdwgc.dll` in the game's `MonoBleedingEdge` folder with the debug version from the Unity Editor's `MonoBleedingEdge` folder.


# Instructions

## Step 1: Set Up PDB State

> If you haven't already, compile [this fork of de4dot](https://github.com/fireundubh/de4dot/tree/pdbgen), which makes [these changes](https://github.com/0xd4d/de4dot/pull/126/commits/28f33354c86cdbfc1d96134fab1132c87a99a5e3).
{.is-info}


This step is required for assemblies that were not compiled with the `/debug` option.

dotPeek does not allow generating PDBs for non-debug assemblies because debuggers do not support them. The `Generate Pdb...` option on the Assembly Explorer context menu will be grayed out and the tooltip will indicate the assembly is missing its `debug` directory.

Using our fork of de4dot, we need to "trick" dotPeek so that we can generate a new Full PDB. Execute the following command:

```
de4dot --dont-rename --keep-types --preserve-tokens --preserve-strings -fpdb <input_assembly.dll> -o <output_assembly.dll>
```

The output assembly should A) have the same name as the input assembly and B) be located at the same path. To achieve B, relocate the input assembly.

> A dummy PDB will be produced in the output folder. Delete this file before loading the assembly into dotPeek.
{.is-warning}


## Step 2: Generate PDB

1. Load the new assembly into dotPeek
2. Right-click the assembly and select `Export to Project...`
3. Check the box labeled `Create *.pdb file`
4. Click the `Export` button

> Call stacks will reference line numbers in files located in the project's destination folder.
{.is-info}

> Do not use the `Generate Pdb...` option. The PDB produced by this option will cause call stacks to reference files in the `DecompilerCache`.
{.is-warning}


## Step 3: Convert PDB to MDB

Unity loads MDB files, not PDB files. We need to convert our new PDB to MDB. Execute this command:

```
"%UNITY_MONO%\bin\mono.exe" "%UNITY_MONO%\lib\mono\4.5\pdb2mdb.exe" "<target_assembly_dll>"
```

`%UNITY_MONO%` is the absolute path to Unity's `MonoBleedingEdge` folder, like `G:\Unity\Editors\2019.4.26f1\Editor\Data\MonoBleedingEdge`.

The MDB file will be generated in the same folder as the target assembly DLL.


# Optional

## Requirements

Type | Name | Developer | Price | License | Website
:--- | :--- | :--- | :--- | :--- | :---
Decompiler/IL Editor | dnSpy | 0xd4d | Open source | GPL v3 | [GitHub](https://github.com/dnSpy/dnSpy)

## Assembly flags for debugging

> This procedure is only useful for live debugging. If your only goal is to produce complete call stacks, you can skip this.
{.is-info}

Using dnSpy, load the assembly and modify the assembly attributes from:

```csharp
[assembly: Debuggable(DebuggableAttribute.DebuggingModes.IgnoreSymbolStoreSequencePoints)]
```

To:

```csharp
[assembly: Debuggable(DebuggableAttribute.DebuggingModes.Default | DebuggableAttribute.DebuggingModes.DisableOptimizations 
  | DebuggableAttribute.DebuggingModes.EnableEditAndContinue | DebuggableAttribute.DebuggingModes.IgnoreSymbolStoreSequencePoints)]
```

For more information, see [0xd4d's guide to Making an Image Easier to Debug](https://github.com/dnSpy/dnSpy/wiki/Making-an-Image-Easier-to-Debug).

Save the module with the following MD Writer Options:

* Check: Preserve All MD Tokens
* Check: Preserve Heap Offsets (all)
* Check: Create Heap Even If Empty (all)
* Check: Misc Options (all except Keep Old MaxStack Value)