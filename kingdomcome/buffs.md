<!-- TITLE: Buffs -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Buffs
## Table

### Common

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:BasicTimed | Effect applies for a duration in game time |  | 
Cpp:Constant | Effect applies always |  | 
Cpp:Fading | Effect applies for a duration in game time and dissipates |  | 
Cpp:Instant | Effect applies once immediately |  | 
Cpp:Void | Returns immediately |  | 
Cpp:WorldTimeFading | Effect applies for a duration in world time and dissipates |  | 
Cpp:WorldTimeTimed | Effect applies for a duration in world time |  | 

### Location

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:CountrysideLocation | Effect applies when outside settlements |  | 
Cpp:ForestLocation | Effect applies when in a forest |  | 
Cpp:SettlementLocation | Effect applies when within a settlement |  | 

### Mannequin

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:Alerted | Adds the `Alerted` mannequin tag for animations |  | 
Cpp:Curious | Adds the `Curious` tag for animations |  | 
Cpp:Drunk | Adds the `Drunk` tag for animations |  | 
Cpp:InjuredTag | Adds the `Injured` tag for animations |  | 
Cpp:Monk | Adds the `Monk` mannequin tag for animations |  | 
Cpp:Sick | Adds the `Sick` tag for animations |  | 
Cpp:StomachPain | Adds the `Shitty` tag for animations |  | 

### Context

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:CombatContextBuff | Effect applies when in combat |  | 
Cpp:DialogSkillCheck | Effect applies when in dialog |  | 
Cpp:DocumentItemBuff | Effect applies when trading `document` items |  | 
Cpp:Educated | Effect applies when interacting with noblemen, monks, and circators |  | 
Cpp:Haggle | Effect applies when haggling |  | 
Cpp:HerbItemBuff | Effect applies when trading `herb` items |  | 
Cpp:Highborn | Effect applies when interacting with highborn souls | HighbornWealthThreshold | 
Cpp:Lowborn | Effect applies when interacting with lowborn souls | HighbornWealthThreshold | 
Cpp:ManlyOdourWoman | Effect applies when interacting with women while Dirtiness greater than threshold | PerkManlyOdourDirtinessThreshold | 
Cpp:ShieldAndArmorBuff | Effect applies when trading `armor`, `weapon`, and `shield` items |  | 
Cpp:VersusAnimal | Effect applies when attacking wild animals |  | 
Cpp:VersusCuman | Effect applies when attacking Cumans  |  | 
Cpp:VersusDog | Effect applies when attacking dogs |  | 
Cpp:VersusEnemy | Effect applies when attacking any enemy |  | 
Cpp:VersusSoldier | Effect applies when attacking soldiers |  | 
Cpp:VersusWoman | Effect applies when attacking women |  | 
Cpp:VersusWomanDialogSkillCheck | Effect applies when interacting with women |  | 

### Two State

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:DrunkChecking | Effect applies when drunk |  | 
Cpp:DuringFader | Effect applies during fader | DuringFaderHysteresis (GameTime) | 
Cpp:Infamous | Effect applies when reputation in location below threshold | LocalHeroInfamousReputationThreshold | 
Cpp:LocalHero | Effect applies when reputation in location above threshold | LocalHeroInfamousReputationThreshold | 
Cpp:ManlyOdourStealth | Effect applies when Dirtiness greater than threshold | PerkManlyOdourDirtinessThreshold | 
Cpp:Night | Effect applies when the world time is night |  | 
Cpp:PerkFlowerPower | Effect applies when herbs in inventory greater than or equal to parameter value | HerbsInInventoryForFlowerPowerPerk | 
Cpp:PerkHorsenip | Effect applies when herbs in horse inventory greater than or equal to parameter value | HerbsInHorseInventoryForHorsenipPerk | 
Cpp:Sadist | Effect applies when opponent bleeding |  | 
Cpp:Still | Effect applies when motionless | StillBuffDuration (WorldTime) | 
Cpp:StillAndHidden | Effect applies when motionless and undetected | StillAndHiddenHysteresis (GameTime) | 
Cpp:Thunderstorm | Effect applies during rainy weather when rain intensity greater than threshold | ThunderstormBuffRainIntensity | 
Cpp:Wanted | Effect applies when wanted in any location | PerkDaringDebonairWantedLevel | 
Cpp:WithoutPlatingArmor | Effect applies when not wearing heavy armor |  | 
Cpp:WithPlatingArmor | Effect applies when wearing heavy armor |  | 

