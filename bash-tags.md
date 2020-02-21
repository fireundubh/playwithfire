---
title: Bash Tags Reference
description: 
published: true
date: 2020-02-21T01:49:01.835Z
tags: 
---

# Special Function Tags

| Tag | Used When The Mod | Specific Record Types/Changes Supported
:--- | :--- | :---
`Deactivate` | Should be deactivated. | N/A
`Filter` | Does not require all its masters to be installed to function. See the Merge Filtering section for more information. | N/A
`IIM` | Is to be used in Item Interchange Mode. See the Item Interchange Mode section for more information. | N/A
`InventOnly` | **Deprecated.** Use Invent in conjunction with IIM instead. | N/A
`Merge` | **Obsolete.** This tag is ignored. | N/A
`MustBeActiveIfImported` | Must be active to function correctly even if it is imported into the Bashed Patch. Currently this tags only function is that Bash won't ask to deactivate the plugin. | N/A
`NoMerge` | Should not be merged even though it is technically mergeable. | N/A