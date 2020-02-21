---
title: Bash Tags Reference
description: 
published: true
date: 2020-02-21T02:08:16.541Z
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

# Common Bash Tags

## Actors.ACBS

> **Supported Games:** FO3, FNV, TES4, TES5, Enderal, SSE

Modifies the (ACBS) Configuration subrecord of actors.

## Actors.AIData

> **Supported Games:** FO3, FNV, TES4, TES5, Enderal, SSE

Modifies the (AIDT) AI Data subrecord of actors.

## Actors.AIPackages

> **Supported Games:** FO3, FNV, TES4

Modifies AI packages lists of actors.

Addition or removal of an (PKID) AI Package in the AI Packages subrecord in the following record types:

Game | Signature | Name
:--- | :--- | :---
FO3, FNV | NPC_ | Non-Player Character
TES4 | CREA | Creature

## Actors.AIPackagesForceAdd

> **Supported Games:** FO3, FNV, TES4

Adds to actor package lists. This tag forces the addition of packages even if they are removed by later-loading plugins tagged with Actors.AIPackages.

Addition of an (PKID) AI Package in the AI Packages subrecord in the following record types:

Game | Signature | Name
:--- | :--- | :---
FO3, FNV | NPC_ | Non-Player Character
TES4 | CREA | Creature

## Actors.Anims

> **Supported Games:** FO3, FNV, TES4

Modifies actor special animations lists.

Modification of the (KFFZ) Animations subrecord in the following record types: 

Game | Signature | Name
:--- | :--- | :---
FO3, FNV | NPC_ | Non-Player Character
TES4 | CREA | Creature

## Actors.CombatStyle

> **Supported Games:** FO3, FNV, TES4

Modifies the assigned combat styles of actors.

Modification of the (ZNAM) Combat Style subrecord in the following record types:

Game | Signature | Name
:--- | :--- | :---
FO3, FNV | NPC_ | Non-Player Character
TES4 | CREA | Creature

## Actors.DeathItem

> **Supported Games:** FO3, FNV, TES4

Modifies actor death items. Modification of the (INAM) Death Item subrecord in the following record types:

Game | Signature | Name
:--- | :--- | :---
FO3, FNV | NPC_ | Non-Player Character
TES4 | CREA | Creature

## Actors.Skeleton

> **Supported Games:** FO3, FNV, TES4

Modifies actor skeletons.

Game | Signature | Subrecord | Name
:--- | :--- | :--- | :---
FO3, FNV | NPC_ | MODL | Model Filename
FO3, FNV | NPC_ | MODB | Bound Radius
FO3, FNV | NPC_ | MODL | Texture File Hashes
TES4 | CREA | MODL | Model Filename
TES4 | CREA | MODB | Bound Radius
TES4 | CREA | MODL | Texture File Hashes

## Actors.Spells

> **Supported Games:** FO3, FNV, TES4

Modifies the Spells (also called Actor Effects) list of actors.

Addition, modification or removal of spells to the (SPLO) Spells subrecord in the following record types:

Game | Signature | Name
:--- | :--- | :---
FO3, FNV | NPC_ | Non-Player Character
TES4 | CREA | Creature

## Actors.SpellsForceAdd

Modifies the Spells (also called Actor Effects) list of actors. This tag forces the addition of spells even if they are removed by other plugins tagged with Actors.Spells. | Addition of (SPLO) spells to the Spells subrecord in the following record types: (CREA) Creature — Oblivion, Fallout 3 & Fallout: New Vegas only (NPC_) Non-Player Character Not available for Fallout 4. |

## Actors.Stats

Modifies actor stats (e.g. health, skills, stamina, etc.). | See the game-specific sections below for record types: See the Oblivion Actors.Stats section for more information. See the Fallout 3 Actors.Stats section for more information. See the Fallout: New Vegas Actors.Stats section for more information. See the Skyrim, Enderal: Forgotten Stories & Skyrim: Special Edition Actors.Stats section for more information. Not available for Fallout 4. |

