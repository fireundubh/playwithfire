<!-- TITLE: Classes -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 
# Classes
Only sections marked as `(completed)` have content. The current version of Wiki.js does not color nonexistent pages.

## Warhorse

Lua Global Name | C++ Class | Function Reference
--- | --- | ---
Actor | wh::entitymodule::C_ScriptBindActor | [Function Reference](classes/actor)
Alchemy | wh::playermodule::C_ScriptBind_Alchemy | [Function Reference](classes/alchemy)
Backgammon | wh::playermodule::C_ScriptBindBackgammon | [Function Reference](classes/backgammon) (completed)
Boids | wh::entitymodule::boids::C_ScriptBindBoids | [Function Reference](classes/boids) (completed)
Calendar | wh::rpgmodule::C_ScriptBindCalendar | [Function Reference](classes/calendar) (completed)
Database | wh::databasemodule::C_ScriptBindDatabase | [Function Reference](classes/database) (completed)
DialogModule | wh::dialogmodule::C_ScriptBindDialog | [Function Reference](classes/dialog)
Dice | wh::playermodule::C_ScriptBind_Dice | [Function Reference](classes/dice) (completed)
EntityModule | wh::entitymodule::C_ScriptBindEntityModule | [Function Reference](classes/entitymodule)
EnvironmentModule | wh::environmentmodule::C_ScriptBindEnvironment | [Function Reference](classes/environmentmodule) (completed)
Framework | wh::framework::C_ScriptBindFramework | [Function Reference](classes/framework) (completed)
Game | wh::game::CScriptBindGame | [Function Reference](classes/game)
GameRules | wh::entitymodule::C_ScriptBindGameRules | [Function Reference](classes/gamerules)
Horse | wh::entitymodule::C_ScriptBindHorse | [Function Reference](classes/horse)
Human | wh::entitymodule::C_ScriptBindHuman | [Function Reference](classes/human)
InteractiveObject | wh::entitymodule::C_ScriptBindInteractiveObject | [Function Reference](classes/interactiveobject)
Inventory | wh::entitymodule::C_ScriptBindInventory | [Function Reference](classes/inventory)
ItemManager | wh::entitymodule::C_ScriptBindItemManager | [Function Reference](classes/itemmanager) (completed)
Minigame | wh::playermodule::C_ScriptBindMinigame | [Function Reference](classes/minigame) (completed)
PickableItem | wh::entitymodule::C_ScriptBindPickableItem | [Function Reference](classes/pickableitem)
Player | wh::entitymodule::C_ScriptBindPlayer | [Function Reference](classes/player)
QuestSystem | wh::questmodule::C_ScriptBindQuest | [Function Reference](classes/questsystem)
RPG | wh::rpgmodule::C_ScriptBindRPGModule | [Function Reference](classes/rpg) (completed)
Sharpening | wh::playermodule::C_ScriptBind_Sharpening | [Function Reference](classes/sharpening)
Shops | wh::shopmodule::C_ScriptBindShop | [Function Reference](classes/shops)
SmartObject | wh::xgenaimodule::C_ScriptBindSmartObject | [Function Reference](classes/smartobject)
Soul | wh::rpgmodule::C_ScriptBindSoul | [Function Reference](classes/soul)
Statistics | wh::rpgmodule::C_ScriptBindStatistics | [Function Reference](classes/statistics)
Trace | wh::framework::C_ScriptBindTrace | [Function Reference](classes/trace)
Tutorial | wh::playermodule::C_ScriptBindTutorial | [Function Reference](classes/tutorial)
UIMap | wh::guimodule::C_ScriptBindMap | [Function Reference](classes/uimap)
Variables | wh::framework::C_ScriptBindVariables | [Function Reference](classes/variables)
XGenAIModule | wh::xgenaimodule::C_ScriptBindXGenAIModule | [Function Reference](classes/xgenaimodule)

### Notes

