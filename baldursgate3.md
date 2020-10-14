---
title: Baldur's Gate 3
description: Modding Reference
published: true
date: 2020-10-14T19:07:08.807Z
tags: 
editor: markdown
dateCreated: 2020-10-14T19:02:29.017Z
---

# Important Paths

The following paths are relative to:

`%USERPROFILE%\Documents\Larian Studios\Baldur's Gate 3`

Path | Description
:--- | :---
`Mods` | Install mods by copying their PAK files here.
`PlayerProfiles\YOUR_PLAYER_NAME` | Find `modsettings.lsx` here.

# meta.lsx

Divinity Engine mods require a `meta.lsx` (XML) file that describes the mod. We're going to customize an existing `meta.lsx` file from the campaign to manufacture our own.

> **Review:** [meta.lsx Template](https://gist.github.com/fireundubh/b60baced4adf7a3070f466536aeeb7ec)
{.is-info}


## Important Nodes

### Dependencies

The campaign module is named `Gustav`. If you will be modifying anything that is specifically in the Gustav module, you will need to add Gustav as a dependency.

Likewise, if you will be modifying anything that is specifically in any other module, except `Shared`, you will need to add that module as a dependency, too.

### ModuleInfo

We care about six attributes:

Attribute Name | Attribute Description
:--- | :---
`Author` | The name of the module's author
`Description` | A brief description of the module. In the release version of the game, this description would appear in the in-game mod manager.
`Folder` | The name of the module's PAK file (without the file extension)
`Name` | The name of the module's PAK file (without the file extension)
`UUID` | A universally unique identifier for this module - [generate a new one!](https://www.uuidgenerator.net)
`Version` | A version number for this module (optional)


# modsettings.lsx

Manually installing a mod is a 3-step process:

1. Copy the PAK file to the appropriate location. (See: [Important Paths](#important-paths))
2. Add the mod to your player profile's `modsettings.lsx` file.
3. Set `modsettings.lsx` to read only.

## Important Nodes

### ModOrder

If you need to change the load order of your mods, you can populate this node like so:

```xml
<node id="ModOrder">
  <children>
    <node id="Module">
      <attribute id="UUID" value="991c9c7a-fb80-40cb-8f0d-b92d4e80e9b1" type="22" />
    </node>
    <!-- additional Module nodes -->
  </children>
</node>
```


### Mods

To enable a module, append a node to the `Mods` node's `children` element.

Each new module node should look like:

```xml
<node id="ModuleShortDesc">
  <!-- Change the value to the module's Folder attribute from meta.lsx -->
  <attribute id="Folder" type="LSWString" value="Gustav"/> 
 
	<attribute id="MD5" type="LSString" value=""/> <!-- leave blank -->
  
	<!-- Change the value to the module's Name attribute from meta.lsx -->
  <attribute id="Name" type="FixedString" value="Gustav"/> 
  
	<!-- Change the value to the module's UUID attribute from meta.lsx -->
  <attribute id="UUID" type="FixedString" value="991c9c7a-fb80-40cb-8f0d-b92d4e80e9b1"/>
  
  <!-- Change the value to the module's Version attribute from meta.lsx -->
	<attribute id="Version" type="int32" value="268435456"/>
</node>
```
