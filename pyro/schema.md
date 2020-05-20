---
title: Papyrus Project Schema
description: 
published: true
date: 2020-05-20T04:50:48.840Z
tags: 
---

# PapyrusProject

> **XPath:** `//PapyrusProject`

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`PapyrusProject` | `Game` | `str` | (determined programmatically)
`PapyrusProject` | `Flags` | `str` | (determined programmatically from game path)
`PapyrusProject` | `Output` | `str` | Path to the `pyro\out` folder
`PapyrusProject` | `Optimize` | `bool` | `false`
`PapyrusProject` | `Release` (FO4 only) | `bool` | `false`
`PapyrusProject` | `Final` (FO4 only) | `bool` | `false`
`PapyrusProject` | `Anonymize` | `bool` | `false`
`PapyrusProject` | `Package` | `bool` | `false`

## Example

```xml
<PapyrusProject
	xmlns="PapyrusProject.xsd"
	Game="FO4"
	Flags="Institute_Papyrus_Flags.flg"
	Output="@modpath\scripts"
	Optimize="true" Release="true" Final="true"
  Anonymize="true"
  Package="true"
  Zip="true">
  <!-- snip -->
</PapyrusProject>
```

# Variables/Variable

> **XPath:** `//Variables/Variable`

Node | Attribute | Type | Default Value | Required 
:--- | :--- | :--- | :--- | :---
`Variable` | `Name` | `string` | `''` | `True`
`Variable` | `Value` | `string` | `''` | `True`

## Example

```xml
<Variables>
	<Variable Name="modname" Value="Auto Loot"/>
	<Variable Name="namespace" Value="AutoLoot"/>
	<Variable Name="modpath" Value="E:\repos\mods\fallout4\@modname"/>
</Variables>
```

# Imports/Import

> **XPath:** `//Imports/Import`

The `Imports` parent node contains `Import` child nodes. None of these nodes have attributes.

## Example

```xml
<Imports>
	<Import>@modpath\scripts\Source\User</Import>
	<Import>E:\SteamLibrary\Fallout 4\Data\Scripts\Source\Base</Import>
</Imports>
```

# Scripts/Script

> **XPath:** `//Scripts/Script`

The `Scripts` parent node contains `Script` child nodes. None of these nodes have attributes.

## Example

```xml
<Scripts>
	<Script>@namespace\dubhAutoLootDummyScript.psc</Script>
	<Script>@namespace\dubhAutoLootEffectBodiesScript.psc</Script>
	<Script>@namespace\dubhAutoLootEffectComponentsScript.psc</Script>
	<Script>@namespace\dubhAutoLootEffectContainersScript.psc</Script>
	<Script>@namespace\dubhAutoLootEffectScript.psc</Script>
	<Script>@namespace\dubhAutoLootEffectTieredScript.psc</Script>
	<Script>@namespace\dubhAutoLootQuestScript.psc</Script>
	<Script>@namespace\dubhAutoLootNoDisintegrateScript.psc</Script>
</Scripts>
```

# Folders/Folder

> **XPath:** `//Folders/Folder`

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :--- 
`Folder` | `NoRecurse` | `bool` | `false`

## Example

```xml
	<Folders>
		<Folder NoRecurse="true">@namespace\Fragments\Terminals</Folder>
	</Folders>
```

# Packages

> **XPath:** `//Packages`

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Packages` | `Output` | `str` | Path to the `pyro\dist` folder


## Packages/Package

> **XPath:** `//Packages/Package`

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Package` | `Name` | `str` | If the attribute is omitted:<ul><li>the package file will be named after the project,<li>the extension will be appropriate to the game, and<li>subsequent package names will be suffixed with `(1)`, `(2)`, and so on.</ul>
`Package` | `RootDir` | `str` | Path to the project folder 
`Include` | `NoRecurse`  | `bool` | `false`


## Example

```xml
<Packages Output="@modpath">
	<Package Name="@modname - Main" RootDir="@modpath">
		<Include NoRecurse="false">**/*.pex</Include>
	</Package>
</Packages>
```

# ZipFiles

> **XPath:** `//ZipFiles`

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`ZipFiles` | `Output` | `str` | Path to the `pyro\dist` folder


## ZipFiles/ZipFile

> **XPath:** `//ZipFiles/ZipFile`

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`ZipFile` | `Name` | `str` | If the attribute is omitted, the ZIP file will be named after the project.
`ZipFile` | `RootDir` | `str` | Path to the project folder
`ZipFile` | `Compression` | `str` | `deflate`
`Include` | `NoRecurse` | `bool` | `false`


## Example

```xml
<ZipFiles Output="@modpath">
  <ZipFile Name="@modname" RootDir="@modpath" Compression="deflate">
    <Include>@modpath\Auto Loot.esp</Include>
    <Include>@modpath\Auto Loot - Main.ba2</Include>
  </ZipFile>
</ZipFiles>
```