* Return values of class methods are not fully tested and are largely the product of guess work.
* Class methods starting with the words "is," "has," or "have" are assumed to return a `boolean`. Most class methods are documented as returning `nil` when their return values cannot be determined from their name.
* In Lua, there is a single data structure, `table`, and eight data types: `nil`, `boolean`, `number`, `string`, `function`, `userdata`, `thread`, and `table`. See: [Lua 5.3 Reference Manual: Values and Types](https://www.lua.org/manual/5.3/manual.html#2.1)

## CryEngine

Lua Global Name | C++ Class | Function Reference
--- | --- | ---
Action | CScriptableBase::CScriptBind_Action | [Function Reference](classes/action)
ActionMapManager | CScriptableBase::CScriptBind_ActionMapManager | [Function Reference](classes/actionmapmanager)
ActorSystem | CScriptableBase::CScriptBind_ActorSystem | [Function Reference](classes/actorsystem)
AI | CScriptableBase::CScriptBind_AI | [Function Reference](classes/ai)
Boids | CScriptableBase::CScriptBind_Boids | [Function Reference](classes/boids)
DialogSystem | CScriptableBase::CScriptBind_DialogSystem | [Function Reference](classes/dialogsystem)
Entity | CScriptableBase::CScriptBind_Entity | [Function Reference](classes/entity)
Game | CScriptableBase::CScriptBind_Game | [Function Reference](classes/game)
GameAI | CScriptableBase::CScriptBind_GameAI | [Function Reference](classes/gameai)
GameAudio | CScriptableBase::CScriptBind_GameAudio | [Function Reference](classes/gameaudio)
GameRules | CScriptableBase::CScriptBind_GameRules | [Function Reference](classes/gamerules)
GameStatistics | CScriptableBase::CScriptBind_GameStatistics | [Function Reference](classes/gamestatistics)
GameToken | CScriptableBase::CScriptBind_GameToken | [Function Reference](classes/gametoken)
HitDeathReactions | CScriptableBase::CScriptBind_HitDeathReactions | [Function Reference](classes/hitdeathreactions)
HUD | CScriptableBase::CScriptBind_HUD | [Function Reference](classes/hud)
Inventory | CScriptableBase::CScriptBind_Inventory | [Function Reference](classes/inventory)
Item | CScriptableBase::CScriptBind_Item | [Function Reference](classes/item)
ItemSystem | CScriptableBase::CScriptBind_ItemSystem | [Function Reference](classes/itemsystem)
MaterialEffects | CScriptableBase::CScriptBind_MaterialEffects | [Function Reference](classes/materialeffects)
Particle | CScriptableBase::CScriptBind_Particle | [Function Reference](classes/particle)
Physics | CScriptableBase::CScriptBindPhysics | [Function Reference](classes/physics)
ProtectedBinds | CScriptableBase::CScriptBind_ProtectedBinds | [Function Reference](classes/protectedbinds)
Script | CScriptableBase::CScriptBind_Script | [Function Reference](classes/script)
Sound | CScriptableBase::CScriptBind_Sound | [Function Reference](classes/sound)
System | CScriptableBase::CScriptBind_System | [Function Reference](classes/system)
Turret | CScriptableBase::CScriptBind_Turret | [Function Reference](classes/turret)
UIAction | CScriptableBase::CScriptBind_UIAction | [Function Reference](classes/uiaction)
Vehicle | CScriptableBase::CScriptBind_Vehicle | [Function Reference](classes/vehicle)
VehicleSeat | CScriptableBase::CScriptBind_VehicleSeat | [Function Reference](classes/vehicleseat)
VehicleSystem | CScriptableBase::CScriptBind_VehicleSystem | [Function Reference](classes/vehiclesystem)
Weapon | CScriptableBase::CScriptBind_Weapon | [Function Reference](classes/weapon)

**Note:** The above implementations may differ from the [official CryEngine C++ API Documentation](http://docs.cryengine.com/display/CPPAPI/Home).