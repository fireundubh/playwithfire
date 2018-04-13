<!-- TITLE: RPG Parameters -->

[&larr; Kingdom Come](/kingdomcome)

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# RPG Parameters
**Data Quality Note:** The following descriptions were dumped directly from the game. The parameter names are correct, but the descriptions contain typos and misspellings. They will be cleaned up later.

## Legend

* <font color="green">Green</font>: The parameter value was increased.
* <font color="red">Red</font>: The parameter value was decreased.
* <font color="blue">Blue</font>: The parameter was added.
* <strike>Strikethrough</strike>: The parameter was removed, or the value is empty and nonzero.

## Table: Changes at a Glance

Parameter | v1.1&ndash;1.2.5 | v1.3&ndash;1.3.4 | v1.4&ndash;1.4.2 | Description
:--- | ---: | ---: | ---: | :---
AlchemyXPPerAutocookBrewingRelative | nil | <font color="blue">0.100000000</font> | 0.100000000 | how many XP you get when you auto-cook a potion, relative to manual brewing
BlindViewRadiusFakeRelative | nil | <font color="blue">0.800000000</font> | 0.800000000 | for blinded (mostly sleeping) NPC we have to calculate stealth XP somehow, so we calculate this fake radius
<strike>CharismaMulOnExtremeExhaustionInterpolation</strike> | nil | nil | nil | Possibly the original name of the `CharismaMulOnExtremeExhaustion` parameter
ControllerLockPickingAppropriateTolerance | nil | <font color="blue">0.060000000</font> | <font color="red">0.045000000</font> | the lock is considered too hard to pick, if the tolerance is smaller than this
ControllerLockPickingToleranceACoef | nil | <font color="blue">0.450000000</font> | 0.450000000 | 
ControllerLockPickingToleranceKCoef | nil | <font color="blue">0.030000000</font> | <font color="green">0.070000000</font> | 
ControllerLockPickingToleranceMCoef | nil | <font color="blue">0.687000000</font> | 0.687000000 | 
ControllerLockPickingToleranceNCoef | nil | <font color="blue">0.355000000</font> | <font color="green">0.480000000</font> | 
DamageToArmorStatus | nil | <font color="blue">1.000000000 | 1.000000000 | for the stopping layer
DamageToArmorStatusHigherLayers | nil | <font color="blue">2.000000000</font> | 2.000000000 | for layers above the stopping layer
DamageToArmorStatusLowerLayers | nil | <font color="blue">0.500000000</font> | 0.500000000 | for layers below the stopping layer
<strike>ImprovedSleepMultiplierSurvival</strike> | nil | nil | nil | Possibly the original name of the `ImprovedSleepMultiplier` parameter
<strike>InactiveTimeToDestroyOversleepCreated</strike> | nil | nil | nil | Possibly the original name of the `InactiveTimeToDestroyOversleep` parameter
LockPickingAdequateTolerance | nil | nil | <font color="blue">0.170000000</font> | locks on a similar level as the player have adequate tolerance
MaxStatToAttackMult | 1.200000000 | <font color="red">1.100000000</font> | 1.100000000 | Maximal relative attack multiplier (for a high stat)
MaxStealthHitSoundMultiplier | 0.400000000 | <font color="red">0.220000000</font> | 0.220000000 | intensity multiplier for max stealth level
MinStealthHitSoundMultiplier | 0.100000000 | <font color="red">0.060000000</font> | 0.060000000 | Intensity multiplier for minimum Stealth level
PickpocketingDistance | nil | <font color="blue">2.000000000</font> | 2.000000000 | Max pickpocketing range (not starting interactor range)
PickpocketingIndicatorSharpness | 0.200000000 | <font color="red">0.000000000</font> | 0.000000000 | 0 - precise slow change<br>1 - sharp change
PickpocketingMisstargetingTolerance | nil | <font color="blue">2000.000000000</font> | 2000.000000000 | Time tolerance for temporarily mistargeting your victim
PickpocketingRandomChanceRollMinCap | nil | <font color="blue">0.100000000</font> | 0.100000000 | Worst random rolls will always be capped to this minimum chance
QuestMoneyRewardScaleConstant | 1.250000000 | <font color="red">1.200000000</font> | 1.200000000 | scale constnat for quest reward item amount
<strike>ReadingRestEffectiveness</strike> | 0.300000000 | nil | nil | If this value is 0.3, reading will regen player as sleeping on bed with comfort 30%.
<strike>ReadingRestUpperLimit</strike> | 1.000000000 | nil | nil | When sleeping, the rest can not exceed bed quality. When reading, the threshold is given by this value.
SkillToDmgConstA | 70.000000000 | <font color="green">250.000000000</font> | 250.000000000 | 
StarvationHealthLossSpeed | 0.000578704 | <font color="green">0.001000000</font> | 0.001000000 | by design the same speed as the digestion
StarvationPlayerEffectMaxMax | 60.000000000 | 60.000000000 | <font color="green">75.000000000</font> | longest interval between effects for high hunger stat
StarvationPlayerEffectMaxMin | 90.000000000 | 90.000000000 | <font color="green">120.000000000</font> | longest interval between effects for low hunger stat
StarvationPlayerEffectMinMax | 30.000000000 | 30.000000000 | <font color="green">45.000000000</font> | shortest interval between effects for high hunger stat
StarvationPlayerEffectMinMin | 60.000000000 | 60.000000000 | <font color="green">90.000000000</font> | shortest interval between effects for low hunger stat
UnarmedHitArmorDamageCoef | nil | <font color="blue">0.250000000</font> | 0.250000000 | relative to armed combat


## Table: All Parameters

