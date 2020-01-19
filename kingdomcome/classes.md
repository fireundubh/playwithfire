---
title: Classes
description: 
published: true
date: 2020-01-19T17:11:23.738Z
tags: 
---

Sections marked as `Done` have content, but may need additional details, such as method descriptions.

# Warhorse

Lua Global Name | C++ Class | Function Reference | Edit Status
--- | --- | --- | ---
Actor | `wh::entitymodule::C_ScriptBindActor` | [Function Reference](/kingdomcome/classes/actor) | Not started
Alchemy | `wh::playermodule::C_ScriptBind_Alchemy` | [Function Reference](/kingdomcome/classes/alchemy) | **Done**
Backgammon | `wh::playermodule::C_ScriptBindBackgammon` | [Function Reference](/kingdomcome/classes/backgammon) | **Done**
Boids | `wh::entitymodule::boids::C_ScriptBindBoids` | [Function Reference](/kingdomcome/classes/boids) | **Done**
Calendar | `wh::rpgmodule::C_ScriptBindCalendar` | [Function Reference](/kingdomcome/classes/calendar) | **Done**
Database | `wh::databasemodule::C_ScriptBindDatabase` | [Function Reference](/kingdomcome/classes/database) | **Done**
DialogModule | `wh::dialogmodule::C_ScriptBindDialog` | [Function Reference](/kingdomcome/classes/dialog) | **Done**
Dice | `wh::playermodule::C_ScriptBind_Dice` | [Function Reference](/kingdomcome/classes/dice) | **Done**
EntityModule | `wh::entitymodule::C_ScriptBindEntityModule` | [Function Reference](/kingdomcome/classes/entitymodule) | **Done**
EnvironmentModule | `wh::environmentmodule::C_ScriptBindEnvironment` | [Function Reference](/kingdomcome/classes/environmentmodule) | **Done**
Framework | `wh::framework::C_ScriptBindFramework` | [Function Reference](/kingdomcome/classes/framework) | **Done**
Game | `wh::game::CScriptBindGame` | [Function Reference](/kingdomcome/classes/game) | Not started
GameRules | `wh::entitymodule::C_ScriptBindGameRules` | [Function Reference](/kingdomcome/classes/gamerules) | Not started
Horse | `wh::entitymodule::C_ScriptBindHorse` | [Function Reference](/kingdomcome/classes/horse) | Not started
Human | `wh::entitymodule::C_ScriptBindHuman` | [Function Reference](/kingdomcome/classes/human) | Not started
InteractiveObject | `wh::entitymodule::C_ScriptBindInteractiveObject` | [Function Reference](/kingdomcome/classes/interactiveobject) | Not started
Inventory | `wh::entitymodule::C_ScriptBindInventory` | [Function Reference](/kingdomcome/classes/inventory) | Not started
ItemManager | `wh::entitymodule::C_ScriptBindItemManager` | [Function Reference](/kingdomcome/classes/itemmanager) | **Done**
Minigame | `wh::playermodule::C_ScriptBindMinigame` | [Function Reference](/kingdomcome/classes/minigame) | **Done**
PickableItem | `wh::entitymodule::C_ScriptBindPickableItem` | [Function Reference](/kingdomcome/classes/pickableitem) | Not started
Player | `wh::entitymodule::C_ScriptBindPlayer` | [Function Reference](/kingdomcome/classes/player) | Not started
QuestSystem | `wh::questmodule::C_ScriptBindQuest` | [Function Reference](/kingdomcome/classes/questsystem) | **Done**
RPG | `wh::rpgmodule::C_ScriptBindRPGModule` | [Function Reference](/kingdomcome/classes/rpg) | **Done**
Sharpening | `wh::playermodule::C_ScriptBind_Sharpening` | [Function Reference](/kingdomcome/classes/sharpening) | Not started
Shops | `wh::shopmodule::C_ScriptBindShop` | [Function Reference](/kingdomcome/classes/shops) | Not started
SmartObject | `wh::xgenaimodule::C_ScriptBindSmartObject` | [Function Reference](/kingdomcome/classes/smartobject) | Not started
Soul | `wh::rpgmodule::C_ScriptBindSoul` | [Function Reference](/kingdomcome/classes/soul) | Not started
Statistics | `wh::rpgmodule::C_ScriptBindStatistics` | [Function Reference](/kingdomcome/classes/statistics) | Not started
Trace | `wh::framework::C_ScriptBindTrace` | [Function Reference](/kingdomcome/classes/trace) | Not started
Tutorial | `wh::playermodule::C_ScriptBindTutorial` | [Function Reference](/kingdomcome/classes/tutorial) | Not started
UIMap | `wh::guimodule::C_ScriptBindMap` | [Function Reference](/kingdomcome/classes/uimap) | Not started
Variables | `wh::framework::C_ScriptBindVariables` | [Function Reference](/kingdomcome/classes/variables) | Not started
XGenAIModule | `wh::xgenaimodule::C_ScriptBindXGenAIModule` | [Function Reference](/kingdomcome/classes/xgenaimodule) | Not started

## Notes

