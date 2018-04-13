<!-- TITLE: RPG Parameters -->

[&larr; Kingdom Come](/kingdomcome)

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# RPG Parameters
**Data Quality Note:** The following descriptions were dumped directly from the game. The parameter names are correct, but the descriptions contain typos and misspellings. They will be cleaned up later.

## Legend

* <font color="green">Green</font>: The parameter value was increased.
* <font color="red">Red</font>: The parameter value was decreased.
* <font color="blue">Blue</font>: The parameter was added.
* <strike>Strikethrough</strike>: The parameter was removed, or the current value is empty and nonzero.

## Table: Changes at a Glance

Parameter | v1.1&ndash;1.2.5 | v1.3&ndash;1.3.4 | v1.4&ndash;1.4.2 | Description
:--- | ---: | ---: | ---: | :---
AlchemyXPPerAutocookBrewingRelative | nil | <font color="blue">0.1</font> | `0.1` | how many XP you get when you auto-cook a potion, relative to manual brewing
BlindViewRadiusFakeRelative | nil | <font color="blue">0.8</font> | `0.8` | for blinded (mostly sleeping) NPC we have to calculate stealth XP somehow, so we calculate this fake radius
<strike>CharismaMulOnExtremeExhaustionInterpolation</strike> | nil | nil | nil | Possibly the original name of the `CharismaMulOnExtremeExhaustion` parameter
ControllerLockPickingAppropriateTolerance | nil | <font color="blue">0.06</font> | <font color="red">0.045</font> | the lock is considered too hard to pick, if the tolerance is smaller than this
ControllerLockPickingToleranceACoef | nil | <font color="blue">0.45</font> | `0.45` | 
ControllerLockPickingToleranceKCoef | nil | <font color="blue">0.03</font> | <font color="green">0.07</font> | 
ControllerLockPickingToleranceMCoef | nil | <font color="blue">0.687</font> | `0.687` | 
ControllerLockPickingToleranceNCoef | nil | <font color="blue">0.355</font> | <font color="green">0.48</font> | 
DamageToArmorStatus | nil | <font color="blue">1.0 | `1.0` | for the stopping layer
DamageToArmorStatusHigherLayers | nil | <font color="blue">2.0</font> | `2.0` | for layers above the stopping layer
DamageToArmorStatusLowerLayers | nil | <font color="blue">0.5</font> | `0.5` | for layers below the stopping layer
<strike>ImprovedSleepMultiplierSurvival</strike> | nil | nil | nil | Possibly the original name of the `ImprovedSleepMultiplier` parameter
<strike>InactiveTimeToDestroyOversleepCreated</strike> | nil | nil | nil | Possibly the original name of the `InactiveTimeToDestroyOversleep` parameter
LockPickingAdequateTolerance | nil | nil | <font color="blue">0.17</font> | locks on a similar level as the player have adequate tolerance
MaxStatToAttackMult | `1.2` | <font color="red">1.1</font> | `1.1` | Maximal relative attack multiplier (for a high stat)
MaxStealthHitSoundMultiplier | `0.4` | <font color="red">0.22</font> | `0.22` | intensity multiplier for max stealth level
MinStealthHitSoundMultiplier | `0.1` | <font color="red">0.06</font> | `0.06` | Intensity multiplier for minimum Stealth level
PickpocketingDistance | nil | <font color="blue">2.0</font> | `2.0` | Max pickpocketing range (not starting interactor range)
PickpocketingIndicatorSharpness | `0.2` | <font color="red">0.0</font> | `0.0` | 0 - precise slow change<br>1 - sharp change
PickpocketingMisstargetingTolerance | nil | <font color="blue">2000.0</font> | `2000.0` | Time tolerance for temporarily mistargeting your victim
PickpocketingRandomChanceRollMinCap | nil | <font color="blue">0.1</font> | `0.1` | Worst random rolls will always be capped to this minimum chance
QuestMoneyRewardScaleConstant | `1.25` | <font color="red">1.2</font> | `1.2` | scale constnat for quest reward item amount
<strike>ReadingRestEffectiveness</strike> | `0.3` | nil | nil | If this value is 0.3, reading will regen player as sleeping on bed with comfort 30%.
<strike>ReadingRestUpperLimit</strike> | `1.0` | nil | nil | When sleeping, the rest can not exceed bed quality. When reading, the threshold is given by this value.
SkillToDmgConstA | `70.0` | <font color="green">250.0</font> | `250.0` | 
StarvationHealthLossSpeed | `0.057874` | <font color="green">0.01</font> | `0.01` | by design the same speed as the digestion
StarvationPlayerEffectMaxMax | `60.0` | 60.0 | <font color="green">75.0</font> | longest interval between effects for high hunger stat
StarvationPlayerEffectMaxMin | `90.0` | 90.0 | <font color="green">120.0</font> | longest interval between effects for low hunger stat
StarvationPlayerEffectMinMax | `30.0` | 30.0 | <font color="green">45.0</font> | shortest interval between effects for high hunger stat
StarvationPlayerEffectMinMin | `60.0` | 60.0 | <font color="green">90.0</font> | shortest interval between effects for low hunger stat
UnarmedHitArmorDamageCoef | nil | <font color="blue">0.25</font> | `0.25` | relative to armed combat


## Table: All Parameters