## C.Acoustic

Modifies cell Acoustic Space. | The Acoustic Space (XCAS) subrecord in Cell (CELL) records. Not available for Oblivion & Fallout 4. |

## C.Climate

Modifies cell climates. | The following subrecords: Oblivion, Fallout 3 & Fallout: New Vegas only. (XCCM) Climate (DATA - flags) Behave Like Exterior Skyrim, Enderal: Forgotten Stories & Skyrim: Special Edition only. (XCCM) Sky/Weather from Region (DATA - flags) Show Sky Not available for Fallout 4. |

## C.Encounter

Modifies cell Encounter Zone. | The Encounter Zone (XEZN) subrecord in Cell (CELL) records. Not available for Oblivion & Fallout 4. |

## C.ForceHideLand

Modifies cell Force Hide Land flags. | The Force Hide Land flags field in the Grid (XCLC) subrecord in Cell (CELL) records. Not available for Oblivion & Fallout 4. |

## C.ImageSpace

Modifies cell ImageSpace. | The Image Space (XCIM) subrecord in Cell (CELL) records. Not available for Oblivion & Fallout 4. |

## C.Light

Modifies cell lighting or fog. | The following subrecords: All but Fallout 4: (XCLL) Lighting Ambient Color Directional Color Fog Color Fog Near Fog Far Fog Clip Dist Fog Power — Not available for Oblivion. Directional Rotation XY Directional Rotation Z Directional Fade (LTMP) Light Template — Not available for Oblivion Fallout 3 & Fallout: New Vegas only: (LNAM) Light Template Inherits Skyrim, Enderal: Forgotten Stories and Skyrim: Special Edition only: (XCLL) Lighting Ambient Colors Ambient Colors Directional Ambient Colors Specular Ambient Colors Scale Fog Color Far Fog Max Light Fade Begin Light Fade End Inherits Not available for Fallout 4. |

## C.LockList

Modifies cell lock list. | The lock list (XILL) subrecord in cell (CELL) records. Available for Skyrim, Enderal: Forgotten Stories and Skyrim: Special Edition only. |

## C.Location

Modifies cell Location. | The Location (XLCN) subrecord in Cell (CELL) records. Available for Skyrim, Enderal: Forgotten Stories and Skyrim: Special Edition only. |

## C.Music

Modifies cell music type. | The following subrecords: (XCMT) Music — Oblivion only. (XCMO) Music — All but Oblivion & Fallout 4. Not available for Fallout 4. |

## C.Name

Modifies cell names. | The (FULL) - Name subrecord in Cell (CELL) records. Not available for Fallout 4. |

## C.Owner

Modifies Cell Ownership. | The following Cell (CELL) subrecords: Ownership (XOWN) Owner (XRNK) Rank (XGLB) Global variable — Oblivion only. (DATA - flags) Public Place Not available for Fallout 4. |

## C.RecordFlags

Modifies the off-limits or dangerous flags. | Any Cell (CELL) record flags not covered by the other Cell-related Bash Tags. Not available for Fallout 4. |

## C.Regions

Modifies the Cells Region subrecord. | Any (XCLR) subrecord of the Cell (CELL) record. Not available for Fallout 4. |

## C.SkyLighting

Modifies Use Sky Lighting cell flag. | (DATA - Flags) Use Sky Lighting Available for Skyrim, Enderal: Forgotten Stories and Skyrim: Special Edition only. |

## C.Water

Modifies cell water type or level. | The following Cell (CELL) subrecords: (XCWT) Water (XCLW) Water Height (DATA - flags) Has Water (XNAM) Water Noise Texture — Not available for Oblivion. (XWEN) Water Environment Map — Skyrim, Enderal: Forgotten Stories and Skyrim: Special Edition only. Not available for Fallout 4. |

## Creatures.Blood

