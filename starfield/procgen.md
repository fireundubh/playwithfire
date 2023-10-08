---
title: Procedural Generation
description: 
published: true
date: 2023-10-08T17:31:00.538Z
tags: 
editor: markdown
dateCreated: 2023-10-08T17:30:05.404Z
---

```mermaid
stateDiagram
  [*] ---> PCM_CellLoadRequest
  PCM_CellLoadRequest ---> PCM_CellLoad_DisabledContent
  PCM_CellLoad_DisabledContent ---> PCM_CellLoad_Hazards_OLD
  PCM_CellLoad_DisabledContent ---> PCM_CellLoad_Hazards_GasVents
  PCM_CellLoad_DisabledContent ---> PCM_CellLoad_Hazards_GasVents_Radiation
  PCM_CellLoad_DisabledContent ---> PackInContent_PCM_CellLoadRequestDUPLICATE000DUPLICATE001DUPLICATE000
```