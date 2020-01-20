---
title: Patch Notes
description: 
published: true
date: 2020-01-20T11:13:49.698Z
tags: 
---

Version | Manifest ID | Patch Notes
:--- | :--- | :--
`1.0.10` | `4137201467282432792` | [Patch Details](https://steamcommunity.com/games/Pathfinder_Kingmaker/announcements/detail/1711824163719704513)
`1.0.9` | `3329346642708156469` | [Patch Details](https://steamcommunity.com/games/Pathfinder_Kingmaker/announcements/detail/2924417816931842509)
`1.0.8c` | `7773343900112385919` | [Patch Details](https://steamcommunity.com/games/Pathfinder_Kingmaker/announcements/detail/2924417816900833325)
`1.0.8b` | `4551845841087663139` | 
`1.0.7` | `5750998838144035341` | [Patch Details](https://steamcommunity.com/games/Pathfinder_Kingmaker/announcements/detail/1708445194439906203)
&nbsp; | `3625063316203614488` | [Assembly Changes](#3625063316203614488)
&nbsp; | `946625482595150857` | [Assembly Changes](#946625482595150857)
`1.0.6` | `6336459653349909543` | [Patch Details](https://steamcommunity.com/games/Pathfinder_Kingmaker/announcements/detail/1708445194413594388)
`1.0.5` | `7894022154904016667` | [Patch Details](https://steamcommunity.com/games/Pathfinder_Kingmaker/announcements/detail/1708445194411519344)
&nbsp; | `4920380694923421717` | [Assembly Changes](#4920380694923421717)
`1.0.4` | `6358573070219561752` | [Patch Details](https://steamcommunity.com/games/Pathfinder_Kingmaker/announcements/detail/2940179248248985616)
`1.0.3` | `229482041491868730` | [Patch Details](https://steamcommunity.com/games/Pathfinder_Kingmaker/announcements/detail/2940179248226283738)
`1.0.2` | `2451367926564256244` | [Patch Details](https://steamcommunity.com/games/Pathfinder_Kingmaker/announcements/detail/2940179248218810867)
`1.0.1` | `1412067188604596331` | [Patch Details](https://steamcommunity.com/games/Pathfinder_Kingmaker/announcements/detail/1711822259759145662)

# Assembly Changes

Unknown patch versions only.

## 3625063316203614488

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem | `SceneEntitiesState.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgradeSystem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeAction.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeActionType.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `EnchantmentFeaturesForFixing.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40261_FixDuplicateEnchantments.cs`

## 946625482595150857

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints/Facts | `Fact.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `ActivateTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DamageToMapObjectTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DeactivateTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DeviceInteractionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DoorInteractionViewTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `EvaluatedUnitCombatTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `EvaluatedUnitDeathTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `EvaluatedUnitHealthTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `GenericInteractionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `MapObjectPerceptionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `PerceptionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `RestTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `ScriptZoneTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `SkillCheckInteractionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `SpellCastTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `SummonPoolTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `TimeOfDayChangedTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `UIEventTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `UnitDeathTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `UnitHealthTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Items | `ItemEntityShield.cs`

## 4920380694923421717

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp/Kingmaker | `GameStarter.cs`
Modified | cs | Assembly-CSharp/Kingmaker | `MainMenu.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBFeatureSelector.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBSelectorLayer.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBuildSelectorItem.cs`
Added | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `AreaDidLoadTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Facts | `AdditionalSneakDamageOnHit.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Facts | `BackToBack.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgradeSystem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeAction.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeActionType.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `JaethalQ3EssentialForGameFixer.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39479_AmiriUnhide1.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39480_JubilostQuest.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `RemoveCutsceneRaiseDeadFromSpellbooks.cs`
Modified | cs | Assembly-CSharp/Kingmaker/RuleSystem/Rules/Abilities | `RuleCastSpell.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Group | `GroupController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/SettingsUI | `GameSettingsController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/SettingsUI | `GraphicsSettingsController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic | `Spellbook.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic | `UnitDescriptor.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Buffs | `RemoveBuffOnLoad.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Buffs/Blueprints | `BlueprintBuff.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Mechanics/Components | `AddInitiatorSkillRollTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Utility | `SystemUtil.cs`
Modified | cs | Assembly-CSharp/Kingmaker/View | `CameraRig.cs`
