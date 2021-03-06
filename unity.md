---
title: Unity
description: 
published: true
date: 2021-02-23T19:27:27.919Z
tags: 
editor: markdown
dateCreated: 2020-01-19T11:05:14.698Z
---

# Games

Name | Developer | Unity Version | .NET Compatibility
:--- | :--- | :--- | :---
Pathfinder: Kingmaker | Owlcat Games | 2018.1f0 ([Documentation](https://docs.unity3d.com/2018.1/Documentation/Manual/index.html)) | .NET 4.x (Assembly-CSharp.dll)
Pathfinder: Wrath of the Righteous | Owlcat Games | 2019.4 ([Documentation](https://docs.unity3d.com/2019.4/Documentation/Manual/index.html)) | .NET 4.x (Assembly-CSharp.dll)
Pillars of Eternity | Obsidian Entertainment | 5.1 ([Documentation](https://docs.unity3d.com/510/Documentation/Manual/index.html)) | .NET 3.5 (Assembly-CSharp.dll)
Pillars of Eternity II: Deadfire | Obsidian Entertainment | 5.6.3 ([Documentation](https://docs.unity3d.com/560/Documentation/Manual/index.html)) | .NET 3.5 (Assembly-CSharp.dll)
Torment: Tides of Numenera |  inXile Entertainment | 5.4.1 ([Documentation](https://docs.unity3d.com/540/Documentation/Manual/index.html)) | .NET 3.5 (Assembly-CSharp.dll)
Tyranny | Obsidian Entertainment | 5.2 ([Documentation](https://docs.unity3d.com/520/Documentation/Manual/index.html)) | .NET 3.5 (Assembly-CSharp.dll)

# Tools

Most of modding Unity games involves decompiling `Assembly-CSharp.dll` and patching in new code.

## Reversing

Type | Name | Developer | Price | License | Website
:--- | :--- | :--- | :--- | :--- | :---
Decompiler | dotPeek | JetBrains | Free | Commercial | [JetBrains](https://www.jetbrains.com/decompiler/)
Decompiler/IL Editor | dnSpy | 0xd4d | Open source | GPL v3 | [GitHub](https://github.com/dnSpy/dnSpy)
Deobfuscator | de4dot | 0xd4d | Open source | GPL v3 | [GitHub Fork](https://github.com/fireundubh/de4dot/pdbgen)
Type Safety Evaluator | PEVerify | Microsoft | Free | Proprietary | [Microsoft](https://docs.microsoft.com/en-us/dotnet/framework/tools/peverify-exe-peverify-tool)

**Note 1:** dnSpy and de4dot were abandoned by the original developer.

**Note 2:** dotPeek produces more accurate IL than dnSpy ever did because dnSpy relied on the ILSpy 2.x engine.

## Patching

Type | Name | Developer | Price | License | Website
:--- | :--- | :--- | :--- | :--- | :---
Patcher (Direct) | Patchwork | Greg Ros | Open source | MIT | [GitHub](https://github.com/GregRos/Patchwork)
Patcher (Injection) | Harmony | pardeike | Open source | MIT | [GitHub](https://github.com/pardeike/Harmony)
Patcher (Injection) | BepInEx (based on Harmony) | bbepis | Open Source | MIT | [GitHub](https://github.com/BepInEx/BepInEx)
Patcher (Direct/Injection) | MonoMod (based on Harmony) | 0x0ade | Open source | MIT | [GitHub](https://github.com/MonoMod/MonoMod)
Injector | Unity Doorstop | denikson | Open source | CC0-1.0 | [GitHub](https://github.com/NeighTools/UnityDoorstop)

## Asset Unbundling

Type | Name | Developer | Price | License | Website
:--- | :--- | :--- | :--- | :--- | :---
AssetBundle Extractor | Asset Studio | Perfare | Open source | MIT | [GitHub](https://github.com/Perfare/AssetStudio)
AssetBundle Extractor | uTinyRipper | mafaca | Free |  | [GitHub](https://github.com/mafaca/UtinyRipper)
AssetBundle Extractor | uTinyRipperExporter CLI | spacehamster | Open source | MIT | [GitHub](https://github.com/spacehamster/UtinyRipperExporter)
AssetBundle Extractor | Unity Assets Bundle Extractor (UABE) | DerPopo | Free | Closed | [7 Days To Die Forum](https://community.7daystodie.com/topic/1871-unity-assets-bundle-extractor/)


## Untested

DevX has a number of [extremely expensive tools](https://devxdevelopment.com/) for reverse engineering Unity games. While some of these tools could be useful to more advanced modders, in most cases, you don't need them.


# References

Tutorial | Description
:--- | :---
[Patchwork Design Patterns](/unity/patchwork-design-patterns) | How to use Patchwork attributes for common problems
[Patchwork Project Structure](/unity/patchwork-project-structure) | How to structure a Patchwork project
[Turning a release build into a debug build](/unity/turning-a-release-build-into-a-debug-build) | ADVANCED. You do not need to do this unless you use debug logging and want Assembly-CSharp line numbers in call stacks.


# Notes

* If you use Microsoft's [PEVerify Tool](https://docs.microsoft.com/en-us/dotnet/framework/tools/peverify-exe-peverify-tool) (e.g., Patchwork's Test Run), you may notice that an unmodded Unity game has IL errors in `Assembly-CSharp.dll`. These errors are likely caused by Unity either writing bad IL or, less likely, performing (probably unnecessary) IL optimizations. For example, the latest version of _Torment: Tides of Numenera_ has 150 IL errors in `Assembly-CSharp.dll`. Most IL errors can be monkey patched.