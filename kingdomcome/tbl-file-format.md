<!-- TITLE: TBL File Format -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# TBL File Format
This information was mirrored from the Nexus Wiki, contributed by "Bodowens86."

## Top-Level File Format

Offset | Name | Type
--- | --- | ---
0 | Header | Header
28 | Row Data | Type depends on table structure, count is `Line Count` in `Header`
28 + line size * line count | String Data |

### Notes

Line size can be calculated as `(file size - header size - string data size) / line count`.

## Header Format

Offset | Name | Type
--- | --- | ---
0 | File Format Version | int32
4 | Descriptors Hash | uint32
8 | Layout Hash | uint32
12 | Table Version | int32
16 | Line Count | int32
20 | String Data Size | int32
24 | Unique String Count | int32

## Data Types

Name | Width in TBL file | Name in XML table descriptor
--- | --- | ---
Int | 32 bit | integer
Int64 | 64 bit | bigint
Float | 32 git | real
Guid | 128 bit | uuid
Bool | 8 bit | boolean
String | 32 bit | text, character varying
Vec3 | 96 bit (3 * 32 bit) | vec3
Quat | 128 bit (4 * 32 bit) | quat
QuatT | 224 bit ((4 + 3) * 32 bit) | quatt
Padding | variable | 

### Notes

* Strings are stored as 32-bit signed integers pointing into the string table​.
* Most tables do not use any padding. Whether table uses or doesn't use padding is hard-coded in KCD source. KCD data can only tell you that there is some padding somewhere, but not where. To see whether table uses padding, compare table description in XML file with line size in TBL file.