Modifies the creature blood subrecords. | The following (CREA) Creature subrecord(s): (NAM0) Blood Spray — Oblivion only. (NAM1) Blood Decal — Oblivion only. (CNAM) Impact Dataset — Fallout 3 & Fallout: New Vegas only. Oblivion, Fallout 3 & Fallout: New Vegas only. |

## Creatures.Type

Modifies the type of creatures. | The following (CREA) Creature subrecords: (DATA) Stats: Type: Animal Mutated Animal Mutated Insect Abomination Super Mutant Feral Ghoul Robot Giant Oblivion, Fallout 3 & Fallout: New Vegas only. |

## Deflst

Removes entries from the FormID List (FLST) record. | Removal of FormID from (FLST) FormID List record: FormIDs (LNAM) FormID Fallout 3 & Fallout: New Vegas only. |

## Delev

Deletes entries from Leveled Lists. | Removal of a (LVLO) Level List Entry from the following record types: (LVLC) Leveled Creature — Oblivion, Fallout 3 & Fallout: New Vegas only. (LVLI) Leveled Item (LVLN) Leveled NPC — Not available for Oblivion. (LVSP) Leveled SPELL — Oblivion, Skyrim, Enderal: Forgotten Stories & Skyrim: Special Edition only. |

## Destructible

Modifies destructible records. | See the game-specific sections below for record types: See the Fallout 3 Destructible section for more information. See the Fallout: New Vegas Destructible section for more information. See the Skyrim, Enderal: Forgotten Stories & Skyrim: Special Edition Destructible section for more information. Not available for Fallout 4. |

## Factions

Changes Creature or Non-Player Character factions. | Addition or removal of a faction, or change of faction rank in Non-Player Character (NPC_) or Creature (CREA) records. Factions (SNAM) Faction (SNAM) Faction - Rank Oblivion, Fallout 3 & Fallout: New Vegas only. |

## Graphics

Is a graphics replacer. | See the game-specific sections below for record types: See the Oblivion Graphics section for more information. See the Fallout 3 Graphics section for more information. See the Fallout: New Vegas Graphics section for more information. See the Skyrim, Enderal: Forgotten Stories & Skyrim: Special Edition Graphics section for more information. Not available for Fallout 4. |

## Invent

Changes inventories. | Addition, removal or change in count/number of an item in records: (CONT) Container (CREA) Creature — Oblivion, Fallout 3 & Fallout: New Vegas only. (NPC_) Non-Player Character Not available for Fallout 4. |

## Keywords

Modifies the lists of keywords attached to things. | Addition or removal of keywords (KWDA / KSIZ subrecord combo) for the following record types: (ACTI) Activator (ALCH) Ingestible (AMMO) Ammunition (ARMO) Armor (BOOK) Book (FLOR) Flora (FURN) Furniture (INGR) Ingredient (KEYM) Key (LCTN) Location (MGEF) Magic Effect (MISC) Misc. Item (NPC_) Non Player Character (SCRL) Scroll (SLGM) Soul Gem (SPEL) Spell (TACT) Talking Activator (WEAP) Weapon Skyrim, Enderal: Forgotten Stories & Skyrim: Special Edition only. |

## Names

Changes the names of things. | See the game-specific sections below for record types: See the Oblivion Names section for more information. See the Fallout 3 Names section for more information. See the Fallout: New Vegas Names section for more information. See the Skyrim, Enderal: Forgotten Stories & Skyrim: Special Edition Names section for more information. Not available for Fallout 4. |

## NPC.Class

Changes the classes of NPCs. | The (CNAM) Class subrecord of (NPC_) Non-Player Character records. Not available for Fallout 4. |

## Npc.EyesOnly

Modifies Non-Player Character eyes. | The Eyes (ENAM) subrecord of Non-Player Character (NPC_) records. Oblivion, Fallout 3 & Fallout: New Vegas only. |

## Npc.HairOnly

Modifies Non-Player Character hair. | The Hair (HNAM) subrecord of Non-Player Character (NPC_) records. Oblivion, Fallout 3 & Fallout: New Vegas only. |

## NPC.Race