Parameter | v1.1&ndash;1.2.5 | v1.3&ndash;1.3.4 | v1.4&ndash;1.4.2 | Description
:--- | ---: | ---: | ---: | :---
AdditionalAttackerCountForMaxFadingBuff | `2.0` | 2.0 | `2.0` | For AdditionalAttackerCountFading buff
AgiDiffToAttackSpeed | `0.2` | 0.2 | `0.2` | Relative attack speed gain for one Agility level difference
AgilityXPLevelBase | `20.0` | 20.0 | `20.0` | 
AgilityXPLevelDiff | `30.0` | 30.0 | `30.0` | 
AimCiriticalLimitTime | `0.75` | 0.75 | `0.75` | Time limit after AI is notified about low Stamina when aiming
AimPainlessDelay | `2.0` | 2.0 | `2.0` | Aiming without Stamina loss
AimSkillToZoom | `1.5` | 1.5 | `1.5` | Zoom increase by each skill level above the base
AimSpreadMax | `15.0` | 15.0 | `15.0` | Aiming spread due to low Stamina and skill. Max angle. Used right before all Stamina is lost.
AimSpreadMinRatio | `0.3` | 0.3 | `0.3` | Aiming spread minimum, relative to max. This value is used after entering the painless zone.
AimSpreadSkillDecrease | `0.05` | 0.05 | `0.05` | Relative decrease of maximum aim spread for each skill level
AimStamCost | `20.0` | 20.0 | `20.0` | Stamina loss after after painless delay
AimZoomBase | `10.0` | 10.0 | `10.0` | aim zoom (=fov decrease) after reaching some skill level
AimZoomBaseSkill | `10.0` | 10.0 | `10.0` | Minimal skill level required to benefit from the zoom effect
AimZoomMax | `25.0` | 25.0 | `25.0` | maximal aim zoom (=fov decrease)
AlchemyRecipeStepsTolerance | `2.0` | 2.0 | `2.0` | How many recipe steps might fail in order to successfully brew the recipe
AlchemyToleranceBase | `0.5` | 0.5 | `0.5` | Base brewing tolerance at level 1
AlchemyTolerancePerLevel | `0.15` | 0.15 | `0.15` | Brewing tolerance gain per level
AlchemyTrialEndErrorPerkTolerance | `1.0` | 1.0 | `1.0` | Additional tolerance gained with Trial and Error perk
AlchemyXPPerAutocookBrewingRelative | nil | <font color="blue">0.1</font> | `0.1` | how many XP you get when you auto-cook a potion, relative to manual brewing
AlchemyXPPerSuccessfullBrewing | `40.0` | 40.0 | `40.0` | Alchemy XP gained when a potion is successfully brewed
AlcoholBaseHangoverDuration | `14400.0` | 14400.0 | `14400.0` | Base max duration for hangover (after blackout) in world time
AlcoholBlackoutDuration | `14400.0` | 14400.0 | `14400.0` | Blackout unconscious duration
AlcoholContentFPAntidoteThreshold | `60.0` | 60.0 | `60.0` | Food with alcohol content above this threshold counters food poisoning
AlcoholDigestSpeedModfifOnEmptyStomache | `2.0` | 2.0 | `2.0` | Alcohol digest speed multiplier on empty stomache
AlcoholDigestSpeedModfifOnFullStomache | `0.5` | 0.5 | `0.5` | Alcohol digest speed multiplieron full stomache
AlcoholDrunkMaxExhaustNegativeEffect | `0.05` | 0.05 | `0.05` | Max negative exhaustion effect while drunk
AlcoholDrunkThreshold | `0.5` | 0.5 | `0.5` | Threshold for Drunkenness mood from max alcohol poisoning
AlcoholHangoverOffsetModif | `1.1` | 1.1 | `1.1` | Starting hangover negative effects are modified by this offset
AlcoholismDuration | `500000.0` | 500000.0 | `500000.0` | Alcoholism duration in world time
AlcoholismMaxSkillLevelThreshold | `1000.0` | 1000.0 | `1000.0` | Temporary alcoholism threshold with max drinking skill
AlcoholismRemoveSpeed | `0.01` | 0.01 | `0.01` | Alcoholism removed per world time second (default: 100 every 4 days)
AlcoholismThreshold | `700.0` | 700.0 | `700.0` | Amount of alcohol that will cause temporary alcoholism
AlcoholismTickInterval | `1.0` | 1.0 | `1.0` | Alcoholism timer expiry
AlcoholMaxAGIEffect | `2.0` | 2.0 | `2.0` | Max negative/positive stat effect
AlcoholMaxCHAEffect | `2.0` | 2.0 | `2.0` | Max negative/positive stat effect
AlcoholMaxCONEffect | `3.0` | 3.0 | `3.0` | Max negative/positive stat effect
AlcoholMaxDrinkingSkillHangoverDurationModifier | `0.333333` | 0.333333 | `0.333333` | Hangover duration modifier for max Drinking skill
AlcoholMaxSPCEffect | `2.0` | 2.0 | `2.0` | Max negative/positive stat effect
AlcoholMaxSTREffect | `2.0` | 2.0 | `2.0` | Max negative/positive stat effect
AlcoholMaxVITEffect | `2.0` | 2.0 | `2.0` | Max negative/positive stat effect
AlcoholMoodMaxExhaustPossitiveEffect | `0.02` | 0.02 | `0.02` | max positive exhaust effect while in mood
AlcoholMoodThreshold | `0.01` | 0.01 | `0.01` | threshold for alcohol mood from max alcohol poisoning
AlcoholPerkBacchusHangoverEffectMod | `1.3` | 1.3 | `1.3` | hangover effects mod
AlcoholPerkCorrectResistanceModif | `0.5` | 0.5 | `0.5` | alcohol content modif for correct resistance
AlcoholPerkDrunkHangoverDurationMod | `2.0` | 2.0 | `2.0` | 
AlcoholPerkDrunkMoodRangeMod | `2.0` | 2.0 | `2.0` | mood range is expanded by this mod
AlcoholPerkLooseTongueSpcChaModif | `1.5` | 1.5 | `1.5` | speech and charisma modif bonus/malus for loose tongue perk
AlcoholPerkTrueSlavHangoverDurationMod | `0.5` | 0.5 | `0.5` | hangover duration mod
AlcoholPerkTrueSlavMaxAlcoholMod | `0.5` | 0.5 | `0.5` | max amount of alcohol is divided by this mod
AlcoholPerkWrongResistanceModif | `2.0` | 2.0 | `2.0` | alcohol content modif for wrong resistance
ArmorDefenseToAttackingWeaponStatus | `0.02` | 0.02 | `0.02` | how opponent's defense value damages my weapon - hit to armor
ArmorDirtToCharismaCoef | `1.0` | 1.0 | `1.0` | 
ArmorLoadDiffToMax | `10.0` | 10.0 | `10.0` | 
ArmorLoadToJumpCost | `2.0` | 2.0 | `2.0` | how armor load coefficient affects the stamina jump cost (times base)
ArmorLoadToRun | `0.5` | 0.5 | `0.5` | how armor load coefficient affects running speed
ArmorLoadToSprint | `1.0` | 1.0 | `1.0` | how armor load coefficient affects sprint
ArmorStatusToCharismaCoef | `0.67` | 0.67 | `0.67` | 
ArmorStatusToDefenseCoef | `0.67` | 0.67 | `0.67` | health to armor defense multiplicative coef
AthleticXPAwardDistance | `500.0` | 500.0 | `500.0` | award xp for travelling some distance
AttackEnergyModifier | `2.0` | 2.0 | `2.0` | utoku
AttackRequiredStamRatio | `0.0` | 0.0 | `0.0` | actual/cost stamina ratio must be > than this value for attack to be allowed
AttackSpeedNormal | `0.5` | 0.5 | `0.5` | normal attack speed, 0-min, 1-max
AttackSpeedNormalAgi | `5.0` | 5.0 | `5.0` | agility required for the normal attack speed
AttackSpeedPlayerRelative | `1.0` | 1.0 | `1.0` | 0 - using opponent's skill<br>1 - attack speed is always calculated using the player
AttackStamModMin | `0.5` | 0.5 | `0.5` | attack strength/power stamina modifier minimum (0stam->Xattack)
AttSkillToHorsePullDown | `0.5` | 0.5 | `0.5` | relative attacker skill to horse pull down
AttStrengthToHorsePullDown | `0.5` | 0.5 | `0.5` | relative attacker stat to horse pull down
AverageArmorDefenseWeight | `0.5` | 0.5 | `0.5` | 0 = only body part defense, 1 = only average defense
AvidReaderReadingSpeed | `0.35` | 0.35 | `0.35` | AvidReader soul ability advances reading progress on one book in inventory during sleep or skiptime. This constant determines speed of reading (reading spot is always None).
BadassnessDiffToSkillCheckResult | `2.0` | 2.0 | `2.0` | 
BarterAngrynessCoefWeightA | `1.0` | 1.0 | `1.0` | 
BarterAngrynessCoefWeightB | `0.7` | 0.7 | `0.7` | 
BarterCoefWeightA | `0.875` | 0.875 | `0.875` | shopkeeper shop barter calculation 'a' coef
BarterCoefWeightB | `80.0` | 80.0 | `80.0` | shopkeeper shop barter calculation 'b' coef
BarterDominanceChaBaseE | `5.0` | 5.0 | `5.0` | barter dominance calculation 'e' coef
BarterDominanceChaWeightC | `0.1` | 0.1 | `0.1` | barter dominance calculation 'c' coef
BarterDominanceRelationshipWeightB | `1.0` | 1.0 | `1.0` | barter dominance calculation 'b' coef
BarterDominanceSpcWeightA | `3.0` | 3.0 | `3.0` | barter dominance calculation 'a' coef
BarterDominanceSpcWeightD | `10.0` | 10.0 | `10.0` | barter dominance calculation 'd' coef
BarterPriceSellRepBuying | `1.5` | 1.5 | `1.5` | price sell vs buy mod
BarterPriceSellRepCoef | `1.5` | 1.5 | `1.5` | sell reputation coef
BarterPriceSellRepMultip | -0.5 | -0.5 | -0.5 | sell reputation multiplier
BaseAttackStaminaCost | `12.0` | 12.0 | `12.0` | how much stamina will attack cost
BaseInventoryCapacity | `66.0` | 66.0 | `66.0` | base inventory capacity
BaseItemDisappearingTime | `3600.0` | 3600.0 | `3600.0` | base game time for dropped items to auto disappear
BasketSuspiciencyNoDealThreashold | `10000000.0` | 10000000.0 | `10000000.0` | Haggle reaction 2 threshold (transaction refused)
BasketSuspiciencyThreashold | `0.1` | 0.1 | `0.1` | Haggle reaction 1 threshold (haggle more difficult)
BestVisVolume | `10000.0` | 10000.0 | `10000.0` | object volume for maximum recognition bonus
BigZoneDistanceSlotMod | `0.8` | 0.8 | `0.8` | temporary solution, slot mod for distance > 1
BlindViewRadiusFakeRelative | nil | <font color="blue">0.8</font> | `0.8` | for blinded (mostly sleeping) NPC we have to calculate stealth XP somehow, so we calculate this fake radius
BowChargeDurationMax | `3.0` | 3.0 | `3.0` | maximum duration of bow charge animation
BowChargeDurationMin | `1.35` | 1.35 | `1.35` | minimum duration of bow charge animation
BowPowerToChargeDuration | `0.1` | 0.1 | `0.1` | nominal charge duration for bow with power = 1
BundleAlchemistPerkAdd | `1.0` | 1.0 | `1.0` | Addition of potions created with Bundle Alchemist perk
CaffeineFromFoodCoef | `2.0` | 2.0 | `2.0` | how much caffeine is added from a unit refresh
CaffeineFullThreshold | `0.9` | 0.9 | `0.9` | you cannot use more refreshing items if above this value
CarriedBodyMaxStamConsumption | `10.0` | 10.0 | `10.0` | uses encumberance to interpolate from 0 to this
CarriedBodyWeightCoef | `0.25` | 0.25 | `0.25` | how much of the carried body weight is added to the carried weight of the carrier
CarriedCarriedWeightCoef | `0.5` | 0.5 | `0.5` | how much of the carried weight of the carried NPC is added to the carried weight of the carrier
CharismaDiffToSkillCheckResult | `0.3` | 0.3 | `0.3` | > 0; scaled charisma diff for result = -1/1
CharismaMulOnExtremeExhaustion | `0.75` | 0.75 | `0.75` | Player will have this charisma multiplied by this value when he has exhaust equal to 0. Charisma will not be changed when exhaust is 50. Linear interpolation on multiplier is applied when exhaust is between 0 and 50;
<strike>CharismaMulOnExtremeExhaustionInterpolation</strike> | nil | nil | nil | Possibly the original name of the `CharismaMulOnExtremeExhaustion` parameter
ClassCourageMoraleWeight | `0.0` | 0.0 | `0.0` | Weight of soul class courage affecting morale
ClothDirtyingUpdatePeriod | `50.0` | 50.0 | `50.0` | how often (in meters walked) do we add dirt to clothing (both for player and NPCs)
CollisionVelocityDeltaToDmgR | `0.25` | 0.25 | `0.25` | 
CombatAutoAggressionDiffScale | `2.0` | 2.0 | `2.0` | the bigger number the bigger difference in aggresion for skill differnce
CombatAutoAttackDelayIncreasePerAttacker | `0.8` | 0.8 | `0.8` | how many times is the period increased for each attacker
CombatAutoAttackDelayIncreasePerAttackerHorse | `0.1` | 0.1 | `0.1` | CombatAutoAttackDelayIncreasePerAttacker if the victim is on horse
CombatAutoAttackDelayIncreasePerAttackerMissile | `0.2` | 0.2 | `0.2` | CombatAutoAttackDelayIncreasePerAttacker if the victim has a missile wpn
CombatAutoAttackDelaySigma | `4.0` | 4.0 | `4.0` | attack delay variation
CombatAutoClinchReactionDelayMaxMax | `1.0` | 1.0 | `1.0` | maximal maximum
CombatAutoClinchReactionDelayMaxMin | `0.5` | 0.5 | `0.5` | maximal minimum
CombatAutoClinchReactionDelayMinMax | -0.5 | -0.5 | -0.5 | minimal maximum
CombatAutoClinchReactionDelayMinMin | -1.0 | -1.0 | -1.0 | minimal minimum
CombatAutoComboStepsSigma | `1.5` | 1.5 | `1.5` | standard deviation of performed combo steps
CombatAutoDodgeWeight | `1.1` | 1.1 | `1.1` | 
CombatAutoEasyZoneWeight | `0.8` | 0.8 | `0.8` | [0-1] how much are easy zones favored by the lame AI (1 = favored)
CombatAutoForcedComboStaminaLimit | `0.7` | 0.7 | `0.7` | stamina threshold
CombatAutoForcedPeriodicalAttackStaminaLimit | `0.2` | 0.2 | `0.2` | stamina threshold
CombatAutoGuardHysteresis | `1.5` | 1.5 | `1.5` | 
CombatAutoLameGuardOffset | `3.0` | 3.0 | `3.0` | offset to max distance
CombatAutoMasterComboSteps | `5.0` | 5.0 | `5.0` | combo steps a skilled npc will typically perform
CombatAutoMasterGuardOffset | `1.0` | 1.0 | `1.0` | offset to max distance
CombatAutoMaxAimDuration | `3.0` | 3.0 | `3.0` | the longest aim time for the lowest skill
CombatAutoMaxAimDurationRandomAdd | `1.0` | 1.0 | `1.0` | max random time added to the aim duration
CombatAutoMaxAtkDistOffset | `0.1` | 0.1 | `0.1` | offset from max attack distance defined in percentage from attack range
CombatAutoMaxAttackDelay | `6.0` | 6.0 | `6.0` | mean delay between attacks for a defensive AI
CombatAutoMaxHuntAttackDuration | `60.0` | 60.0 | `60.0` | maximal time the NPC is hunting/chasing
CombatAutoMinAtkDistOffset | `0.0` | 0.0 | `0.0` | offset from min attack distance defined in percentage from attack range
CombatAutoMinDefenseModeWeight | `0.4` | 0.4 | `0.4` | [0-1] the lowest weight for the defense mode
CombatAutoMinHuntAttackDuration | `15.0` | 15.0 | `15.0` | minimal time the NPC is hunting/chasing
CombatAutoMoveActivityDecreasePerAttacker | `0.5` | 0.5 | `0.5` | my activity decrease per opponents aditinal attackers
CombatAutoNaturalComboRatio | `0.5` | 0.5 | `0.5` | [0-1] ratio of natural combos
CombatAutoNoDefenseWeight | `0.4` | 0.4 | `0.4` | 
CombatAutoNormalBWeight | `2.8` | 2.8 | `2.8` | 
CombatAutoOppZoneAdaptDelayMaxMax | `2.0` | 2.0 | `2.0` | reaction delay maximal maximum
CombatAutoOppZoneAdaptDelayMaxMin | `1.0` | 1.0 | `1.0` | reaction delay maximal minimum
CombatAutoOppZoneAdaptDelayMinMax | `0.2` | 0.2 | `0.2` | reaction delay minimal maximum
CombatAutoOppZoneAdaptDelayMinMin | `0.0` | 0.0 | `0.0` | reaction delay minimal minimum
CombatAutoPBWeight | `2.5` | 2.5 | `2.5` | 
CombatAutoReactionDelayRangeSpread | `0.3` | 0.3 | `0.3` | [0-1] higher nunber -> changes state less often
CombatAutoReactivePreblockMaxDelay | `0.8` | 0.8 | `0.8` | 
CombatAutoReactivePreblockMinDelay | `0.3` | 0.3 | `0.3` | 
CombatAutoRiposteAggressionWeight | `0.5` | 0.5 | `0.5` | 
CombatAutoScaleDefensivenessDelayRel | `2.0` | 2.0 | `2.0` | relative to attack delay, time to override defensiveness and go near
CombatAutoSPBWeight | `1.5` | 1.5 | `1.5` | 
CombatAutoStaticPreblockMaxTime | `15.0` | 15.0 | `15.0` | 
CombatAutoStaticPreblockRandBias | `0.8` | 0.8 | `0.8` | 
CombatAutoTrickAttackProb | `0.8` | 0.8 | `0.8` | [0-1] attack prob for the first step
CombatAutoTrickDelayVariability | `0.3` | 0.3 | `0.3` | added to the lower bound
CombatAutoTrickInvalidBlockAttackMaxProb | `0.5` | 0.5 | `0.5` | [0-1] max trick prob for a skilled AI if the block is invalid
CombatAutoTrickMaxProb | `0.5` | 0.5 | `0.5` | [0-1] max trick prob for the first step
CombatAutoTrickMinMaxDelay | `0.8` | 0.8 | `0.8` | lower bound of the max delay
CombatAutoTrickNoAttackProb | `0.1` | 0.1 | `0.1` | [0-1] no attack prob for the first step
CombatAutoTrickReactionMaxDelay | `8.0` | 8.0 | `8.0` | 
CombatAutoTrickReactionMinDelay | `0.1` | 0.1 | `0.1` | 
CombatAutoTrickReactionSkillWeight | `4.0` | 4.0 | `4.0` | 
CombatAutoTrickReactionStaWeight | `1.0` | 1.0 | `1.0` | 0 - use just stamina<br>1 - use just aggression
CombatAutoUnarmedBlockProb | `1.6` | 1.6 | `1.6` | 
CombatAutoWpnHealthBlockMax | `20.0` | 20.0 | `20.0` | 
CombatAutoWpnHealthMinBlockProb | `0.8` | 0.8 | `0.8` | 
CombatAutoZoneChangeDelayMaxMax | `10.0` | 10.0 | `10.0` | zone change timeout maximal maximum
CombatAutoZoneChangeDelayMaxMin | `5.0` | 5.0 | `5.0` | zone change timeout maximal minimum
CombatAutoZoneChangeDelayMinMax | `6.0` | 6.0 | `6.0` | zone change timeout minimal maximum
CombatAutoZoneChangeDelayMinMin | `2.0` | 2.0 | `2.0` | zone change timeout minimal minimum
CombatDangerCooldown | `3.0` | 3.0 | `3.0` | how long is the combat danger active after last enemy stops to be a threat
CombatDmgRBonusFromBehind | `1.2` | 1.2 | `1.2` | multiplicative DmgR bohus for attacks from behind
CombatHitImmortalUnconsciousDepth | `120.0` | 120.0 | `120.0` | depth for immortal knock-out
CombatHitUnconsciousDepth | `60.0` | 60.0 | `60.0` | depth after a combat hit
CombatMoveApproachHysteresis | `1.5` | 1.5 | `1.5` | 
CombatMoveApproachSprintMinStamina | `1.0` | 1.0 | `1.0` | do not allow sprint during the approach
ControllerLockPickingAppropriateTolerance | nil | <font color="blue">0.06</font> | <font color="red">0.045</font> | the lock is considered too hard to pick, if the tolerance is smaller than this
ControllerLockPickingToleranceACoef | nil | <font color="blue">0.45</font> | `0.45` | 
ControllerLockPickingToleranceKCoef | nil | <font color="blue">0.03</font> | <font color="green">0.07</font> | 
ControllerLockPickingToleranceMCoef | nil | <font color="blue">0.687</font> | `0.687` | 
ControllerLockPickingToleranceNCoef | nil | <font color="blue">0.355</font> | <font color="green">0.48</font> | 
CorpseDisappearanceTimeDiscovered | `5.0` | 5.0 | `5.0` | time before a NPC corpse is hidden when discovered
CorpseDisappearanceTimeUndiscovered | `25.0` | 25.0 | `25.0` | time before a NPC corpse is hidden when undiscovered
CorpseDisapperanceMinDistanceFromPlayer | `100.0` | 100.0 | `100.0` | distance from player below which a corpse will never disappear
DamageToArmorStatus | nil | <font color="blue">1.0 | `1.0` | for the stopping layer
DamageToArmorStatusHigherLayers | nil | <font color="blue">2.0</font> | `2.0` | for layers above the stopping layer
DamageToArmorStatusLowerLayers | nil | <font color="blue">0.5</font> | `0.5` | for layers below the stopping layer
DawnTime | `4.5` | 4.5 | `4.5` | Time when night ends, used by rpg (default 04:30)
DefaultReadingQuality | `0.5` | 0.5 | `0.5` | Reading quality when doing nothing special (standing).
DefaultRelationship | `0.5` | 0.5 | `0.5` | default value for the alied forces
DefaultStateDeltaSpeed | `1.0` | 1.0 | `1.0` | any soul state regen / losing speed
DefaultVisVolume | `0.03` | 0.03 | `0.03` | default item size-volume that have no visibility recognition penalty
DefaultWorldTimeRatio | `15.0` | 15.0 | `15.0` | default world time ratio useed to calculate game time ration in superspeed skiptime
DigestionSpeed | `0.057874` | 0.057874 | `0.057874` | amount of food 'lost' per world-time second (global base value)
DistanceCheckInterval | `1.0` | 1.0 | `1.0` | check distance travelled for statistics
DmgRToHealthCoefA | `3.0` | 3.0 | `3.0` | 
DmgRToHealthCoefB | `1.6` | 1.6 | `1.6` | 
DuringFaderHysteresis | `1.0` | 1.0 | `1.0` | the in-fader state is kept for how longer
DuskTime | `21.5` | 21.5 | `21.5` | Time when night begins, used by rpg (default 21:30)
EncumberanceForSecondaryModifiers | `0.5` | 0.5 | `0.5` | when the buff will activate the secondary group
EncumberedToSpeedSurfaceCoef | `0.3` | 0.3 | `0.3` | Coef that controls terrain/surface influence in encumbered speed mod
EquippedWeightSubWithWellWornPerk | `0.333333` | 0.333333 | `0.333333` | when player has Well Worn perk, weight of items is lowered when they are equipped
ExhaustedPlayerEffectMaxMax | `60.0` | 60.0 | `60.0` | the longest interval between effects for high exhaust stat
ExhaustedPlayerEffectMaxMin | `30.0` | 30.0 | `30.0` | the longest interval between effects for low exhaust stat
ExhaustedPlayerEffectMinMax | `30.0` | 30.0 | `30.0` | the shortest interval between effects for high exhaust stat
ExhaustedPlayerEffectMinMin | `10.0` | 10.0 | `10.0` | the shortest interval between effects for low exhaust stat
ExhaustedThreshold | `50.0` | 50.0 | `50.0` | player will have the 'exhausted' debuff when 'exhaust' stat is lower or equal to this value (in percents)
ExhaustionSpeed | `0.057874` | 0.057874 | `0.057874` | amount of energy/vigour 'lost' per world-time second (global base value)
ExtremeExhaustionFaintAveragePeriod | `300.0` | 300.0 | `300.0` | How often (on average, in real time) should player faint when extremely exhausted (exhaust stat is on 0).
FactionAngrinessDecayBase | `2.0` | 2.0 | `2.0` | Faction angriness decay speed base, whatever it is.
FactionAngrinessDecayExp | `2.0` | 2.0 | `2.0` | Faction angriness decay speed exponent.
FactionAngrinessDecayMod | `0.02` | 0.02 | `0.02` | Faction angriness decay speed mod, whatever it is.
FactionAngrinessDecayShift | `0.25` | 0.25 | `0.25` | Faction angriness decay speed shift.
FactionAngrinessPropagationCoef | `1987.0` | 1987.0 | `1987.0` | Faction angriness is propagated through space between factions.
FactionAngrinessPropagationScale | `0.1` | 0.1 | `0.1` | Faction angriness propagation distance scale.
FactionRepWeight | `3.0` | 3.0 | `3.0` | Weight of player - faction reputation (reputation median)
FallDamageMultiplierAtMaxAgility | `0.666667` | 0.666667 | `0.666667` | fall damage multiplier when agility is maxed out
FatalFallHeight | `8.0` | 8.0 | `8.0` | falling height above which fatal health damage is taken at agility 0
FatCollisionWeightMul | `1.4` | 1.4 | `1.4` | multiplies the archetype body weight if the character is fat
FoodFull | `100.0` | 100.0 | `100.0` | you are full
FoodHealSpeed | `2.0` | 2.0 | `2.0` | hp regen speed
FoodHealthThreshold | `0.5` | 0.5 | `0.5` | Health threshold for possitive/negative food effect
FoodOverEat | `120.0` | 120.0 | `120.0` | you cannot eat more
FoodPoisoningMaxHealthEffectSpeed | `0.5` | 0.5 | `0.5` | Maximum loss of health/s for food poisoning
FoodPoisoningMaxStatPenalty | `10.0` | 10.0 | `10.0` | maximum temporary penalty for affected stats while food poisoning
FoodPoisoningMaxValue | `100.0` | 100.0 | `100.0` | Max amount of food poisoning
FoodPoisoningMinHealthEffectSpeed | `0.1` | 0.1 | `0.1` | minimum loss of health/s for food poisoning
FoodPoisoningThreshold | `0.05` | 0.05 | `0.05` | threshold for food posioning to start taking affecting
FoodPreserverHealthIncreaseAmount | `0.5` | 0.5 | `0.5` | this amount is added to food's health when food preserver is applied
FoodSaltOrSmokePerkDecayModif | `0.75` | 0.75 | `0.75` | food decay perk modifier
FoodTickInterval | `2.0` | 2.0 | `2.0` | food timer expiry
FoodWitcherPerkNutritionModif | `0.7` | 0.7 | `0.7` | potion nutrition wicher perk modifier
ForcedFireAimSpreadMalus | `7.0` | 7.0 | `7.0` | spread added when the rpg forces the firing on low stamina
FromBehindAngle | `2.35619` | 2.35619 | `2.35619` | minimal angle to classify the attack as 'from behind' - 0 face, PI back
FullClothDirtyingOnFullSpeed | `4000.0` | 4000.0 | `4000.0` | how far do we walk with full speed (1.0 walk speed) to get 100% dirty
FullClothDirtyingOnZeroSpeed | `1.0` | 1.0 | `1.0` | how far do we walk with half speed to get 100% dirty (other speeds than FullSpeed and HalfSpeed are linearly interpolated)
GoodArmorDefense | `2.0` | 2.0 | `2.0` | mainly for AI, used to judge armor
GoodWeaponAttack | `3.5` | 3.5 | `3.5` | mainly for AI, used to judge weapon
GoodWeaponDefense | `4.5` | 4.5 | `4.5` | 
HarmlessFallHeight | `1.0` | 1.0 | `1.0` | falling height below which no health or stamina damage is taken at agility 0
HeadHitKnockOutBaseProbability | `0.0` | 0.0 | `0.0` | for hits dealing a hp damage
HealthDamageToInjury | `0.02` | 0.02 | `0.02` | note: health is [0-100] but injury is [0-1]
HealthDeltaAbsLimit | `1000.0` | 1000.0 | `1000.0` | abs max of health delta
HealthFadingFromLimitValue | `0.75` | 0.75 | `0.75` | health percentage to activate health fading buff
HealthFull | `100.0` | 100.0 | `100.0` | maximum health
HealthToKnockOut | `0.0` | 0.0 | `0.0` | threshold for unarmed combat, health cannot reach this level
HealthToMoraleMinCoef | `0.2` | 0.2 | `0.2` | multiplicative coef for health = 0
HearingToFov | `3.0` | 3.0 | `3.0` | 
HeavyWeaponWeight | `4.0` | 4.0 | `4.0` | used to deduce 'attack weight'
HerbGatherSkillToCount | `0.3` | 0.3 | `0.3` | multiplied by sqrt(skill level) to modify the number of collected herbs
HerbGatherSkillToRadius | `0.25` | 0.25 | `0.25` | multiplied by skill level to calculate radius
HerbGatherXP | `7.0` | 7.0 | `7.0` | final XP reward for one herb gathering
HerbsInHorseInventoryForHorsenipPerk | `30.0` | 30.0 | `30.0` | number of herbs in horse inventory needed for Horsenip perk to be active
HerbsInInventoryForFlowerPowerPerk | `30.0` | 30.0 | `30.0` | number of herbs in inventory needed for Flower Power perk to be active
HighbornWealthThreshold | `10.0` | 10.0 | `10.0` | social class wealth threshold for perks
HorseAttackMaxSpeed | `7.0` | 7.0 | `7.0` | speed of the attacking rider to gain maximal attack bonus
HorseMaxAttackCoef | `2.5` | 2.5 | `2.5` | [1,inf] maximal multiplicative coefficient a rider will gain when attacking on HorseMaxAttackSpeed
HorseMoraleToThrowOffRider | `0.2` | 0.2 | `0.2` | if the horse morale is below this, it throws off the rider
HorseRidingAwardDistance | `500.0` | 500.0 | `500.0` | Horsemanship XP for travelling some distance on horse
HorseRidingToHorseCourage | `0.05` | 0.05 | `0.05` | how the rider's horse riding skill increases courage of his horse
HorseRidingToHorseStamina | `0.02` | 0.02 | `0.02` | how the rider's horse riding skill lowers sta consumption of his horse
HorseRidingXPPerDistance | `12.5` | 12.5 | `12.5` | horse riding xp gain after riding HorseRidingAwardDistance
HourglassTimeout | `10.0` | 10.0 | `10.0` | the time until all the sand goes down
HunterLootAmountAddCoef | `0.3` | 0.3 | `0.3` | add coef, the fixed portion
HunterXPKill | `15.0` | 15.0 | `15.0` | Hunting XP gain after a kill, multiplied by the game db coef and level
HunterXPLoot | `10.0` | 10.0 | `10.0` | Hunting XP gain after a loot, multiplied by the game db coef and level
ImmortalHealthMin | `1.0` | 1.0 | `1.0` | Minimum health for immortal souls
ImprovedSleepMultiplier | `2.0` | 2.0 | `2.0` | How much better better (Rest regeneration speed) is SleepImproved than Sleep buff. This buff is used for reading when player has perk InTheFlow.
<strike>ImprovedSleepMultiplierSurvival</strike> | nil | nil | nil | Possibly the original name of the `ImprovedSleepMultiplier` parameter
InactiveTimeToDestroyOversleep | `8.0` | 8.0 | `8.0` | how long to let inactive oversleep buff survive (in game seconds) (we have this threshold so that the buff will not be destroyed right after being created in SkipTime class)
<strike>InactiveTimeToDestroyOversleepCreated</strike> | nil | nil | nil | Possibly the original name of the `InactiveTimeToDestroyOversleep` parameter
InjuringFallHeight | `2.5` | 2.5 | `2.5` | falling height above which health damage is taken at agility 0
InjuryBleedingInterval | `6.0` | 6.0 | `6.0` | bleeding interval, the time required to lose 1HP
InjuryHighThreshold | `0.8` | 0.8 | `0.8` | limb is bleeding if above this threshold
InjuryLowThreshold | `0.2` | 0.2 | `0.2` | limb is considered healthy if below this treshold
InjuryRegenInterval | `10.0` | 10.0 | `10.0` | injuries fade-out, the time required to regen 1% of injury
ItemDisappearingMulti | `3.0` | 3.0 | `3.0` | multiplier 1/x - x limit(up/down) for item disappearing speed in extremes (cheap vs. expensive, small vs. large)
ItemHealthPriceStatusWeight | `0.8` | 0.8 | `0.8` | item health status weight price coef
ItemOwnerDescFadeToSuspiciencyExp | `0.25` | 0.25 | `0.25` | 
ItemOwnerFactionDistanceCoef1 | `500.0` | 500.0 | `500.0` | 
ItemOwnerFactionDistanceCoef2 | `300.0` | 300.0 | `300.0` | 
ItemOwnerFactionDistanceToSuspiciencyMax | `1.0` | 1.0 | `1.0` | 
ItemOwnerFactionDistanceToSuspiciencyMin | `0.25` | 0.25 | `0.25` | 
ItemOwnerFadeCoefToSuspiciencyExp | `3.0` | 3.0 | `3.0` | 
ItemOwnerFadeCoefToSuspiciencyMul | `2.0` | 2.0 | `2.0` | 
ItemOwnerFadeConspicuousnessToHours | `10.0` | 10.0 | `10.0` | world time hours
ItemOwnerFadePriceToHours | `1.0` | 1.0 | `1.0` | world time hours per decigrosh
ItemOwnerIsShopkeeperToSuspiciency | `8.0` | 8.0 | `8.0` | basket suspiciency calculation
ItemOwnerNeverFadesToSuspiciency | `10.0` | 10.0 | `10.0` | 
ItemOwnerRelationshipToSuspiciencyMin | `0.1` | 0.1 | `0.1` | 
JailRecoveryDebuffDurationMultiplier | `0.2` | 0.2 | `0.2` | duration of JailRecovery debuff is calculated as `jail duration * this multiplier`
JailRecoveryDebuffMaxHours | `240.0` | 240.0 | `240.0` | hours spent in jail after JailRecovery debuff reaches its maximal values
JumpCostBase | `6.0` | 6.0 | `6.0` | Stamina cost of one jump
LethalDmgR | `10.0` | 10.0 | `10.0` | DmgR that is known to cause death
LocalHeroInfamousReputationThreshold | `0.7` | 0.7 | `0.7` | above this rep local hero, under infamous
LocationReputationHatedThreshold | `0.2` | 0.2 | `0.2` | reputation threshold below which a location will hate the player
LocationReputationLovedThreshold | `0.8` | 0.8 | `0.8` | reputation threshold above which a location will love the player
LockPickingAdequateTolerance | nil | nil | <font color="blue">0.17</font> | locks on a similar level as the player have adequate tolerance
LockPickingAppropriateTolerance | `0.045` | 0.045 | `0.045` | the lock is considered too hard to pick, if the tolerance is smaller than this
LockPickingCursorShakeRange | `0.08` | 0.08 | `0.08` | how much does cursor shake during lock picking (maximum/base value)
LockPickingCursorShakeSpeed | `30.0` | 30.0 | `30.0` | how fast does cursor shake during lock picking
LockPickingFailRelativeXPMulCoef | `0.11563` | 0.11563 | `0.11563` | multiplicative constant to derive XP reward relative to the success
LockpickingFailSoundIntensity | `0.5` | 0.5 | `0.5` | one-shot intensity relative to the database
LockpickingLockpickBreakChance | `1.0` | 1.0 | `1.0` | base lockpick break chance
LockpickingRelDistanceToSoundIntensity | `0.5` | 0.5 | `0.5` | how relative distance influences sound
LockPickingSkillToShakeRel | `0.03` | 0.03 | `0.03` | how much does the skill decrease the cursor shake (`skill * this is relative to maximum/base`)
LockpickingSoundIntensityMin | `0.3` | 0.3 | `0.3` | minimal multiplier the lockpicking minigame will generate
LockPickingStealthXP | `8.0` | 8.0 | `8.0` | xp to stealth for each successful lock-pick
LockPickingSuccessXPDivCoef | `0.046875` | 0.046875 | `0.046875` | constant used in the denominator to derive XP reward for a successfully opened lock
LockPickingSuccessXPMulCoef | `18.0` | 18.0 | `18.0` | multiplicative constant to derive XP reward for a successfully opened lock
LockPickingToleranceACoef | `0.45` | 0.45 | `0.45` | the lockpicking tolerance formula
LockPickingToleranceKCoef | `0.07` | 0.07 | `0.07` | the lockpicking tolerance formula
LockPickingToleranceMCoef | `0.687` | 0.687 | `0.687` | the lockpicking tolerance formula
LockPickingToleranceNCoef | `0.48` | 0.48 | `0.48` | the lockpicking tolerance formula
LockPickingTurnBackDivCoef | `0.1` | 0.1 | `0.1` | constant used in the denominator to derive the turnback speed of a lock
LockPickingTurnBackMulCoef | `5.0` | 5.0 | `5.0` | multiplicative constant to derive the turnback speed of a lock
LowHealthThreshold | `40.0` | 40.0 | `40.0` | threshold for low health effects (for npcs)
MatPierceableMaxArmor | `10.0` | 10.0 | `10.0` | armor of a rock-solid material
MatPierceableMin | `6.0` | 6.0 | `6.0` | OBSOLETE: projectiles with stab damage can stab into
MaxAgilityToMovementSpeedAddition | `0.15` | 0.15 | `0.15` | max positive addition (for maximal vit), the same amount is subtracted on level 0
MaxArmorLoad | `0.2` | 0.2 | `0.2` | 
MaxAttackSpeedMod | `0.4` | 0.4 | `0.4` | maximal relative change in the attack speed
MaxCloudAverageForShiningArmor | `0.3` | 0.3 | `0.3` | used by perk Knight in a Shining Armor; this is maximal current cloud average that still allows this perk to be active
MaxCourageMoraleContextFadingMod | `0.03` | 0.03 | `0.03` | how much can courage affect morale context fading
MaxDamage | `200.0` | 200.0 | `200.0` | all stam and health damages are clamped
MaxDmgR | `4.0` | 4.0 | `4.0` | ceil of DmgR ('damage raw')
MaxFencingWeaponUsageMod | `0.2` | 0.2 | `0.2` | relative weapon status damage for max fencing
MaxHearingSoundAttenuationCoef | `0.2` | 0.2 | `0.2` | minimal attenuation for non-zero hearing stat
MaxItemDisappearingTime | `32400.0` | 32400.0 | `32400.0` | max game time for dropped items to disapper
MaxLightProbeValue | `65.0` | 65.0 | `65.0` | value for the max visibility
MaxModConspicuousness | `1.0` | 1.0 | `1.0` | final modified conspicuousness stat maximum (the most conspicuous actor)
MaxModVisibility | `3.5` | 3.5 | `3.5` | final modified visibility stat maximum (the most visible actor)
MaxMorale | `1.0` | 1.0 | `1.0` | max deriv stat value
MaxPedalCost | `2.0` | 2.0 | `2.0` | pedaling STA cost (pressure 1)
MaxPerfectBlockSlotModifier | `0.85` | 0.85 | `0.85` | modifier of PB slot window - determined as (t_hit - t_pbslot) from attack * this value.
MaxPerkPoints | `10.0` | 10.0 | `10.0` | total number of perk points player will gain per stat/skill
MaxSlashBuffApplyChance | `1.5` | 1.5 | `1.5` | chance to apply buff on slash when giving max hp damage
MaxSmashBuffApplyChance | `0.7` | 0.7 | `0.7` | chance to apply buff on smash when giving max hp damage
MaxSpecialPerfectBlockSlotModifier | `0.6` | 0.6 | `0.6` | modifier of SPB slot window - determined as (t_hit - t_pbslot) from attack x this value.
MaxStabBuffApplyChance | `2.0` | 2.0 | `2.0` | Chance to apply buff on stab when giving maximum health damage
MaxStatToAttackMult | `1.2` | <font color="red">1.1</font> | `1.1` | Maximal relative attack multiplier (for a high stat)
MaxStatToAttackStaminaCostMult | `2.0` | 2.0 | `2.0` | Maximum Stamina cost multiplier for a low stat
MaxStatToAttackStaminaCostStatDiff | `5.0` | 5.0 | `5.0` | stat difference for max/min cost multiplier
MaxStatToAttackStatDiff | `5.0` | 5.0 | `5.0` | stat difference for max/min relative attack multiplier
MaxStealthHitSoundMultiplier | `0.4` | <font color="red">0.22</font> | `0.22` | intensity multiplier for max stealth level
MaxViewRadius | `100.0` | 100.0 | `100.0` | the maximal view radius a superman NPC will have
MaxWeaponBuffCharge | `30.0` | 30.0 | `30.0` | max number of uses
MaxWeatherSoundAttenuationCoef | `0.2` | 0.2 | `0.2` | 0 - allow weather conditions to mute the sounds<br>1 - no influence
MetabolismAbsorbSpeed | `0.069` | 0.069 | `0.069` | food/alcohol metabolised (removed) in world time
MetabolismDigestSpeed | `0.0277` | 0.0277 | `0.0277` | food/alcohol digested (added) in world time
MetabolismDigestSpeedMultiplier | `1.5` | 1.5 | `1.5` | accelerate digest speed multiplier to_digest = max_poisoning
MinHealthToBeAbleToSleepOrSkiptime | `30.0` | 30.0 | `30.0` | player will not be able to sleep or wait if health would go under this threshold during sleep or waiting
MinLeftoverPerks | `1.0` | 1.0 | `1.0` | Preferred number of leftovers
MinLightProbeVisibility | -1.0 | -1.0 | -1.0 | Minimum value for the minimal probe result
MinModConspicuousness | -1.0 | -1.0 | -1.0 | Final modified Conspicuousness stat minimum (the least conspicuous actor)
MinModVisibility | -2.0 | -2.0 | -2.0 | Final modified Visibility stat minimum (the most invisible actor)
MinMorale | `0.0` | 0.0 | `0.0` | Minimum derived stat value
MinPedalCost | `1.0` | 1.0 | `1.0` | Pedaling Stamina cost (pressure 0)
MinPerfectBlockSlot01 | `0.3` | 0.3 | `0.3` | the smallest Perfect Block slot for the lowest level
MinPerkPoints | `5.0` | 5.0 | `5.0` | no leftovers if the number of perk points would be &lt;= than this
MinPossibleSleepTime | `1.01` | 1.01 | `1.01` | player will reject to lie into bed when he will not be able to sleep at least this long (due to bleeding/hunger/etc in hours)
MinRelativeStaminaMax | `0.3` | 0.3 | `0.3` | Short-term Stamina maximum relative to long-term maximum
MinStatToAttackMult | `0.5` | 0.5 | `0.5` | Minimal relative attack multiplier for a low stat
MinStatToAttackStaminaCostMult | `0.8` | 0.8 | `0.8` | Minimum Stamina cost multiplier for a high stat
MinStealthHitSoundMultiplier | `0.1` | <font color="red">0.06</font> | `0.06` | Intensity multiplier for minimum Stealth level
MinTrueRelationDistThreshold | `1.5` | 1.5 | `1.5` | Minimal distance required to see the true faction
MinViewRadius | `2.5` | 2.5 | `2.5` | Minimal view radius an almost blind NPC will have, also threshold for instant detection
MinWeaponBuffCharge | `15.0` | 15.0 | `15.0` | 
MoraleContextFadingSpeed | `0.05` | 0.05 | `0.05` | Speed of Morale context increasing/decreasing to 0
MoraleDecisionReliability | `0.15` | 0.15 | `0.15` | Reliability of morale checks
MoraleForCombat | `0.2` | 0.2 | `0.2` | How much morale an NPC must have to not flee from combat
NightCoefToNoise | `0.2` | 0.2 | `0.2` | 
NightCoefToVis | -0.5 | -0.5 | -0.5 | `nightCoef = 1 - daytimeCoef`
NonSkillBookXP | `30.0` | 30.0 | `30.0` | Reading XP rewarded for reading non-skill books
NPCRepWeight | `5.0` | 5.0 | `5.0` | Weight of player - npc reputation (reputation median)
OverallArmorDefenseMoraleWeight | `3.0` | 3.0 | `3.0` | Weight of normalized load affecting morale
OverallWeaponAttackMoraleWeight | `3.0` | 3.0 | `3.0` | Weight of normalized attack affecting morale
OverreadnessEmptyTime | `16.0` | 16.0 | `16.0` | how long (in game hours) does it take to empty the oversleepness stat (time player have to be not reading to be able to read max time again)
OverreadnessFillTime | `8.0` | 8.0 | `8.0` | how long (in game hours) does it take to fill the oversleepness stat (max time player can read)
OversleepnessEmptyTime | `12.0` | 12.0 | `12.0` | how long (in game hours) does it take to empty the oversleepness stat (time player have to be awake to be able to sleep max time again)
OversleepnessFillTime | `12.0` | 12.0 | `12.0` | how long (in game hours) does it take to fill the oversleepness stat (max time player can sleep)
PerceivedSuperfactionImportanceThresholdRel | `0.333333` | 0.333333 | `0.333333` | superfaction items must occupy more than this for the soul to look like the superfaction
PerceptionBaseCha | `10.0` | 10.0 | `10.0` | 
PerceptionMaxFov | `180.0` | 180.0 | `180.0` | the maximal field of view a superman NPC will have
PerceptionMeanDist | `5.0` | 5.0 | `5.0` | 
PerceptionMinFov | `90.0` | 90.0 | `90.0` | the minimal field of view a deaf NPC will have
PerceptionPriorBoostPlayer | `12.0` | 12.0 | `12.0` | boost for player
PerceptionPriorBoostRangedWeapon | `100.0` | 100.0 | `100.0` | boost for ranged weapons (multiplied by PriorWeapon!)
PerceptionPriorCha | `0.3` | 0.3 | `0.3` | 
PerceptionPriorConsp | `3.0` | 3.0 | `3.0` | 
PerceptionPriorCrimeLockpick | `12.0` | 12.0 | `12.0` | 
PerceptionPriorCrimeLoot | `12.0` | 12.0 | `12.0` | priority boost for crime
PerceptionPriorDead | `25.0` | 25.0 | `25.0` | dead or unconscious
PerceptionPriorDist | `2.0` | 2.0 | `2.0` | 
PerceptionPriorEnemyRelationship | -50.0 | -50.0 | -50.0 | 
PerceptionPriorFriendRelationship | -4.0 | -4.0 | -4.0 | 
PerceptionPriorGender | `2.0` | 2.0 | `2.0` | 
PerceptionPriorNotHumanRace | -15.0 | -15.0 | -15.0 | 
PerceptionPriorTarget | `10.0` | 10.0 | `10.0` | target priority estimation
PerceptionPriorThreatened | -5.0 | -5.0 | -5.0 | 
PerceptionPriorVisCrimes | `6.0` | 6.0 | `6.0` | 
PerceptionPriorVisItems | `0.5` | 0.5 | `0.5` | 
PerceptionPriorVisPeople | `2.0` | 2.0 | `2.0` | 
PerceptionPriorWeapon | `8.0` | 8.0 | `8.0` | 
PerkBerserkDuration | `30.0` | 30.0 | `30.0` | how long are buffs active after the perk is triggered
PerkBerserkHealthThreshold | `0.15` | 0.15 | `0.15` | activate on health
PerkBloodRushDistance | `5.0` | 5.0 | `5.0` | distance from dying enemy when Blood Rush perk bonuses are activated
PerkBloodRushDuration | `15.0` | 15.0 | `15.0` | duration of Blood Rush perk bonuses after an enemy dies nearby
PerkBrutusCombatDmgRBonusFromBehind | `1.3` | 1.3 | `1.3` | brutus perk multiplicative base Dmg (CombatDmgRBonusFromBehind)
PerkCarriedBodyGravediggerWeightMul | `0.5` | 0.5 | `0.5` | carried body weight multiplier for gravedigger perk
PerkChainStrikeMaxChain | `5.0` | 5.0 | `5.0` | maximal successive strikes
PerkDaringDebonairWantedLevel | `1.0` | 1.0 | `1.0` | Daring Debonair wanted level threshold
PerkLastGaspCooldown | `600.0` | 600.0 | `600.0` | how fast can the perk be activated again
PerkManlyOdourDirtinessThreshold | `0.5` | 0.5 | `0.5` | Manly Odour perk bonuses are activated above this dirtiness threshold
PerkProperDietActivationTime | `120.0` | 120.0 | `120.0` | hours until ProperDiet perk bonuses are activated
PerkTauntAttackerMoraleMultiplier | `3.0` | 3.0 | `3.0` | multiplier for 'combat_dodge_attacker' morale change when victim has Taunt perk
PerkWaterOfLifeAlcoholMultiplier | `0.5` | 0.5 | `0.5` | potion alcohol effect multiplier for Water of life perk
PerkWaterOfLifeHealthMultiplier | `1.5` | 1.5 | `1.5` | potion health effect multiplier for Water of life perk
PicklockDmgSpeed | `10.0` | 10.0 | `10.0` | how fast is picklock durability decreasing (will be multiplied by the relative distance)
PicklockFatalRelativeDist | `5.0` | 5.0 | `5.0` | maximal relative distance, if futher the pick lock is destroyer
PickpocketingAngleChancePenalty | `0.027` | 0.027 | `0.027` | penalty in (0-1) to chance pickpocketing for each angle from optimal possition exactly from behind victim (180 max)
PickpocketingComradePerkBonus | `0.3` | 0.3 | `0.3` | max bonus in (0-1) to pickpocketing for comrade perk
PickpocketingDistance | nil | <font color="blue">2.0</font> | `2.0` | Max pickpocketing range (not starting interactor range)
PickpocketingFailXPMod | `0.3` | 0.3 | `0.3` | Pickpocketing XP modified on failure
PickpocketingIndicatorSharpness | `0.2` | <font color="red">0.0</font> | `0.0` | 0 - precise slow change<br>1 - sharp change
PickpocketingItemUncoverTimePerWeight | `0.1` | 0.1 | `0.1` | time to uncover item per weight unit
PickpocketingMaxSkillChargeSpeedRatio | `6.0` | 6.0 | `6.0` | charge speed ratio boost with best skill
PickpocketingMaxSkillChargeTime | `30.0` | 30.0 | `30.0` | max charge time with best skill
PickpocketingMinChargeTime | `2.0` | 2.0 | `2.0` | min charge time needed
PickpocketingMisstargetingTolerance | nil | <font color="blue">2000.0</font> | `2000.0` | Time tolerance for temporarily mistargeting your victim
PickpocketingNPCDrunkTimeChanceMod | `0.5` | 0.5 | `0.5` | Modifies TimeChancePenalty when drunk
PickpocketingNPCHurtTimeChanceMod | `0.75` | 0.75 | `0.75` | Modifies TimeChancePenalty when hurt
PickpocketingNPCSleepingTimeChanceMod | `0.5` | 0.5 | `0.5` | Modifies TimeChancePenalty when sleeping
PickpocketingRandomChanceRollMinCap | nil | <font color="blue">0.1</font> | `0.1` | Worst random rolls will always be capped to this minimum chance
PickpocketingRobbedAngrinessChancePenalty | `0.05` | 0.05 | `0.05` | penalty in (0-1) to pickpocketing chance for each time victim was robbed before
PickpocketingStealthXP | `12.0` | 12.0 | `12.0` | Stealth XP for each successful pickpocketing
PickpocketingTimeChancePenaltyBest | `0.0133` | 0.0133 | `0.0133` | penalty in pickpocketing chance in best case(s)
PickpocketingTimeChancePenaltyWorst | `0.1` | 0.1 | `0.1` | penalty in pickpocketing chance in worst case(s)
PickpocketingTreasurePriceXP | `100.0` | 100.0 | `100.0` | Additional XP gain calculated by stolen items total value
PickpocketingXP | `15.0` | 15.0 | `15.0` | Pickpocketing XP for each pocket successfully picked
PoorWeaponDefense | `1.0` | 1.0 | `1.0` | 
ProjectileMaxBreakProb | `0.7` | 0.7 | `0.7` | probability of breaking an arrow when a rock-solid material is hit
QuestMoneyRewardScaleConstant | `1.25` | <font color="red">1.2</font> | `1.2` | scale constnat for quest reward item amount
RangedWpnCosThetaToAttackMin | `0.7` | 0.7 | `0.7` | cos(theta) linearly lowers the attack in the range [this,1]
RangedWpnMinPowerCoef | `0.1` | 0.1 | `0.1` | the power coefficient for a really weak soul (the stats are far below requirements)
RangedWpnMinStrCoef | `0.5` | 0.5 | `0.5` | if the curr/req strength ratio goes below this, the power is minimal
RangedWpnOptimalDistanceToMinamal | `0.5` | 0.5 | `0.5` | ratio between the database attack distance and the minimal range for the AI
RangedWpnPowerConstA | `1.85` | 1.85 | `1.85` | used to convert strength requirements to the resulting power
RangedWpnPwrToSpeed | `1.0` | 1.0 | `1.0` | total power to launch speed
RangedWpnSelfHarmCoef | `15.0` | 15.0 | `15.0` | Special constant used in self harm equation
RangedWpnSpeedToAttack | `0.012` | 0.012 | `0.012` | attack mod deduced from impact speed
<strike>ReadingRestEffectiveness</strike> | `0.3` | nil | nil | If this value is 0.3, reading will regen player as sleeping on bed with comfort 30%.
<strike>ReadingRestUpperLimit</strike> | `1.0` | nil | nil | When sleeping, the rest can not exceed bed quality. When reading, the threshold is given by this value.
ReadingXpPerHour | `20.0` | 20.0 | `20.0` | Reading XP gained after one hour of reading with 100% reading speed
RecognitionSpeedNotVisible | -0.5 | -0.5 | -0.5 | must be negative, how the recognition is decreased
RecognitionTimeDistanceGain | `0.1` | 0.1 | `0.1` | perlin gain for the distance influencing the recognition time
RecognitionTimeKNegativeCoef | -6.0 | -6.0 | -6.0 | multiplicative coef for negative values of conspicuousness
RecognitionTimeKPositiveCoef | -3.0 | -3.0 | -3.0 | multiplicative coef for positive values of conspicuousness
RecognitionTimePCoef | `8.0` | 8.0 | `8.0` | recognition time for a character with conspicuousness = 0
RelationshipToImpressCharisma | `0.8` | 0.8 | `0.8` | [0,inf]: how much reputation is used to raise charisma
RelationshipToPersuadeSpeech | `0.8` | 0.8 | `0.8` | [0,inf]: how much reputation is used to raise speech
RelationshipToThreatenBadassness | `0.8` | 0.8 | `0.8` | [0,inf]: how much reputation is used to raise badassness
RepairKitCapacity | `200.0` | 200.0 | `200.0` | Repair kit capacity to repair
RepairKitItemHealthBestLimit | `0.6` | 0.6 | `0.6` | With high skill/quality repair kit, can repair items until this health limit
RepairKitItemHealthDefaultLimit | `0.8` | 0.8 | `0.8` | Default repair kit item health limit
RepairKitItemPerkBuffHealthThreshold | `0.3` | 0.3 | `0.3` | Buffs added by repair kit perks won't be functional under this item health
RepairKitMaxSkillCapacityCoef | `1.5` | 1.5 | `1.5` | Max skill coefficient for repair kit total capacity
RepairPriceModif | `0.65` | 0.65 | `0.65` | Default repairing shop price modifier
ReputationPropagationBiasTime | `1800.0` | 1800.0 | `1800.0` | random bias to propagation time (world time)
ReputationPropagationCoef | `0.3` | 0.3 | `0.3` | Propagation coef up (soul->faction->superfaction)
ReputationPropagationTime | `10800.0` | 10800.0 | `10800.0` | propagation time from npc to faction/superfaction (world time)
ResetNearbyRelationshipRange | `50.0` | 50.0 | `50.0` | range for relationship reset
ResetPublicFriendsRelationshipMin | `0.15` | 0.15 | `0.15` | minimal relationship for the alied forces after reset
RespawnTimeBase | `800.0` | 800.0 | `800.0` | Time before a hidden corpse respawns (base time)
RespawnTimeVariation | `60.0` | 60.0 | `60.0` | Time before a hidden corpse respawns (random extra time)
RiderAgilityToHorsePullDown | `0.5` | 0.5 | `0.5` | Relative rider Agility to horse pull down
RiderHorseStaminaCoef | `0.25` | 0.25 | `0.25` | Ratio between Stamina consumption of a horse and its rider
RiderSkillToHorsePullDown | `0.5` | 0.5 | `0.5` | Relative riding skill skill to horse pull down
RiderThreatToHorseMorale | `0.1` | 0.1 | `0.1` | Morale decrease per one rider threat
SecondaryStatXPRatio | `0.5` | 0.5 | `0.5` | secondary weapon stat ratio
SharpeningFullNegativeHealthXP | `20.0` | 20.0 | `20.0` | 
SharpeningFullPositiveHealthXP | `100.0` | 100.0 | `100.0` | change in weapon health at which the sharpening is considered successful
SharpeningMaxDestructionAngle | `0.7` | 0.7 | `0.7` | 
SharpeningMaxIdealAngle | `0.5` | 0.5 | `0.5` | 
SharpeningMinDestructionAngle | `0.6` | 0.6 | `0.6` | 
SharpeningMinEfficiencyHealth | `0.3` | 0.3 | `0.3` | health you can achieve with the worst efficiency
SharpeningMinIdealAngle | `0.3` | 0.3 | `0.3` | 
SharpeningSuccessfulHealthDelta | `0.1` | 0.1 | `0.1` | 
ShoeHealthDecrease | `0.01` | 0.01 | `0.01` | status delta per traveled m
ShoeHealthUpdateDistance | `50.0` | 50.0 | `50.0` | shoe health is update after traveling N m
ShortTermNutritionDigestionSpeedMultiplier | `5.0` | 5.0 | `5.0` | digestion multiplier for part of the food with low nutrition value
SkillCap | `20.0` | 20.0 | `20.0` | max skill level, also effects of a general skill are maximal at this level
SkillDiffToAttackSpeed | `0.1` | 0.1 | `0.1` | relative attack speed gain for one skill level difference
SkillToDefense | `0.02857` | 0.02857 | `0.02857` | 
SkillToDmgConstA | `70.0` | <font color="green">250.0</font> | `250.0` | 
SkillToFencingBase | `0.8` | 0.8 | `0.8` | 
SkillToPerfectBlockPowTo | `0.5` | 0.5 | `0.5` | `slot = relativeSkill ^ this`
SkillToRangedWpnAIRange | `0.5` | 0.5 | `0.5` | how the relative skill influences the weapon range for the AI
SkillXPBlock | `2.0` | 2.0 | `2.0` | XP gain after a successful block
SkillXPComboHit | `4.0` | 4.0 | `4.0` | weapon XP gain after a hit in a combo
SkillXPDrinkAlcohol | `1.0` | 1.0 | `1.0` | XP gain per 1 alcohol content drinked
SkillXPHit | `2.0` | 2.0 | `2.0` | weapon XP gain after a hit
SkillXPKill | `12.0` | 12.0 | `12.0` | weapon XP gain after a kill
SkillXPLevelBase | `20.0` | 20.0 | `20.0` | base value (additive) to calculate XPs needed for the next level
SkillXPLevelDiff | `30.0` | 30.0 | `30.0` | multiplicative value to calculate XPs needed
SkillXPPerfectBlock | `8.0` | 8.0 | `8.0` | XP gain after a successful perfect block
SkillXPRiposte | `8.0` | 8.0 | `8.0` | successful riposte (attack after perfect block)
SkillXPUseRepairKit | `5.0` | 5.0 | `5.0` | XP gain per 1 health repaired by repairkit
SleepHealthRegenBaseSpeed | `0.0347222` | 0.0347222 | `0.0347222` | full regen after 8 world-time hours
SleepToSaveThreshold | `1.0` | 1.0 | `1.0` | sleeping at least this time triggers autosave.
SlimCollisionWeightMul | `0.8` | 0.8 | `0.8` | multiplies the archetype body weight if the character is slim
SoulCourageMoraleWeight | `5.0` | 5.0 | `5.0` | Weight of soul courage affecting morale
SpeechDiffToSkillCheckResult | `0.3` | 0.3 | `0.3` | > 0; speech diff for result = -1/1
SpeechMulOnExtremeExhaustion | `0.75` | 0.75 | `0.75` | Player will have this speech multiplied by this value when he has exhaust equal to 0. Speech will not be changed when exhaust is 50. Linear interpolation on multiplier is applied when exhaust is between 0 and 50;
SpeechXPLevelBase | `20.0` | 20.0 | `20.0` | 
SpeechXPLevelDiff | `30.0` | 30.0 | `30.0` | 
SprintCost | `3.5` | 3.5 | `3.5` | stamina cost of sprint
StamDamage | `8.0` | 8.0 | `8.0` | see: rpglib::calcStaminaDamageCost
StaminaDamageToInjury | `0.0` | 0.0 | `0.0` | note: stamina is [0-100] but injury is [0-1]
StaminaToHealthDamageMax | `0.75` | 0.75 | `0.75` | stamina-health damage transfer for dmgr=1
StaminaToHealthDamageMin | `0.25` | 0.25 | `0.25` | stamina-health damage transfer for dmgr=0
StamRegenBase | `22.0` | 22.0 | `22.0` | base regeneration speed
StamRegenBlockMod | `0.6` | 0.6 | `0.6` | relative stam regen speed during active block or raised weapon
StamRegenCooldown | `1.5` | 1.5 | `1.5` | cooldown timer expiry
StamRegenFromVit | `1.0` | 1.0 | `1.0` | how our VIT stat affects stamina regeneration
StamRegenMoveMod | `0.75` | 0.75 | `0.75` | relative stam regen speed during movement
StamRegenRelativeDiff | `0.666667` | 0.666667 | `0.666667` | maximal relative difference to the base speed on low/high stamina
StarvationExtremeThreshold | `0.0` | 0.0 | `0.0` | when nutrition is below this value, extreme hunger starts
StarvationHealthLossSpeed | `0.057874` | <font color="green">0.01</font> | `0.01` | by design the same speed as the digestion
StarvationHugeThreshold | `25.0` | 25.0 | `25.0` | when nutrition is below this value, significant hunger starts
StarvationPlayerEffectMaxMax | `60.0` | 60.0 | <font color="green">75.0</font> | longest interval between effects for high hunger stat
StarvationPlayerEffectMaxMin | `90.0` | 90.0 | <font color="green">120.0</font> | longest interval between effects for low hunger stat
StarvationPlayerEffectMinMax | `30.0` | 30.0 | <font color="green">45.0</font> | shortest interval between effects for high hunger stat
StarvationPlayerEffectMinMin | `60.0` | 60.0 | <font color="green">90.0</font> | shortest interval between effects for low hunger stat
StarvationThreshold | `50.0` | 50.0 | `50.0` | when nutrition is below this value, hunger starts
StatCap | `20.0` | 20.0 | `20.0` | max stat level
StatsToDodgePowTo | `0.5` | 0.5 | `0.5` | `slot = relativeStats ^ this`
StatToMainLevelBase | `0.5` | 0.5 | `0.5` | a1 of the geometric progression
StatXPAgilityPerDodge | `2.0` | 2.0 | `2.0` | XP gain after a dodge
StatXPComboHit | `4.0` | 4.0 | `4.0` | XP gain after combo hit
StatXPHit | `2.0` | 2.0 | `2.0` | XP gain after a hit
StatXPKill | `8.0` | 8.0 | `8.0` | XP gain after a kill
StatXPSpeechPerSequence | `1.0` | 1.0 | `1.0` | Speech XP gain after selecting an unused sequence (multiplied by speech_coef of that sequence)
StatXPSpeechPersuadeSuccessMax | `10.0` | 10.0 | `10.0` | Maximal XP gain for persuade
StatXPVitalityPerDistance | `8.0` | 8.0 | `8.0` | Vitality XP gain after sprinting `AthleticXPAwardDistance`
StatXPVitalityPerJump | `0.5` | 0.5 | `0.5` | Vitality XP gain for each jump
StatXPVitalityPerKill | `15.0` | 15.0 | `15.0` | Vitality XP gain after a kill
StatXPVitalityPerVault | `0.7` | 0.7 | `0.7` | Vitality XP gain for each vault over a ledge
StealthAttackFailXp | `10.0` | 10.0 | `10.0` | Stealth XP gain for failed stealth kill or take-down
StealthAttackMaxXp | `50.0` | 50.0 | `50.0` | Stealth XP gain for successful stealth kill or take-down, strongest enemy
StealthAttackMinXp | `25.0` | 25.0 | `25.0` | Stealth XP gain for successful stealth kill or take-down, weakest enemy
StealthCooldown | `5.0` | 5.0 | `5.0` | after last detector npc stops seeing player
StealthKillDamage | `100.0` | 100.0 | `100.0` | damage given to the victim
StealthKillProbCoefA | `4.0` | 4.0 | `4.0` | coefficient for stealth kill/knock-out probability formula
StealthKillProbCoefB | `1.0` | 1.0 | `1.0` | coefficient for stealth kill/knock-out probability formula
StealthKillProbCoefC | `1.0` | 1.0 | `1.0` | coefficient for stealth kill/knock-out probability formula
StealthKnockOutUnconsciousDepthBase | `250.0` | 250.0 | `250.0` | the base unconsciousness depth for stealth knockout
StealthSkillToFootstepSoundMult | `0.4` | 0.4 | `0.4` | how much are footsteps attenuated for the max skill
StealthSkillToRecogTime | `0.05` | 0.05 | `0.05` | how much is the required time extended by the skill level (relative)
StealthSkillToViewRadiusDecr | `0.02` | 0.02 | `0.02` | how much is the view radius decreased by the skill level (relative)
StealthSneakBaseDistance | `4.0` | 4.0 | `4.0` | Sneaked distance that triggers Stealth leveling
StealthSneakBaseXp | `1.0` | 1.0 | `1.0` | Base XP gain when sneaking
StealthSneakCheckRadius | `15.0` | 15.0 | `15.0` | NPC query radius when sneaking
StealthSneakXpSumCoefA | `5.0` | 5.0 | `5.0` | Combine XP from each NPC
StealthSneakXpSumCoefB | `4.0` | 4.0 | `4.0` | 
StealthToUnconsciousDepth | `250.0` | 250.0 | `250.0` | modifies the time victim is unconscious
StillAndHiddenHysteresis | `1.5` | 1.5 | `1.5` | switch the state after this timeout
StillBuffDuration | `600.0` | 600.0 | `600.0` | duration of standing still after which Still buff bonuses are activated (in worldtime seconds)
StolenGoodsForcedDiscount | `0.4` | 0.4 | `0.4` | price multiplier for when merchant detects that the sold items are stolen
StoryProgressXPLevelBase | `20.0` | 20.0 | `20.0` | 
StoryProgressXPLevelDiff | `30.0` | 30.0 | `30.0` | 
StrAgiToEqwArmorLoad | `1.0` | 1.0 | `1.0` | 
StrengthToInventoryCapacity | `4.0` | 4.0 | `4.0` | derives inventory capacity from Strength
StrengthXPLevelBase | `20.0` | 20.0 | `20.0` | 
StrengthXPLevelDiff | `30.0` | 30.0 | `30.0` | 
SuperFactionRepWeight | `1.0` | 1.0 | `1.0` | Weight of superfaction reputation (reputation median)
SuperWeaponDefense | `20.0` | 20.0 | `20.0` | like the best shield - mainly for AI, used to judge weapon
SurfaceToArmorLoadALWCoef | `1.0` | 1.0 | `1.0` | Coef alw from terrain/surface to armor load influence calculation
SurfaceToArmorLoadTWCoef | `0.15` | 0.15 | `0.15` | Coef tw from terrain/surface to armor load influence calculation
ThreatenStrenghtWeight | `0.5` | 0.5 | `0.5` | 0 - full weight to morale<br>1- full weight to strength
ThunderstormBuffRainIntensity | `0.3` | 0.3 | `0.3` | rain intensity threshold when Thunderstorm buff bonuses are activated
TreasureItemPricee | `1000.0` | 1000.0 | `1000.0` | starting price of treasure items
TrueRelationDistThresholdRel | `0.333333` | 0.333333 | `0.333333` | distance, relative to observers maximum distance, required to see the true faction
UnarmedAttackBase | `2.0` | 2.0 | `2.0` | attack value for attack with relative stam cost = 1
UnarmedAttackReqStrBase | `2.0` | 2.0 | `2.0` | for attack with relative stam cost = 1
UnarmedBlockDefense | `3.0` | 3.0 | `3.0` | defense value for unarmed block
UnarmedHitArmorDamageCoef | nil | <font color="blue">0.25</font> | `0.25` | relative to armed combat
UnconsciousDepthFadeoutSpeedBase | `1.0` | 1.0 | `1.0` | how fast is the depth consumed
UnconsciousTimeWhenTimeIsNotRunning | `8.0` | 8.0 | `8.0` | if world time is not running, skiptime can not be started when player is unconscious; screen will only fade for this long instead; this is slightly modified by some rpg stats
VigourFull | `100.0` | 100.0 | `100.0` | Maximum vigour
VigourTickInterval | `2.0` | 2.0 | `2.0` | Vigour timer expiry
VisionToViewRadius | `2.0` | 2.0 | `2.0` | an increase of FOV caused by the hea stat
VitalityToUnconsciousDepthFadeoutSpeed | `1.0` | 1.0 | `1.0` | relative vitality
VitalityXPLevelBase | `20.0` | 20.0 | `20.0` | 
VitalityXPLevelDiff | `30.0` | 30.0 | `30.0` | 
WeakBlockStamCoef | `2.0` | 2.0 | `2.0` | 
WeaponDefenseToAttackingWeaponStatus | `0.01` | 0.01 | `0.01` | how opponent's defense value damages my weapon - hit to weapon/block
WeaponStatusToAttackCoef | `0.5` | 0.5 | `0.5` | weapon health to status multiplicative coef

