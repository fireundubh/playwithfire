<!-- TITLE: Buffs -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Buffs
## Table

### Common

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:BasicTimed | Effect applies for a duration in game time |  | Release
Cpp:Constant | Effect applies always |  | Release
Cpp:Fading | Effect applies for a duration in game time and dissipates |  | Release
Cpp:Instant | Effect applies once immediately |  | Release
Cpp:Void | Returns immediately |  | Release
Cpp:WorldTimeFading | Effect applies for a duration in world time and dissipates |  | Release
Cpp:WorldTimeTimed | Effect applies for a duration in world time |  | Release

### Location

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:CountrysideLocation | Effect applies when outside settlements |  | Release
Cpp:ForestLocation | Effect applies when in a forest |  | Release
Cpp:SettlementLocation | Effect applies when within a settlement |  | Release

### Mannequin

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:Alerted | Adds `Alerted` tag for animations |  | Release
Cpp:Curious | Adds `Curious` tag for animations |  | Release
Cpp:Drunk | Adds `Drunk` tag for animations |  | Release
Cpp:InjuredTag | Adds `Injured` tag for animations |  | Release
Cpp:Monk | Adds `Monk` mannequin tag for animations |  | Release
Cpp:Sick | Adds `Sick` tag for animations |  | Release
Cpp:StomachPain | Adds `Shitty` tag for animations |  | Release

### Context

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:CombatContextBuff | Effect applies when in combat |  | Release
Cpp:DialogSkillCheck | Effect applies when in dialog |  | Release
Cpp:DocumentItemBuff | Effect applies when trading `document` items |  | Release
Cpp:Educated | Effect applies when interacting with noblemen, monks, and circators |  | Release
Cpp:Haggle | Effect applies when haggling |  | Release
Cpp:HerbItemBuff | Effect applies when trading `herb` items |  | Release
Cpp:Highborn | Effect applies when interacting with highborn souls | HighbornWealthThreshold | Release
Cpp:Lowborn | Effect applies when interacting with lowborn souls | HighbornWealthThreshold | Release
Cpp:ManlyOdourWoman | Effect applies when interacting with women while Dirtiness greater than threshold | PerkManlyOdourDirtinessThreshold | Release
Cpp:ShieldAndArmorBuff | Effect applies when trading `armor`, `weapon`, and `shield` items |  | Release
Cpp:VersusAnimal | Effect applies when attacking wild animals |  | Release
Cpp:VersusCuman | Effect applies when attacking Cumans  |  | Release
Cpp:VersusDog | Effect applies when attacking dogs |  | Release
Cpp:VersusEnemy | Effect applies when attacking any enemy |  | Release
Cpp:VersusSoldier | Effect applies when attacking soldiers |  | Release
Cpp:VersusWoman | Effect applies when attacking women |  | Release
Cpp:VersusWomanDialogSkillCheck | Effect applies when interacting with women |  | Release

### Two State

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:DrunkChecking | Effect applies when drunk |  | Release
Cpp:DuringFader | Effect applies during fader | DuringFaderHysteresis (GameTime) | Release
Cpp:Infamous | Effect applies when reputation in location below threshold | LocalHeroInfamousReputationThreshold | Release
Cpp:LocalHero | Effect applies when reputation in location above threshold | LocalHeroInfamousReputationThreshold | Release
Cpp:ManlyOdourStealth | Effect applies when Dirtiness greater than threshold | PerkManlyOdourDirtinessThreshold | Release
Cpp:Night | Effect applies when the world time is night |  | Release
Cpp:PerkFlowerPower | Effect applies when herbs in inventory greater than or equal to parameter value | HerbsInInventoryForFlowerPowerPerk | Release
Cpp:PerkHorsenip | Effect applies when herbs in horse inventory greater than or equal to parameter value | HerbsInHorseInventoryForHorsenipPerk | Release
Cpp:Sadist | Effect applies when opponent bleeding |  | Release
Cpp:Still | Effect applies when motionless | StillBuffDuration (WorldTime) | Release
Cpp:StillAndHidden | Effect applies when motionless and undetected | StillAndHiddenHysteresis (GameTime) | Release
Cpp:Thunderstorm | Effect applies during rainy weather when rain intensity greater than threshold | ThunderstormBuffRainIntensity | Release
Cpp:Wanted | Effect applies when wanted in any location | PerkDaringDebonairWantedLevel | Release
Cpp:WithoutPlatingArmor | Effect applies when not wearing heavy armor |  | Release
Cpp:WithPlatingArmor | Effect applies when wearing heavy armor |  | Release

