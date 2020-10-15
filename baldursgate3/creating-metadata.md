---
title: Creating Metadata
description: A quick look at mod metadata
published: true
date: 2020-10-15T00:04:21.671Z
tags: 
editor: markdown
dateCreated: 2020-10-15T00:04:21.671Z
---

Divinity Engine mods require a `meta.lsx` (XML) file that describes the mod. We're going to customize an existing `meta.lsx` file from the campaign to manufacture our own.

> **Review:** [meta.lsx Template](https://gist.github.com/fireundubh/b60baced4adf7a3070f466536aeeb7ec)
{.is-info}


# Important Nodes

## Dependencies

The campaign module is named `Gustav`. If you will be modifying anything that is specifically in the Gustav module, you will need to add Gustav as a dependency. Likewise, if you will be modifying anything that is specifically in any other module, except `Shared`, you will need to add that module as a dependency, too.

## ModuleInfo

We care about six attributes:

Attribute Name | Attribute Description
:--- | :---
`Author` | The name of the module's author
`Description` | A brief description of the module. In the release version of the game, this description would appear in the in-game mod manager.
`Folder` | The name of the module's PAK file (without the file extension)
`Name` | The name of the module's PAK file (without the file extension)
`UUID` | A universally unique identifier for this module - [generate a new one!](https://www.uuidgenerator.net)
`Version` | A version number for this module (optional)