* Return values of class methods are not fully tested and are largely the product of guess work.
* Class methods starting with the words "is," "has," or "have" are assumed to return a `boolean`. Most class methods are documented as returning `nil` when their return values cannot be determined from their name.
* In Lua, there is a single data structure, `table`, and eight data types: `nil`, `boolean`, `number`, `string`, `function`, `userdata`, `thread`, and `table`. See: [Lua 5.3 Reference Manual: Values and Types](https://www.lua.org/manual/5.3/manual.html#2.1)

# CryEngine

These are huge classes and will be added last.

Lua Global Name | C++ Class | Function Reference | Edit Status
--- | --- | --- | ---
Action | `CScriptableBase::CScriptBind_Action` | [Function Reference](/kingdomcome/classes/action) | Not started
ActionMapManager | `CScriptableBase::CScriptBind_ActionMapManager` | [Function Reference](/kingdomcome/classes/actionmapmanager) | Not started
ActorSystem | `CScriptableBase::CScriptBind_ActorSystem` | [Function Reference](/kingdomcome/classes/actorsystem) | Not started
AI | `CScriptableBase::CScriptBind_AI` | [Function Reference](/kingdomcome/classes/ai) | Not started
Boids | `CScriptableBase::CScriptBind_Boids` | [Function Reference](/kingdomcome/classes/boids) | Not started
DialogSystem | `CScriptableBase::CScriptBind_DialogSystem` | [Function Reference](/kingdomcome/classes/dialogsystem) | Not started
Entity | `CScriptableBase::CScriptBind_Entity` | [Function Reference](/kingdomcome/classes/entity) | Not started
Game | `CScriptableBase::CScriptBind_Game` | [Function Reference](/kingdomcome/classes/game) | Not started
GameAI | `CScriptableBase::CScriptBind_GameAI` | [Function Reference](/kingdomcome/classes/gameai) | Not started
GameAudio | `CScriptableBase::CScriptBind_GameAudio` | [Function Reference](/kingdomcome/classes/gameaudio) | Not started
GameRules | `CScriptableBase::CScriptBind_GameRules` | [Function Reference](/kingdomcome/classes/gamerules) | Not started
GameStatistics | `CScriptableBase::CScriptBind_GameStatistics` | [Function Reference](/kingdomcome/classes/gamestatistics) | Not started
GameToken | `CScriptableBase::CScriptBind_GameToken` | [Function Reference](/kingdomcome/classes/gametoken) | Not started
HitDeathReactions | `CScriptableBase::CScriptBind_HitDeathReactions` | [Function Reference](/kingdomcome/classes/hitdeathreactions) | Not started
HUD | `CScriptableBase::CScriptBind_HUD` | [Function Reference](/kingdomcome/classes/hud) | Not started
Inventory | `CScriptableBase::CScriptBind_Inventory` | [Function Reference](/kingdomcome/classes/inventory) | Not started
Item | `CScriptableBase::CScriptBind_Item` | [Function Reference](/kingdomcome/classes/item) | Not started
ItemSystem | `CScriptableBase::CScriptBind_ItemSystem` | [Function Reference](/kingdomcome/classes/itemsystem) | Not started
MaterialEffects | `CScriptableBase::CScriptBind_MaterialEffects` | [Function Reference](/kingdomcome/classes/materialeffects) | Not started
Particle | `CScriptableBase::CScriptBind_Particle` | [Function Reference](/kingdomcome/classes/particle) | Not started
Physics | `CScriptableBase::CScriptBindPhysics` | [Function Reference](/kingdomcome/classes/physics) | Not started
ProtectedBinds | `CScriptableBase::CScriptBind_ProtectedBinds` | [Function Reference](/kingdomcome/classes/protectedbinds) | Not started
Script | `CScriptableBase::CScriptBind_Script` | [Function Reference](/kingdomcome/classes/script) | **Done**
Sound | `CScriptableBase::CScriptBind_Sound` | [Function Reference](/kingdomcome/classes/sound) | Not started
System | `CScriptableBase::CScriptBind_System` | [Function Reference](/kingdomcome/classes/system) | Not started
Turret | `CScriptableBase::CScriptBind_Turret` | [Function Reference](/kingdomcome/classes/turret) | Not started
UIAction | `CScriptableBase::CScriptBind_UIAction` | [Function Reference](/kingdomcome/classes/uiaction) | Not started
Vehicle | `CScriptableBase::CScriptBind_Vehicle` | [Function Reference](/kingdomcome/classes/vehicle) | Not started
VehicleSeat | `CScriptableBase::CScriptBind_VehicleSeat` | [Function Reference](/kingdomcome/classes/vehicleseat) | Not started
VehicleSystem | `CScriptableBase::CScriptBind_VehicleSystem` | [Function Reference](/kingdomcome/classes/vehiclesystem) | Not started
Weapon | `CScriptableBase::CScriptBind_Weapon` | [Function Reference](/kingdomcome/classes/weapon) | Not started

**Note:** The above implementations may differ from the [official CryEngine C++ API Documentation](http://docs.cryengine.com/display/CPPAPI/Home).