### Specialized

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:AdditionalAttackerCountFading | Effect applies when outnumbered in combat | AdditionalAttackerCountForMaxFadingBuff | 
Cpp:AgilityWeaponBuff | Effect applies when Agility weapon requirement greater than Strength requirement |  | 
Cpp:Berserk | Effect applies when Health below threshold | PerkBerserkHealthThreshold, PerkBerserkDuration (GameTime) | 
Cpp:BloodRush | Effect applies when nearby enemy killed | PerkBloodRushDistance, PerkBloodRushDuration (GameTime) | 
Cpp:ChainStrike | Effect applies and stacks when chaining strikes | PerkChainStrikeMaxChain | 
Cpp:HealthFadingFromLimit | Effect magnitude derived from Health | HealthFadingFromLimitValue | 
Cpp:HealthinessFading | Effect magnitude derived from Healthiness |  | 
Cpp:Horseman | Effect applies for a duration in game time and/or while attacking dogs |  | 
Cpp:KnightInAShiningArmor | Effect applies when wearing plate armor between dawn and dusk | MaxCloudAverageForShiningArmor | 
Cpp:ProperDiet | Effect applies when eating well | PerkProperDietActivationTime | 
Cpp:ReadingCartographer | Reveals all locations on map |  | 
Cpp:Respec |  |  | 1.3
Cpp:StrengthWeaponBuff | Effect applies when Strength weapon requirement greater than Agility requirement |  | 
Cpp:TipplerPotion | Effect applies for a duration in world time and removes other buffs when applied |  | 
Cpp:WeaponHealthIntensity | Effect magnitude derived from item durability |  | 

### System

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:AdditionalWeight | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 1.3
Cpp:Bleeding | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:Caffeine | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:CarryingBody | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:CarryingBodyGravedigger | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:Drunkenness | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:Encumbered | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:EquippableItemWeighted | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:Exhausted | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:FoodHealth | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:FoodPoisoning | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:Hangover | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:Injured | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:ItemHealthChecking | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:ItemHealthMyItemChecking | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 1.3
Cpp:JailRecovery | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:LastGasp | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:LowHealth | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:MoraleContext | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:Overeat | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:Overread | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:Oversleep | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:PotionHealth | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:ReadingQuality | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:RiddenHorse | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:SharpeningPressure | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:ShortTermFood | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:Sleep | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:SleepImproved | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:Starvation | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:TestRealSpeed | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:Unconscious | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Cpp:WellWorn | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 
Script:BasicBuff | Not recommended for use in mods. See [Nexus Wiki](https://wiki.nexusmods.com/index.php/Buffs_in_KCD) for details. |  | 

### Undocumented

Implementation | Description | Governing RPG Parameters | Version Added
--- | --- | --- | ---
Cpp:BuffInstanceBase |  |  | 
Cpp:ConstantContextChecking |  |  | 
Cpp:ConsumablePoisoning |  |  | 
Cpp:DeathProtection |  |  | 
Cpp:LocalHeroInfamousSwitch |  |  | 
Cpp:LocalReputationBuffBase |  |  | 
Cpp:LocationMonitorBuffBase |  |  | 
Cpp:SoulBuffInstance |  |  | 
Cpp:TwoState |  |  | 
Cpp:TwoStateLocationMonitorBuffBase |  |  | 
Cpp:UniversalHealth |  |  | 

## Credits

**Moggabor** for categories, descriptions, and *future* patch data (probably a developer)