Changes the races of NPCs. | The (RNAM) Race subrecord of (NPC_) Non-Player Character records. Not available for Fallout 4. |

## NpcFaces

Modifies Non-Player Character faces. | The following Non-Player Character (NPC_) subrecords: FaceGen Data (FGGS) FaceGen Geometry-Symmetric (FGGA) FaceGen Geometry-Asymmetric (FGTS) FaceGen Texture-Symmetry (ENAM) Eyes (HNAM) Hair (LNAM) Hair Length (HCLR) Hair Color Oblivion, Fallout 3 & Fallout: New Vegas only. |

## NpcFacesForceFullImport

Modifies Non-Player Character faces, and you wish to import the unmodified subrecords as well as the modified subrecords. | The following Non-Player Character (NPC_) subrecords: FaceGen Data (FGGS) FaceGen Geometry-Symmetric (FGGA) FaceGen Geometry-Asymmetric (FGTS) FaceGen Texture-Symmetry (ENAM) Eyes (HNAM) Hair (LNAM) Hair Length (HCLR) Hair Color Oblivion, Fallout 3 & Fallout: New Vegas only. |

## ObjectBounds

Changes the object bounds of things. | See the game-specific sections below for record types: See the Fallout 3 ObjectBounds section for more information. See the Fallout: New Vegas ObjectBounds section for more information. See the Skyrim, Enderal: Forgotten Stories & Skyrim: Special Edition ObjectBounds section for more information. See the Fallout 4 ObjectBounds section for more information. Not available for Oblivion. |

## Relev

Re-levels leveled list entries. | Changes to the Level or Count of a (LVLO) leveled list entry in: (LVLC) Leveled Creature — Oblivion, Fallout 3 & Fallout: New Vegas only. (LVLI) Leveled Item (LVLN) Leveled NPC — Not available for Oblivion. (LVSP) Leveled SPELL — Oblivion, Skyrim, Enderal: Forgotten Stories & Skyrim: Special Edition only. |

## Scripts

Modifies scripts attached to various things. | See the game-specific sections below for record types: See the Oblivion Scripts section for more information. See the Fallout 3 Scripts section for more information. See the Fallout: New Vegas Scripts section for more information. Oblivion, Fallout 3 & Fallout: New Vegas only. |

## Sound

Replaces sounds. | See the game-specific sections below for record types: See the Oblivion Sound section for more information. See the Fallout 3 Sound section for more information. See the Fallout: New Vegas Sound section for more information. See the Skyrim, Enderal: Forgotten Stories & Skyrim: Special Edition Sound section for more information. Not available for Fallout 4. |

## SpellStats

Modifies spell stats. | The following Spell (SPEL) subrecords: All but Fallout 4: (EDID) Editor ID (FULL) Name (SPIT) Cost (SPIT) Spell Type Oblivion, Fallout 3 & Fallout: New Vegas only: (SPIT) Level Skyrim, Enderal: Forgotten Stories and Skyrim: Special Edition only: (SPIT) Cast Duration (SPIT) Cast Type (SPIT) Charge Time (SPIT) Half-Cost Perk (SPIT) Range (SPIT) Target Type Not available for Fallout 4. |

## Stats

Modifies the stats (e.g. weight, value, etc.) of items and other objects. | See the game-specific sections below for record types: See the Oblivion Stats section for more information. See the Fallout 3 Stats section for more information. See the Fallout: New Vegas Stats section for more information. See the Skyrim, Enderal: Forgotten Stories & Skyrim: Special Edition Stats section for more information. Not available for Fallout 4. |

## Text

Modifies long-form text (e.g. the text in a book, or descriptions of armor, spells, weapons, etc.) of things. | See the game-specific sections below for record types: See the Oblivion Text section for more information. See the Fallout 3 Text section for more information. See the Fallout: New Vegas Text section for more information. See the Skyrim, Enderal: Forgotten Stories & Skyrim: Special Edition Text section for more information. Not Available for Fallout 4. |