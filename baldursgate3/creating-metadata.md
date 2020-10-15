---
title: Creating Metadata
description: A quick look at mod metadata
published: true
date: 2020-10-15T00:15:50.031Z
tags: 
editor: markdown
dateCreated: 2020-10-15T00:04:21.671Z
---

Divinity Engine mods require a `meta.lsx` (XML) file that describes each mod.

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

# Example

```xml
<?xml version="1.0" encoding="UTF-8"?>
<save>
	<version major="4" minor="0" revision="0" build="49"/>
	<region id="Config">
		<node id="root">
			<children>
				<!-- <node id="Dependencies"/> -->
				<!-- If you're changing anything specific to the main story module, you'll need to add this dependency. -->
				<node id="Dependencies">
					<children>
						<node id="ModuleShortDesc">
							<attribute id="Folder" value="Gustav" type="30" />
							<attribute id="MD5" value="" type="23" />
							<attribute id="Name" value="Gustav" type="22" />
							<attribute id="UUID" value="991c9c7a-fb80-40cb-8f0d-b92d4e80e9b1" type="22" />
							<attribute id="Version" value="273876636" type="4" />
						</node>
					</children>
				</node>
				<node id="ModuleInfo">
					<!-- What's your name? -->
					<attribute id="Author" type="LSWString" value="fireundubh"/>

					<!-- What does the mod do? -->
					<attribute id="Description" type="LSWString" value="Changes per short rest and per long rest to per turn"/>

					<!-- This should be identical to the name of the PAK you will create. -->
					<attribute id="Folder" type="LSWString" value="NoRestForTheWicked"/>

					<!-- This should be identical to the name of the PAK you will create. -->
					<attribute id="Name" type="FixedString" value="NoRestForTheWicked"/>

					<!-- Generate a new UUID. Google how! -->
					<attribute id="UUID" type="FixedString" value="6160b6ed-de6a-4163-9603-9187e2bff481"/>

					<!-- Optionally, you can use your own version number. -->
					<attribute id="Version" type="int32" value="268435456"/>

					<!-- For most mods, at this time, there's generally no reason to change any of these values. -->
					<attribute id="CharacterCreationLevelName" type="FixedString" value=""/>
					<attribute id="GMTemplate" type="FixedString" value=""/>
					<attribute id="LobbyLevelName" type="FixedString" value=""/>
					<attribute id="MD5" type="LSString" value=""/>
					<attribute id="MainMenuBackgroundVideo" type="FixedString" value=""/>
					<attribute id="MenuLevelName" type="FixedString" value=""/>
					<attribute id="NumPlayers" type="uint8" value="4"/>
					<attribute id="PhotoBooth" type="FixedString" value="SYS_NPC_Portrait_A"/>
					<attribute id="StartupLevelName" type="FixedString" value="_TMPL_Sandbox"/>
					<attribute id="Tags" type="LSWString" value=""/>
					<attribute id="Type" type="FixedString" value="Adventure"/>
					<children>
						<node id="PublishVersion">
							<attribute id="Version" type="int32" value="268435456"/>
						</node>
						<node id="Scripts"/>
						<node id="TargetModes">
							<children>
								<node id="Target">
									<attribute id="Object" type="FixedString" value="Story"/>
								</node>
							</children>
						</node>
					</children>
				</node>
			</children>
		</node>
	</region>
</save>
```