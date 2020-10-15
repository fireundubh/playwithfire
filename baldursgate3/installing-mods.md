---
title: Installing Mods
description: A step-by-step guide
published: true
date: 2020-10-15T00:11:55.186Z
tags: 
editor: markdown
dateCreated: 2020-10-15T00:11:55.186Z
---

Manually installing a mod is a 3-step process:

1. Copy your `.pak` file to the appropriate location. (See: [Important Paths](/baldursgate3/#important-paths))
2. Add the mod to your player profile's `modsettings.lsx` file.
3. Set `modsettings.lsx` to read only. If you do not set this file to read only, the game will overwrite the file and you'll have to make your changes again.


# Important Nodes

## ModOrder

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


## Mods

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
