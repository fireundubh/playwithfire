---
title: Bash Tags Reference
description: 
published: true
date: 2020-02-22T01:47:54.672Z
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

**Note:** TES5 includes Enderal.

Tag | Description | Supported Games
:--- | :--- | :---
Actors.ACBS | Modifies ACBS subrecord of actors | FO3, FNV, TES4, TES5, SSE
Actors.AIData | Modifies AIDT subrecord of actors | FO3, FNV, TES4, TES5, SSE
[Actors.AIPackages](#actorsaipackages) | Modifies AI packages lists of actors | FO3, FNV, TES4
[Actors.AIPackagesForceAdd](#actorsaipackagesforceadd) | Like Actors.AIPackages, but also forces addition of packages even if removed by similarly tagged plugins | FO3, FNV, TES4
[Actors.Anims](#actorsanims) | Modifies actor special animations lists | FO3, FNV, TES4
[Actors.CombatStyle](#actorscombatstyle) | Modifies the assigned combat styles of actors | FO3, FNV, TES4
[Actors.DeathItem](#actorsdeathitem) | Modifies actor death items | FO3, FNV, TES4
[Actors.Skeleton](#actorsskeleton) | Modifies actor skeletons | FO3, FNV, TES4
[Actors.Spells](#actorsspells) | Modifies the Spells\Actor Effects list of actors | FO3, FNV, TES4
[Actors.SpellsForceAdd](#actorsspellsforceadd) | Like Actors.Spells, but also forces addition of spells even if removed by similarly tagged plugins | FO3, FNV, TES4
Actors.Stats | Modifies actor stats (e.g. health, skills, stamina, etc.) | FO3, FNV, TES4, TES5, SSE
C.Acoustic | Modifies XCAS subrecord in CELL records | FO3, FNV, TES5, SSE
[C.Climate](#cclimate) | Modifies cell climates | FO3, FNV, TES4, TE5, SSE
C.Encounter | Modifies XEZN subrecord in CELL records | FO3, FNV, TES5, SSE
C.ForceHideLand | Modifies Force Hide Land flags in XCLC subrecord in CELL records | FO3, FNV, TES5, SSE
C.ImageSpace | Modifies XCIM subrecord in CELL records | FO3, FNV, TES5, SSE

## Actors.AIPackages

Addition or removal of an (PKID) AI Package in the AI Packages subrecord in the following record types:

Game | Signature | Name
:--- | :--- | :---
FO3, FNV | NPC_ | Non-Player Character
TES4 | CREA | Creature

## Actors.AIPackagesForceAdd

Addition of an (PKID) AI Package in the AI Packages subrecord in the following record types:

Game | Signature | Name
:--- | :--- | :---
FO3, FNV | NPC_ | Non-Player Character
TES4 | CREA | Creature

## Actors.Anims

Modification of the (KFFZ) Animations subrecord in the following record types: 

Game | Signature | Name
:--- | :--- | :---
FO3, FNV | NPC_ | Non-Player Character
TES4 | CREA | Creature

## Actors.CombatStyle

Modification of the (ZNAM) Combat Style subrecord in the following record types:

Game | Signature | Name
:--- | :--- | :---
FO3, FNV | NPC_ | Non-Player Character
TES4 | CREA | Creature

## Actors.DeathItem

Modification of the (INAM) Death Item subrecord in the following record types:

Game | Signature | Name
:--- | :--- | :---
FO3, FNV | NPC_ | Non-Player Character
TES4 | CREA | Creature

## Actors.Skeleton

Modification of the MODL, MODB, and MODL subrecords in NPC_ and CREA records.

Game | Signature | Subrecord | Name
:--- | :--- | :--- | :---
FO3, FNV | NPC_ | MODL | Model Filename
FO3, FNV | NPC_ | MODB | Bound Radius
FO3, FNV | NPC_ | MODL | Texture File Hashes
TES4 | CREA | MODL | Model Filename
TES4 | CREA | MODB | Bound Radius
TES4 | CREA | MODL | Texture File Hashes

## Actors.Spells

Addition, modification or removal of spells to the (SPLO) Spells subrecord in the following record types:

Game | Signature | Name
:--- | :--- | :---
FO3, FNV | NPC_ | Non-Player Character
TES4 | CREA | Creature

## Actors.SpellsForceAdd

Addition of (SPLO) spells to the Spells subrecord in the following record types:

Game | Signature | Name
:--- | :--- | :---
FO3, FNV | NPC_ | Non-Player Character
TES4 | CREA | Creature

## C.Climate

Game | Element | Name
:--- | :--- | :---
FO3, FNV, TES4 | XCCM | Climate
FO3, FNV, TES4 | DATA | Behave Like Exterior
TES5, Enderal, SSE | XCCM | Sky/Weather from Region
TES5, Enderal, SSE | DATA | Show Sky

## C.Light

> **Supported Games:** All games except FO4

Modifies cell lighting or fog.

Game | Element | Name | Subrecords
:--- | :--- | :--- | :---
All | XCLL | Lighting | Ambient Color<br>Directional Color<br>Fog Color<br>Fog Near<br>Fog Clip Dist<br>Directional Rotation XY<br>Directional Rotation Z<br>Directional Fade
All except TES4 | XCLL | Lighting | Fog Power
All except TES4 | LTMP | Light Template | 
FO3, FNV | LNAM | Light Template Inherits |
TES5, Enderal, SSE | XCLL | Lighting | Ambient Colors<br>Ambient Colors Directional<br>Ambient Colors Specular<br>Ambient Colors Scale<br>Fog Color Far<br>Fog Max<br>Light Fade Begin<br>Light Fade End<br>Inherits

## C.LockList

> **Supported Games:** TES5, Enderal, SSE

Modifies cell lock list. The lock list (XILL) subrecord in cell (CELL) records.

## C.Location

> **Supported Games:** TES5, Enderal, SSE

Modifies cell Location. The Location (XLCN) subrecord in Cell (CELL) records.

## C.Music

> **Supported Games:** FO3, FNV, TES4, TES5, Enderal, SSE

Modifies cell music type. 

Game | Element | Name
:--- | :--- | :---
TES4 | XCMT | Music
All except TES4 | XCMO | Music

## C&#46;Name

> **Supported Games:** All except FO4

Modifies cell names. The (FULL) - Name subrecord in Cell (CELL) records.

## C.Owner

> **Supported Games:** All except FO4

Modifies Cell Ownership. The following Cell (CELL) subrecords:

Game | Element | Subrecords
:--- | :--- | :---
All | Ownership | XOWN<br>XRNK
TES4 | Ownership | XGLB
All | DATA |

## C.RecordFlags

> **Supported Games:** All except FO4

Modifies the off-limits or dangerous flags. Any Cell (CELL) record flags not covered by the other Cell-related Bash Tags.

## C.Regions

> **Supported Games:** All except FO4

Modifies the Cells Region subrecord. Any (XCLR) subrecord of the Cell (CELL) record.

## C.SkyLighting

> **Supported Games:** TES5, Enderal, SSE

Modifies Use Sky Lighting cell flag.

Game | Element | Paths
:--- | :--- | :---
TES5, Enderal, SSE | CELL | DATA\Use Sky Lighting Available

## C.Water

> **Supported Games:** All except FO4

Modifies cell water type or level.

The following Cell (CELL) subrecords:

Game | Element | Name
:--- | :--- | :---
All supported | XCWT | Water
All supported | XCLW | Water Height
All supported | DATA | Has Water
All except TES4 | XNAM | Water Noise Texture
TES5, Enderal, SSE | XWEN | Water Environment Map

## Creatures.Blood

> **Supported Games:** FO3, FNV, TES4

Modifies the creature blood subrecords.

The following (CREA) Creature subrecord(s):

Game | Element | Name
:--- | :--- | :---
TES4 | NAM0 | Blood Spray
TES4 | NAM1 | Blood Decal
FO3, FNV | CNAM | Impact Dataset

## Creatures.Type

> **Supported Games:** FO3, FNV

Modifies the type of creatures.

The following (CREA) Creature subrecords:

Game | Element | Paths
:--- | :--- | :---
FO3, FNV | DATA | Type\Animal<br>Type\Mutated Animal<br>Type\Mutated Insect<br>Type\Abomination<br>Type\Super Mutant<br>Type\Feral Ghoul<br>Type\Robot<br>Type\Giant

## Deflst

> **Supported Games:** FO3, FNV

Removes entries from the FormID List (FLST) record. 

Game | Element | Paths
:--- | :--- | :---
FO3, FNV | FormIDs | LNAM

## Delev

> **Supported Games:** FO3, FNV, TES4, TES5, Enderal, SSE

Deletes entries from Leveled Lists. Removal of a (LVLO) Level List Entry from the following record types:

Game | Signature | Name
:--- | :--- | :---
FO3, FNV, TES4 | LVLC | Leveled Creature
All | LVLI | Leveled Item
All except TES4 | LVLN | Leveled NPC
TES4, TES5, Enderal, SSE | LVSP | Leveled Spell

## Destructible

> **Supported Games:** FO3, FNV, TES5, Enderal, SSE

Modifies destructible records.

## Factions

> **Supported Games:** FO3, FNV, TES4

Changes Creature or Non-Player Character factions.

Game | Element | Paths
:--- | :--- | :---
FO3, FNV, TES4 | Factions | SNAM\Faction
FO3, FNV, TES4 | Factions | SNAM\Faction Rank

## Graphics

> **Supported Games:** FO3, FNV, TES4, TES5, Enderal, SSE

Is a graphics replacer.

## Invent

> **Supported Games:** All except FO4

Changes inventories.

Game | Signature | Name
:--- | :--- | :---
All | CONT | Container
FO3, FNV, TES4 | CREA | Creature
All | NPC_ | Non-Player Character

## Keywords

> **Supported Games:** TES5, Enderal, SSE

Modifies the lists of keywords attached to things. | Addition or removal of keywords (KWDA / KSIZ subrecord combo) for the following record types:

Game | Signature | Name
:--- | :--- | :---
TES5, Enderal, SSE | ACTI | Activator
TES5, Enderal, SSE | ALCH | Ingestible
TES5, Enderal, SSE | AMMO | Ammunition
TES5, Enderal, SSE | ARMO | Armor
TES5, Enderal, SSE | BOOK | Book
TES5, Enderal, SSE | FLOR | Flora
TES5, Enderal, SSE | FURN | Furniture
TES5, Enderal, SSE | INGR | Ingredient
TES5, Enderal, SSE | KEYM | Key
TES5, Enderal, SSE | LCTN | Location
TES5, Enderal, SSE | MGEF | Magic Effect
TES5, Enderal, SSE | MISC | Misc. Item
TES5, Enderal, SSE | NPC_ | Non Player Character
TES5, Enderal, SSE | SCRL | Scroll
TES5, Enderal, SSE | SLGM | Soul Gem
TES5, Enderal, SSE | SPEL | Spell
TES5, Enderal, SSE | TACT | Talking Activator
TES5, Enderal, SSE | WEAP | Weapon

## Names

> **Supported Games:** FO3, FNV, TES4, TES5, Enderal, SSE

Changes the names of things. 

## NPC.Class

> **Supported Games:** All except FO4

Changes the classes of NPCs. The (CNAM) Class subrecord of (NPC_) Non-Player Character records.

## Npc.EyesOnly

> **Supported Games:** FO3, FNV, TES4

Modifies Non-Player Character eyes. The Eyes (ENAM) subrecord of Non-Player Character (NPC_) records. 

## Npc.HairOnly

> **Supported Games:** FO3, FNV, TES4

Modifies Non-Player Character hair. The Hair (HNAM) subrecord of Non-Player Character (NPC_) records.

## NPC.Race

> **Supported Games:** All except FO4

Changes the races of NPCs. The (RNAM) Race subrecord of (NPC_) Non-Player Character records.

## NpcFaces

> **Supported Games:** FO3, FNV, TES4

Modifies Non-Player Character faces. The following Non-Player Character (NPC_) subrecords:

Element | Paths
:--- | :---
FaceGen Data | FGGS - FaceGen Geometry-Symmetric<br>FGGA - FaceGen Geometry-Asymmetric<br>FGTS - FaceGen Texture-Symmetry
ENAM - Eyes | 
HNAM - Hair |
LNAM - Hair Length |
HCLR - Hair Color |

## NpcFacesForceFullImport

> **Supported Games:** FO3, FNV, TES4

Modifies Non-Player Character faces, and you wish to import the unmodified subrecords as well as the modified subrecords. 

The following Non-Player Character (NPC_) subrecords:

Element | Paths
:--- | :---
FaceGen Data | FGGS - FaceGen Geometry-Symmetric<br>FGGA - FaceGen Geometry-Asymmetric<br>FGTS - FaceGen Texture-Symmetry
ENAM - Eyes | 
HNAM - Hair |
LNAM - Hair Length |
HCLR - Hair Color |

## ObjectBounds

> **Supported Games:** FO3, FNV, TES5, Enderal, SSE

Changes the object bounds of things.

## Relev

> **Supported Games:** FO3, FNV, TES4, TES5, Enderal, SSE

Re-levels leveled list entries. Changes to the Level or Count of a (LVLO) leveled list entry in:

Game | Signature | Name
:--- | :--- | :---
FO3, FNV, TES4 | LVLC | Leveled Creature
All | LVLI | Leveled Item
All except TES4 | LVLN | Leveled NPC
TES4, TES5, Enderal, SSE | LVSP | Leveled Spell

## Scripts

> **Supported Games:** FO3, FNV, TES4

Modifies scripts attached to various things.

## Sound

> **Supported Games:** FO3, FNV, TES4, TES5, Enderal, SSE

Replaces sounds.

## SpellStats

Modifies spell stats. | The following Spell (SPEL) subrecords:

Game | Element | Paths
:--- | :--- | :---
All except FO4 | EDID - Editor ID | 
All except FO4 | FULL - Name | 
All except FO4 | SPIT | Cost<br>Spell Type 
FO3, FNV, TES4 | SPIT | Level
TES5, Enderal, SSE | SPIT | Cast Duration<br>Cast Type<br>Charge Time<br>Half-Cost Perk<br>Range<br>Target Type

## Stats

> **Supported Games:** FO3, FNV, TES4, TES5, Enderal, SSE

Modifies the stats (e.g. weight, value, etc.) of items and other objects.

## Text

> **Supported Games:** FO3, FNV, TES4, TES5, Enderal, SSE

Modifies long-form text (e.g. the text in a book, or descriptions of armor, spells, weapons, etc.) of things.