Parameter | v1.1&ndash;1.2.5 | v1.3&ndash;1.3.4 | v1.4&ndash;1.4.2 | Description
:--- | ---: | ---: | ---: | :---
AdditionalAttackerCountForMaxFadingBuff | 2.000000000 | 2.000000000 | 2.000000000 | For AdditionalAttackerCountFading buff
AgiDiffToAttackSpeed | 0.200000000 | 0.200000000 | 0.200000000 | Relative attack speed gain for one Agility level difference
AgilityXPLevelBase | 20.000000000 | 20.000000000 | 20.000000000 | 
AgilityXPLevelDiff | 30.000000000 | 30.000000000 | 30.000000000 | 
AimCiriticalLimitTime | 0.750000000 | 0.750000000 | 0.750000000 | Time limit after AI is notified about low Stamina when aiming
AimPainlessDelay | 2.000000000 | 2.000000000 | 2.000000000 | Aiming without Stamina loss
AimSkillToZoom | 1.500000000 | 1.500000000 | 1.500000000 | Zoom increase by each skill level above the base
AimSpreadMax | 15.000000000 | 15.000000000 | 15.000000000 | Aiming spread due to low Stamina and skill. Max angle. Used right before all Stamina is lost.
AimSpreadMinRatio | 0.300000000 | 0.300000000 | 0.300000000 | Aiming spread minimum, relative to max. This value is used after entering the painless zone.
AimSpreadSkillDecrease | 0.050000000 | 0.050000000 | 0.050000000 | Relative decrease of maximum aim spread for each skill level
AimStamCost | 20.000000000 | 20.000000000 | 20.000000000 | Stamina loss after after painless delay
AimZoomBase | 10.000000000 | 10.000000000 | 10.000000000 | aim zoom (=fov decrease) after reaching some skill level
AimZoomBaseSkill | 10.000000000 | 10.000000000 | 10.000000000 | Minimal skill level required to benefit from the zoom effect
AimZoomMax | 25.000000000 | 25.000000000 | 25.000000000 | maximal aim zoom (=fov decrease)
AlchemyRecipeStepsTolerance | 2.000000000 | 2.000000000 | 2.000000000 | How many recipe steps might fail in order to successfully brew the recipe
AlchemyToleranceBase | 0.500000000 | 0.500000000 | 0.500000000 | Base brewing tolerance at level 1
AlchemyTolerancePerLevel | 0.150000000 | 0.150000000 | 0.150000000 | Brewing tolerance gain per level
AlchemyTrialEndErrorPerkTolerance | 1.000000000 | 1.000000000 | 1.000000000 | Additional tolerance gained with Trial and Error perk
AlchemyXPPerAutocookBrewingRelative | nil | <font color="blue">0.100000000</font> | 0.100000000 | how many XP you get when you auto-cook a potion, relative to manual brewing
AlchemyXPPerSuccessfullBrewing | 40.000000000 | 40.000000000 | 40.000000000 | Alchemy XP gained when a potion is successfully brewed
AlcoholBaseHangoverDuration | 14400.000000000 | 14400.000000000 | 14400.000000000 | Base max duration for hangover (after blackout) in world time
AlcoholBlackoutDuration | 14400.000000000 | 14400.000000000 | 14400.000000000 | Blackout unconscious duration
AlcoholContentFPAntidoteThreshold | 60.000000000 | 60.000000000 | 60.000000000 | Food with alcohol content above this threshold counters food poisoning
AlcoholDigestSpeedModfifOnEmptyStomache | 2.000000000 | 2.000000000 | 2.000000000 | Alcohol digest speed multiplier on empty stomache
AlcoholDigestSpeedModfifOnFullStomache | 0.500000000 | 0.500000000 | 0.500000000 | Alcohol digest speed multiplieron full stomache
AlcoholDrunkMaxExhaustNegativeEffect | 0.005000000 | 0.005000000 | 0.005000000 | Max negative exhaustion effect while drunk
AlcoholDrunkThreshold | 0.500000000 | 0.500000000 | 0.500000000 | Threshold for Drunkenness mood from max alcohol poisoning
AlcoholHangoverOffsetModif | 1.100000000 | 1.100000000 | 1.100000000 | Starting hangover negative effects are modified by this offset
AlcoholismDuration | 500000.000000000 | 500000.000000000 | 500000.000000000 | Alcoholism duration in world time
AlcoholismMaxSkillLevelThreshold | 1000.000000000 | 1000.000000000 | 1000.000000000 | Temporary alcoholism threshold with max drinking skill
AlcoholismRemoveSpeed | 0.001000000 | 0.001000000 | 0.001000000 | Alcoholism removed per world time second (default: 100 every 4 days)
AlcoholismThreshold | 700.000000000 | 700.000000000 | 700.000000000 | Amount of alcohol that will cause temporary alcoholism
AlcoholismTickInterval | 1.000000000 | 1.000000000 | 1.000000000 | Alcoholism timer expiry
AlcoholMaxAGIEffect | 2.000000000 | 2.000000000 | 2.000000000 | Max negative/positive stat effect
AlcoholMaxCHAEffect | 2.000000000 | 2.000000000 | 2.000000000 | Max negative/positive stat effect
AlcoholMaxCONEffect | 3.000000000 | 3.000000000 | 3.000000000 | Max negative/positive stat effect
AlcoholMaxDrinkingSkillHangoverDurationModifier | 0.333333000 | 0.333333000 | 0.333333000 | Hangover duration modifier for max Drinking skill
AlcoholMaxSPCEffect | 2.000000000 | 2.000000000 | 2.000000000 | Max negative/positive stat effect
AlcoholMaxSTREffect | 2.000000000 | 2.000000000 | 2.000000000 | Max negative/positive stat effect
AlcoholMaxVITEffect | 2.000000000 | 2.000000000 | 2.000000000 | Max negative/positive stat effect
AlcoholMoodMaxExhaustPossitiveEffect | 0.000200000 | 0.000200000 | 0.000200000 | max positive exhaust effect while in mood
AlcoholMoodThreshold | 0.010000000 | 0.010000000 | 0.010000000 | threshold for alcohol mood from max alcohol poisoning
AlcoholPerkBacchusHangoverEffectMod | 1.300000000 | 1.300000000 | 1.300000000 | hangover effects mod
AlcoholPerkCorrectResistanceModif | 0.500000000 | 0.500000000 | 0.500000000 | alcohol content modif for correct resistance
AlcoholPerkDrunkHangoverDurationMod | 2.000000000 | 2.000000000 | 2.000000000 | 
AlcoholPerkDrunkMoodRangeMod | 2.000000000 | 2.000000000 | 2.000000000 | mood range is expanded by this mod
AlcoholPerkLooseTongueSpcChaModif | 1.500000000 | 1.500000000 | 1.500000000 | speech and charisma modif bonus/malus for loose tongue perk
AlcoholPerkTrueSlavHangoverDurationMod | 0.500000000 | 0.500000000 | 0.500000000 | hangover duration mod
AlcoholPerkTrueSlavMaxAlcoholMod | 0.500000000 | 0.500000000 | 0.500000000 | max amount of alcohol is divided by this mod
AlcoholPerkWrongResistanceModif | 2.000000000 | 2.000000000 | 2.000000000 | alcohol content modif for wrong resistance
ArmorDefenseToAttackingWeaponStatus | 0.020000000 | 0.020000000 | 0.020000000 | how opponent's defense value damages my weapon - hit to armor
ArmorDirtToCharismaCoef | 1.000000000 | 1.000000000 | 1.000000000 | 
ArmorLoadDiffToMax | 10.000000000 | 10.000000000 | 10.000000000 | 
ArmorLoadToJumpCost | 2.000000000 | 2.000000000 | 2.000000000 | how armor load coefficient affects the stamina jump cost (times base)
ArmorLoadToRun | 0.500000000 | 0.500000000 | 0.500000000 | how armor load coefficient affects running speed
ArmorLoadToSprint | 1.000000000 | 1.000000000 | 1.000000000 | how armor load coefficient affects sprint
ArmorStatusToCharismaCoef | 0.670000000 | 0.670000000 | 0.670000000 | 
ArmorStatusToDefenseCoef | 0.670000000 | 0.670000000 | 0.670000000 | health to armor defense multiplicative coef
AthleticXPAwardDistance | 500.000000000 | 500.000000000 | 500.000000000 | award xp for travelling some distance
AttackEnergyModifier | 2.000000000 | 2.000000000 | 2.000000000 | utoku
AttackRequiredStamRatio | 0.000000000 | 0.000000000 | 0.000000000 | actual/cost stamina ratio must be > than this value for attack to be allowed
AttackSpeedNormal | 0.500000000 | 0.500000000 | 0.500000000 | normal attack speed, 0-min, 1-max
AttackSpeedNormalAgi | 5.000000000 | 5.000000000 | 5.000000000 | agility required for the normal attack speed
AttackSpeedPlayerRelative | 1.000000000 | 1.000000000 | 1.000000000 | 0 - using opponent's skill<br>1 - attack speed is always calculated using the player
AttackStamModMin | 0.500000000 | 0.500000000 | 0.500000000 | attack strength/power stamina modifier minimum (0stam->Xattack)
AttSkillToHorsePullDown | 0.500000000 | 0.500000000 | 0.500000000 | relative attacker skill to horse pull down
AttStrengthToHorsePullDown | 0.500000000 | 0.500000000 | 0.500000000 | relative attacker stat to horse pull down
AverageArmorDefenseWeight | 0.500000000 | 0.500000000 | 0.500000000 | 0 = only body part defense, 1 = only average defense
AvidReaderReadingSpeed | 0.350000000 | 0.350000000 | 0.350000000 | AvidReader soul ability advances reading progress on one book in inventory during sleep or skiptime. This constant determines speed of reading (reading spot is always None).
BadassnessDiffToSkillCheckResult | 2.000000000 | 2.000000000 | 2.000000000 | 
BarterAngrynessCoefWeightA | 1.000000000 | 1.000000000 | 1.000000000 | 
BarterAngrynessCoefWeightB | 0.700000000 | 0.700000000 | 0.700000000 | 
BarterCoefWeightA | 0.875000000 | 0.875000000 | 0.875000000 | shopkeeper shop barter calculation 'a' coef
BarterCoefWeightB | 80.000000000 | 80.000000000 | 80.000000000 | shopkeeper shop barter calculation 'b' coef
BarterDominanceChaBaseE | 5.000000000 | 5.000000000 | 5.000000000 | barter dominance calculation 'e' coef
BarterDominanceChaWeightC | 0.100000000 | 0.100000000 | 0.100000000 | barter dominance calculation 'c' coef
BarterDominanceRelationshipWeightB | 1.000000000 | 1.000000000 | 1.000000000 | barter dominance calculation 'b' coef
BarterDominanceSpcWeightA | 3.000000000 | 3.000000000 | 3.000000000 | barter dominance calculation 'a' coef
BarterDominanceSpcWeightD | 10.000000000 | 10.000000000 | 10.000000000 | barter dominance calculation 'd' coef
BarterPriceSellRepBuying | 1.500000000 | 1.500000000 | 1.500000000 | price sell vs buy mod
BarterPriceSellRepCoef | 1.500000000 | 1.500000000 | 1.500000000 | sell reputation coef
BarterPriceSellRepMultip | -0.500000000 | -0.500000000 | -0.500000000 | sell reputation multiplier
BaseAttackStaminaCost | 12.000000000 | 12.000000000 | 12.000000000 | how much stamina will attack cost
BaseInventoryCapacity | 66.000000000 | 66.000000000 | 66.000000000 | base inventory capacity
BaseItemDisappearingTime | 3600.000000000 | 3600.000000000 | 3600.000000000 | base game time for dropped items to auto disappear
BasketSuspiciencyNoDealThreashold | 10000000.000000000 | 10000000.000000000 | 10000000.000000000 | Haggle reaction 2 threshold (transaction refused)
BasketSuspiciencyThreashold | 0.100000000 | 0.100000000 | 0.100000000 | Haggle reaction 1 threshold (haggle more difficult)
BestVisVolume | 10000.000000000 | 10000.000000000 | 10000.000000000 | object volume for maximum recognition bonus
BigZoneDistanceSlotMod | 0.800000000 | 0.800000000 | 0.800000000 | temporary solution, slot mod for distance > 1
BlindViewRadiusFakeRelative | nil | <font color="blue">0.800000000</font> | 0.800000000 | for blinded (mostly sleeping) NPC we have to calculate stealth XP somehow, so we calculate this fake radius
BowChargeDurationMax | 3.000000000 | 3.000000000 | 3.000000000 | maximum duration of bow charge animation
BowChargeDurationMin | 1.350000000 | 1.350000000 | 1.350000000 | minimum duration of bow charge animation
BowPowerToChargeDuration | 0.100000000 | 0.100000000 | 0.100000000 | nominal charge duration for bow with power = 1
BundleAlchemistPerkAdd | 1.000000000 | 1.000000000 | 1.000000000 | Addition of potions created with Bundle Alchemist perk
CaffeineFromFoodCoef | 2.000000000 | 2.000000000 | 2.000000000 | how much caffeine is added from a unit refresh
CaffeineFullThreshold | 0.900000000 | 0.900000000 | 0.900000000 | you cannot use more refreshing items if above this value
CarriedBodyMaxStamConsumption | 10.000000000 | 10.000000000 | 10.000000000 | uses encumberance to interpolate from 0 to this
CarriedBodyWeightCoef | 0.250000000 | 0.250000000 | 0.250000000 | how much of the carried body weight is added to the carried weight of the carrier
CarriedCarriedWeightCoef | 0.500000000 | 0.500000000 | 0.500000000 | how much of the carried weight of the carried NPC is added to the carried weight of the carrier
CharismaDiffToSkillCheckResult | 0.300000000 | 0.300000000 | 0.300000000 | > 0; scaled charisma diff for result = -1/1
CharismaMulOnExtremeExhaustion | 0.750000000 | 0.750000000 | 0.750000000 | Player will have this charisma multiplied by this value when he has exhaust equal to 0. Charisma will not be changed when exhaust is 50. Linear interpolation on multiplier is applied when exhaust is between 0 and 50;
<strike>CharismaMulOnExtremeExhaustionInterpolation</strike> | nil | nil | nil | Possibly the original name of the `CharismaMulOnExtremeExhaustion` parameter
ClassCourageMoraleWeight | 0.000000000 | 0.000000000 | 0.000000000 | Weight of soul class courage affecting morale
ClothDirtyingUpdatePeriod | 50.000000000 | 50.000000000 | 50.000000000 | how often (in meters walked) do we add dirt to clothing (both for player and NPCs)
CollisionVelocityDeltaToDmgR | 0.250000000 | 0.250000000 | 0.250000000 | 
CombatAutoAggressionDiffScale | 2.000000000 | 2.000000000 | 2.000000000 | the bigger number the bigger difference in aggresion for skill differnce
CombatAutoAttackDelayIncreasePerAttacker | 0.800000000 | 0.800000000 | 0.800000000 | how many times is the period increased for each attacker
CombatAutoAttackDelayIncreasePerAttackerHorse | 0.100000000 | 0.100000000 | 0.100000000 | CombatAutoAttackDelayIncreasePerAttacker if the victim is on horse
CombatAutoAttackDelayIncreasePerAttackerMissile | 0.200000000 | 0.200000000 | 0.200000000 | CombatAutoAttackDelayIncreasePerAttacker if the victim has a missile wpn
CombatAutoAttackDelaySigma | 4.000000000 | 4.000000000 | 4.000000000 | attack delay variation
CombatAutoClinchReactionDelayMaxMax | 1.000000000 | 1.000000000 | 1.000000000 | maximal maximum
CombatAutoClinchReactionDelayMaxMin | 0.500000000 | 0.500000000 | 0.500000000 | maximal minimum
CombatAutoClinchReactionDelayMinMax | -0.500000000 | -0.500000000 | -0.500000000 | minimal maximum
CombatAutoClinchReactionDelayMinMin | -1.000000000 | -1.000000000 | -1.000000000 | minimal minimum
CombatAutoComboStepsSigma | 1.500000000 | 1.500000000 | 1.500000000 | standard deviation of performed combo steps
CombatAutoDodgeWeight | 1.100000000 | 1.100000000 | 1.100000000 | 
CombatAutoEasyZoneWeight | 0.800000000 | 0.800000000 | 0.800000000 | [0-1] how much are easy zones favored by the lame AI (1 = favored)
CombatAutoForcedComboStaminaLimit | 0.700000000 | 0.700000000 | 0.700000000 | stamina threshold
CombatAutoForcedPeriodicalAttackStaminaLimit | 0.200000000 | 0.200000000 | 0.200000000 | stamina threshold
CombatAutoGuardHysteresis | 1.500000000 | 1.500000000 | 1.500000000 | 
CombatAutoLameGuardOffset | 3.000000000 | 3.000000000 | 3.000000000 | offset to max distance
CombatAutoMasterComboSteps | 5.000000000 | 5.000000000 | 5.000000000 | combo steps a skilled npc will typically perform
CombatAutoMasterGuardOffset | 1.000000000 | 1.000000000 | 1.000000000 | offset to max distance
CombatAutoMaxAimDuration | 3.000000000 | 3.000000000 | 3.000000000 | the longest aim time for the lowest skill
CombatAutoMaxAimDurationRandomAdd | 1.000000000 | 1.000000000 | 1.000000000 | max random time added to the aim duration
CombatAutoMaxAtkDistOffset | 0.100000000 | 0.100000000 | 0.100000000 | offset from max attack distance defined in percentage from attack range
CombatAutoMaxAttackDelay | 6.000000000 | 6.000000000 | 6.000000000 | mean delay between attacks for a defensive AI
CombatAutoMaxHuntAttackDuration | 60.000000000 | 60.000000000 | 60.000000000 | maximal time the NPC is hunting/chasing
CombatAutoMinAtkDistOffset | 0.000000000 | 0.000000000 | 0.000000000 | offset from min attack distance defined in percentage from attack range
CombatAutoMinDefenseModeWeight | 0.400000000 | 0.400000000 | 0.400000000 | [0-1] the lowest weight for the defense mode
CombatAutoMinHuntAttackDuration | 15.000000000 | 15.000000000 | 15.000000000 | minimal time the NPC is hunting/chasing
CombatAutoMoveActivityDecreasePerAttacker | 0.500000000 | 0.500000000 | 0.500000000 | my activity decrease per opponents aditinal attackers
CombatAutoNaturalComboRatio | 0.500000000 | 0.500000000 | 0.500000000 | [0-1] ratio of natural combos
CombatAutoNoDefenseWeight | 0.400000000 | 0.400000000 | 0.400000000 | 
CombatAutoNormalBWeight | 2.800000000 | 2.800000000 | 2.800000000 | 
CombatAutoOppZoneAdaptDelayMaxMax | 2.000000000 | 2.000000000 | 2.000000000 | reaction delay maximal maximum
CombatAutoOppZoneAdaptDelayMaxMin | 1.000000000 | 1.000000000 | 1.000000000 | reaction delay maximal minimum
CombatAutoOppZoneAdaptDelayMinMax | 0.200000000 | 0.200000000 | 0.200000000 | reaction delay minimal maximum
CombatAutoOppZoneAdaptDelayMinMin | 0.000000000 | 0.000000000 | 0.000000000 | reaction delay minimal minimum
CombatAutoPBWeight | 2.500000000 | 2.500000000 | 2.500000000 | 
CombatAutoReactionDelayRangeSpread | 0.300000000 | 0.300000000 | 0.300000000 | [0-1] higher nunber -> changes state less often
CombatAutoReactivePreblockMaxDelay | 0.800000000 | 0.800000000 | 0.800000000 | 
CombatAutoReactivePreblockMinDelay | 0.300000000 | 0.300000000 | 0.300000000 | 
CombatAutoRiposteAggressionWeight | 0.500000000 | 0.500000000 | 0.500000000 | 
CombatAutoScaleDefensivenessDelayRel | 2.000000000 | 2.000000000 | 2.000000000 | relative to attack delay, time to override defensiveness and go near
CombatAutoSPBWeight | 1.500000000 | 1.500000000 | 1.500000000 | 
CombatAutoStaticPreblockMaxTime | 15.000000000 | 15.000000000 | 15.000000000 | 
CombatAutoStaticPreblockRandBias | 0.800000000 | 0.800000000 | 0.800000000 | 
CombatAutoTrickAttackProb | 0.800000000 | 0.800000000 | 0.800000000 | [0-1] attack prob for the first step
CombatAutoTrickDelayVariability | 0.300000000 | 0.300000000 | 0.300000000 | added to the lower bound
CombatAutoTrickInvalidBlockAttackMaxProb | 0.500000000 | 0.500000000 | 0.500000000 | [0-1] max trick prob for a skilled AI if the block is invalid
CombatAutoTrickMaxProb | 0.500000000 | 0.500000000 | 0.500000000 | [0-1] max trick prob for the first step
CombatAutoTrickMinMaxDelay | 0.800000000 | 0.800000000 | 0.800000000 | lower bound of the max delay
CombatAutoTrickNoAttackProb | 0.100000000 | 0.100000000 | 0.100000000 | [0-1] no attack prob for the first step
CombatAutoTrickReactionMaxDelay | 8.000000000 | 8.000000000 | 8.000000000 | 
CombatAutoTrickReactionMinDelay | 0.100000000 | 0.100000000 | 0.100000000 | 
CombatAutoTrickReactionSkillWeight | 4.000000000 | 4.000000000 | 4.000000000 | 
CombatAutoTrickReactionStaWeight | 1.000000000 | 1.000000000 | 1.000000000 | 0 - use just stamina<br>1 - use just aggression
CombatAutoUnarmedBlockProb | 1.600000000 | 1.600000000 | 1.600000000 | 
CombatAutoWpnHealthBlockMax | 20.000000000 | 20.000000000 | 20.000000000 | 
CombatAutoWpnHealthMinBlockProb | 0.800000000 | 0.800000000 | 0.800000000 | 
CombatAutoZoneChangeDelayMaxMax | 10.000000000 | 10.000000000 | 10.000000000 | zone change timeout maximal maximum
CombatAutoZoneChangeDelayMaxMin | 5.000000000 | 5.000000000 | 5.000000000 | zone change timeout maximal minimum
CombatAutoZoneChangeDelayMinMax | 6.000000000 | 6.000000000 | 6.000000000 | zone change timeout minimal maximum
CombatAutoZoneChangeDelayMinMin | 2.000000000 | 2.000000000 | 2.000000000 | zone change timeout minimal minimum
CombatDangerCooldown | 3.000000000 | 3.000000000 | 3.000000000 | how long is the combat danger active after last enemy stops to be a threat
CombatDmgRBonusFromBehind | 1.200000000 | 1.200000000 | 1.200000000 | multiplicative DmgR bohus for attacks from behind
CombatHitImmortalUnconsciousDepth | 120.000000000 | 120.000000000 | 120.000000000 | depth for immortal knock-out
CombatHitUnconsciousDepth | 60.000000000 | 60.000000000 | 60.000000000 | depth after a combat hit
CombatMoveApproachHysteresis | 1.500000000 | 1.500000000 | 1.500000000 | 
CombatMoveApproachSprintMinStamina | 1.000000000 | 1.000000000 | 1.000000000 | do not allow sprint during the approach
ControllerLockPickingAppropriateTolerance | nil | <font color="blue">0.060000000</font> | <font color="red">0.045000000</font> | the lock is considered too hard to pick, if the tolerance is smaller than this
ControllerLockPickingToleranceACoef | nil | <font color="blue">0.450000000</font> | 0.450000000 | 
ControllerLockPickingToleranceKCoef | nil | <font color="blue">0.030000000</font> | <font color="green">0.070000000</font> | 
ControllerLockPickingToleranceMCoef | nil | <font color="blue">0.687000000</font> | 0.687000000 | 
ControllerLockPickingToleranceNCoef | nil | <font color="blue">0.355000000</font> | <font color="green">0.480000000</font> | 
CorpseDisappearanceTimeDiscovered | 5.000000000 | 5.000000000 | 5.000000000 | time before a NPC corpse is hidden when discovered
CorpseDisappearanceTimeUndiscovered | 25.000000000 | 25.000000000 | 25.000000000 | time before a NPC corpse is hidden when undiscovered
CorpseDisapperanceMinDistanceFromPlayer | 100.000000000 | 100.000000000 | 100.000000000 | distance from player below which a corpse will never disappear
DamageToArmorStatus | nil | <font color="blue">1.000000000 | 1.000000000 | for the stopping layer
DamageToArmorStatusHigherLayers | nil | <font color="blue">2.000000000</font> | 2.000000000 | for layers above the stopping layer
DamageToArmorStatusLowerLayers | nil | <font color="blue">0.500000000</font> | 0.500000000 | for layers below the stopping layer
DawnTime | 4.500000000 | 4.500000000 | 4.500000000 | Time when night ends, used by rpg (default 04:30)
DefaultReadingQuality | 0.500000000 | 0.500000000 | 0.500000000 | Reading quality when doing nothing special (standing).
DefaultRelationship | 0.500000000 | 0.500000000 | 0.500000000 | default value for the alied forces
DefaultStateDeltaSpeed | 1.000000000 | 1.000000000 | 1.000000000 | any soul state regen / losing speed
DefaultVisVolume | 0.030000000 | 0.030000000 | 0.030000000 | default item size-volume that have no visibility recognition penalty
DefaultWorldTimeRatio | 15.000000000 | 15.000000000 | 15.000000000 | default world time ratio useed to calculate game time ration in superspeed skiptime
DigestionSpeed | 0.000578704 | 0.000578704 | 0.000578704 | amount of food 'lost' per world-time second (global base value)
DistanceCheckInterval | 1.000000000 | 1.000000000 | 1.000000000 | check distance travelled for statistics
DmgRToHealthCoefA | 3.000000000 | 3.000000000 | 3.000000000 | 
DmgRToHealthCoefB | 1.600000000 | 1.600000000 | 1.600000000 | 
DuringFaderHysteresis | 1.000000000 | 1.000000000 | 1.000000000 | the in-fader state is kept for how longer
DuskTime | 21.500000000 | 21.500000000 | 21.500000000 | Time when night begins, used by rpg (default 21:30)
EncumberanceForSecondaryModifiers | 0.500000000 | 0.500000000 | 0.500000000 | when the buff will activate the secondary group
EncumberedToSpeedSurfaceCoef | 0.300000000 | 0.300000000 | 0.300000000 | Coef that controls terrain/surface influence in encumbered speed mod
EquippedWeightSubWithWellWornPerk | 0.333333000 | 0.333333000 | 0.333333000 | when player has Well Worn perk, weight of items is lowered when they are equipped
ExhaustedPlayerEffectMaxMax | 60.000000000 | 60.000000000 | 60.000000000 | the longest interval between effects for high exhaust stat
ExhaustedPlayerEffectMaxMin | 30.000000000 | 30.000000000 | 30.000000000 | the longest interval between effects for low exhaust stat
ExhaustedPlayerEffectMinMax | 30.000000000 | 30.000000000 | 30.000000000 | the shortest interval between effects for high exhaust stat
ExhaustedPlayerEffectMinMin | 10.000000000 | 10.000000000 | 10.000000000 | the shortest interval between effects for low exhaust stat
ExhaustedThreshold | 50.000000000 | 50.000000000 | 50.000000000 | player will have the 'exhausted' debuff when 'exhaust' stat is lower or equal to this value (in percents)
ExhaustionSpeed | 0.000578704 | 0.000578704 | 0.000578704 | amount of energy/vigour 'lost' per world-time second (global base value)
ExtremeExhaustionFaintAveragePeriod | 300.000000000 | 300.000000000 | 300.000000000 | How often (on average, in real time) should player faint when extremely exhausted (exhaust stat is on 0).
FactionAngrinessDecayBase | 2.000000000 | 2.000000000 | 2.000000000 | Faction angriness decay speed base, whatever it is.
FactionAngrinessDecayExp | 2.000000000 | 2.000000000 | 2.000000000 | Faction angriness decay speed exponent.
FactionAngrinessDecayMod | 0.000020000 | 0.000020000 | 0.000020000 | Faction angriness decay speed mod, whatever it is.
FactionAngrinessDecayShift | 0.250000000 | 0.250000000 | 0.250000000 | Faction angriness decay speed shift.
FactionAngrinessPropagationCoef | 1987.000000000 | 1987.000000000 | 1987.000000000 | Faction angriness is propagated through space between factions.
FactionAngrinessPropagationScale | 0.100000000 | 0.100000000 | 0.100000000 | Faction angriness propagation distance scale.
FactionRepWeight | 3.000000000 | 3.000000000 | 3.000000000 | Weight of player - faction reputation (reputation median)
FallDamageMultiplierAtMaxAgility | 0.666667000 | 0.666667000 | 0.666667000 | fall damage multiplier when agility is maxed out
FatalFallHeight | 8.000000000 | 8.000000000 | 8.000000000 | falling height above which fatal health damage is taken at agility 0
FatCollisionWeightMul | 1.400000000 | 1.400000000 | 1.400000000 | multiplies the archetype body weight if the character is fat
FoodFull | 100.000000000 | 100.000000000 | 100.000000000 | you are full
FoodHealSpeed | 2.000000000 | 2.000000000 | 2.000000000 | hp regen speed
FoodHealthThreshold | 0.500000000 | 0.500000000 | 0.500000000 | Health threshold for possitive/negative food effect
FoodOverEat | 120.000000000 | 120.000000000 | 120.000000000 | you cannot eat more
FoodPoisoningMaxHealthEffectSpeed | 0.500000000 | 0.500000000 | 0.500000000 | Maximum loss of health/s for food poisoning
FoodPoisoningMaxStatPenalty | 10.000000000 | 10.000000000 | 10.000000000 | maximum temporary penalty for affected stats while food poisoning
FoodPoisoningMaxValue | 100.000000000 | 100.000000000 | 100.000000000 | Max amount of food poisoning
FoodPoisoningMinHealthEffectSpeed | 0.100000000 | 0.100000000 | 0.100000000 | minimum loss of health/s for food poisoning
FoodPoisoningThreshold | 0.000500000 | 0.000500000 | 0.000500000 | threshold for food posioning to start taking affecting
FoodPreserverHealthIncreaseAmount | 0.500000000 | 0.500000000 | 0.500000000 | this amount is added to food's health when food preserver is applied
FoodSaltOrSmokePerkDecayModif | 0.750000000 | 0.750000000 | 0.750000000 | food decay perk modifier
FoodTickInterval | 2.000000000 | 2.000000000 | 2.000000000 | food timer expiry
FoodWitcherPerkNutritionModif | 0.700000000 | 0.700000000 | 0.700000000 | potion nutrition wicher perk modifier
ForcedFireAimSpreadMalus | 7.000000000 | 7.000000000 | 7.000000000 | spread added when the rpg forces the firing on low stamina
FromBehindAngle | 2.356190000 | 2.356190000 | 2.356190000 | minimal angle to classify the attack as 'from behind' - 0 face, PI back
FullClothDirtyingOnFullSpeed | 4000.000000000 | 4000.000000000 | 4000.000000000 | how far do we walk with full speed (1.0 walk speed) to get 100% dirty
FullClothDirtyingOnZeroSpeed | 1.000000000 | 1.000000000 | 1.000000000 | how far do we walk with half speed to get 100% dirty (other speeds than FullSpeed and HalfSpeed are linearly interpolated)
GoodArmorDefense | 2.000000000 | 2.000000000 | 2.000000000 | mainly for AI, used to judge armor
GoodWeaponAttack | 3.500000000 | 3.500000000 | 3.500000000 | mainly for AI, used to judge weapon
GoodWeaponDefense | 4.500000000 | 4.500000000 | 4.500000000 | 
HarmlessFallHeight | 1.000000000 | 1.000000000 | 1.000000000 | falling height below which no health or stamina damage is taken at agility 0
HeadHitKnockOutBaseProbability | 0.000000000 | 0.000000000 | 0.000000000 | for hits dealing a hp damage
HealthDamageToInjury | 0.020000000 | 0.020000000 | 0.020000000 | note: health is [0-100] but injury is [0-1]
HealthDeltaAbsLimit | 1000.000000000 | 1000.000000000 | 1000.000000000 | abs max of health delta
HealthFadingFromLimitValue | 0.750000000 | 0.750000000 | 0.750000000 | health percentage to activate health fading buff
HealthFull | 100.000000000 | 100.000000000 | 100.000000000 | maximum health
HealthToKnockOut | 0.000000000 | 0.000000000 | 0.000000000 | threshold for unarmed combat, health cannot reach this level
HealthToMoraleMinCoef | 0.200000000 | 0.200000000 | 0.200000000 | multiplicative coef for health = 0
HearingToFov | 3.000000000 | 3.000000000 | 3.000000000 | 
HeavyWeaponWeight | 4.000000000 | 4.000000000 | 4.000000000 | used to deduce 'attack weight'
HerbGatherSkillToCount | 0.300000000 | 0.300000000 | 0.300000000 | multiplied by sqrt(skill level) to modify the number of collected herbs
HerbGatherSkillToRadius | 0.250000000 | 0.250000000 | 0.250000000 | multiplied by skill level to calculate radius
HerbGatherXP | 7.000000000 | 7.000000000 | 7.000000000 | final XP reward for one herb gathering
HerbsInHorseInventoryForHorsenipPerk | 30.000000000 | 30.000000000 | 30.000000000 | number of herbs in horse inventory needed for Horsenip perk to be active
HerbsInInventoryForFlowerPowerPerk | 30.000000000 | 30.000000000 | 30.000000000 | number of herbs in inventory needed for Flower Power perk to be active
HighbornWealthThreshold | 10.000000000 | 10.000000000 | 10.000000000 | social class wealth threshold for perks
HorseAttackMaxSpeed | 7.000000000 | 7.000000000 | 7.000000000 | speed of the attacking rider to gain maximal attack bonus
HorseMaxAttackCoef | 2.500000000 | 2.500000000 | 2.500000000 | [1,inf] maximal multiplicative coefficient a rider will gain when attacking on HorseMaxAttackSpeed
HorseMoraleToThrowOffRider | 0.200000000 | 0.200000000 | 0.200000000 | if the horse morale is below this, it throws off the rider
HorseRidingAwardDistance | 500.000000000 | 500.000000000 | 500.000000000 | Horsemanship XP for travelling some distance on horse
HorseRidingToHorseCourage | 0.050000000 | 0.050000000 | 0.050000000 | how the rider's horse riding skill increases courage of his horse
HorseRidingToHorseStamina | 0.020000000 | 0.020000000 | 0.020000000 | how the rider's horse riding skill lowers sta consumption of his horse
HorseRidingXPPerDistance | 12.500000000 | 12.500000000 | 12.500000000 | horse riding xp gain after riding HorseRidingAwardDistance
HourglassTimeout | 10.000000000 | 10.000000000 | 10.000000000 | the time until all the sand goes down
HunterLootAmountAddCoef | 0.300000000 | 0.300000000 | 0.300000000 | add coef, the fixed portion
HunterXPKill | 15.000000000 | 15.000000000 | 15.000000000 | Hunting XP gain after a kill, multiplied by the game db coef and level
HunterXPLoot | 10.000000000 | 10.000000000 | 10.000000000 | Hunting XP gain after a loot, multiplied by the game db coef and level
ImmortalHealthMin | 1.000000000 | 1.000000000 | 1.000000000 | Minimum health for immortal souls
ImprovedSleepMultiplier | 2.000000000 | 2.000000000 | 2.000000000 | How much better better (Rest regeneration speed) is SleepImproved than Sleep buff. This buff is used for reading when player has perk InTheFlow.
<strike>ImprovedSleepMultiplierSurvival</strike> | nil | nil | nil | Possibly the original name of the `ImprovedSleepMultiplier` parameter
InactiveTimeToDestroyOversleep | 8.000000000 | 8.000000000 | 8.000000000 | how long to let inactive oversleep buff survive (in game seconds) (we have this threshold so that the buff will not be destroyed right after being created in SkipTime class)
<strike>InactiveTimeToDestroyOversleepCreated</strike> | nil | nil | nil | Possibly the original name of the `InactiveTimeToDestroyOversleep` parameter
InjuringFallHeight | 2.500000000 | 2.500000000 | 2.500000000 | falling height above which health damage is taken at agility 0
InjuryBleedingInterval | 6.000000000 | 6.000000000 | 6.000000000 | bleeding interval, the time required to lose 1HP
InjuryHighThreshold | 0.800000000 | 0.800000000 | 0.800000000 | limb is bleeding if above this threshold
InjuryLowThreshold | 0.200000000 | 0.200000000 | 0.200000000 | limb is considered healthy if below this treshold
InjuryRegenInterval | 10.000000000 | 10.000000000 | 10.000000000 | injuries fade-out, the time required to regen 1% of injury
ItemDisappearingMulti | 3.000000000 | 3.000000000 | 3.000000000 | multiplier 1/x - x limit(up/down) for item disappearing speed in extremes (cheap vs. expensive, small vs. large)
ItemHealthPriceStatusWeight | 0.800000000 | 0.800000000 | 0.800000000 | item health status weight price coef
ItemOwnerDescFadeToSuspiciencyExp | 0.250000000 | 0.250000000 | 0.250000000 | 
ItemOwnerFactionDistanceCoef1 | 500.000000000 | 500.000000000 | 500.000000000 | 
ItemOwnerFactionDistanceCoef2 | 300.000000000 | 300.000000000 | 300.000000000 | 
ItemOwnerFactionDistanceToSuspiciencyMax | 1.000000000 | 1.000000000 | 1.000000000 | 
ItemOwnerFactionDistanceToSuspiciencyMin | 0.250000000 | 0.250000000 | 0.250000000 | 
ItemOwnerFadeCoefToSuspiciencyExp | 3.000000000 | 3.000000000 | 3.000000000 | 
ItemOwnerFadeCoefToSuspiciencyMul | 2.000000000 | 2.000000000 | 2.000000000 | 
ItemOwnerFadeConspicuousnessToHours | 10.000000000 | 10.000000000 | 10.000000000 | world time hours
ItemOwnerFadePriceToHours | 1.000000000 | 1.000000000 | 1.000000000 | world time hours per decigrosh
ItemOwnerIsShopkeeperToSuspiciency | 8.000000000 | 8.000000000 | 8.000000000 | basket suspiciency calculation
ItemOwnerNeverFadesToSuspiciency | 10.000000000 | 10.000000000 | 10.000000000 | 
ItemOwnerRelationshipToSuspiciencyMin | 0.100000000 | 0.100000000 | 0.100000000 | 
JailRecoveryDebuffDurationMultiplier | 0.200000000 | 0.200000000 | 0.200000000 | duration of JailRecovery debuff is calculated as `jail duration * this multiplier`
JailRecoveryDebuffMaxHours | 240.000000000 | 240.000000000 | 240.000000000 | hours spent in jail after JailRecovery debuff reaches its maximal values
JumpCostBase | 6.000000000 | 6.000000000 | 6.000000000 | Stamina cost of one jump
LethalDmgR | 10.000000000 | 10.000000000 | 10.000000000 | DmgR that is known to cause death
LocalHeroInfamousReputationThreshold | 0.700000000 | 0.700000000 | 0.700000000 | above this rep local hero, under infamous
LocationReputationHatedThreshold | 0.200000000 | 0.200000000 | 0.200000000 | reputation threshold below which a location will hate the player
LocationReputationLovedThreshold | 0.800000000 | 0.800000000 | 0.800000000 | reputation threshold above which a location will love the player
LockPickingAdequateTolerance | nil | nil | <font color="blue">0.170000000</font> | locks on a similar level as the player have adequate tolerance
LockPickingAppropriateTolerance | 0.045000000 | 0.045000000 | 0.045000000 | the lock is considered too hard to pick, if the tolerance is smaller than this
LockPickingCursorShakeRange | 0.080000000 | 0.080000000 | 0.080000000 | how much does cursor shake during lock picking (maximum/base value)
LockPickingCursorShakeSpeed | 30.000000000 | 30.000000000 | 30.000000000 | how fast does cursor shake during lock picking
LockPickingFailRelativeXPMulCoef | 0.101563000 | 0.101563000 | 0.101563000 | multiplicative constant to derive XP reward relative to the success
LockpickingFailSoundIntensity | 0.500000000 | 0.500000000 | 0.500000000 | one-shot intensity relative to the database
LockpickingLockpickBreakChance | 1.000000000 | 1.000000000 | 1.000000000 | base lockpick break chance
LockpickingRelDistanceToSoundIntensity | 0.500000000 | 0.500000000 | 0.500000000 | how relative distance influences sound
LockPickingSkillToShakeRel | 0.030000000 | 0.030000000 | 0.030000000 | how much does the skill decrease the cursor shake (`skill * this is relative to maximum/base`)
LockpickingSoundIntensityMin | 0.300000000 | 0.300000000 | 0.300000000 | minimal multiplier the lockpicking minigame will generate
LockPickingStealthXP | 8.000000000 | 8.000000000 | 8.000000000 | xp to stealth for each successful lock-pick
LockPickingSuccessXPDivCoef | 0.046875000 | 0.046875000 | 0.046875000 | constant used in the denominator to derive XP reward for a successfully opened lock
LockPickingSuccessXPMulCoef | 18.000000000 | 18.000000000 | 18.000000000 | multiplicative constant to derive XP reward for a successfully opened lock
LockPickingToleranceACoef | 0.450000000 | 0.450000000 | 0.450000000 | the lockpicking tolerance formula
LockPickingToleranceKCoef | 0.070000000 | 0.070000000 | 0.070000000 | the lockpicking tolerance formula
LockPickingToleranceMCoef | 0.687000000 | 0.687000000 | 0.687000000 | the lockpicking tolerance formula
LockPickingToleranceNCoef | 0.480000000 | 0.480000000 | 0.480000000 | the lockpicking tolerance formula
LockPickingTurnBackDivCoef | 0.100000000 | 0.100000000 | 0.100000000 | constant used in the denominator to derive the turnback speed of a lock
LockPickingTurnBackMulCoef | 5.000000000 | 5.000000000 | 5.000000000 | multiplicative constant to derive the turnback speed of a lock
LowHealthThreshold | 40.000000000 | 40.000000000 | 40.000000000 | threshold for low health effects (for npcs)
MatPierceableMaxArmor | 10.000000000 | 10.000000000 | 10.000000000 | armor of a rock-solid material
MatPierceableMin | 6.000000000 | 6.000000000 | 6.000000000 | OBSOLETE: projectiles with stab damage can stab into
MaxAgilityToMovementSpeedAddition | 0.150000000 | 0.150000000 | 0.150000000 | max positive addition (for maximal vit), the same amount is subtracted on level 0
MaxArmorLoad | 0.200000000 | 0.200000000 | 0.200000000 | 
MaxAttackSpeedMod | 0.400000000 | 0.400000000 | 0.400000000 | maximal relative change in the attack speed
MaxCloudAverageForShiningArmor | 0.300000000 | 0.300000000 | 0.300000000 | used by perk Knight in a Shining Armor; this is maximal current cloud average that still allows this perk to be active
MaxCourageMoraleContextFadingMod | 0.030000000 | 0.030000000 | 0.030000000 | how much can courage affect morale context fading
MaxDamage | 200.000000000 | 200.000000000 | 200.000000000 | all stam and health damages are clamped
MaxDmgR | 4.000000000 | 4.000000000 | 4.000000000 | ceil of DmgR ('damage raw')
MaxFencingWeaponUsageMod | 0.200000000 | 0.200000000 | 0.200000000 | relative weapon status damage for max fencing
MaxHearingSoundAttenuationCoef | 0.200000000 | 0.200000000 | 0.200000000 | minimal attenuation for non-zero hearing stat
MaxItemDisappearingTime | 32400.000000000 | 32400.000000000 | 32400.000000000 | max game time for dropped items to disapper
MaxLightProbeValue | 65.000000000 | 65.000000000 | 65.000000000 | value for the max visibility
MaxModConspicuousness | 1.000000000 | 1.000000000 | 1.000000000 | final modified conspicuousness stat maximum (the most conspicuous actor)
MaxModVisibility | 3.500000000 | 3.500000000 | 3.500000000 | final modified visibility stat maximum (the most visible actor)
MaxMorale | 1.000000000 | 1.000000000 | 1.000000000 | max deriv stat value
MaxPedalCost | 2.000000000 | 2.000000000 | 2.000000000 | pedaling STA cost (pressure 1)
MaxPerfectBlockSlotModifier | 0.850000000 | 0.850000000 | 0.850000000 | modifier of PB slot window - determined as (t_hit - t_pbslot) from attack * this value.
MaxPerkPoints | 10.000000000 | 10.000000000 | 10.000000000 | total number of perk points player will gain per stat/skill
MaxSlashBuffApplyChance | 1.500000000 | 1.500000000 | 1.500000000 | chance to apply buff on slash when giving max hp damage
MaxSmashBuffApplyChance | 0.700000000 | 0.700000000 | 0.700000000 | chance to apply buff on smash when giving max hp damage
MaxSpecialPerfectBlockSlotModifier | 0.600000000 | 0.600000000 | 0.600000000 | modifier of SPB slot window - determined as (t_hit - t_pbslot) from attack x this value.
MaxStabBuffApplyChance | 2.000000000 | 2.000000000 | 2.000000000 | Chance to apply buff on stab when giving maximum health damage
MaxStatToAttackMult | 1.200000000 | <font color="red">1.100000000</font> | 1.100000000 | Maximal relative attack multiplier (for a high stat)
MaxStatToAttackStaminaCostMult | 2.000000000 | 2.000000000 | 2.000000000 | Maximum Stamina cost multiplier for a low stat
MaxStatToAttackStaminaCostStatDiff | 5.000000000 | 5.000000000 | 5.000000000 | stat difference for max/min cost multiplier
MaxStatToAttackStatDiff | 5.000000000 | 5.000000000 | 5.000000000 | stat difference for max/min relative attack multiplier
MaxStealthHitSoundMultiplier | 0.400000000 | <font color="red">0.220000000</font> | 0.220000000 | intensity multiplier for max stealth level
MaxViewRadius | 100.000000000 | 100.000000000 | 100.000000000 | the maximal view radius a superman NPC will have
MaxWeaponBuffCharge | 30.000000000 | 30.000000000 | 30.000000000 | max number of uses
MaxWeatherSoundAttenuationCoef | 0.200000000 | 0.200000000 | 0.200000000 | 0 - allow weather conditions to mute the sounds<br>1 - no influence
MetabolismAbsorbSpeed | 0.006900000 | 0.006900000 | 0.006900000 | food/alcohol metabolised (removed) in world time
MetabolismDigestSpeed | 0.027700000 | 0.027700000 | 0.027700000 | food/alcohol digested (added) in world time
MetabolismDigestSpeedMultiplier | 1.500000000 | 1.500000000 | 1.500000000 | accelerate digest speed multiplier to_digest = max_poisoning
MinHealthToBeAbleToSleepOrSkiptime | 30.000000000 | 30.000000000 | 30.000000000 | player will not be able to sleep or wait if health would go under this threshold during sleep or waiting
MinLeftoverPerks | 1.000000000 | 1.000000000 | 1.000000000 | Preferred number of leftovers
MinLightProbeVisibility | -1.000000000 | -1.000000000 | -1.000000000 | Minimum value for the minimal probe result
MinModConspicuousness | -1.000000000 | -1.000000000 | -1.000000000 | Final modified Conspicuousness stat minimum (the least conspicuous actor)
MinModVisibility | -2.000000000 | -2.000000000 | -2.000000000 | Final modified Visibility stat minimum (the most invisible actor)
MinMorale | 0.000000000 | 0.000000000 | 0.000000000 | Minimum derived stat value
MinPedalCost | 1.000000000 | 1.000000000 | 1.000000000 | Pedaling Stamina cost (pressure 0)
MinPerfectBlockSlot01 | 0.300000000 | 0.300000000 | 0.300000000 | the smallest Perfect Block slot for the lowest level
MinPerkPoints | 5.000000000 | 5.000000000 | 5.000000000 | no leftovers if the number of perk points would be &lt;= than this
MinPossibleSleepTime | 1.001000000 | 1.001000000 | 1.001000000 | player will reject to lie into bed when he will not be able to sleep at least this long (due to bleeding/hunger/etc in hours)
MinRelativeStaminaMax | 0.300000000 | 0.300000000 | 0.300000000 | Short-term Stamina maximum relative to long-term maximum
MinStatToAttackMult | 0.500000000 | 0.500000000 | 0.500000000 | Minimal relative attack multiplier for a low stat
MinStatToAttackStaminaCostMult | 0.800000000 | 0.800000000 | 0.800000000 | Minimum Stamina cost multiplier for a high stat
MinStealthHitSoundMultiplier | 0.100000000 | <font color="red">0.060000000</font> | 0.060000000 | Intensity multiplier for minimum Stealth level
MinTrueRelationDistThreshold | 1.500000000 | 1.500000000 | 1.500000000 | Minimal distance required to see the true faction
MinViewRadius | 2.500000000 | 2.500000000 | 2.500000000 | Minimal view radius an almost blind NPC will have, also threshold for instant detection
MinWeaponBuffCharge | 15.000000000 | 15.000000000 | 15.000000000 | 
MoraleContextFadingSpeed | 0.050000000 | 0.050000000 | 0.050000000 | Speed of Morale context increasing/decreasing to 0
MoraleDecisionReliability | 0.150000000 | 0.150000000 | 0.150000000 | Reliability of morale checks
MoraleForCombat | 0.200000000 | 0.200000000 | 0.200000000 | How much morale an NPC must have to not flee from combat
NightCoefToNoise | 0.200000000 | 0.200000000 | 0.200000000 | 
NightCoefToVis | -0.500000000 | -0.500000000 | -0.500000000 | `nightCoef = 1 - daytimeCoef`
NonSkillBookXP | 30.000000000 | 30.000000000 | 30.000000000 | Reading XP rewarded for reading non-skill books
NPCRepWeight | 5.000000000 | 5.000000000 | 5.000000000 | Weight of player - npc reputation (reputation median)
OverallArmorDefenseMoraleWeight | 3.000000000 | 3.000000000 | 3.000000000 | Weight of normalized load affecting morale
OverallWeaponAttackMoraleWeight | 3.000000000 | 3.000000000 | 3.000000000 | Weight of normalized attack affecting morale
OverreadnessEmptyTime | 16.000000000 | 16.000000000 | 16.000000000 | how long (in game hours) does it take to empty the oversleepness stat (time player have to be not reading to be able to read max time again)
OverreadnessFillTime | 8.000000000 | 8.000000000 | 8.000000000 | how long (in game hours) does it take to fill the oversleepness stat (max time player can read)
OversleepnessEmptyTime | 12.000000000 | 12.000000000 | 12.000000000 | how long (in game hours) does it take to empty the oversleepness stat (time player have to be awake to be able to sleep max time again)
OversleepnessFillTime | 12.000000000 | 12.000000000 | 12.000000000 | how long (in game hours) does it take to fill the oversleepness stat (max time player can sleep)
PerceivedSuperfactionImportanceThresholdRel | 0.333333000 | 0.333333000 | 0.333333000 | superfaction items must occupy more than this for the soul to look like the superfaction
PerceptionBaseCha | 10.000000000 | 10.000000000 | 10.000000000 | 
PerceptionMaxFov | 180.000000000 | 180.000000000 | 180.000000000 | the maximal field of view a superman NPC will have
PerceptionMeanDist | 5.000000000 | 5.000000000 | 5.000000000 | 
PerceptionMinFov | 90.000000000 | 90.000000000 | 90.000000000 | the minimal field of view a deaf NPC will have
PerceptionPriorBoostPlayer | 12.000000000 | 12.000000000 | 12.000000000 | boost for player
PerceptionPriorBoostRangedWeapon | 100.000000000 | 100.000000000 | 100.000000000 | boost for ranged weapons (multiplied by PriorWeapon!)
PerceptionPriorCha | 0.300000000 | 0.300000000 | 0.300000000 | 
PerceptionPriorConsp | 3.000000000 | 3.000000000 | 3.000000000 | 
PerceptionPriorCrimeLockpick | 12.000000000 | 12.000000000 | 12.000000000 | 
PerceptionPriorCrimeLoot | 12.000000000 | 12.000000000 | 12.000000000 | priority boost for crime
PerceptionPriorDead | 25.000000000 | 25.000000000 | 25.000000000 | dead or unconscious
PerceptionPriorDist | 2.000000000 | 2.000000000 | 2.000000000 | 
PerceptionPriorEnemyRelationship | -50.000000000 | -50.000000000 | -50.000000000 | 
PerceptionPriorFriendRelationship | -4.000000000 | -4.000000000 | -4.000000000 | 
PerceptionPriorGender | 2.000000000 | 2.000000000 | 2.000000000 | 
PerceptionPriorNotHumanRace | -15.000000000 | -15.000000000 | -15.000000000 | 
PerceptionPriorTarget | 10.000000000 | 10.000000000 | 10.000000000 | target priority estimation
PerceptionPriorThreatened | -5.000000000 | -5.000000000 | -5.000000000 | 
PerceptionPriorVisCrimes | 6.000000000 | 6.000000000 | 6.000000000 | 
PerceptionPriorVisItems | 0.500000000 | 0.500000000 | 0.500000000 | 
PerceptionPriorVisPeople | 2.000000000 | 2.000000000 | 2.000000000 | 
PerceptionPriorWeapon | 8.000000000 | 8.000000000 | 8.000000000 | 
PerkBerserkDuration | 30.000000000 | 30.000000000 | 30.000000000 | how long are buffs active after the perk is triggered
PerkBerserkHealthThreshold | 0.150000000 | 0.150000000 | 0.150000000 | activate on health
PerkBloodRushDistance | 5.000000000 | 5.000000000 | 5.000000000 | distance from dying enemy when Blood Rush perk bonuses are activated
PerkBloodRushDuration | 15.000000000 | 15.000000000 | 15.000000000 | duration of Blood Rush perk bonuses after an enemy dies nearby
PerkBrutusCombatDmgRBonusFromBehind | 1.300000000 | 1.300000000 | 1.300000000 | brutus perk multiplicative base Dmg (CombatDmgRBonusFromBehind)
PerkCarriedBodyGravediggerWeightMul | 0.500000000 | 0.500000000 | 0.500000000 | carried body weight multiplier for gravedigger perk
PerkChainStrikeMaxChain | 5.000000000 | 5.000000000 | 5.000000000 | maximal successive strikes
PerkDaringDebonairWantedLevel | 1.000000000 | 1.000000000 | 1.000000000 | Daring Debonair wanted level threshold
PerkLastGaspCooldown | 600.000000000 | 600.000000000 | 600.000000000 | how fast can the perk be activated again
PerkManlyOdourDirtinessThreshold | 0.500000000 | 0.500000000 | 0.500000000 | Manly Odour perk bonuses are activated above this dirtiness threshold
PerkProperDietActivationTime | 120.000000000 | 120.000000000 | 120.000000000 | hours until ProperDiet perk bonuses are activated
PerkTauntAttackerMoraleMultiplier | 3.000000000 | 3.000000000 | 3.000000000 | multiplier for 'combat_dodge_attacker' morale change when victim has Taunt perk
PerkWaterOfLifeAlcoholMultiplier | 0.500000000 | 0.500000000 | 0.500000000 | potion alcohol effect multiplier for Water of life perk
PerkWaterOfLifeHealthMultiplier | 1.500000000 | 1.500000000 | 1.500000000 | potion health effect multiplier for Water of life perk
PicklockDmgSpeed | 10.000000000 | 10.000000000 | 10.000000000 | how fast is picklock durability decreasing (will be multiplied by the relative distance)
PicklockFatalRelativeDist | 5.000000000 | 5.000000000 | 5.000000000 | maximal relative distance, if futher the pick lock is destroyer
PickpocketingAngleChancePenalty | 0.002700000 | 0.002700000 | 0.002700000 | penalty in (0-1) to chance pickpocketing for each angle from optimal possition exactly from behind victim (180 max)
PickpocketingComradePerkBonus | 0.300000000 | 0.300000000 | 0.300000000 | max bonus in (0-1) to pickpocketing for comrade perk
PickpocketingDistance | nil | <font color="blue">2.000000000</font> | 2.000000000 | Max pickpocketing range (not starting interactor range)
PickpocketingFailXPMod | 0.300000000 | 0.300000000 | 0.300000000 | Pickpocketing XP modified on failure
PickpocketingIndicatorSharpness | 0.200000000 | <font color="red">0.000000000</font> | 0.000000000 | 0 - precise slow change<br>1 - sharp change
PickpocketingItemUncoverTimePerWeight | 0.100000000 | 0.100000000 | 0.100000000 | time to uncover item per weight unit
PickpocketingMaxSkillChargeSpeedRatio | 6.000000000 | 6.000000000 | 6.000000000 | charge speed ratio boost with best skill
PickpocketingMaxSkillChargeTime | 30.000000000 | 30.000000000 | 30.000000000 | max charge time with best skill
PickpocketingMinChargeTime | 2.000000000 | 2.000000000 | 2.000000000 | min charge time needed
PickpocketingMisstargetingTolerance | nil | <font color="blue">2000.000000000</font> | 2000.000000000 | Time tolerance for temporarily mistargeting your victim
PickpocketingNPCDrunkTimeChanceMod | 0.500000000 | 0.500000000 | 0.500000000 | Modifies TimeChancePenalty when drunk
PickpocketingNPCHurtTimeChanceMod | 0.750000000 | 0.750000000 | 0.750000000 | Modifies TimeChancePenalty when hurt
PickpocketingNPCSleepingTimeChanceMod | 0.500000000 | 0.500000000 | 0.500000000 | Modifies TimeChancePenalty when sleeping
PickpocketingRandomChanceRollMinCap | nil | <font color="blue">0.100000000</font> | 0.100000000 | Worst random rolls will always be capped to this minimum chance
PickpocketingRobbedAngrinessChancePenalty | 0.050000000 | 0.050000000 | 0.050000000 | penalty in (0-1) to pickpocketing chance for each time victim was robbed before
PickpocketingStealthXP | 12.000000000 | 12.000000000 | 12.000000000 | Stealth XP for each successful pickpocketing
PickpocketingTimeChancePenaltyBest | 0.013300000 | 0.013300000 | 0.013300000 | penalty in pickpocketing chance in best case(s)
PickpocketingTimeChancePenaltyWorst | 0.100000000 | 0.100000000 | 0.100000000 | penalty in pickpocketing chance in worst case(s)
PickpocketingTreasurePriceXP | 100.000000000 | 100.000000000 | 100.000000000 | Additional XP gain calculated by stolen items total value
PickpocketingXP | 15.000000000 | 15.000000000 | 15.000000000 | Pickpocketing XP for each pocket successfully picked
PoorWeaponDefense | 1.000000000 | 1.000000000 | 1.000000000 | 
ProjectileMaxBreakProb | 0.700000000 | 0.700000000 | 0.700000000 | probability of breaking an arrow when a rock-solid material is hit
QuestMoneyRewardScaleConstant | 1.250000000 | <font color="red">1.200000000</font> | 1.200000000 | scale constnat for quest reward item amount
RangedWpnCosThetaToAttackMin | 0.700000000 | 0.700000000 | 0.700000000 | cos(theta) linearly lowers the attack in the range [this,1]
RangedWpnMinPowerCoef | 0.100000000 | 0.100000000 | 0.100000000 | the power coefficient for a really weak soul (the stats are far below requirements)
RangedWpnMinStrCoef | 0.500000000 | 0.500000000 | 0.500000000 | if the curr/req strength ratio goes below this, the power is minimal
RangedWpnOptimalDistanceToMinamal | 0.500000000 | 0.500000000 | 0.500000000 | ratio between the database attack distance and the minimal range for the AI
RangedWpnPowerConstA | 1.850000000 | 1.850000000 | 1.850000000 | used to convert strength requirements to the resulting power
RangedWpnPwrToSpeed | 1.000000000 | 1.000000000 | 1.000000000 | total power to launch speed
RangedWpnSelfHarmCoef | 15.000000000 | 15.000000000 | 15.000000000 | Special constant used in self harm equation
RangedWpnSpeedToAttack | 0.012000000 | 0.012000000 | 0.012000000 | attack mod deduced from impact speed
<strike>ReadingRestEffectiveness</strike> | 0.300000000 | nil | nil | If this value is 0.3, reading will regen player as sleeping on bed with comfort 30%.
<strike>ReadingRestUpperLimit</strike> | 1.000000000 | nil | nil | When sleeping, the rest can not exceed bed quality. When reading, the threshold is given by this value.
ReadingXpPerHour | 20.000000000 | 20.000000000 | 20.000000000 | Reading XP gained after one hour of reading with 100% reading speed
RecognitionSpeedNotVisible | -0.500000000 | -0.500000000 | -0.500000000 | must be negative, how the recognition is decreased
RecognitionTimeDistanceGain | 0.100000000 | 0.100000000 | 0.100000000 | perlin gain for the distance influencing the recognition time
RecognitionTimeKNegativeCoef | -6.000000000 | -6.000000000 | -6.000000000 | multiplicative coef for negative values of conspicuousness
RecognitionTimeKPositiveCoef | -3.000000000 | -3.000000000 | -3.000000000 | multiplicative coef for positive values of conspicuousness
RecognitionTimePCoef | 8.000000000 | 8.000000000 | 8.000000000 | recognition time for a character with conspicuousness = 0
RelationshipToImpressCharisma | 0.800000000 | 0.800000000 | 0.800000000 | [0,inf]: how much reputation is used to raise charisma
RelationshipToPersuadeSpeech | 0.800000000 | 0.800000000 | 0.800000000 | [0,inf]: how much reputation is used to raise speech
RelationshipToThreatenBadassness | 0.800000000 | 0.800000000 | 0.800000000 | [0,inf]: how much reputation is used to raise badassness
RepairKitCapacity | 200.000000000 | 200.000000000 | 200.000000000 | Repair kit capacity to repair
RepairKitItemHealthBestLimit | 0.600000000 | 0.600000000 | 0.600000000 | With high skill/quality repair kit, can repair items until this health limit
RepairKitItemHealthDefaultLimit | 0.800000000 | 0.800000000 | 0.800000000 | Default repair kit item health limit
RepairKitItemPerkBuffHealthThreshold | 0.300000000 | 0.300000000 | 0.300000000 | Buffs added by repair kit perks won't be functional under this item health
RepairKitMaxSkillCapacityCoef | 1.500000000 | 1.500000000 | 1.500000000 | Max skill coefficient for repair kit total capacity
RepairPriceModif | 0.650000000 | 0.650000000 | 0.650000000 | Default repairing shop price modifier
ReputationPropagationBiasTime | 1800.000000000 | 1800.000000000 | 1800.000000000 | random bias to propagation time (world time)
ReputationPropagationCoef | 0.300000000 | 0.300000000 | 0.300000000 | Propagation coef up (soul->faction->superfaction)
ReputationPropagationTime | 10800.000000000 | 10800.000000000 | 10800.000000000 | propagation time from npc to faction/superfaction (world time)
ResetNearbyRelationshipRange | 50.000000000 | 50.000000000 | 50.000000000 | range for relationship reset
ResetPublicFriendsRelationshipMin | 0.150000000 | 0.150000000 | 0.150000000 | minimal relationship for the alied forces after reset
RespawnTimeBase | 800.000000000 | 800.000000000 | 800.000000000 | Time before a hidden corpse respawns (base time)
RespawnTimeVariation | 60.000000000 | 60.000000000 | 60.000000000 | Time before a hidden corpse respawns (random extra time)
RiderAgilityToHorsePullDown | 0.500000000 | 0.500000000 | 0.500000000 | Relative rider Agility to horse pull down
RiderHorseStaminaCoef | 0.250000000 | 0.250000000 | 0.250000000 | Ratio between Stamina consumption of a horse and its rider
RiderSkillToHorsePullDown | 0.500000000 | 0.500000000 | 0.500000000 | Relative riding skill skill to horse pull down
RiderThreatToHorseMorale | 0.100000000 | 0.100000000 | 0.100000000 | Morale decrease per one rider threat
SecondaryStatXPRatio | 0.500000000 | 0.500000000 | 0.500000000 | secondary weapon stat ratio
SharpeningFullNegativeHealthXP | 20.000000000 | 20.000000000 | 20.000000000 | 
SharpeningFullPositiveHealthXP | 100.000000000 | 100.000000000 | 100.000000000 | change in weapon health at which the sharpening is considered successful
SharpeningMaxDestructionAngle | 0.700000000 | 0.700000000 | 0.700000000 | 
SharpeningMaxIdealAngle | 0.500000000 | 0.500000000 | 0.500000000 | 
SharpeningMinDestructionAngle | 0.600000000 | 0.600000000 | 0.600000000 | 
SharpeningMinEfficiencyHealth | 0.300000000 | 0.300000000 | 0.300000000 | health you can achieve with the worst efficiency
SharpeningMinIdealAngle | 0.300000000 | 0.300000000 | 0.300000000 | 
SharpeningSuccessfulHealthDelta | 0.100000000 | 0.100000000 | 0.100000000 | 
ShoeHealthDecrease | 0.001000000 | 0.001000000 | 0.001000000 | status delta per traveled m
ShoeHealthUpdateDistance | 50.000000000 | 50.000000000 | 50.000000000 | shoe health is update after traveling N m
ShortTermNutritionDigestionSpeedMultiplier | 5.000000000 | 5.000000000 | 5.000000000 | digestion multiplier for part of the food with low nutrition value
SkillCap | 20.000000000 | 20.000000000 | 20.000000000 | max skill level, also effects of a general skill are maximal at this level
SkillDiffToAttackSpeed | 0.100000000 | 0.100000000 | 0.100000000 | relative attack speed gain for one skill level difference
SkillToDefense | 0.028570000 | 0.028570000 | 0.028570000 | 
SkillToDmgConstA | 70.000000000 | <font color="green">250.000000000</font> | 250.000000000 | 
SkillToFencingBase | 0.800000000 | 0.800000000 | 0.800000000 | 
SkillToPerfectBlockPowTo | 0.500000000 | 0.500000000 | 0.500000000 | `slot = relativeSkill ^ this`
SkillToRangedWpnAIRange | 0.500000000 | 0.500000000 | 0.500000000 | how the relative skill influences the weapon range for the AI
SkillXPBlock | 2.000000000 | 2.000000000 | 2.000000000 | XP gain after a successful block
SkillXPComboHit | 4.000000000 | 4.000000000 | 4.000000000 | weapon XP gain after a hit in a combo
SkillXPDrinkAlcohol | 1.000000000 | 1.000000000 | 1.000000000 | XP gain per 1 alcohol content drinked
SkillXPHit | 2.000000000 | 2.000000000 | 2.000000000 | weapon XP gain after a hit
SkillXPKill | 12.000000000 | 12.000000000 | 12.000000000 | weapon XP gain after a kill
SkillXPLevelBase | 20.000000000 | 20.000000000 | 20.000000000 | base value (additive) to calculate XPs needed for the next level
SkillXPLevelDiff | 30.000000000 | 30.000000000 | 30.000000000 | multiplicative value to calculate XPs needed
SkillXPPerfectBlock | 8.000000000 | 8.000000000 | 8.000000000 | XP gain after a successful perfect block
SkillXPRiposte | 8.000000000 | 8.000000000 | 8.000000000 | successful riposte (attack after perfect block)
SkillXPUseRepairKit | 5.000000000 | 5.000000000 | 5.000000000 | XP gain per 1 health repaired by repairkit
SleepHealthRegenBaseSpeed | 0.003472220 | 0.003472220 | 0.003472220 | full regen after 8 world-time hours
SleepToSaveThreshold | 1.000000000 | 1.000000000 | 1.000000000 | sleeping at least this time triggers autosave.
SlimCollisionWeightMul | 0.800000000 | 0.800000000 | 0.800000000 | multiplies the archetype body weight if the character is slim
SoulCourageMoraleWeight | 5.000000000 | 5.000000000 | 5.000000000 | Weight of soul courage affecting morale
SpeechDiffToSkillCheckResult | 0.300000000 | 0.300000000 | 0.300000000 | > 0; speech diff for result = -1/1
SpeechMulOnExtremeExhaustion | 0.750000000 | 0.750000000 | 0.750000000 | Player will have this speech multiplied by this value when he has exhaust equal to 0. Speech will not be changed when exhaust is 50. Linear interpolation on multiplier is applied when exhaust is between 0 and 50;
SpeechXPLevelBase | 20.000000000 | 20.000000000 | 20.000000000 | 
SpeechXPLevelDiff | 30.000000000 | 30.000000000 | 30.000000000 | 
SprintCost | 3.500000000 | 3.500000000 | 3.500000000 | stamina cost of sprint
StamDamage | 8.000000000 | 8.000000000 | 8.000000000 | see: rpglib::calcStaminaDamageCost
StaminaDamageToInjury | 0.000000000 | 0.000000000 | 0.000000000 | note: stamina is [0-100] but injury is [0-1]
StaminaToHealthDamageMax | 0.750000000 | 0.750000000 | 0.750000000 | stamina-health damage transfer for dmgr=1
StaminaToHealthDamageMin | 0.250000000 | 0.250000000 | 0.250000000 | stamina-health damage transfer for dmgr=0
StamRegenBase | 22.000000000 | 22.000000000 | 22.000000000 | base regeneration speed
StamRegenBlockMod | 0.600000000 | 0.600000000 | 0.600000000 | relative stam regen speed during active block or raised weapon
StamRegenCooldown | 1.500000000 | 1.500000000 | 1.500000000 | cooldown timer expiry
StamRegenFromVit | 1.000000000 | 1.000000000 | 1.000000000 | how our VIT stat affects stamina regeneration
StamRegenMoveMod | 0.750000000 | 0.750000000 | 0.750000000 | relative stam regen speed during movement
StamRegenRelativeDiff | 0.666667000 | 0.666667000 | 0.666667000 | maximal relative difference to the base speed on low/high stamina
StarvationExtremeThreshold | 0.000000000 | 0.000000000 | 0.000000000 | when nutrition is below this value, extreme hunger starts
StarvationHealthLossSpeed | 0.000578704 | <font color="green">0.001000000</font> | 0.001000000 | by design the same speed as the digestion
StarvationHugeThreshold | 25.000000000 | 25.000000000 | 25.000000000 | when nutrition is below this value, significant hunger starts
StarvationPlayerEffectMaxMax | 60.000000000 | 60.000000000 | <font color="green">75.000000000</font> | longest interval between effects for high hunger stat
StarvationPlayerEffectMaxMin | 90.000000000 | 90.000000000 | <font color="green">120.000000000</font> | longest interval between effects for low hunger stat
StarvationPlayerEffectMinMax | 30.000000000 | 30.000000000 | <font color="green">45.000000000</font> | shortest interval between effects for high hunger stat
StarvationPlayerEffectMinMin | 60.000000000 | 60.000000000 | <font color="green">90.000000000</font> | shortest interval between effects for low hunger stat
StarvationThreshold | 50.000000000 | 50.000000000 | 50.000000000 | when nutrition is below this value, hunger starts
StatCap | 20.000000000 | 20.000000000 | 20.000000000 | max stat level
StatsToDodgePowTo | 0.500000000 | 0.500000000 | 0.500000000 | `slot = relativeStats ^ this`
StatToMainLevelBase | 0.500000000 | 0.500000000 | 0.500000000 | a1 of the geometric progression
StatXPAgilityPerDodge | 2.000000000 | 2.000000000 | 2.000000000 | XP gain after a dodge
StatXPComboHit | 4.000000000 | 4.000000000 | 4.000000000 | XP gain after combo hit
StatXPHit | 2.000000000 | 2.000000000 | 2.000000000 | XP gain after a hit
StatXPKill | 8.000000000 | 8.000000000 | 8.000000000 | XP gain after a kill
StatXPSpeechPerSequence | 1.000000000 | 1.000000000 | 1.000000000 | Speech XP gain after selecting an unused sequence (multiplied by speech_coef of that sequence)
StatXPSpeechPersuadeSuccessMax | 10.000000000 | 10.000000000 | 10.000000000 | Maximal XP gain for persuade
StatXPVitalityPerDistance | 8.000000000 | 8.000000000 | 8.000000000 | Vitality XP gain after sprinting `AthleticXPAwardDistance`
StatXPVitalityPerJump | 0.500000000 | 0.500000000 | 0.500000000 | Vitality XP gain for each jump
StatXPVitalityPerKill | 15.000000000 | 15.000000000 | 15.000000000 | Vitality XP gain after a kill
StatXPVitalityPerVault | 0.700000000 | 0.700000000 | 0.700000000 | Vitality XP gain for each vault over a ledge
StealthAttackFailXp | 10.000000000 | 10.000000000 | 10.000000000 | Stealth XP gain for failed stealth kill or take-down
StealthAttackMaxXp | 50.000000000 | 50.000000000 | 50.000000000 | Stealth XP gain for successful stealth kill or take-down, strongest enemy
StealthAttackMinXp | 25.000000000 | 25.000000000 | 25.000000000 | Stealth XP gain for successful stealth kill or take-down, weakest enemy
StealthCooldown | 5.000000000 | 5.000000000 | 5.000000000 | after last detector npc stops seeing player
StealthKillDamage | 100.000000000 | 100.000000000 | 100.000000000 | damage given to the victim
StealthKillProbCoefA | 4.000000000 | 4.000000000 | 4.000000000 | coefficient for stealth kill/knock-out probability formula
StealthKillProbCoefB | 1.000000000 | 1.000000000 | 1.000000000 | coefficient for stealth kill/knock-out probability formula
StealthKillProbCoefC | 1.000000000 | 1.000000000 | 1.000000000 | coefficient for stealth kill/knock-out probability formula
StealthKnockOutUnconsciousDepthBase | 250.000000000 | 250.000000000 | 250.000000000 | the base unconsciousness depth for stealth knockout
StealthSkillToFootstepSoundMult | 0.400000000 | 0.400000000 | 0.400000000 | how much are footsteps attenuated for the max skill
StealthSkillToRecogTime | 0.050000000 | 0.050000000 | 0.050000000 | how much is the required time extended by the skill level (relative)
StealthSkillToViewRadiusDecr | 0.020000000 | 0.020000000 | 0.020000000 | how much is the view radius decreased by the skill level (relative)
StealthSneakBaseDistance | 4.000000000 | 4.000000000 | 4.000000000 | Sneaked distance that triggers Stealth leveling
StealthSneakBaseXp | 1.000000000 | 1.000000000 | 1.000000000 | Base XP gain when sneaking
StealthSneakCheckRadius | 15.000000000 | 15.000000000 | 15.000000000 | NPC query radius when sneaking
StealthSneakXpSumCoefA | 5.000000000 | 5.000000000 | 5.000000000 | Combine XP from each NPC
StealthSneakXpSumCoefB | 4.000000000 | 4.000000000 | 4.000000000 | 
StealthToUnconsciousDepth | 250.000000000 | 250.000000000 | 250.000000000 | modifies the time victim is unconscious
StillAndHiddenHysteresis | 1.500000000 | 1.500000000 | 1.500000000 | switch the state after this timeout
StillBuffDuration | 600.000000000 | 600.000000000 | 600.000000000 | duration of standing still after which Still buff bonuses are activated (in worldtime seconds)
StolenGoodsForcedDiscount | 0.400000000 | 0.400000000 | 0.400000000 | price multiplier for when merchant detects that the sold items are stolen
StoryProgressXPLevelBase | 20.000000000 | 20.000000000 | 20.000000000 | 
StoryProgressXPLevelDiff | 30.000000000 | 30.000000000 | 30.000000000 | 
StrAgiToEqwArmorLoad | 1.000000000 | 1.000000000 | 1.000000000 | 
StrengthToInventoryCapacity | 4.000000000 | 4.000000000 | 4.000000000 | derives inventory capacity from Strength
StrengthXPLevelBase | 20.000000000 | 20.000000000 | 20.000000000 | 
StrengthXPLevelDiff | 30.000000000 | 30.000000000 | 30.000000000 | 
SuperFactionRepWeight | 1.000000000 | 1.000000000 | 1.000000000 | Weight of superfaction reputation (reputation median)
SuperWeaponDefense | 20.000000000 | 20.000000000 | 20.000000000 | like the best shield - mainly for AI, used to judge weapon
SurfaceToArmorLoadALWCoef | 1.000000000 | 1.000000000 | 1.000000000 | Coef alw from terrain/surface to armor load influence calculation
SurfaceToArmorLoadTWCoef | 0.150000000 | 0.150000000 | 0.150000000 | Coef tw from terrain/surface to armor load influence calculation
ThreatenStrenghtWeight | 0.500000000 | 0.500000000 | 0.500000000 | 0 - full weight to morale<br>1- full weight to strength
ThunderstormBuffRainIntensity | 0.300000000 | 0.300000000 | 0.300000000 | rain intensity threshold when Thunderstorm buff bonuses are activated
TreasureItemPricee | 1000.000000000 | 1000.000000000 | 1000.000000000 | starting price of treasure items
TrueRelationDistThresholdRel | 0.333333000 | 0.333333000 | 0.333333000 | distance, relative to observers maximum distance, required to see the true faction
UnarmedAttackBase | 2.000000000 | 2.000000000 | 2.000000000 | attack value for attack with relative stam cost = 1
UnarmedAttackReqStrBase | 2.000000000 | 2.000000000 | 2.000000000 | for attack with relative stam cost = 1
UnarmedBlockDefense | 3.000000000 | 3.000000000 | 3.000000000 | defense value for unarmed block
UnarmedHitArmorDamageCoef | nil | <font color="blue">0.250000000</font> | 0.250000000 | relative to armed combat
UnconsciousDepthFadeoutSpeedBase | 1.000000000 | 1.000000000 | 1.000000000 | how fast is the depth consumed
UnconsciousTimeWhenTimeIsNotRunning | 8.000000000 | 8.000000000 | 8.000000000 | if world time is not running, skiptime can not be started when player is unconscious; screen will only fade for this long instead; this is slightly modified by some rpg stats
VigourFull | 100.000000000 | 100.000000000 | 100.000000000 | Maximum vigour
VigourTickInterval | 2.000000000 | 2.000000000 | 2.000000000 | Vigour timer expiry
VisionToViewRadius | 2.000000000 | 2.000000000 | 2.000000000 | an increase of FOV caused by the hea stat
VitalityToUnconsciousDepthFadeoutSpeed | 1.000000000 | 1.000000000 | 1.000000000 | relative vitality
VitalityXPLevelBase | 20.000000000 | 20.000000000 | 20.000000000 | 
VitalityXPLevelDiff | 30.000000000 | 30.000000000 | 30.000000000 | 
WeakBlockStamCoef | 2.000000000 | 2.000000000 | 2.000000000 | 
WeaponDefenseToAttackingWeaponStatus | 0.010000000 | 0.010000000 | 0.010000000 | how opponent's defense value damages my weapon - hit to weapon/block
WeaponStatusToAttackCoef | 0.500000000 | 0.500000000 | 0.500000000 | weapon health to status multiplicative coef

