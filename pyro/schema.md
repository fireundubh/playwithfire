---
title: Pyro Project Schema
description: 
published: true
date: 2021-06-14T22:46:30.801Z
tags: 
editor: markdown
dateCreated: 2020-01-19T11:07:53.276Z
---

This reference documents the elements and attribute defaults in the Pyro Project Schema.


# PapyrusProject

The `PapyrusProject` block contains the `<Variables>`, `<Imports>`, `<Scripts>`, `<Folders>`, `<Packages>`, and `<ZipFiles>` blocks.

```xml
<PapyrusProject
	xmlns="PapyrusProject.xsd"
	Game="FO4"
	Flags="Institute_Papyrus_Flags.flg"
	Output="@modpath\scripts"
	Optimize="true"
  Release="true"
  Final="true"
  Anonymize="true"
  Package="true"
  Zip="true">
  <!-- block children -->
</PapyrusProject>
```

#### Attribute Details

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


# Variables

The `Variables` block contains `Variable` child nodes.

```xml
<Variables>
  <!-- block children -->
</Variables>
```

## Variable

Each `Variable` node declares a variable name and its associated value.

```xml
<Variable Name="modname" Value="Auto Loot"/>
```

#### Attribute Details

Node | Attribute | Type | Default Value | Required 
:--- | :--- | :--- | :--- | :---
`Variable` | `Name` | `string` | `''` | `True`
`Variable` | `Value` | `string` | `''` | `True`


# Imports

The `Imports` block contains `Import` child nodes.

```xml
<Imports>
  <!-- block children -->
</Imports>
```

## Import

Each `Import` node contains the local path or remote URL for an import folder.

```xml
<Import>F:\SDKs\SKSE\@SourceDir</Import>
<Import>https://github.com/fireundubh/LibFire.git</Import>
<Import>@RepoBaseURL/skyui/contents/dist/Data/Scripts/Source?ref=master</Import>
<Import>@OutputPath\@SourceDir</Import>
<Import>@ScriptsPath\Base</Import>
```


# Scripts

The `Scripts` block contains `Script` child nodes.

```xml
<Scripts>
  <!-- block children -->
</Scripts>
```

## Script

Each `Script` node contains the path to a script file.

```xml
<Script>@namespace\dubhAutoLootDummyScript.psc</Script>
```


# Folders

The `Folders` block contains `Folder` child nodes.

```xml
<Folders>
  <!-- block children -->
</Folders>
```

## Folder

Each `Folder` node contains a path to a script sources folder.

```xml
<Folder NoRecurse="true">@namespace\Fragments\Terminals</Folder>
```

#### Attribute Details

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :--- 
`Folder` | `NoRecurse` | `bool` | `false`


# Packages

The `Packages` block contains `Package` child nodes.

```xml
<Packages Output="@OutputPath">
  <!-- block children -->
</Packages>
```

#### Attribute Details

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Packages` | `Output` | `str` | Path to the `pyro\dist` folder


## Package

Each `Package` block contains `Include` and/or `Match` child nodes.

```xml
<Package Name="@ModName" RootDir="@OutputPath">
  <!-- block children -->
</Package>
```

#### Attribute Details

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Package` | `Name` | `str` | If the attribute is omitted:<ul><li>the package file will be named after the project,<li>the extension will be appropriate to the game, and<li>subsequent package names will be suffixed with `(1)`, `(2)`, and so on.</ul>
`Package` | `RootDir` | `str` | Path to the project folder 


### Include

Each `Include` node contains an absolute or relative file or folder path, or a glob expression.

```xml
<Include NoRecurse="false">**/*.pex</Include>
```

#### Attribute Details

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Include` | `NoRecurse`  | `bool` | `false`
`Include` | `Path` | `str` | If not empty, this value will be prepended to the file's location in the package.


### Match

Each `Match` node contains a wildcard file expression, which may also include file negation and directory exclusion patterns.

```xml
<Match In="Textures">*.dds</Match>
```

#### Attribute Details

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Match` | `In`  | `str` | Path to the project folder
`Match` | `Exclude` | `str` | If not empty, this pattern can be used to exclude directories from matches.
`Include` | `NoRecurse`  | `bool` | `false`


# ZipFiles

The `ZipFiles` block contains `ZipFile` child nodes.

```xml
<ZipFiles Output="@modpath">
  <!-- block children -->
</ZipFiles>
```

#### Attribute Details

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`ZipFiles` | `Output` | `str` | Path to the `pyro\dist` folder


## ZipFile

Each `ZipFile` block contains `Include` and/or `Match` child nodes.

```xml
<ZipFile Name="@modname" RootDir="@modpath" Compression="deflate">
  <!-- block children -->
</ZipFile>
```

#### Attribute Details

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`ZipFile` | `Name` | `str` | If the attribute is omitted, the ZIP file will be named after the project.
`ZipFile` | `RootDir` | `str` | Path to the project folder
`ZipFile` | `Compression` | `str` | `deflate`


### Include

Each `Include` node contains an absolute or relative file or folder path, or a glob expression.

```xml
<Include Path="optional">@modpath\MyOptionalPlugin.esp</Include>
```

#### Attribute Details

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Include` | `NoRecurse` | `bool` | `false`
`Include` | `Path` | `str` | If not empty, this value will be prepended to the file's location in the archive.


### Match

Each `Match` node contains a wildcard file expression, which may also include file negation and directory exclusion patterns.

```xml
<Match In="Strings">*.*STRINGS</Match>
```

#### Attribute Details

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Match` | `In`  | `str` | Path to the project folder
`Match` | `Exclude` | `str` | If not empty, this pattern can be used to exclude directories from matches.
`Include` | `NoRecurse`  | `bool` | `false`
