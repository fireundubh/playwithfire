<!-- TITLE: Cleaning PAKs -->

# Cleaning PAKs

## Essential Files

File | Extension | Description
:--- | :--- | :---
`meta.lsx` | `.lsx` | mod metadata displayed within the in-game mod manager
`story.div.osi` | `.osi` | primarily used to optimize runtime compile performance
`story_orphanqueries_ignore.txt` | `.txt` | 
`story_orphanqueries_local.txt` | `.txt` | 

## Nonessential Files

File | Extension | Description
:--- | :--- | :---
`story_ac.dat` | `.dat` | used for autocomplete in the editor
`goals.div` | `.div` | intermediate product of compiler
`story.div` | `.div` | intermediate product of compiler
`story_header.div` | `.div` | intermediate product of compiler; used for syntax highlighting in the editor
`goals.raw` | `.raw` | intermediate product of compiler

**Note:** In earlier versions of The Divinity Engine 2, log files and crash dumps were included in PAKs but this does not appear to be the case anymore.