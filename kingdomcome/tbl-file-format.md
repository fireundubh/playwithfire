<!-- TITLE: TBL File Format -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# TBL File Format
_This information was mirrored from the Nexus Wiki, contributed by Bodowens86, with some additions._

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
--- | --- | --- | --- | ---
0 | File Format Version | int32
4 | Descriptors Hash | uint32
8 | Layout Hash | uint32
12 | Table Version | int32
16 | Line Count | int32
20 | String Data Size | int32
24 | Unique String Count | int32

## Descriptors and Layout Hashes

Generating new hashes is unnecessary because new XML files cannot be added without modifying the game binaries.

These hashes are not dynamically generated based on the table content; they are hardcoded.

Hash | Algorithm | Initial Value
--- | --- | ---
Descriptors Hash | 32-bit FNV-1a | `0x811c9dc5`
Layout Hash | 32-bit FNV-1a | `0x811c9dc5`

_Additional hash information and pseudocode provided by moggabor and Bodowens86._

### Hash Generation Pseudocode

```text
descriptorsHash = 0x811c9dc5
layoutHash = 0x811c9dc5
explicitPaddingSize = 0
maxColumnAlignment = 1
lineSize = 0

for column in columns:
	descriptorsHash = crc32(column.name, descriptorsHash)
	descriptorsHash = crc32(column.typeID, descriptorsHash)
	layoutHash = crc32(column.offset, layoutHash)

	if columnDataType == Padding:
		explicitPaddingSize += column.size
		continue

	nextOffset = column.offset + column.size
	if lineSize < nextOffset:
		lineSize = nextOffset

	if maxColumnAlignment < column.alignment:
		maxColumnAlignment = column.alignment

lineSize += explicitPaddingSize

if lineSize % maxColumnAlignment:
	lineSize = maxColumnAlignment * ((lineSize + maxColumnAlignment - 1) / maxColumnAlignment)

layoutHash = crc32(lineSize, layoutHash)
```

## Data Types

Type ID | Name | Width in TBL file | Name in XML table descriptor
--- | --- | --- | ---
-1 | InvalidType | |
0 | Int | 32 bit | integer
1 | Int64 | 64 bit | bigint
2 | Float | 32 git | real
3 | Guid | 128 bit | uuid
4 | Bool | 8 bit | boolean
5 | String | 32 bit | text, character varying
6 | Vec3 | 96 bit (3 * 32 bit) | vec3
7 | Quat | 128 bit (4 * 32 bit) | quat
8 | QuatT | 224 bit ((4 + 3) * 32 bit) | quatt
9 | Padding | variable | 

_Type IDs provided by moggabor._

### Notes

* Strings are stored as 32-bit signed integers pointing into the string table​.
* Most tables do not use any padding. Whether table uses or doesn't use padding is hard-coded in KCD source. KCD data can only tell you that there is some padding somewhere, but not where. To see whether table uses padding, compare table description in XML file with line size in TBL file.