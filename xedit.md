---
title: xEdit
description: 
published: true
date: 2020-01-20T12:22:51.605Z
tags: 
---

# General Purpose

Name | Hotkey | Has GUI | Purpose
:--- | :--- | :--- | :---
[Search Elements by Path](https://github.com/fireundubh/xedit-scripts/blob/master/gui/Search%20Elements%20By%20Path.pas) | Ctrl+F | Yes | Allows you to search in elements by path and returns a list of results
[Search Elements by Group](https://github.com/fireundubh/xedit-scripts/blob/master/gui/Search%20Elements%20by%20Group.pas) | Ctrl+G | Yes | Allows you to search in elements by specified group and returns a list of results
[StringOps](https://github.com/fireundubh/xedit-scripts/blob/master/gui/StringOps.pas) | Ctrl+R | Yes | Allows you to perform these operations on elements in the selected records:<ul><li>Find and Replace<li>Add Prefix<li>Add Suffix<li>Change to Proper/Title Case<li>Change to Sentence Case</ul>Other features:<ul><li>Easy to use GUI that supports nonstandard DPIs<li>Automatically saves and restores settings<li>Automatically replaces tab and newline tokens with their respective characters (`#9` -> `\t`, `#10` -> `\r`, `#13` -> `\n`)<li>Automatically lowercases articles (a, an, the), coordinating conjunctions, and prepositions</ul>Supports:<ul><li>Element signatures (e.g., `EDID`, `FULL`)<li>Element names (e.g., `Sounds`, `FormIDs`)<li>Element paths (e.g., `Sounds\Sound Files\ANAM`)<li>Element paths with array tokens (e.g., `Sounds\[*]\ANAM`)<li>Indexed element paths (e.g., `Sounds\[0]\ANAM`)<li>Indexed element paths with array tokens (e.g., `VMAD\Scripts\[*]\Script\[0]`)</ul>
