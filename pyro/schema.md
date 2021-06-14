---
title: Pyro Project Schema
description: 
published: true
date: 2021-06-14T22:12:34.846Z
tags: 
editor: markdown
dateCreated: 2020-01-19T11:07:53.276Z
---

This reference documents the attribute defaults in the Pyro Project Schema.

# //PapyrusProject

The `PapyrusProject` node is the root node from which all other nodes descend.

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
	Optimize="true"
  Release="true"
  Final="true"
  Anonymize="true"
  Package="true"
  Zip="true">
  <!-- snip -->
</PapyrusProject>
```


# //Variables

The `Variables` parent node contains `Variable` child nodes.


## Example

```xml
<Variables>
  <!-- block children -->
</Variables>
```


# //Variables/Variable

Node | Attribute | Type | Default Value | Required 
:--- | :--- | :--- | :--- | :---
`Variable` | `Name` | `string` | `''` | `True`
`Variable` | `Value` | `string` | `''` | `True`


## Example

```xml
<Variable Name="modname" Value="Auto Loot"/>
```

# //Imports/Import

Each `Import` node contains the local path or remote URL for an import folder.


## Example

```xml
<Import>F:\SDKs\SKSE\@SourceDir</Import>
<Import>https://github.com/fireundubh/LibFire.git</Import>
<Import>@RepoBaseURL/skyui/contents/dist/Data/Scripts/Source?ref=master</Import>
<Import>@OutputPath\@SourceDir</Import>
<Import>@ScriptsPath\Base</Import>
```


# //Scripts

The `Scripts` parent node contains `Script` child nodes.


## Example

```xml
<Scripts>
  <!-- block children -->
</Scripts>
```


# //Scripts/Script

Each `Script` node contains the path to a script file.

## Example

```xml
<Script>@namespace\dubhAutoLootDummyScript.psc</Script>
```

# //Folders/Folder

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :--- 
`Folder` | `NoRecurse` | `bool` | `false`

## Example

```xml
<Folder NoRecurse="true">@namespace\Fragments\Terminals</Folder>
```

# //Packages

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Packages` | `Output` | `str` | Path to the `pyro\dist` folder


## Example

```xml
<Packages Output="@OutputPath">
  <!-- block children -->
</Packages>
```


# //Packages/Package

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Package` | `Name` | `str` | If the attribute is omitted:<ul><li>the package file will be named after the project,<li>the extension will be appropriate to the game, and<li>subsequent package names will be suffixed with `(1)`, `(2)`, and so on.</ul>
`Package` | `RootDir` | `str` | Path to the project folder 


## Example

```xml
<Package Name="@ModName" RootDir="@OutputPath">
  <!-- block children -->
</Package>
```


# //Packages/Package/Include

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Include` | `NoRecurse`  | `bool` | `false`
`Include` | `Path` | `str` | If not empty, this value will be prepended to the file's location in the package.


## Example

```xml
<Include NoRecurse="false">**/*.pex</Include>
```

# //Packages/Package/Match

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Match` | `In`  | `str` | Path to the project folder
`Match` | `Exclude` | `str` | If not empty, this pattern can be used to exclude directories from matches.
`Include` | `NoRecurse`  | `bool` | `false`


## Example

```xml
<Match In="Textures">*.dds</Match>
```

# //ZipFiles

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`ZipFiles` | `Output` | `str` | Path to the `pyro\dist` folder

## Example

```xml
<ZipFiles Output="@modpath">
  <!-- block children -->
</ZipFiles>
```


# //ZipFiles/ZipFile

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`ZipFile` | `Name` | `str` | If the attribute is omitted, the ZIP file will be named after the project.
`ZipFile` | `RootDir` | `str` | Path to the project folder
`ZipFile` | `Compression` | `str` | `deflate`

## Example

```xml
<ZipFile Name="@modname" RootDir="@modpath" Compression="deflate">
  <!-- block children -->
</ZipFile>
```


# //ZipFiles/ZipFile/Include

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Include` | `NoRecurse` | `bool` | `false`
`Include` | `Path` | `str` | If not empty, this value will be prepended to the file's location in the archive.

## Example

```xml
<Include Path="optional">@modpath\MyOptionalPlugin.esp</Include>
```


# //ZipFiles/ZipFile/Match

Node | Attribute | Type | Default Value
:--- | :--- | :--- | :---
`Match` | `In`  | `str` | Path to the project folder
`Match` | `Exclude` | `str` | If not empty, this pattern can be used to exclude directories from matches.
`Include` | `NoRecurse`  | `bool` | `false`

## Example

```xml
<Match In="Strings">*.*STRINGS</Match>
```

