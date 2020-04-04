---
title: Papyrus Project Schema
description: 
published: true
date: 2020-04-04T18:38:03.237Z
tags: 
---

# Attribute Defaults

## PapyrusProject

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

### Example

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

## Variables

Node | Attribute | Type | Default Value | Required 
:--- | :--- | :--- | :--- | :---
`Variable` | `Name` | `string` | `''` | `True`
`Variable` | `Value` | `string` | `''` | `True`

### Example

```xml
<Variables>
	<Variable Name="modname" Value="Auto Loot"/>
	<Variable Name="namespace" Value="AutoLoot"/>
	<Variable Name="modpath" Value="E:\repos\mods\fallout4\@modname"/>
</Variables>
```

## Folders

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :--- 
`Folder` | `NoRecurse` | `bool` | `false`

### Example

```xml
	<Folders>
		<Folder NoRecurse="true">@namespace\Fragments\Terminals</Folder>
	</Folders>
```

## Packages

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Packages` | `Output` | `str` | Path to the `pyro\dist` folder
`Package` | `Name` | `str` | If the attribute is omitted:<ul><li>the package file will be named after the project,<li>the extension will be appropriate to the game, and<li>subsequent package names will be suffixed with `(1)`, `(2)`, and so on.</ul>
`Package` | `RootDir` | `str` | Path to the project folder 
`Include` | `NoRecurse`  | `bool` | `false`

### Example

```xml
<Packages Output="@modpath">
	<Package Name="@modname - Main" RootDir="@modpath">
		<Include NoRecurse="false">**/*.pex</Include>
	</Package>
</Packages>
```

## ZipFile

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`ZipFile` | `Name` | `str` | If the attribute is omitted, the ZIP file will be named after the project.
`ZipFile` | `RootDir` | `str` | Path to the project folder
`ZipFile` | `Output` | `str` | Path to the `pyro\dist` folder
`ZipFile` | `Compression` | `str` | `deflate`
`Include` | `NoRecurse` | `bool` | `false`

### Example

```xml
<ZipFile Name="@modname" RootDir="@modpath" Output="@modpath" Compression="deflate">
	<Include>@modpath\Auto Loot.esp</Include>
	<Include>@modpath\Auto Loot - Main.ba2</Include>
</ZipFile>
```