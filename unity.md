---
title: Unity
description: 
published: true
date: 2021-11-24T15:55:00.125Z
tags: 
editor: markdown
dateCreated: 2020-01-19T11:05:14.698Z
---

Creating mods for Unity games (with Mono backends) involves decompiling assemblies and patching in new code.

# Games

## Mono

Name |  Unity<br>Ver. | .NET<br>Compat. | .NET<br>Ver. | C#<br>Ver.
:--- | :--- | :--- | :--- | :---
Guild of Dungeoneering Ultimate Edition | 2020.3.9 ([Documentation](https://docs.unity3d.com/2020.3/Documentation/Manual/index.html)) | 4.x | [4.7.1](https://docs.unity3d.com/2020.3/Documentation/Manual/overview-of-dot-net-in-unity.html) | [8.0](https://docs.unity3d.com/2020.3/Documentation/Manual/CSharpCompiler.html)
Pathfinder: Kingmaker | 2018.1f0 ([Documentation](https://docs.unity3d.com/2018.1/Documentation/Manual/index.html)) | 4.x | 4.6 | 6.0
Pathfinder: Wrath of the Righteous | 2019.4.26f1 ([Documentation](https://docs.unity3d.com/2019.4/Documentation/Manual/index.html)) | 4.x | 4.6 | 7.3
Pillars of Eternity | 5.1 ([Documentation](https://docs.unity3d.com/510/Documentation/Manual/index.html)) | 3.5 | 3.5 | 3.0
Pillars of Eternity II: Deadfire | 5.6.3 ([Documentation](https://docs.unity3d.com/560/Documentation/Manual/index.html)) | 3.5 | 3.5 | 3.0
Rogue Lords | 2019.4.22 ([Documentation](https://docs.unity3d.com/2019.4/Documentation/Manual/index.html)) | 4.x | 4.6 | 7.3
Solasta: Crown of the Magister | 2019.4.32 ([Documentation](https://docs.unity3d.com/2019.4/Documentation/Manual/index.html)) | 4.x | 4.6 | 7.3
Star Dynasties | 2017.1.3f1 ([Documentation](https://docs.unity3d.com/2017.1/Documentation/Manual/index.html)) | 4.x | 4.6 | 6.0
Torment: Tides of Numenera | 5.4.1 ([Documentation](https://docs.unity3d.com/540/Documentation/Manual/index.html)) | 3.5 | 3.5 | 3.0
Tyranny | 5.2 ([Documentation](https://docs.unity3d.com/520/Documentation/Manual/index.html)) |3.5 | 3.5 | 3.0

## IL2CPP

> Mods will likely never exist for these games as long as they are compiled with IL2CPP.
{.is-info}

Name |  Unity<br>Ver. | .NET<br>Compat. | .NET<br>Ver. | C#<br>Ver.
:--- | :--- | :--- | :--- | :---
Disco Elysium: The Final Cut | 2020.2.3 ([Documentation](https://docs.unity3d.com/2020.2/Documentation/Manual/index.html)) | 4.x | 4.7.1 | 8.0
Encased | 2019.4.21 ([Documentation](https://docs.unity3d.com/2019.4/Documentation/Manual/index.html)) | 4.x | 4.6 | 7.3
Legend of Keepers | 2019.4.18 ([Documentation](https://docs.unity3d.com/2019.4/Documentation/Manual/index.html)) | 4.x | 4.6 | 7.3

# Tools

## Decompilers

- [dotPeek](https://www.jetbrains.com/decompiler/): a free .NET decompiler by JetBrains
- [dnSpy](https://github.com/dnSpy/dnSpy): an (abandoned) open source .NET decompiler by 0xd4d

You should be using dotPeek under most circumstances, filling out any stubbed out methods in the decompilation output with dnSpy.

dotPeek produces more accurate IL than dnSpy, owing to the fact dnSpy relied on the ILSpy 2.x engine. In addition, dotPeek is actively supported by a major company while dnSpy is abandoned.


## Patching

Type | Name | Developer | Price | License | Website
:--- | :--- | :--- | :--- | :--- | :---
Patcher (Injection) | MelonLoader (based on HarmonyX/MonoMod) | LavaGang | Open source | Apache 2.0 | [GitHub](https://github.com/LavaGang/MelonLoader) &middot; [melonwiki.xyz](https://melonwiki.xyz) 
Patcher (Injection) | Harmony | pardeike | Open source | MIT | [GitHub](https://github.com/pardeike/Harmony)
Patcher (Injection) | BepInEx (based on Harmony) | bbepis | Open Source | MIT | [GitHub](https://github.com/BepInEx/BepInEx)
Patcher (Direct/Injection) | MonoMod (based on Harmony) | 0x0ade | Open source | MIT | [GitHub](https://github.com/MonoMod/MonoMod)
Patcher (Direct) | Patchwork | Greg Ros | Open source | MIT | [GitHub](https://github.com/GregRos/Patchwork)
Injector | Unity Doorstop | denikson | Open source | CC0-1.0 | [GitHub](https://github.com/NeighTools/UnityDoorstop)


## Asset Bundles

Name | Developer | Licensing | Website
:--- | :--- | :--- | :---
Asset Studio | Perfare | Open source (MIT) | [GitHub](https://github.com/Perfare/AssetStudio)
AssetTools&period;NET (based on UABE) | nesrak1 | Open source (MIT) | [GitHub](https://github.com/nesrak1/AssetsTools.NET)
uTinyRipper | mafaca | Open source (MIT) | [GitHub](https://github.com/mafaca/UtinyRipper)
uTinyRipperExporter CLI | spacehamster | Open source (MIT) | [GitHub](https://github.com/spacehamster/UtinyRipperExporter)
Unity Assets Bundle Extractor (UABE) | DerPopo | N/A | [7 Days To Die Forum](https://community.7daystodie.com/topic/1871-unity-assets-bundle-extractor/)


## Misc.

Type | Name | Developer | Price | License | Website
:--- | :--- | :--- | :--- | :--- | :---
Deobfuscator | de4dot | 0xd4d | Open source | GPL v3 | [GitHub Fork](https://github.com/fireundubh/de4dot/pdbgen)
Type Safety Evaluator | PEVerify | Microsoft | Free | Proprietary | [Microsoft](https://docs.microsoft.com/en-us/dotnet/framework/tools/peverify-exe-peverify-tool)

> If you use Microsoft's [PEVerify Tool](https://docs.microsoft.com/en-us/dotnet/framework/tools/peverify-exe-peverify-tool) (e.g., Patchwork's Test Run), you may notice that an unmodded Unity game has IL errors in `Assembly-CSharp.dll`. These errors could be caused by bad IL or IL optimizations. For example, the latest version of _Torment: Tides of Numenera_ has 150 IL errors in `Assembly-CSharp.dll`. Most IL errors can be monkey patched.
{.is-warning}


## Untested

DevX has a number of [extremely expensive tools](https://devxdevelopment.com/) for reverse engineering Unity games. While some of these tools could be useful to more advanced modders, in most cases, you don't need them.


# References

Tutorial | Description
:--- | :---
[Patchwork Design Patterns](/unity/patchwork-design-patterns) | How to use Patchwork attributes for common problems
[Patchwork Project Structure](/unity/patchwork-project-structure) | How to structure a Patchwork project
[Turning a release build into a debug build](/unity/turning-a-release-build-into-a-debug-build) | How to get line numbers, full PDBs, and live debugging working