### Specialized

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:AdditionalAttackerCountFading | Effect applies when outnumbered in combat | AdditionalAttackerCountForMaxFadingBuff | Release
Cpp:AgilityWeaponBuff | Effect applies when Agility weapon requirement greater than Strength requirement |  | Release
Cpp:Berserk | Effect applies when Health below threshold | PerkBerserkHealthThreshold, PerkBerserkDuration (GameTime) | Release
Cpp:BloodRush | Effect applies when nearby enemy killed | PerkBloodRushDistance, PerkBloodRushDuration (GameTime) | Release
Cpp:ChainStrike | Effect applies and stacks when chaining strikes | PerkChainStrikeMaxChain | Release
Cpp:HealthFadingFromLimit | Effect magnitude derived from Health | HealthFadingFromLimitValue | Release
Cpp:HealthinessFading | Effect magnitude derived from Healthiness |  | Release
Cpp:Horseman | Effect applies for a duration in game time and/or while attacking dogs |  | Release
Cpp:KnightInAShiningArmor | Effect applies when wearing plate armor between dawn and dusk | MaxCloudAverageForShiningArmor | Release
Cpp:ProperDiet | Effect applies when eating well | PerkProperDietActivationTime | Release
Cpp:ReadingCartographer | Reveals all locations on map |  | Release
Cpp:Respec |  |  | Patch v1.3
Cpp:StrengthWeaponBuff | Effect applies when Strength weapon requirement greater than Agility requirement |  | Release
Cpp:TipplerPotion | Effect applies for a duration in world time and removes other buffs when applied |  | Release
Cpp:WeaponHealthIntensity | Effect magnitude derived from item durability |  | Release

### System

Per Moggabor, these buff implementations are not recommended for use in mods, so they are not detailed here.

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:AdditionalWeight | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Patch v1.3
Cpp:Bleeding | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:Caffeine | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:CarryingBody | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:CarryingBodyGravedigger | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:Drunkenness | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:Encumbered | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:EquippableItemWeighted | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:Exhausted | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:FoodHealth | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:FoodPoisoning | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:Hangover | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:Injured | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:ItemHealthChecking | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:ItemHealthMyItemChecking | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Patch v1.3
Cpp:JailRecovery | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:LastGasp | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:LowHealth | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:MoraleContext | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:Overeat | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:Overread | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:Oversleep | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:PotionHealth | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:ReadingQuality | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:RiddenHorse | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:SharpeningPressure | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:ShortTermFood | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:Sleep | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:SleepImproved | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:Starvation | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:TestRealSpeed | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:Unconscious | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Cpp:WellWorn | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release
Script:BasicBuff | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | Release

### Undocumented

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:BuffInstanceBase |  |  | Release
Cpp:ConstantContextChecking |  |  | Release
Cpp:ConsumablePoisoning |  |  | Release
Cpp:DeathProtection |  |  | Release
Cpp:LocalHeroInfamousSwitch |  |  | Release
Cpp:LocalReputationBuffBase |  |  | Release
Cpp:LocationMonitorBuffBase |  |  | Release
Cpp:SoulBuffInstance |  |  | Release
Cpp:TwoState |  |  | Release
Cpp:TwoStateLocationMonitorBuffBase |  |  | Release
Cpp:UniversalHealth |  |  | Release

## Credits

* Warhorse developer **Moggabor** for categories, descriptions, and *future* patch data
* Undocumented implementations were found via disassembly