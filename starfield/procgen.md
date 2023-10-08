---
title: Procedural Generation
description: 
published: true
date: 2023-10-08T17:30:05.404Z
tags: 
editor: markdown
dateCreated: 2023-10-08T17:30:05.404Z
---

```mermaid
stateDiagram
  [*] ---> PlanetContentManagerTree_LoadingCells_DO
  PlanetContentManagerTree_LoadingCells_DO ---> PCM_CellLoadRequest
  PCM_CellLoadRequest ---> PCM_CellLoad_GeneralDebug
  PCM_CellLoad_GeneralDebug ---> PCM_CellLoad_ManMadeTest8
   ---> PCM_CellLoad_ManMadeTest8Content
   ---> ContentNode_PCM_CellLoadRequest8
   ---> PackInContent_PCM_CellLoadRequest255
  PIPCMManMade_AbandondedIndustrialLarge01 ---> PackInPIPCMManMadeAbandondedIndustrialLarge01StorageCell
   ---> PackInContent_PCM_CellLoadRequest256
  PIPCMManMade_AbandondedIndustrialLarge02 ---> PackInPIPCMManMadeAbandondedIndustrialLarge02StorageCell
   ---> PackInContent_PCM_CellLoadRequest296
  PIPCMManMade_AbandondedIndustrialLarge03 ---> PackInPIPCMManMadeAbandondedIndustrialLarge03StorageCell
  PCM_CellLoad_GeneralDebug ---> PCM_CellLoad_VerifyLeveledPackinBranch
   ---> PCM_CellLoad_VerifyLeveledPackinContent
   ---> LeveledPackInContent_PCM_CellLoadRequest
  PCM_CellLoad_GeneralDebug ---> PCM_CellLoad_SpawnGroupTestBranch
   ---> PCM_CellLoad_SpawnGroupContentDebug03
   ---> PackInContent_PCM_CellLoadRequestDUPLICATE000DUPLICATE000DUPLICATE000
   ---> LeveledPackInContent_PCM_CellLoadRequest004DUPLICATE001DUPLICATE000
   ---> LeveledPackInContent_PCM_CellLoadRequest005DUPLICATE001DUPLICATE000
   ---> PCM_CellLoad_SpawnGroupContentDebug02
   ---> PackInContent_PCM_CellLoadRequestDUPLICATE000DUPLICATE000
   ---> LeveledPackInContent_PCM_CellLoadRequest004DUPLICATE001
   ---> LeveledPackInContent_PCM_CellLoadRequest005DUPLICATE001
   ---> PCM_CellLoad_SpawnGroupContentDebug01
   ---> PackInContent_PCM_CellLoadRequestDUPLICATE000
   ---> LeveledPackInContent_PCM_CellLoadRequest004
   ---> LeveledPackInContent_PCM_CellLoadRequest005
```