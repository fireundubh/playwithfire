<!-- TITLE: Turning a release build into a debug build -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Turning a release build into a debug build
## Requirements

* de4dot
* dnSpy
* dotPeek
* Unity Editor

## Instructions

### Step 1: Fix Assembly Flags

Using dnSpy, load the assembly and modify the assembly attributes from:

```
[assembly: Debuggable(DebuggableAttribute.DebuggingModes.IgnoreSymbolStoreSequencePoints)]
```

To:

```
[assembly: Debuggable(DebuggableAttribute.DebuggingModes.Default | DebuggableAttribute.DebuggingModes.DisableOptimizations | DebuggableAttribute.DebuggingModes.EnableEditAndContinue)]
```

Save the module with the following MD Writer Options:

* Check: Preserve All MD Tokens
* Check: Preserve Heap Offsets (all)
* Check: Create Heap Even If Empty (all)
* Check: Misc Options (all except Keep Old MaxStack Value)

Source: [https://github.com/0xd4d/dnSpy/wiki/Making-an-Image-Easier-to-Debug](https://github.com/0xd4d/dnSpy/wiki/Making-an-Image-Easier-to-Debug)

### Step 2: Set Up Debug Binaries

**For Unity 2017.2 and above.** For older versions, see [0xd4d's guide to debugging Unity games](https://github.com/0xd4d/dnSpy/wiki/Debugging-Unity-Games).

Before you do anything, backup the game's player `.exe`, `UnityPlayer.dll`, and the `Managed` folder.

1. Download and install the correct version of Unity from the [official Unity download archive](https://unity3d.com/get-unity/download/archive).
2. Determine whether the game is 32-bit or 64-bit.
3. In the Unity installation directory, go to the `Editor\Data\PlaybackEngines\windowsstandalonesupport\Variations` folder.
4. Go to `win32_development_mono` or `win64_development_mono`.
5. Delete the game's `.exe` and `UnityPlayer.dll`.
6. Copy the debug `WindowsPlayer.exe` and `UnityPlayer.dll` to the game's root directory.
7. Rename game's `WindowsPlayer.exe` appropriately.
8. Copy the contents of `Data\Managed` to the game's respective folder, overwriting all files when prompted.
9. Create a new plain text file in the game's Data folder named `boot.config`.
10. Edit `boot.config`, add the line `player-connection-debug=1`, and save.

### Step 3: Compile de4dot

Compile these changes into de4dot:

https://github.com/0xd4d/de4dot/pull/126/commits/28f33354c86cdbfc1d96134fab1132c87a99a5e3

### Step 4: Set Up PDB State

We need to set up the assembly so that dotPeek can generate a new PDB file. (Currently, dnSpy does not offer PDB generation.)

**Note:** The line numbers in stack traces will be accurate to dotPeek's decompilation output because we're using dotPeek to generate the PDB.

1. Run de4dot from the command prompt/shell to see the command line parser arguments.
2. Execute the following command: `de4dot --dont-rename --keep-types --preserve-tokens --preserve-strings -fpdb <source_assembly_dll> -o <target_assembly_dll>`

A dummy PDB will be produced in the output folder.

### Step 5: Generate PDB

1. Load the new assembly into dotPeek.
2. Generate the PDB file.

You may have to wait a while for dotPeek to generate the DecompilerCache and write the PDB file.

### Step 6: Convert PDB to MDB

Unity loads MDB files, not PDB files, so we need to convert our new PDB to MDB. Fortunately, we have all the tools already.

Execute the following command:

```
"<unity_install_path_base>\Editor\Data\MonoBleedingEdge\bin\mono.exe" "<unity_install_path_base>\Editor\Data\MonoBleedingEdge\lib\mono\4.5\pdb2mdb.exe" "<target_assembly_dll>"
```

The MDB file be generated in the same folder as the target assembly DLL.

### Step 7: Replace Mono Binary

Finally, replace `mono-2.0-bdwgc.dll` in the game's `MonoBleedingEdge` folder with the debug version from the Unity Editor's `MonoBleedingEdge` folder.