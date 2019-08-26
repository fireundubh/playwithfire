<!-- TITLE: Reversing Mods -->

# Reversing Mods
## Use Cases

1. You want to add a third-party mod as a dependency, but...
2. You want to load a third-party mod to see how things work, but...
3. You want to load a third-party mod to make personal changes to the mod, but...

...after extracting the PAK to the game data folder, The Divinity Engine 2 project menu does not show the project.

## Instructions

### Step 1. Download and install

#### Steam Workshop Mods

Subscribe to the mod from the Steam Workshop. The PAK will be downloaded to one of these folders:

- `%USERPROFILE%\Documents\Larian Studios\Divinity Original Sin 2 Definitive Edition\Mods`
- `%PROGRAMFILES(X86)%\Steam\steamapps\workshop\content\435150\`

#### Nexus Mods

Download the mod from the Nexus. Extract the PAK from the downloaded ZIP, RAR, or 7Z archive wherever you want.

### Step 2. Extract the PAK

Use the Divine CLI from [lslib](https://github.com/Norbyte/lslib/releases) to extract the PAK file using the following command:

```
cd "%USERPROFILE%\Documents\Larian Studios\Divinity Original Sin 2 Definitive Edition\Mods"
divine -g dos2de -a extract-package -s "%CD%\NotMyMod_c6a7eddf-ce98-43dc-a823-7187697e61fe.pak" -d "%PROGRAMFILES(X86)%\Steam\steamapps\common\Divinity Original Sin 2\DefEd\Data"
```

### Step 3. Set up the project

Create a folder named `Projects` in the `Data` directory.

```
mkdir "%PROGRAMFILES(X86)%\Steam\steamapps\common\Divinity Original Sin 2\DefEd\Data\Projects"
```

Create a folder in the `Projects` directory named after the mod.

```
mkdir "%PROGRAMFILES(X86)%\Steam\steamapps\common\Divinity Original Sin 2\DefEd\Data\Projects\NotMyMod"
```

In that folder, create a file named `meta.lsx` with these contents:

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<save>
    <header version="2" time="1536381346" />
    <version major="3" minor="6" revision="0" build="4" />
    <region id="MetaData">
        <node id="root">
            <attribute id="Module" value="c6a7eddf-ce98-43dc-a823-7187697e61fe" type="23" />
            <attribute id="Name" value="NotMyMod" type="23" />
            <attribute id="Type" value="Add-on" type="23" />
            <attribute id="UUID" value="5c0c0387-0f39-46e3-8acc-c5935a6d6ea3" type="23" />
        </node>
    </region>
</save>
```

#### Notes

1. The value of `attribute[@id="Module"]` should be the UUID that follows the mod name in the PAK file name.
2. The value of `attribute[@id="UUID"]` should be a new UUID. You can generate UUIDs [here](https://www.uuidgenerator.net/).

### Step 4. Load the project

If you did everything correctly, the mod should appear in The Divinity Engine 2's project menu and you will be able to load the project successfully.