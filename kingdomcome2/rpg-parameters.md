---
title: RPG Parameters
description: 
published: true
date: 2025-02-09T00:38:42.082Z
tags: 
editor: markdown
dateCreated: 2025-02-09T00:38:42.082Z
---

# Parameter Defaults

> No parameter defaults yet, but this table is a good start. (8 Feb 2025 @ 4:38 PM)
{.is-info}


Parameter Name | Description | Notes (?)
:--- | :--- | :--
AddedDirtOnCarryItem | Dirt added on player when picking or putting down an item through the carry item action (the sack carrying feature). | `[%]`
AdditionalAttackerCountForMaxFadingBuff | for AdditionalAttackerCountFading buff | `[-]`
AgiDiffToAttackSpeed | relative attak speed gain for one agi level difference | `[speed/agi]`
AgiToEqwArmorLoad | maximal gain on level cap, GDD: 17/218 | `[-]`
AgilityBaddassWeight | Weight of relative agility affecting badassness | `[]`
AgilityLevelForNonClumsyLedges | Minimal agility required for normal (non-clumsy) ledges | `[-]`
AgilityMulOnExtremeExhaustion | Player will have this agility multiplied by this value when he has exhaust equal to 0. Agility will not be changed when exhaust is 50. Linear interpolation on multiplier is applied when exhaust is between 0 and 50; | `[%]`
AgilityXPLevelBase | see GDD 44/218 | `[-]`
AgilityXPLevelDiff | see GDD 44/218 | `[-]`
AimCiriticalLimitTime | time limit after when AI is notified about low stamina when aiming | `[s]`
AimPainlessDelay | aiming without stam. loss | `[s]`
AimSkillToZoom | zoom increase by each skill level above the base | `[deg/skill]`
AimSpreadMax | aiming spread due to low stam and skill - max angle - used right before all the stamina is lost | `[deg]`
AimSpreadMinRatio | aiming spread min relative to max - this value is used right after entering the painless zone | `[-]`
AimSpreadSkillDecrease | relative decrease of MAX aim spread on max skill level | `[-]`
AimZoomBase | aim zoom (=fov decrease) after reaching some skill level | `[deg]`
AimZoomBaseSkill | minimal skill level required to benefit from the zoom effect | `[]`
AimZoomMax | maximal aim zoom (=fov decrease) | `[deg]`
AlchemyDecayedHerbQuality | Quality of decayed herb used in alchemy cooking | `[-]`
AlchemyDryHerbQuality | Quality of dried herb used in alchemy cooking | `[-]`
AlchemyFreshHerbQuality | Quality of fresh herb used in alchemy cooking | `[-]`
AlchemyPotionBaseQualityWeight | How much the quality of the base is reflected in the result of cooking | `[-]`
AlchemyRecipeStepsTolerance | how many recipe steps might fail in order to successfully brew the recipe | `[-]`
AlchemyResourcesQualityWeight | How much the quality of the resources is reflected in the result of cooking | `[-]`
AlchemyResultCoefToFirstQuality | Minimum brew result coefficient to create the best possible quality potion | `[-]`
AlchemyResultCoefToSecondQuality | Minimum brew result coefficient to create the second best possible quality potion | `[-]`
AlchemyToleranceBase | base brewing tolerance on level 0 | `[-]`
AlchemyToleranceMaxLevel | base brewing tolerance on max level | `[-]`
AlchemyTrialEndErrorPerkTolerance | Additional tolerance gained by having Train And Error perk. | `[-]`
AlchemyXPMultiplierSecondQualityPotion | multiple the basic amount of XP for brewing potion of the second quality | `[xp]`
AlchemyXPMultiplierThirdQualityPotion | multiple the basic amount of XP for brewing potion of the third quality | `[xp]`
AlchemyXPOverride | Multiply XP gained for this skill | `[]`
AlchemyXPPerFailedBrewing | how many XP you get when failed brew a potion | `[xp]`
AlcoholBaseHangoverDuration | base max duration for hangover (after blackout) in world time | `[s]`
AlcoholBlackoutDuration | blackout unconscious duration | `[s]`
AlcoholContentFPAntidoteThreshold | food with alcohol content above this threashold have anti food poisoning effect. | `[alcohol]`
AlcoholDigestSpeedModfifOnEmptyStomache | multiplier for alc. digest speed on empty stomache | `[coeff]`
AlcoholDigestSpeedModfifOnFullStomache | multiplier for alc. digest speed on full stomache | `[coeff]`
AlcoholDrunkMaxExhaustNegativeEffect | max negative exhaust effect while drunk | `[stat/s]`
AlcoholDrunkThreshold | threshold for drunkenness mood from max alcohol poisoning | `[coeff]`
AlcoholDrunkThresholdNPC | threshold for drunkenness for NPCs | `[coeff]`
AlcoholHangoverHeadInjuryVisual | Head injury caused by hangover will show the head injury debuff filled by this many % (or add this many if there already is existing injury). | `[%]`
AlcoholHangoverOffsetModif | starting hangover negative effects are modified by this offset | `[coeff]`
AlcoholMaxAGIEffect | max negative/positive stat effect | `[stat]`
AlcoholMaxCHAEffect | max negative/positive stat effect | `[stat]`
AlcoholMaxCONEffect | max negative/positive stat effect | `[stat]`
AlcoholMaxDrinkingSkillHangoverDurationModifier | hangover duration modifier for max=best drinking skill | `[-]`
AlcoholMaxHPAfterHangover | Hangover will cause head injury, reducing health to this many % of max health. If player has less, health will not be reduced. | `[%]`
AlcoholMaxSPCEffect | max negative/positive stat effect | `[stat]`
AlcoholMaxSTREffect | max negative/positive stat effect | `[stat]`
AlcoholMaxVITEffect | max negative/positive stat effect | `[stat]`
AlcoholMoodMaxExhaustPossitiveEffect | max positive exhaust effect while in mood | `[stat/s]`
AlcoholMoodThreshold | threshold for alcohol mood from max alcohol poisoning | `[coef]`
AlcoholMoodToDrunkUIFill | Drunkenness changes from Mood to Drunk at 50, but we want to visually fill from 0 -> for the first AlcoholMoodToDrunkUIFill s, show only a portion of the real value, gradually increasing to the full value. | `[s]`
AlcoholPerkBacchusHangoverEffectMod | hangover effects mod | `[]`
AlcoholPerkCorrectResistanceModif | alcohol content modif for correct resistance | `[]`
AlcoholPerkLooseTongueSpcCha | speech and charisma bonus/malus for loose tongue perk | `[]`
AlcoholPerkWrongResistanceModif | alcohol content modif for wrong resistance | `[]`
AlcoholUnconsciousAddedDirt | Dirt added to someone who passed-out from alcohol. | `[%]`
AlcoholUnconsciousRandomItemChance | Chance that a player will get a random item when waking up from alcohol-induced unconsciousness | `[%]`
AlcoholUnconsciousRandomItemIsGoodChance | Chance that a item obtained from alcohol-induced unconsciousness will be from the set of good items. | `[%]`
AlcoholismCravingLevel1 | After a level 1 alcoholic has a drink, this many seconds pass until they get a debuff (need another drink). Game time. | `[s]`
AlcoholismCravingLevel6 | Like AlcoholismCravingLevel1, but for level 6. Remaining levels are linearly interpolated. Game time. | `[s]`
AlcoholismLevel1 | Amount of alcoholism points that will start addiction. | `[alcohol]`
AlcoholismLevel2 | Threshold of alcoholism points for second level of alcohol addiction. | `[alcohol]`
AlcoholismLevel3 | Threshold of alcoholism points for third level of alcohol addiction. | `[alcohol]`
AlcoholismLevel4 | Threshold of alcoholism points for fourth level of alcohol addiction. | `[alcohol]`
AlcoholismLevel5 | Threshold of alcoholism points for fifth level of alcohol addiction. | `[alcohol]`
AlcoholismLevel6 | Threshold of alcoholism points for sixth level of alcohol addiction. | `[alcohol]`
AlcoholismRemoveSpeed | alcoholism removed per world-time second (default 100 / 4days) | `[alcoholism/s]`
AngrinessArmingThreshold | If Angriness is higher, NPCs will start equipping weapons everywhere. | `[-]`
AngrinessFromNervousnessCoef | Angriness gain from nervousness change. | `[]`
ArmorConditionThresholdForDamage | Threshold of armor condition where armor damage is increasing. | `[-]`
ArmorDefenseToAttackingWeaponStatus | how opponet's defense value damages my weapon - hit to armor | `[status/defense]`
ArmorDirtToCharismaCoef | health to armor defense multiplicative coef | `[-]`
ArmorLoadDiffToMax | GDD: 17/218 | `[-]`
ArmorLoadToJumpCost | how armor load coefficient affects the stamina jump cost (times base) | `[-]`
ArmorLoadToRun | how armor load coefficient affects running speed | `[-]`
ArmorLoadToSprint | how armor load coefficient affects sprint | `[-]`
ArmorStatusToCharismaCoef | health to armor defense multiplicative coef | `[-]`
ArmorStatusToDefenseCoef | health to armor defense multiplicative coef | `[-]`
AthleticXPAwardDistance | award xp for traveling some distance | `[m]`
AttSkillToHorsePullDown | relative attacker skill to horse pull down | `[-]`
AttStrengthToHorsePullDown | relative attacker stat to horse pull down | `[-]`
AttackChargingAttMod | damage modification in maximum charge | `[%]`
AttackChargingBeginCooldown | cooldown before actual charging is started | `[s]`
AttackChargingCooldown | cooldown of charging to maximum value | `[s]`
AttackEnergyModifier | #energie utoku | `[-]`
AttackRequiredStamRatio | actual/cost stamina ratio must be > than this value for attack to be allowed | `[-]`
AttackSpeedNormal | normal attack speed, 0-min, 1-max | `[-]`
AttackSpeedNormalAgi | agility required for the normal attack speed | `[agi]`
AttackSpeedPlayerRelative | 1 - attack speed is always calculated using the player, 0 - using opponents skill | `[-]`
AttackStamModMin | attack strength/power stamina modifier minimum (0stam->Xattack) | `[-]`
AutolearnCombatTechniqueReliability | The probability that the soul will have the autolearnable combat technique perk | `[-]`
AverageArmorDefenseWeight | 0 = only body part defense, 1 = only average defense | `[-]`
AvidReaderReadingSpeed | AvidReader soul ability advances reading progress on one book in inventory during sleep or skiptime. This constant determines speed of reading (reading spot is always None). | `[.]`
BadassnessDifficultyModifier | convert general difficulty to badassness range | `[]`
BadassnessMoraleWeight | Weight of badassness affecting morale | `[]`
BarterAngrinessCoefWeightA | shopkeeper shop barter calculation 'a' coef | `[-]`
BarterAngrinessCoefWeightB | shopkeeper shop barter calculation 'b' coef | `[-]`
BarterCoefWeightA | shopkeeper shop barter calculation 'a' coef | `[-]`
BarterCoefWeightB | shopkeeper shop barter calculation 'b' coef | `[-]`
BarterDominanceChaBaseE | barter dominance calculation 'e' coef | `[-]`
BarterDominanceChaWeightC | barter dominance calculation 'c' coef | `[-]`
BarterDominanceRelationshipWeightB | barter dominance calculation 'b' coef | `[-]`
BarterDominanceSpcWeightA | barter dominance calculation 'a' coef | `[-]`
BarterDominanceSpcWeightD | barter dominance calculation 'd' coef | `[-]`
BarterPriceSellRepBuying | price sell vs buy mod | `[-]`
BarterPriceSellRepCoef | sell reputation coef | `[-]`
BarterPriceSellRepMultip | sell reputation multiplier | `[-]`
BaseAttackStaminaCost | how much stamina will attack cost | `[stamina]`
BaseDodgeStaminaCost | how much stamina will dodge cost | `[stamina]`
BaseInventoryCapacity | base inventory capacity | `[lb]`
BaseItemDisappearingTime | base game time for dropped items to auto disappear | `[s]`
BasketSuspiciencyHaggleThreshold | Haggle reaction 1 threshold (haggle more difficult) | `[-]`
BasketSuspiciencyNoDealThreshold | Haggle reaction 2 threshold (transaction refused) | `[-]`
BedQualityModificationCap | Bed quality modifiers (eg. perk buffs) can only increase the bed quality until this cap. | `[%]`
BestVisVolume | object volume for maximum recognition bonus | `[dm3]`
BigZoneDistanceSlotMod | temporary solution, slot mod for distance > 1 | `[-]`
BlackArtsApprenticeBuffEndTime | Time when buff for perk Black arts apprentice stop to be activated | `[h]`
BlackArtsApprenticeBuffStartTime | Time when buff for perk Black arts apprentice start to be activated | `[h]`
BlacksmithingAlmostCriticalQualityOffset | quality when workpiece is almost broken | -
BlacksmithingEffectivityToXP | effectiveness to XP gain | `[-]`
BlacksmithingFinishingXP | XP gained after minigame was successfuly finished when quality is maximum | -
BlacksmithingIntensityToStamina | stroke intensity to stamina drain | `[-]`
BlacksmithingMaxCompletionGainFactor | maximal completion gain per stroke | `[-]`
BlacksmithingMaxCondition | max condition of product | `[-]`
BlacksmithingMaxEffectivityToQualityLoss | max effectiveness for quality loss - loss is minimal | `[-]`
BlacksmithingMaxIntensity | maximal intensity value | `[-]`
BlacksmithingMaxQualityLossFactor | maximal quality loss per stroke | BlacksmithingMinTemperature `[-]`
BlacksmithingMaxTemperature | maximal temperature for max effectiveness | `[C]`
BlacksmithingMinCondition | min condition of product | `[-]`
BlacksmithingMinEffectivityToQualityLoss | min effectiveness for quality loss - loss is maximal | `[-]`
BlacksmithingMinIntensity | minimal intensity value | `[-]`
BlacksmithingMinTemperature | minimal temperature for any effectiveness | `[C]`
BlacksmithingMinimalCover | minimal cover value when stroke is 100 percent effective | `[%]`
BlacksmithingOverheatQualityLossCoef | coef for quality loss during overheating effect | -
BlacksmithingRhythmicBonus | percentual gain to effectivity when rhythmic bonus is active | `[%]`
BlacksmithingStamRegenMax | regen of stamina at maximal skill level | `[-]`
BlacksmithingStamRegenMin | regen of stamina at minimal skill level | `[-]`
BlacksmithingStrokeGain | stroke gain to potential | `[-]`
BlacksmithingStrokeLoss | stroke loss to potential | `[-]`
BlindViewRadiusFakeRelative | for blinded (mostly sleeping) NPC we have to calculate stealth XP somehow, so we calculate this fake radius | `[-]`
BlockingDmgRBonus | bonus for blocking weapon when dmgr is > 0 | `[-]`
BlockingDmgRCoef | dmgr coefficient for blocking weapon | `[-]`
BordererSprintBuffChargingDuration | Sprint time for which the BordererSprint buff is activated | `[s]`
BordererSprintBuffCooldownDuration | How long the BordererSprint buff is active after finishing sprint | `[s]`
BowAimStamCost | after painless delay, stam loss | `[%/s]`
BowChargeDurationMax | maximum duration of bow charge animation | `[s]`
BowChargeDurationMin | minimum duration of bow charge animation | `[s]`
BowPowerToChargeDuration | nominal charge duration for bow with power = 1 | `[s]`
BundleAlchemistPerkAdd | Addition of potions created with Bundle Alchemist perk | `[-]`
ButcheringBloodOffsetMin | AddedBlood when butchering = `animalWeight x bloodPerPound x bloodOffset`, bloodOffset is random between <ButcheringBloodOffsetMin; 1> . | `[]`
ButcheringBloodPerPound | For adding blood on player when butchering animal, `addedBlood = animalWeight x bloodPerPound x bloodOffset`. | `[]`
ButcheringMaxDistance | Butchering action is shown only when player is closer than this to the animal's bounding box. | `[m]`
CaffeineFromFoodCoef | how much caffeine is added from a unit refresh | `[caf/exh]`
CallActionCooldown | Minimum time until horse call action / stealth lure can be activated again | `[s]`
CarriedBodyMaxStamConsumption | uses encumberence to interpolate from 0 to this | `[-]`
CarriedBodyWeightCoef | how much of the carried body weight is added to the carried weight of the carrier | `[-]`
CarriedCarriedWeightCoef | how much of the carried weight of the carried NPC is added to the carried weight of the carrier | `[-]`
ChainmailCombinedFoleyThreshold | Play combined foley if chainmail is the second most important surface and covers this surface ratio | `[]`
CharismaMulOnExtremeExhaustion | Player will have this charisma multiplied by this value when he has exhaust equal to 0. Charisma will not be changed when exhaust is 50. Linear interpolation on multiplier is applied when exhaust is between 0 and 50; | `[%]`
ClassCourageMoraleWeight | Weight of soul class courage affecting morale | `[]`
CleanlinessIsNextToGodlinessWashHeal | Amount of health regenerated after washing | `[]`
ClinchBackOffDmgRWeight | formula from DLC-8619
ClinchBackOffSkillWeight | formula from DLC-8619
ClothesBloodSoakOnMaxBleeding | After how many seconds will clothing become completely bloody when bleeding with max intensity (the injury has bleeding value 1), speed at lower intensity is linearly interpolated (0 at intensity 0). | `[s]`
CoerceSkillcheckSpeechWeight | Weight of speech in coerce skillcheck | `[]`
CollisionDmgRBias | DmgR offset for collision hits. | `[-]`
CollisionVelocityDeltaToDmgR | &nbsp; | `[attack/ms-1]`
CombatActiveNPCRadius | When NPC is closer than the value Active combat icon is used else only Danger icon is set. | `[m]`
CombatAutoAggressionDiffScale | the bigger number the bigger difference in aggresion for skill differnce | `[-]`
CombatAutoAttackDelayIncreasePerAttacker | how many times is the period increased for each attacker | -
CombatAutoAttackDelayIncreasePerAttackerHorse | CombatAutoAttackDelayIncreasePerAttacker if the victim is on horse | -
CombatAutoAttackDelayIncreasePerAttackerMissile | CombatAutoAttackDelayIncreasePerAttacker if the victim has a missile wpn | -
CombatAutoAttackDelaySigma | attack delay variation | `[s]`
CombatAutoClinchAlternativeMaxProbability | prob of transition to alternative guard on max skill level | `[-]`
CombatAutoClinchAlternativeMinFencing | minimal fencing level for alternative guard | `[-]`
CombatAutoClinchReactionDelayMaxMax | maximal maximum | `[s]`
CombatAutoClinchReactionDelayMaxMin | maximal minimum | `[s]`
CombatAutoClinchReactionDelayMinMax | minimal maximum | `[s]`
CombatAutoClinchReactionDelayMinMin | minimal minimum | `[s]`
CombatAutoEasyZoneWeight | `[0-1]` how much are easy zones favored by the lame AI (1 = favored) | `[-]`
CombatAutoForcedComboStaminaLimit | stamina threshold | `[-]`
CombatAutoForcedPeriodicalAttackStaminaLimit | stamina threshold | `[-]`
CombatAutoGuardHysteresis | &nbsp; | `[m]`
CombatAutoLameGuardOffset | offset to max distance | `[m]`
CombatAutoMasterGuardOffset | offset to max distance | `[m]`
CombatAutoMaxAimDuration | the longest aim time for the lowest skill | `[s]`
CombatAutoMaxAimDurationRandomAdd | max random time added to the aim duration | `[s]`
CombatAutoMaxAtkDistOffset | offset from max attack distance defined in percentage from attack range | `[%]`
CombatAutoMaxAttackDelay | mean delay between attacks for a defensive AI | `[s]`
CombatAutoMaxHuntAttackDuration | maximal time the NPC is hunting/chasing | `[s]`
CombatAutoMinDefenseModeWeight | `[0-1]` the lowest weight for the defense mode | `[-]`
CombatAutoMinHuntAttackDuration | minimal time the NPC is hunting/chasing | `[s]`
CombatAutoMoveActivityDecreasePerAttacker | my activity decrease per opponents aditinal attackers | `[ma]`
CombatAutoMoveProficiencyHPCoef | HP coefficient for movement proficiency | `[-]`
CombatAutoMoveProficiencySkillCoef | Skill coefficient for movement proficiency | `[-]`
CombatAutoNPCOpponentAtkDelayCoef | shortening attack delay when opponent is npc | `[%]`
CombatAutoOppZoneAdaptDelayMaxMax | reaction delay maximal maximum | `[s]`
CombatAutoOppZoneAdaptDelayMaxMin | reaction delay maximal minimum | `[s]`
CombatAutoOppZoneAdaptDelayMinMax | reaction delay minimal maximum | `[s]`
CombatAutoOppZoneAdaptDelayMinMin | reaction delay minimal minimum | `[s]`
CombatAutoReactionDelayRangeSpread | of the maximal range | `[]`
CombatAutoScaleDefensivenessDelayRel | relative to attack delay, time to override defensiveness and go near | `[-]`
CombatAutoSyncRiposteWeight | KCD_TechDesignDefenseControl | `[]`
CombatAutoTrickAttackProb | `[0-1]` attack prob for the first step | `[-]`
CombatAutoTrickDelayVariability | added to the lower bound | `[s]`
CombatAutoTrickInvalidBlockAttackMaxProb | `[0-1]` max trick prob for a skilled AI if the block is invalid | `[-]`
CombatAutoTrickMaxProb | `[0-1]` max trick prob for the first step | `[-]`
CombatAutoTrickMinMaxDelay | lower bound of the max delay | `[s]`
CombatAutoTrickNoAttackProb | `[0-1]` no attack prob for the first step | `[-]`
CombatAutoTrickReactionMaxDelay | KCD_TechDesignDefenseControl | `[s]`
CombatAutoTrickReactionMinDelay | KCD_TechDesignDefenseControl | `[s]`
CombatAutoTrickReactionSkillWeight | KCD_TechDesignDefenseControl | `[]`
CombatAutoTrickReactionStaWeight | KCD_TechDesignDefenseControl | `[]`
CombatAutoZoneAdaptDefenseWeight | modifier for global adaptation weight dependent on defense | `[-]`
CombatAutoZoneAdaptMSWeight | modifier for MS adaption weight dependent on fencing | `[-]`
CombatAutoZoneAdaptMinDefense | minimal defense where npc begins some adaptation | `[-]`
CombatAutoZoneChangeDelayMaxMax | zone change timeout maximal maximum | `[s]`
CombatAutoZoneChangeDelayMaxMin | zone change timeout maximal minimum | `[s]`
CombatAutoZoneChangeDelayMinMax | zone change timeout minimal maximum | `[s]`
CombatAutoZoneChangeDelayMinMin | zone change timeout minimal minimum | `[s]`
CombatDangerCooldown | how long is the combat danger active after last enemy stops to be a threat | `[s]`
CombatDistanceFromStartPointForForcedUncertain | distance from the point where the combat started beyond which Uncertain is forced | `[m]`
CombatDmgRBonusFromBehind | multiplicative DmgR bohus for attacks from behind | `[-]`
CombatDodgeProb0 | KCD_TechDesignDefenseControl | `[]`
CombatDodgeProb1 | KCD_TechDesignDefenseControl | `[]`
CombatDodgeProbCoef | KCD_TechDesignDefenseControl | `[]`
CombatHitImmortalUnconsciousDepth | depth for immortal knock-out | `[depth]`
CombatHitUnconsciousDepth | depth after a combat hit | `[depth]`
CombatLevelMinToCombatRPGBonus | starting combat level for bonus in attack and health hit, KCD2-492146 | `[-]`
CombatLevelToRelativeAttackIncrease | relative attack increase for max combat level, KCD2-492146 | `[-]`
CombatLevelToRelativeHealthLossDecrease | relative health hit decrease for max combat level, KCD2-492146 | `[-]`
CombatMasterStrikePowTo | KCD_TechDesignDefenseControl | `[]`
CombatMasterStrikeProb0 | KCD_TechDesignDefenseControl | `[]`
CombatMasterStrikeProb1 | KCD_TechDesignDefenseControl | `[]`
CombatMoveApproachSprintMinStamina | do not allow sprint during the approach | `[sta]`
CombatNoBlockProb0 | KCD_TechDesignDefenseControl | `[]`
CombatNoBlockProb1 | KCD_TechDesignDefenseControl | `[]`
CombatNormalBlockProb0 | KCD_TechDesignDefenseControl | `[]`
CombatNormalBlockProb1 | KCD_TechDesignDefenseControl | `[]`
CombatPerfectBlockNPCvsNPCCoef | KCD_TechDesignDefenseControl | `[]`
CombatPerfectBlockOnRiposteCoef | KCD_TechDesignDefenseControl | `[]`
CombatPerfectBlockPowTo | KCD_TechDesignDefenseControl | `[]`
CombatPerfectBlockProb0 | KCD_TechDesignDefenseControl | `[]`
CombatPerfectBlockProb1 | KCD_TechDesignDefenseControl | `[]`
CombatPerfectBlockZoneDistanceCoef | KCD_TechDesignDefenseControl | `[]`
CombatSyncPerfectBlockProb0 | KCD_TechDesignDefenseControl | `[]`
CombatSyncPerfectBlockProb1 | KCD_TechDesignDefenseControl | `[]`
ComboHitCancelProb | prob to cancel combo when hit opponent | `[-]`
ComboMinProb | minimal combo prob when combo count > 0 | `[-]`
ComboMinSteps | minimal combo step count | `[-]`
ComboNextStepProbBlocked | combo prob dec when opponent blocks | `[-]`
ComboNextStepProbHit | combo prob dec when opponent hit | `[-]`
ComboNoActionNeutralProb | combo prob for no action | `[-]`
ComboPerComboProb | per combo prob increase | `[-]`
ComboStepPerFen | per fencing level step increase | `[-]`
ComboStepSyncActionMod | modifier of combo steps when attacker is in sync action | `[-]`
CompanionLegalizationPriceCoeficient | price multiplier for legalization of a companion | `[-]`
CompanionMerchantFeeCoeficient | price multiplier representing a percentage fee for the vendor | `[-]`
CompanionPriceReputationScale | reputation multiplier for price when bying/selling a companion | `[-]`
ConfiscateItemsInRadius | Items laying this far from the player will be considered when confiscating. | `[m]`
ControllerLockPickingAppropriateTolerance | gamepad/controller: the lock is considered too hard to pick, if the tolerance is smaller than this | `[-]`
ControllerLockPickingToleranceBaseCoef | gamepad/controller: lockpicking sweet spot size: base value | `[-]`
ControllerLockPickingToleranceDifficultyCoef | gamepad/controller: lockpicking sweet spot size: difficulty coefficient | `[-]`
ControllerLockPickingToleranceSkillCoef | gamepad/controller: lockpicking sweet spot size: skill coefficient | `[-]`
ControllerLockPickingToleranceSkillExpCoef | gamepad/controller: lockpicking sweet spot size: skill exponential coefficient | `[-]`
CorpseDisappearanceTimeDiscovered | time before an NPC corpse is hidden when discovered | `[seconds GameTime]`
CorpseDisappearanceTimeUndiscovered | time before an NPC corpse is hidden when undiscovered | `[seconds GameTime]`
CraftsmanshipXPOverride | Multiply XP gained for this skill | `[]`
CreativeSoulExhaustPerSec | Amount of rest added to player each second while in minigame with CreativeSoul perk | `[]`
CrimeDoorSoundMod | switch the perk state after this timeout | `[]`
CrossbowAimStamCost | stam loss | `[%/s]`
DamageToArmorStatus | for the stopping layer | `[status/damage]`
DamageToArmorStatusHigherLayers | for layers above the stopping layer | `[status/damage]`
DamageToArmorStatusLowerLayers | for layers below the stopping layer | `[status/damage]`
DamageToArmorStatusMinimalValue | minimal normalized Dmgr value for damage to armor calculations | `[-]`
DawnTime | Time when night ends, used by rpg (default 05:00) | `[h]`
DefaultLocationMonitorHysteresis | switch the state after this timeout | `[s]`
DefaultReadingQuality | Reading quality when doing nothing special (standing). | `[.]`
DefaultStateDeltaSpeed | any soul state regen / loosing speed | `[%/s]`
DefaultVisVolume | default item size-volume that have no visibility recognition penalty | `[dm3]`
DefaultWorldTimeRatio | default world time ratio useed to calculate game time ration in superspeed skiptime | `[-]`
DiceAntibustHighThreshold | if this threshold is lower than currentScore or scoreRatio use antibust right away | `[-]`
DiceAvailableCountWeight | weight by which available count is devided in double take | `[-]`
DiceBadgeUseThreshold | express in percentage how big should the gain be to use the set dice badge | `[-]`
DiceDoubleTakeMultiplier | double take value by which score is multiplied | `[-]`
DiceGameTypeScoreBeggar | Beggar game type score | `[-]`
DiceGameTypeScoreCardinal | Cardinal game type score | `[-]`
DiceGameTypeScoreCourtier | Courtier game type score | `[-]`
DiceGameTypeScoreCraftsman | Craftsman game type score | `[-]`
DiceGameTypeScoreEmperor | Emperror game type score | `[-]`
DiceGameTypeScoreKing | King game type score | `[-]`
DiceGameTypeScoreKnight | Knight game type score | `[-]`
DiceGameTypeScoreLord | Lord game type score | `[-]`
DiceGameTypeScoreMiner | Miner game type score | `[-]`
DiceGameTypeScoreNovice | Novice game type score | `[-]`
DiceGameTypeScorePeasant | Peasant game type score | `[-]`
DiceGameTypeScorePriest | Priest game type score | `[-]`
DiceGameTypeScoreSoldier | Soldier game type score | `[-]`
DiceGameTypeScoreWagoner | Wagoner game type score | `[-]`
DiceMultiplyingHighThreshold | if this threshold is lower than currentScore or scoreRatio use antibust right away | `[-]`
DiceSetDiceAbsoluteThreshold | Minimum score that has to be reached to use the set dice badge | `[-]`
DigestionSpeed | amount of food 'lost' per world-time second (global base value) | `[%/s]`
DistractVerticalViewLimit | While holding a decoy during the distract minigame, the player can only look this low or high. | `[deg]`
DmgRToHealthCoefA | &nbsp; | `[-]`
DmgRToHealthCoefB | &nbsp; | `[-]`
DodgeRelArmorLoadThreshold | relative armor load threshold for dodge distance computation | `[-]`
DodgeRelDistanceThreshold | relative distance threshold refering to DodgeRelArmorLoadThreshold | `[-]`
DogCommandMoraleThreshold | morale must be greater than this value for the dog to obey interactor commands | `[-]`
DogDisobeyMoraleThreshold | morale must be <= this value to disobey, set to -1 to disable the feature | `[mor]`
DogDisobeyTimeout | how long the dog will be unavailable after its morale reaches zero | `[s]`
DogDistractBarkTime | Time after which the dog spends barking after the initial wait | `[s]`
DogDistractFleeDistance | The distance the dog flees. | `[m]`
DogDistractFleeRadius | If an enemy comes any closer the dog flees. | `[m]`
DogDistractInitialWaitTime | Time after which the dog starts barking after starting the Distract objective | `[s]`
DogFoundEventHoundmasterXp | Amount of experience the player gets when dog found event during fast travel | `[]`
DogGuardAlarmRadius | Distance from enemy, where dog in Guard mode can start Alarm objective by itself | `[m]`
DogGuardAttackRadius | Distance from enemy, where dog in Guard mode can start MeleeCombat objective by itself | `[m]`
DogMoraleBuffAnimalKill | &nbsp; | `[mor]`
DogMoraleBuffContextCommand | &nbsp; | `[mor]`
DogMoraleBuffDistraction | &nbsp; | `[mor]`
DogMoraleBuffFeed | &nbsp; | `[mor]`
DogMoraleBuffFetch | &nbsp; | `[mor]`
DogMoraleBuffKill | &nbsp; | `[mor]`
DogMoraleBuffPOIDiscovery | &nbsp; | `[mor]`
DogMoraleBuffPlay | &nbsp; | `[mor]`
DogMoraleBuffPraise | &nbsp; | `[mor]`
DogMoraleBuffSigma | &nbsp; | `[mor]`
DogMoraleDecreaseWithoutInteraction | &nbsp; | `[mor/s]`
DogMoraleDecreaseWithoutInteractionFasterRelative | faster fadeout of buffed morale relative to the base speed | `[-]`
DogMoraleDefaultMax | default dog morale for maximal hound master skill | `[-]`
DogMoraleDefaultMin | starting value for morale (with lowest hound master skill) | `[-]`
DogMoraleEventBuffCooldown | how long it takes to recharge the buff | `[s]`
DogMoraleFromHitDamage | morale change for full health damage | `[mor]`
DogMoraleIncreaseSkipTime | how fast it grows during skiptime or fast-travel | `[mor/s]`
DogPOISearchRadiusMax | maximal search radius (for highest hound-maser) | `[m]`
DogPOISearchRadiusMin | minimal search radius (for lowest hound-maser) | `[m]`
DogTargetPriorityBoostCurrent | implements hysteresis (new target has to have higher priority) | `[m]`
DogTargetPriorityBoostEnemy | positive number will increase priority | `[m]`
DogTargetPriorityBoostPrey | positive number will increase priority | `[m]`
DogTargetSearchRadiusMax | maximal search radius (for highest hearing) | `[m]`
DogTargetSearchRadiusMin | minimal search radius (for lowest hearing) | `[m]`
DogXpAntiExploitTimeout | After this time the dog XP antiexploit mechanism resets. | `[s]`
DominateSkillcheckSpeechWeight | Weight of speech in dominate skillcheck | `[]`
DreadSkillcheckBloodinessWeight | Weight of bloodiness in dread skillcheck | `[]`
DreadSkillcheckDirtinessWeight | Weight of dirtiness in dread skillcheck | `[]`
DuringFaderHysteresis | the in-fader state is kept for how longer | `[s]`
DuskTime | Time when night begins, used by rpg (default 21:00) | `[h]`
EasyDifficultySkillcheckOpponentValue | Value of the opponent's skillcheck for which the skillcheck is considered easy in UI | `[]`
EncumberanceForSecondaryModifiers | when the buff will activate the secondary group | `[-]`
EncumberedToSpeedSurfaceCoef | Coef that controls terrain/surface influence in encumbered speed mod #encumbered | `[-]`
EquippedWeightSubWithWellWornPerk | when player has Well Worn perk, weight of items is lowered when they are equipped; `equippedWeight=standardWeight*(1.0 - EquippedWeightSubWithWellWornPerk)` | `[.]`
EventAmbushWeightDetectionResult | weight E for computing event ambush chance = `s*stealth + v*(1-visibility) + E*eventDetectionResult / (v+s+E)` | `[]`
EventAmbushWeightStealth | weight S for computing event ambush chance = `v*(1-visibility) + S*stealth + e*eventDetectionResult / (v+S+e)` | `[]`
EventAmbushWeightVisibility | weight V for computing event ambush chance =` V*(1-visibility)  + s*stealth + e*eventDetectionResult / (V+s+e)` | `[]`
EventConcealWeightRadiusVsVisibility | event concealment (how easily event detects player) is `[this weight x EVR + (1-weight) x player's visibility]`. must be <0-1> | `[]`
EventEvadeWeightDetectionResult | weight E for computing event evade chance = `v*(1-visibility) + s*survival + E*eventDetectionResult / (v+s+E)` | `[]`
EventEvadeWeightSurvival | weight S for computing event evade chance = `v*(1-visibility) + S*survival + e*eventDetectionResult / (v+S+e)` | `[]`
EventEvadeWeightVisibility | weight V for computing event evade chance = `V*(1-visibility) + s*survival + e*eventDetectionResult / (V+s+e)` | `[]`
EventFleeWeightDetectionResult | weight E for computing event flee chance = `v*vitality + E*(1-|eventDetectionResult|) / (v+E)` | `[]`
EventFleeWeightVitality | weight V for computing event flee chance =` V*vitality + e*(1-|eventDetectionResult|) / (V+e)` | `[]`
EventViewRadiusWeightVariantVsPlace | event view radius (EVR) is `[this weight x variant VR + (1-weight) x place VR]`. must be <0-1> | `[]`
ExhaustedPlayerEffectMaxMax | the longest interval between effects for high exhaust stat | `[s]`
ExhaustedPlayerEffectMaxMin | the longest interval between effects for low exhaust stat | `[s]`
ExhaustedPlayerEffectMinMax | the shortest interval between effects for high exhaust stat | `[s]`
ExhaustedPlayerEffectMinMin | the shortest interval between effects for low exhaust stat | `[s]`
ExhaustedThreshold | player will have the 'exhausted' debuff when 'exhaust' stat is lower or equal to this value (in percents) | `[%]`
ExhaustionSpeed | amount of energy/vigour 'lost' per world-time second (global base value) | `[%/s]`
ExteriorCrouchHysteresis | switch the perk state after this timeout | `[s]`
ExtremeExhaustionFaintAveragePeriod | How often (on average, in real time) should player faint when extremely exhausted (exhaust stat is on 0). | `[s]`
ExtremeExhaustionFaintDuration | Length of unconsciousness in seconds (world time), when player faints (due to having exhaust 0). | `[s]`
FTRadiusWeightViewRadiusVsSurvival | view radius of player during fast travel (how easily player detects event) is `[this weight x PVR + (1-weight) x player's survival]`. must be <0-1> | `[]`
FabricCombinedFoleyThreshold | Play combined foley if fabric is the second most important surface and covers this surface ratio | `[]`
FactionAngrinessDecayRate | Faction angriness decay rate. 1e-6 means decay 1->0 in about 12 days. | `[1/s]`
FactionAngrinessDelay | Time until an angriness change takes effect. | `[h]`
FactionAngrinessMaximum | Faction angriness maximum. | `[]`
FactionAngrinessMinimum | Faction angriness minimum. | `[]`
FactionAngrinessPropagationCoef | Faction angriness is propagated through space between factions. | `[]`
FactionAngrinessPropagationCutoff | Faction angriness propagation distance cutoff. | `[]`
FactionAngrinessPropagationScale | Faction angriness propagation distance scale. | `[]`
FactionRepWeight | Weight of player - faction reputation (reputation median) | `[]`
FallDamageEnabledNpcCombatCooldown | how long after combat with player NPC has enabled fall damage | `[s]`
FallDamageMultiplierAtMaxAgility | fall damage multiplier when agility is maxed out | `[-]`
FatalFallHeight | falling height above which fatal health damage is taken at agility 0 | `[m]`
FinestGoodsMinItemHealth | Minimum item health that is considered good in Finest Goods perk buff | `[]`
FoodFull | you are full | `[%]`
FoodHealSpeed | hp regen speed | `[%/s]`
FoodHealthThreshold | Health threshold for possitive/negative food effect | `[0-1]`
FoodOverEat | you cannot eat more | `[%]`
FoodPoisoningMaxHealthEffectSpeed | Maximum loose of health per sec for food poisoning | `[health/s]`
FoodPoisoningMaxStatPenalty | maximum temporary penalty for affected stats while food poisoning | `[stats penalty]`
FoodPoisoningMaxValue | Max amount of food poisoning | `[foodPoisoning]`
FoodPoisoningMinHealthEffectSpeed | minimum loose of health per sec for food poisoning | `[health/s]`
FoodPoisoningThreshold | threshold for food posioning to start taking affecting | `[foodPoisoning]`
FoodPreserverHealthIncreaseAmount | this amount is added to food's health when food preserver is applied | `[-]`
FoodSaltOrSmokePerkDecayModif | food decay perk modif | `[mod]`
FoodWitcherPerkNutritionModif | potion nutrition wicher perk modif | `[mod]`
FootstepSoundMultHeadroomFactor | multiply fsm before clamping to give it some headroom #perception | `[]`
ForcedFireAimSpreadMalus | spread added when the rpg forces the firing on low stamina | `[deg]`
FriskProbabilityMod | Modifier for the frisk probability | `[]`
FromBehindAngle | minimal angle to classify the attack as 'from behind' - 0 face, PI back | `[rad]`
FrozenRenownValue | Fixed value for frozen renown | `[]`
FullClothDirtyingOnFullSpeed | how far do we walk with full speed (1.0 walk speed) to get 100% dirty | `[m]`
FullClothDirtyingOnZeroSpeed | how far do we walk with half speed to get 100% dirty (other speeds than FullSpeed and HalfSpeed are linearly interpolated) | `[m]`
GeneralPropertyDiffToSkillCheckResult | > 0; scaled soul property diff for result = -1/1 | `[]`
GoodArmorDefense | mainly for AI, used to judge armor | `[defense]`
GoodWeaponAttack | mainly for AI, used to judge weapon | `[attack]`
GoodWeaponDefense | mainly for AI, used to judge weapon | `[defense]`
GoodWeaponDefenseCoef | block prob modifier when victim has good weapon defense | `[defense]`
GreatReputationIconThreshold | reputation threshold above which a faction will be very friendly with the player | `[]`
HardDifficultySkillcheckOpponentValue | Value of the opponent's skillcheck for which the skillcheck is considered hard in UI | `[]`
HarmlessFallHeight | falling height below which no health or stamina damage is taken at agility 0 | `[m]`
HeadHitKnockOutBaseProbability | for hits dealing a hp damage | `[]`
HealthDamageToInjury | note: health is `[0-100]` but injury is `[0-1]` | `[/%]`
HealthDeltaAbsLimit | abs max of health delta | `[hp/s]`
HealthFadingFromLimitValue | health percentage to activate health fading buff | `[-]`
HealthFull | maximum health | `[%]`
HealthToBadassnessMinCoef | multiplicative coef for health = 0 | `[-]`
HealthToKnockOut | threshold for unarmed combat, health cannot reach this level | `[hp]`
HearingToFov | an increase of FOV caused by the hea stat | `[deg/hea]`
HeavyLightArmorThreshold | should be between -MaxArmorLoad and MaxArmorLoad. #ArmorLoad | `[-]`
HeavyWeaponWeight | used to deduce 'attack weight' | `[lb]`
HerbGatherSkillToCount | multiplied by sqrt(skill level) to modify the number of collected herbs (#herb) | `[xp^-1]`
HerbGatherSkillToRadius | multiplied by skill level to calculate radius (#herb) | `[m/xp]`
HerbGatherSkillToRadiusAdd | modify the base radius of collected herbs at first skill level (#herb) | `[m]`
HerbGatherXP | final XP reward for one herb gathering(#herb) | `[xp]`
HerbsInHorseInventoryForHorsenipPerk | number of herbs in horse inventory needed for Horsenip perk to be active (#herb) | `[#]`
HerbsInInventoryForFlowerPowerPerk | number of herbs in inventory needed for FlowerPower perk to be active (#herb) | `[#]`
HighReputationIconThreshold | reputation threshold above which a faction will be friendly with the player | `[]`
HighbornWealthThreshold | social class wealth threshold for perks | `[]`
HoleDiggingDirtiness | Determines how dirty player will be after digging a hole/grave | -
HorseAttackMaxSpeed | speed of the attacking rider to gain maximal attack bonus | `[m/s]`
HorseDashBufferLength | Maximum length of the horse's dash buffer. | `[s]`
HorseDashSlowdownThreshold | The horse will start slowing down (from dash to sprint) if the dash buffer drops below this value. | `[s]`
HorseEquipHealthDecrease | status delta per traveled m | `[status/m]`
HorseEquipHealthUpdateDistance | horse equip health is update after traveling N m | `[m]`
HorseExhaustedStaminaLimit | If horse stamina falls bellow this level it becomes exhausted | `[]`
HorseForcedRearMoraleHitRange | Range of moral hit to nearby enemies, when you force rear on your horse. | `[m]`
HorseForcedRearingStaminaCost | stamina cost taken by forced rearing | `[-]`
HorseJumpHeightModifier | Horse Jump Height = wh_horse_JumpHeight * (vitality/30 + 1) * this. | `[-]`
HorseMagnetismTurnSlowdown | This is how much the horse's speed decreases during sharp turns when the road magnetizer is on. | `[%]`
HorseMaxAttackCoef | \[1,inf) maximal multiplicative coef a rider will gain when attacking on HorseMaxAttackSpeed | `[-]`
HorseMinFinalPrice | minimum horse price | `[groshen]`
HorseMoraleOverspurrHitAmount | Morale hit for each horse overspurr. | `[mor]`
HorseMoraleToThrowOffRider | if the horse mor is below this, it throws off the rider | `[mor]`
HorseMountMaxRelativeEncumberance | maximum allowed relative encumberance for player mounting a horse | `[%]`
HorseRidingAwardDistance | award xp for traveling some distance on horse | `[m]`
HorseRidingToHorseCourage | how the rider's horse riding skill increases courage of his horse | `[sta/lvl]`
HorseRidingToHorseStamina | how the rider's horse riding skill lowers sta consumption of his horse on max skill level | `[sta/lvl]`
HorseRidingXPOverride | Multiply XP gained for this skill | `[]`
HorseRidingXPPerDistance | horse riding xp gain after riding HorseRidingAwardDistance | `[-]`
HorseSlowSpeedStaminaRegen | The additional stamina that player's horse should regenerate in speeds smaller than sprint. | `[sta/s]`
HorseSlowdownTimeSlowSpeed | How long does it take forthe horse to start slowing down from run or walk if we do not hold any key. | `[s]`
HorseSlowdownTimeSprint | How long does it take for the horse to start slowing down from sprint if we do not hold any key. | `[s]`
HorseSlowdownTimeSprintIfDashed | How long does it take for the horse to start slowing down from sprint if it dashed previously. | `[s]`
HorseSpurDashIncrement | How much will rider's horse dash buffer increase per one spur. | `[s]`
HorseSpurDebuffLength | How long does the overspur debuff remain active. | `[s]`
HorseStaminaDrainPerSpurLevel | How much stamina the horse should lose per each exceeded level of spur. | `[sta/s]`
HorseWithMaxStatsPrice | price for a horse with all stats equal to the maximum possible stat value | `[groshen]`
HorseWithMinStatsPrice | price for a horse with all stats equal to zero | `[groshen]`
HorseridingSkillXPForKillFromHorseback | Amount XP to horseriding gained for killing opponent from horseback | `[xp]`
HoundmasterXPAnimalKill | dog companion master xp gain | `[xp]`
HoundmasterXPContextCommand | dog companion master xp gain | `[xp]`
HoundmasterXPDistraction | dog companion master xp gain | `[xp]`
HoundmasterXPFeed | dog companion master xp gain | `[xp]`
HoundmasterXPFetch | dog companion master xp gain | `[xp]`
HoundmasterXPHit | dog companion master xp gain | `[xp]`
HoundmasterXPKill | dog companion master xp gain | `[xp]`
HoundmasterXPOverride | Multiply XP gained for this skill | `[]`
HoundmasterXPPOIDiscovery | dog companion master xp gain | `[xp]`
HoundmasterXPPlay | dog companion master xp gain | `[xp]`
HoundmasterXPPraise | dog companion master xp gain | `[xp]`
HourglassTimeout | the time until all the sand goes down | `[s]`
HunterLootAmountAddCoef | add coef, the fixed portion (#hunter) | `[-]`
HunterXPKill | hunter skill XP gain after a kill, multiplied by the game db coef and level | `[xp]`
HunterXPLoot | hunter skill XP gain after a loot, multiplied by the game db coef and level | `[xp]`
HuntingAlarmSoundMaximalMultiplier | Maximal multiplier of hunting alarm sound loudness. | `[-]`
HuntingAlarmSoundMinimalMultiplier | Minimal multiplier of hunting alarm sound loudness. | `[-]`
HuntingAlarmSoundSkillToSmellRatio | How much more valuable is full skill than smell, when computing hunting alarm sound loudness | `[-]`
ImmortalHealthMin | min health for immortal souls | `[%]`
ImpressSkillcheckSpeechWeight | Weight of speech in impress skillcheck | `[]`
ImprovedSleepMultiplier | How much better better (Rest regeneration speed) is SleepImproved than Sleep buff. This buff is used for reading when player has perk InTheFlow. | `[.]`
InactiveTimeToDestroyOversleep | how long to let inactive oversleep buff survive (in game seconds) (we have this threshold so that the buff will not be destroyed right after being created in SkipTime class) | `[s]`
IndulgencePriceFactor | Multiply by total reconcile reputation improvement | `[]`
IndulgencePriceMax | Maximum indulgence price. | `[grosh]`
IndulgencePriceMin | Minimum indulgence price. 0 means no reconciliation necessary | `[grosh]`
InfoTextNotificationCooldown | cooldown for UI notification | `[s]`
InformationBroadcastDelay | Fresh information will broadcast only if it is at least this old. | `[min]`
InformationBroadcastIgnoreRadius | NPCs around the player will not receive information from periodic broadcasts. | `[m]`
InformationBroadcastPeriod | Information is broadcast in a faction subtree periodically after this amount of time. | `[day]`
InformationExpirationBase | Multiply by a modifier from crime table to get amount of time after which an information expires. | `[day]`
InformationVersionRefresh | If identical information is created after this amount of time, it is considered as new. | `[s]`
InjuringFallHeight | falling height above which health damage is taken at agility 0 | `[m]`
InjuryBleedingInterval | bleeding interval, the time required to lose 1HP | `[s]`
InjuryHighThreshold | limb is bleeding if above this threshold | `[-]`
InjuryLowThreshold | limb is considered healthy if below this treshold | `[-]`
InjuryRegenInterval | injuries fade-out, the time required to regen 1% of injury | `[s]`
InteriorCrouchHysteresis | switch the perk state after this timeout | `[s]`
InteriorDrunkHysteresis | switch the perk state after this timeout | `[s]`
InvestigatingNPCRadius | NPCs investigating this far from the player will trigger the Investigating icon. | `[m]`
IsCleanBuffMaxDirtiness | The maximum dirtiness that we consider the soul to be clean | `[]`
ItemDestroyProbabilityCoef | Maximal probability when item reached the lowest HP. | `[-]`
ItemDestroyProbabilityThreshold | Threshold determines HP value where prob is growing in the last quality interval. | `[-]`
ItemDisappearingMulti | multiplier 1/x - x limit(up/down) for item disappearing speed in extremes (cheap vs. expensive, small vs. large) | `[s]`
ItemHealthAlmostBrokenThreshold | Relative threshold where UI notification appears (stage 2). | `[-]`
ItemHealthDamagedBuffThreshold | Relative threshold where buff appears in HUD. | `[-]`
ItemHealthDamagedThreshold | Relative threshold where UI notification appears (stage 1). | `[-]`
ItemHealthOverlapCoef | Percentual overlap between two quality intervals. | `[-]`
ItemHealthPriceStatusWeight | item health status weight price coef | `[-]`
ItemOwnerDescFadeToSuspiciencyExp | basket suspiciency calculation | `[-]`
ItemOwnerFactionDistanceInnerRadius | basket suspiciency calculation: items stolen closer than this get max faction distance suspiciency | `[m]`
ItemOwnerFactionDistanceOuterRadius | basket suspiciency calculation: items stolen further than this get min faction distance suspiciency | `[m]`
ItemOwnerFactionDistanceToSuspiciencyMax | basket suspiciency calculation | `[-]`
ItemOwnerFactionDistanceToSuspiciencyMin | basket suspiciency calculation | `[-]`
ItemOwnerFadeCoefToSuspiciencyExp | basket suspiciency calculation | `[-]`
ItemOwnerFadeCoefToSuspiciencyMul | basket suspiciency calculation | `[-]`
ItemOwnerFadeConspicuousnessToHours | world time hours | `[h/con]`
ItemOwnerFadePriceToHours | world time hours per decigrosh | `[h/decigrosh]`
ItemOwnerIsShopkeeperToSuspiciency | basket suspiciency calculation | `[-]`
ItemOwnerNeverFadesToSuspiciency | basket suspiciency calculation | `[-]`
ItemOwnerRelationshipToSuspiciencyMin | basket suspiciency calculation | `[-]`
ItemOwnerSpatialFadeThreshold | If distance part of basket suspiciency calculation falls below this, the item is locally faded. Tune with ItemOwnerFactionDistanceToSuspiciencyMin in consideration. | `[-]`
ItemQualityDecreaseProbabilityCoef | Maximum probability when min health is reached (relatively to current interval). | `[-]`
ItemQualityDecreaseProbabilityThreshold | Threshold when probability of quality decrease begins grow (relatively to overlap). | `[-]`
ItsaTrapPerkStealthXp | XP gained to stealth skill after It's a trap perk activaction | `[xp]`
JailRecoveryDebuffDurationMultiplier | duration of JailRecovery debuff is calculated as jail duration * this multiplier | `[-]`
JailRecoveryDebuffMaxHours | hours spent in jail after JailRecovery debuff reaches its maximal values | `[h]`
JumpCostBase | stamina cost of one jump | `[-]`
LethalDmgR | DmgR that is known to cause death | `[-]`
LocalHeroInfamousReputationThreshold | above this rep local hero, under infamous | `[-]`
LockPickingAdequateTolerance | locks on a similar level as the player have adequate tolerance | `[-]`
LockPickingAgilityXP | xp to agility for each successful lock-pick | `[-]`
LockPickingAppropriateTolerance | the lock is considered too hard to pick, if the tolerance is smaller than this | `[-]`
LockPickingCursorShakeRangeMax | how much does cursor shake during lock picking (for max lock difficulty) | `[-]`
LockPickingCursorShakeRangeMin | how much does cursor shake during lock picking (for min lock difficulty) | `[-]`
LockPickingCursorShakeSpeed | how fast does cursor shake during lock picking | `[-]`
LockPickingFailRelativeXPMulCoef | multiplicative constant to derive XP reward relative to the success | `[-]`
LockPickingSkillToShakeRel | how much does the skill decrease the cursor shake (skill * this is relative to maximum/base) | `[xp^-1]`
LockPickingStealthXP | xp to stealth for each successful lock-pick | `[-]`
LockPickingSuccessXPDivCoef | constant used in the denominator to derive XP reward for a successfully opened lock | `[-]`
LockPickingSuccessXPMulCoef | multiplicative constant to derive XP reward for a successfully opened lock | `[-]`
LockPickingToleranceBaseCoef | lockpicking sweet spot size: base value | `[-]`
LockPickingToleranceDifficultyCoef | lockpicking sweet spot size: difficulty coefficient | `[-]`
LockPickingToleranceSkillCoef | lockpicking sweet spot size: skill coefficient | `[-]`
LockPickingToleranceSkillExpCoef | lockpicking sweet spot size: skill exponential coefficient | `[-]`
LockPickingTurnBackDivCoef | constant used in the denominator to derive the turnback speed of a lock | `[-]`
LockPickingTurnBackMulCoef | multiplicative constant to derive the turnback speed of a lock | `[-]`
LockpickingFailSoundIntensity | one-shot intensity relative to the database | `[inten]`
LockpickingLockpickBreakChance | base lockpick break chance | `[inten]`
LockpickingRelDistanceToSoundIntensity | how relative distance influences sound | `[inten/dist]`
LockpickingSoundIntensityMin | minimal multiplier the lockpicking minigame will generate | `[-]`
LowHealthThreshold | threshold for low health effects (for npcs) | `[%]`
LowReputationIconThreshold | reputation threshold above which a faction will be little hostile to the player | `[]`
MajorFailSkillCheckLevel | everything below this level from the given range is considered a Major Fail | `[]`
MajorSuccessSkillCheckLevel | everything above this level from the given range is considered a Major Success | `[]`
MarksmanshipSkillXPShootingTargetHitPerDistance | Amount XP to marksmanship gained for shooting target | `[xp]`
MatPierceableMaxArmor | armor of a rock-solid material | `[]`
MatPierceableMin | OBSOLETE: projectiles with stab damage can stab into | `[]`
MatPierceableReduction | armor reduction per one point of piercability | `[]`
MaxAggregatedItemAmountPerPoison | maximum number of aggregated items affected when applying a single poison | `[mod]`
MaxAgilityToMovementSpeedAddition | max positive addition (for maximal vit), the same amount is subtracted on level 0 | `[-]`
MaxArmorLoad | #ArmorLoad | `[-]`
MaxAttackSpeedMod | maximal relative change in the attack speed for NPC vs player | `[-]`
MaxAttackSpeedNpcVsNpcMod | maximal relative change in the attack speed for NPC vs NPC | `[-]`
MaxAttackSpeedPlayerMod | maximal relative change in the attack speed for player vs NPC | `[-]`
MaxBaseInventoryCapacity | Base maximum of inventory capacity without taking the archetype multiplier into account | `[lb]`
MaxCloudAverageForShiningArmor | used by perk Knight in a shining armor; this is maximal current cloud average that still allows this perk to be active | `[.]`
MaxCourageMoraleContextFadingMod | how much can courage affect morale context fading | `[]`
MaxDamage | all stam and health damages are clamped | `[-]`
MaxEncumberanceXPAwardDistance | Distance that has to be covered while encumbered by at least double of carry weight to get StatXPStrAndVitPerDistanceEncumbered (linear interpolation with EncumberanceXPAwardDistanceMin). | `[m]`
MaxFencingWeaponUsageMod | relative weapon status damage for max fencing | `[-]`
MaxHearingSoundAttenuationCoef | minimal attenuation for non-zero hearing stat | `[-]`
MaxItemDisappearingTime | max game time for dropped items to disappear | `[s]`
MaxModConspicuousness | final modified conspicuousness stat maximum (the most conspicuous actor) | `[con]`
MaxModVisibility | final modified visibility stat maximum (the most visible actor) | `[vis]`
MaxMorale | max deriv stat value | `[cou]`
MaxPedalCost | pedaling STA cost (pressure 1) | `[stam]`
MaxPerfectBlockSlotModifier | modifier of PB slot window - determined as (`t_hit - t_pbslot`) from attack * this value. | `[%]`
MaxPerkPoints | total number of perk points player will gain per stat/skill | `[-]`
MaxSlashBuffApplyChance | chance to apply buff on slash when giving max hp damage | `[-]`
MaxSmashBuffApplyChance | chance to apply buff on smash when giving max hp damage | `[-]`
MaxSpecialPerfectBlockSlotModifier | modifier of SPB slot window - determined as (t_hit - t_pbslot) from attack x this value. | `[%]`
MaxStabBuffApplyChance | chance to apply buff on stab when giving max hp damage | `[-]`
MaxStaminaDamage | max stamina damage | `[-]`
MaxStaminaDmgR | max DmgR for stamina | `[-]`
MaxStatToAttackMult | maximal relative attack multiplier (for a high stat) | `[-]`
MaxStatToAttackStaminaCostMult | max stamina cost mult for a low stat | `[-]`
MaxStatToAttackStaminaCostStatDiff | stat difference for max/min cost multiplier | `[stat]`
MaxStatToAttackStatDiff | stat difference for max/min relative attack multiplier | `[stat]`
MaxStealthHitSoundMultiplier | intensity multiplier for min stealth level | `[]`
MaxViewRadius | the maximal view radius a superman NPC will have | `[m]`
MaxWeaponBuffCharge | max number of uses | `[-]`
MaxWeatherSoundAttenuationCoef | 0 - allow weather conditions to mute the sounds, 1 - no influence | `[-]`
MaximalItemQualityForDamage | Maximal quality of item which is counted to the item damage (for decal visualization). | `[-]`
MediumDifficultySkillcheckOpponentValue | Value of the opponent's skillcheck for which the skillcheck is considered moderate in UI | `[]`
MetabolismAbsorbSpeed | food/alcohol metabolised(removed) in world time | `[s]`
MetabolismDigestSpeed | food/alcohol digested(added) in world time | `[s]`
MetabolismDigestSpeedMultiplier | accelerate digest speed multiplier to_digest = max_poisoning | `[]`
MinAnimalWeightToWithstandGunshot | Animals that weigh less than this will be turned into bloody mess by gunshot and have a special inventory assigned instead of their regular loot inventory. | `[lb]`
MinDmgR | min DmgR | `[-]`
MinEncumberanceXPAwardDistance | Distance that has to be covered while minimally encumbered to get StatXPStrAndVitPerDistanceEncumbered (linear interpolation with EncumberanceXPAwardDistanceMax). | `[m]`
MinHealthToBeAbleToSleepOrSkiptime | player will not be able to go sleep or skiptime if his health would go under this threshold during the sleep or skiptime | `[%]`
MinLeftoverPerks | preferred number of leftovers | `[-]`
MinLevelForPerkPoints | at what minimum level will perk points be earned | `[-]`
MinModConspicuousness | final modified conspicuousness stat minimum (the least conspicuous actor) | `[con]`
MinModVisibility | final modified visibility stat minimum (the most invisible actor) | `[vis]`
MinMorale | min deriv stat value | `[cou]`
MinPedalCost | pedaling STA cost (pressure 0) | `[stam]`
MinPerfectBlockSlot01 | the smallest PB slot for the lowest level | `[-]`
MinPerkPoints | no leftovers if the number of perk points would be <= than this | `[-]`
MinPossibleSleepTime | player will reject to lie into bed when he will not be able to sleep at least this long (due to bleeding/hunger/etc, in hours) | `[h]`
MinRelativeStaminaMax | short-term stamina maximum relative to long-term maximum | `[-]`
MinStaminaDamage | min stamina damage | `[-]`
MinStaminaDmgR | min DmgR for stamina | `[-]`
MinStatToAttackMult | minimal relative attack multiplier (for a low stat) | `[-]`
MinStatToAttackStaminaCostMult | min stamina cost mult for a high stat | `[-]`
MinStealthHitSoundMultiplier | intensity multiplier for max stealth level | `[]`
MinTrueRelationDistThreshold | minimal distance required to see the true faction #perception | `[-/skill]`
MinViewRadius | the minimal view radius an almost blind NPC will have, also threshold for instant detection | `[m]`
MinViewRadiusFogCoef | Relative impact of fog on view radius will not be worse than this. | `[-]`
MinViewRadiusTimeOfDayCoef | Relative impact of night on view radius will not be worse than this. | `[-]`
MinWeaponBuffCharge | max number of uses | `[-]`
MissileWeaponDamageStatus | how missile weapon is damaged after each shot | `[status]`
MoraleContextFadingSpeed | Speed of Morale context increasing/decreasing to 0 | `[]`
MoraleDecisionReliability | Reliability of morale checks | `[]`
MoraleForCombat | how much must an NPC have to not flee from combat | `[]`
MoraleLinearShiftBase | Biasing of morale checks | `[]`
MoraleLinearShiftFactor | Biasing of morale checks | `[]`
NPCRepWeight | Weight of player - npc reputation (reputation median) | `[]`
NPCRobbedValueBottomThreshold | If the robbed value drops to this threshold, it is no longer considered noteworthy. | `[grosh]`
NPCRobbedValueDecayRate | Decay rate of value of items stolen from a NPC. | `[grosh/h]`
NPCSpawnMinDistanceFromPlayer | distance from player below which a corpse will never disappear or respawned NPC appear | `[m]`
NervousnessCourageousWeight | Courageous characters only get this much of each nervousness change. <0, 1>. | `[]`
NervousnessDecayRate | Nervousness decay rate. 1e-5 means decay 1->0 in about 1 day. | `[1/s]`
NervousnessMaximum | Nervousness maximum. | `[]`
NervousnessMinimum | Nervousness minimum. | `[]`
NervousnessPropagationCoef | Nervousness is propagated through space between NPCs. | `[]`
NervousnessPropagationRadius | Nervousness propagation radius. | `[m]`
NeutralReputationIconThreshold | reputation threshold above which a faction will be neutral to the player | `[]`
NeverSurrenderBuffHealthThreshold | HP threshold when NeverSurrender buff triggers | `[%]`
NightTransitionPeriod | Symmetric offset to dusk / dawn time. | `[h]`
NonPlayerRecognitionTimeMod | Multiple recognition time of everything but the player | `[]`
NonSkillBookXP | XP rewarded for reading non-skill books | `[xp]`
OverallArmorDefenseBadassWeight | Weight of normalized oad affecting badassness | `[]`
OverallStatsBaddassWeight | Weight of stats affecting badassness | `[]`
OverallWeaponAttackBadassWeight | Weight of normalized attack affecting badassness | `[]`
OverreadnessEmptyTime | how long (in game hours) does it take to empty the oversleepness stat (time player have to be not reading to be able to read max time again) | `[h]`
OverreadnessFillTime | how long (in game hours) does it take to fill the oversleepness stat (max time player can read) | `[h]`
OversleepnessEmptyTime | how long (in game hours) does it take to empty the oversleepness stat (time player have to be awake to be able to sleep max time again) | `[h]`
OversleepnessFillTime | how long (in game hours) does it take to fill the oversleepness stat (max time player can sleep) | `[h]`
PerceivedSocialClassImportanceThresholdRel | social class items must occupy more than this for the soul to look like the social class #perception | `[-]`
PerceivedStateRecognitionDistanceMax | Beyond this relative distance in the perception cone all perceived states are never recognized. | `[-]`
PerceivedStateRecognitionDistanceMin | At this relative distance in the perception cone all perceived states are recognized immediately. | `[-]`
PerceivedStateThreatDistance | Anyone closer than this with a drawn weapon is considered a threat. | `[m]`
PerceivedSuperfactionImportanceThresholdRel | superfaction items must occupy more than this for the soul to look like the superfaction #perception | `[-]`
PerceptionBaseCha | target priority estimation, #perception | `[]`
PerceptionInnerConeMaxRelSize | Maximal relative size of perception inner cone. #perception | `[-]`
PerceptionInnerConeMinRelSize | Minimal relative size of perception inner cone. #perception | `[-]`
PerceptionInnerConeNervousnessLimit | When nervousness reaches this value the inner cone should be the largest. #perception | `[-]`
PerceptionMaxFov | the maximal field of view a superman NPC will have | `[deg]`
PerceptionMeanDist | target priority estimation, #perception | `[]`
PerceptionMinFov | the minimal field of view a deaf NPC will have | `[deg]`
PerceptionPriorBoostPlayer | boost for player #perception | `[]`
PerceptionPriorBoostRangedWeapon | boost for ranged weapons (multiplied by PriorWeapon!), #perception | `[]`
PerceptionPriorBoostScriptContext | Boost perception priority from soul A to soul B defined by a script context. | `[]`
PerceptionPriorCha | target priority estimation, #perception | `[]`
PerceptionPriorConsp | target priority estimation, #perception | `[]`
PerceptionPriorCrimeCarryCorpse | priority boost for crime #perception | `[]`
PerceptionPriorCrimeLockpick | priority boost for crime #perception | `[]`
PerceptionPriorCrimeLoot | priority boost for crime #perception | `[]`
PerceptionPriorDead | dead or unconscious, #perception | `[]`
PerceptionPriorDist | target priority estimation, #perception | `[]`
PerceptionPriorEnemyRelationship | target priority estimation, #perception | `[]`
PerceptionPriorEnemyRelationshipBonus | target priority estimation, #perception | `[]`
PerceptionPriorFriendRelationship | target priority estimation, #perception | `[]`
PerceptionPriorGender | target priority estimation, #perception | `[]`
PerceptionPriorNotHumanRace | target priority estimation, #perception | `[]`
PerceptionPriorVisCrimes | target priority estimation, #perception | `[]`
PerceptionPriorVisItems | target priority estimation, #perception | `[]`
PerceptionPriorVisPeople | target priority estimation, #perception | `[]`
PerceptionPriorWeapon | target priority estimation, #perception | `[]`
PerceptionSecondaryCrowdMembers | When the crowd around player is this large they become invisible for secondary perception | `[alive humans]`
PerceptionSecondaryCrowdRadius | People this far from the player are considered a crowd for secondary perception | `[m]`
PerceptionSecondaryDecayTime | Amount of time needed for NPCs to become unaware of the player after secondary perception drops to 0 | `[s]`
PerfectionistAchievementIncomeLimit | income needed to unlock Perfectionist achievement | `[groshen]`
PerkBalancedDietActivationTime | hours until BalancedDiet perk bonuses are activated | `[h]`
PerkBloodRushDuration | duration of BloodRush perk bonuses after an enemy is killed with melee weapon | `[s]`
PerkBrutusCombatDmgRBonusFromBehind | brutus perk multiplicative base Dmg (CombatDmgRBonusFromBehind) | `[]`
PerkCarriedBodyGravediggerWeightMul | carried body weight multiplier for gravedigger perk | `[-]`
PerkChainStrikeMaxChain | maximal successive strikes | `[-]`
PerkLastGaspCooldown | how fast can the perk be activated again | `[s]`
PerkLastGaspLongTermCooldown | how fast can the perk be activated again | `[s]`
PerkLastGaspShortTermDuration | how long the buff stays on the player | `[s]`
PerkLuckyFindTriggerChance | Chance that a random item will be found | `[]`
PerkManlyOdourDirtinessThreshold | above this dirtiness manly odour perk bonuses are activated | `[-]`
PerkNoRestForTheWickedCooldown | how fast can the perk be activated again | `[s]`
PerkNoRestForTheWickedStaminaLimit | If horse stamina falls bellow this level the perk can be activated | `[]`
PerkRageDuration | how long are buffs active after the perk is triggered | `[s]`
PerkRageHealthThreshold | activation health | `[%]`
PerkTauntAttackerMoraleMultiplier | multiplier for 'combat_dodge_attacker' morale change when victim has Taunt perk | `[-]`
PerkUndauntedCavalierCharismaLimit | minimal charisma for Undaunted cavalier perk activation | `[-]`
PerkVeteranChargeCount | Number of charges for Veteran z kosova pole perk. | `[]`
PersuadeSkillcheckSpeechWeight | Weight of speech in persuade skillcheck | `[]`
PicklockDmgSpeed | how fast is picklock durability decreasing (will be multiplied by the relative distance) | `[dmg/s]`
PickpocketingAllTilesUncoveredAtSkill | If thievery is higher than this, all tiles in rosette will be uncovered from the start. | `[-]`
PickpocketingAngleChancePenalty | penalty in (0-1) to chance pickpocketing for each angle from optimal possition exactly from behind victim (180 max) | `[%]`
PickpocketingComradePerkBonus | max bonus in (0-1) to pickpocketing for comrade perk | `[%]`
PickpocketingDistance | Max pickpocketing range (not starting interactor range) | `[m]`
PickpocketingFailXPMod | XP modified on fail | `[-]`
PickpocketingIndicatorSharpness | 0 - precise slow change, 1 - sharp change | `[]`
PickpocketingItemUncoverTimePerWeight | time to uncover item per weight unit | `[s]`
PickpocketingLooterPerkExtraMoneyRewardMax | Max extra money reward from pickpocketed victim (also depends on victim social class) | `[-]`
PickpocketingLooterPerkExtraMoneyRewardMin | Min extra money reward from pickpocketed victim | `[-]`
PickpocketingMaxSkillChargeSpeedRatio | charge speed ratio boost with best skill | `[s]`
PickpocketingMaxSkillChargeTime | max charge time with best skill | `[s]`
PickpocketingMinChargeTime | min charge time needed | `[s]`
PickpocketingMisstargetingTolerance | Time tolerange for temporary misstargeting your victim. | `[ms]`
PickpocketingNPCDrunkTimeChanceMod | Modifies TimeChancePenalty when drunk | `[-]`
PickpocketingNPCHurtTimeChanceMod | Modifies TimeChancePenalty when hurt | `[-]`
PickpocketingNPCSleepingTimeChanceMod | Modifies TimeChancePenalty when sleeping | `[-]`
PickpocketingOneTileUncoveredAtSkill | If thievery is higher than this but lower than PickpocketingThreeTilesUncoveredAtSkill, one random tile in rosette will be uncovered from the start. | `[-]`
PickpocketingRandomChanceRollMinCap | Worst random rolls will alawys be capped to this minimum change 0-1 | `[%]`
PickpocketingRobbedAngrinessChancePenalty | penalty in (0-1) to pickpocketing chance for each time victim was robbed before | `[%]`
PickpocketingRosetteMaxSpeed | Speed of moving between two rosette tiles at max thievery skill (speed is linearly interpolated between min and max by thievery). | `[s]`
PickpocketingRosetteMinSpeed | Speed of moving between two rosette tiles at minimal thievery skill (speed is linearly interpolated between min and max by thievery). | `[s]`
PickpocketingStartedAgilityXP | XP to agility for starting pickpocketing | `[xp]`
PickpocketingStealthXP | XP to stealth for each successful pickpocketing | `[-]`
PickpocketingThreeTilesUncoveredAtSkill | If thievery is higher than this but lower than PickpocketingAllTilesUncoveredAtSkill, three random tiles in rosette will be uncovered from the start. | `[-]`
PickpocketingTimeChancePenaltyBest | penalty in pickpocketing chance in best case (s) | `[%]`
PickpocketingTimeChancePenaltyWorst | penalty in pickpocketing chance in worst case (s) | `[%]`
PickpocketingTreasurePriceXP | additional XP gain calculated by stolen items total value | `[xp/value]`
PickpocketingXP | XP for each successful pickpocketing | `[-]`
PlateCombinedFoleyThreshold | Play combined foley if plate is the second most important surface and covers this surface ratio | `[]`
PrimaryStatXPShootingTargetHitPerDistance | Amount XP to primary stat gained for shooting target | `[xp]`
ProjectileMaxBreakProb | probability of breaking an arrow if a rock-solid material is hit | `[]`
QuestMoneyRewardScaleConstant | scale constant for quest reward item amount | `[-]`
RPGContextInjuredHealthThreshold | Health threshold that soul is considered as injured | `[-]`
RPGContextSkillIntervalVariationRelative | Variation of skill intervals when computing current skill | `[%]`
RangedWpnCosThetaToAttackMin | cos(theta) lieary lowers the attack in the range `[this,1]` | `[-]`
RangedWpnLimbResistanceEffect | Determines how much limb resistance affects arrow speed. No effect at zero. At 100, the formula becomes basically arrowWeight/limbResistance. | `[-]`
RangedWpnMinPowerCoef | the power coef for a really weak soul (the stats are far below requirements) | `[-]`
RangedWpnMinStrCoef | if the curr/req strength ratio goes below this, the power is minimal, GDD: 25/222 | `[-]`
RangedWpnOptimalDistanceToMinamal | ratio between the database attack distance and the minimal range for the AI | `[-]`
RangedWpnPowerConstA | used to convert strength requirements to the resulting power, GDD: 25/222 | `[-]`
RangedWpnPwrToEnergy | Coefficient weapon draw length to energy (lb-to-N (4.44) * drawlength (50cm) / 2 (aproximates the loss of draw weight over draw length) ) | `[-]`
RangedWpnPwrToSpeed | total power to launch speed | `[m/s]`
RangedWpnRadiusForMoraleHit | Morale hit radius from gunshot fire. | `[m]`
RangedWpnSelfHarmCoef | Special constant used in self harm equation. | `[-]`
RangedWpnSpeedToAttack | attack mod deduced from impact speed | `[s/m]`
RangedWpnWeightNormalization | Average arrow weight, used to normalize damage. | `[g]`
RazorSharpBuffHealthThreshold | Buff on sharpened weapon will not be functional under this item health | `[-]`
ReadingSpeechXPBase | how much base xp in speech player gets after reading a book | `[xp]`
ReadingSpeechXPScholarshipMultiplier | after reading a book, player gets speech xp based on scholarship | `[xp]`
ReadingXpPerHour | how much xp in reading skill player gets after one hour of reading with reading speed 100% | `[xp]`
RecognitionSpeedNotVisible | must be negative, how the recognition is decreased | `[recog/s]`
RecognitionTimeDistanceGain | perlin gain for the distance influencing the recognition time | `[-]`
RecognitionTimeKNegativeCoef | multiplicative coef for negative values of conspicuousness #perception | `[s/vib]`
RecognitionTimeKPositiveCoef | multiplicative coef for positive values of conspicuousness #perception | `[s/vib]`
RecognitionTimePCoef | recognition time for a character with conspicuousness = 0 | `[s]`
RelationshipToGeneralSkillCheck | `[0,inf]`: how much is the repuation used to raise a general skill | `[]`
RelationshipToImpressCharisma | `[0,inf]`: how much is the repuation used to raise charisma | `[]`
RelationshipToPersuadeSpeech | `[0,inf]`: how much is the repuation used to raise speech | `[]`
RelationshipToThreatenBadassness | `[0,inf]`: how much is the repuation used to raise badassness | `[]`
RepairKitCapacity | Repair kit capacity to repair | `[grosh]`
RepairKitItemPerkBuffHealthThreshold | Buffs added by repair kit perks wont be functional under this item health | `[-]`
RepairKitMaxSkillCapacityCoef | Max skill coef for repair kit total capacity. | `[-]`
RepairKitMinSkillForQuality2 | Minimal skill to repair item of quality 2 with repairkit. | `[-]`
RepairKitMinSkillForQuality3 | Minimal skill to repair item of quality 3 with repairkit. | `[-]`
RepairKitMinSkillForQuality4 | Minimal skill to repair item of quality 4 with repairkit. | `[-]`
RepairPriceModif | Default repairing shop price modif | `[-]`
RepairShopMinSkillForQuality2 | Minimal skill to repair item of quality 2 in shop. | `[-]`
RepairShopMinSkillForQuality3 | Minimal skill to repair item of quality 3 in shop. | `[-]`
RepairShopMinSkillForQuality4 | Minimal skill to repair item of quality 4 in shop. | `[-]`
RepairShopSkillPriceMultiplier | Ratio between skill of shopKeeper and repair price increase | `[-]`
ReputationPropagationBiasTime | random bias to propagation time (world time) | `[s]`
ReputationPropagationCoefCap | Maximum propagation from faction to its parent | `[coef]`
ReputationPropagationTime | propagation time from npc to faction/superfaction (world time) | `[s]`
ReputationSpatialPrapagation | mod amount propagated to nearby factions | `[m]`
ReputationSpatialPropagationDistance | max distance to propagate reputation to nearby factions | `[m]`
ResetNearbyRelationshipRange | range for relationship reset | `[]`
ResetPublicFriendsRelationshipMin | minimal relationship for the alied forces after reset | `[]`
RespawnPeriod | a dead soul is respawned after this many days after death | `[days WorldTime]`
RespawnPeriodPublicEnemies | see RespawnPeriod, used for souls from factions that are public enemies | `[days WorldTime]`
RestockPeriodSoul | How many days it takes to fully restock a soul's inventory from nothing to its default items. 0 to disable. | `[day]`
RestockRepairPerDay | Automatically repair default non-player items by this many % (up to their default value). | `[%]`
RevenantBuffMaxHealthRegeneration | Up to what percentage will regenerate health in revenant perk | `[]`
RiderAgilityToHorsePullDown | relative rider agility to horse pull down | `[-]`
RiderBaddassWeight | Weight of relative rider skill affecting badassness | `[]`
RiderDogThreatToHorseMoraleRelative | relative to RiderThreatToHorseMorale | `[-]`
RiderForcedRearingStaminaCost | stamina cost taken by forced rearing | `[-]`
RiderHorseStaminaCoef | the ratio between stamina consumption of a horse and its rider | `[-]`
RiderSkillToHorsePullDown | relative riding skill skill to horse pull down | `[-]`
RiderThreatToHorseMorale | morale decrease per one rider threat | `[mor]`
RifleAimStamCost | stam loss | `[%/s]`
RifleDestroyDamage | HP damage to the user when riffle is destroyed. | `[hp]`
RunSpeedBaseGuiMax | Maximum value in transformation function of run speed to GUI | `[-]`
RunSpeedBaseGuiMaxHorse | Maximum value in transformation function of run speed to GUI for horse | `[-]`
RunSpeedBaseGuiMin | Minimum value in transformation function of run speed to GUI | `[-]`
RunSpeedBaseGuiMinHorse | Minimum value in transformation function of run speed to GUI for horse | `[-]`
SchedulerDrunkednessPerSecond | Amount of drunkedness gained per second through scheduler effect. | `[drunk%/s]`
SchedulerHealPerSecond | Amount of HP healed every second that scheduler healing effect is active. | `[HP/s]`
SchedulerSoilPerSecond | Amount of dirt gained per second through scheduler effect. | `[dirt/s]`
SecondaryStatXPRatio | secondary weapon stat ratio | `[-]`
SecondaryStatXPShootingTargetHitPerDistance | Amount XP to secondary stat gained for shooting target | `[xp]`
SharpeningFullNegativeHealthXP | &nbsp; | `[xp]`
SharpeningFullPositiveHealthXP | &nbsp; | `[xp]`
SharpeningMaxDestructionAngle | `[0,1]` | `[stam]`
SharpeningMaxIdealAngle | `[0,1]` | `[stam]`
SharpeningMinDestructionAngle | `[0,1]` | `[stam]`
SharpeningMinEfficiencyHealth | health you can achieve with the worst efficiency | `[-]`
SharpeningMinIdealAngle | `[0,1]` | `[stam]`
SharpeningSuccessfulConditionDelta | change in weapon condition at which the sharpening is considered successful | `[-]`
SharpeningWeaponBouncingMaxOffset | Maximum angle offset that is set to rotation of the weapon `[0,1]` | `[-]`
SharpeningZoneConditionForPerkEffects | At which item zone condition the perk effects are applied `[0,1]` | `[-]`
ShoeHealthDecrease | status delta per traveled m | `[status/m]`
ShoeHealthUpdateDistance | shoe health is update after traveling N m | `[m]`
ShopLargeTransaction | Percentage of total price of default items, if player spends more than this amount of money, large transaction barks are played. | `[%]`
ShortTermNutritionDigestionSpeedMultiplier | digestion multiplier for part of the food with low nutrition value | `[-]`
SimpleDrunkednessFadeSpeed | Amount of drunkedness faded per second for SimpleDrunkedness | `[drunk%/s]`
SkillCap | max skill level, also effects of a general skill are maximal at this level | `[skill]`
SkillDiffToAttackSpeed | relative attak speed gain for one skill level difference | `[speed/skill]`
SkillToDefense | GDD: 23/218 | &nbsp; | `[-]`
SkillToDmgConstA | &nbsp; | `[-]`
SkillToFencingBase | a1 of the geometric progression | `[-]`
SkillToPerfectBlockPowTo | slot = relativeSkill ^ this, see GDD: #defense | `[-]`
SkillToRangedWpnAIRange | how the relative skill influences the weapon range for the AI | `[-]`
SkillXPBlock | XP gain after a successful block | `[-]`
SkillXPComboHit | weapon XP gain after a hit in a combo | `[-]`
SkillXPDrinkAlcohol | XP gain per 1 alcohol content drinked | `[-]`
SkillXPHit | weapon XP gain after a hit | `[-]`
SkillXPKill | weapon XP gain after a kill see GDD: 42/218 | `[-]`
SkillXPLevelBase | base value (additive) to calculate XPs needed for the next level #level | `[-]`
SkillXPLevelDiff | multiplicative value to calculate XPs needed #level | `[-]`
SkillXPPerfectBlock | XP gain after a successful perfect block | `[-]`
SkillXPRiposte | successful riposte (attack after perfect block) | `[-]`
SkillXPSkillCheckFail | skill xp gain for a skillcheck fail | `[xp]`
SkillXPSkillCheckSuccess | skill xp gain for a skillcheck success | `[xp]`
SkillXPUseRepairKit | XP gain per 1 health repaired by repairkit | `[-]`
SkillcheckReputationPenalty | If below this reputation the skillcheck will be harder | `[]`
SkipTimeCacheSize | size of skip time cache in skip time dialogue, default is 24 hours | `[]`
SkipTimeCacheValidityThreshold | duration for which the skip time cache remains valid | `[]`
SkirmishCheckThreatLevel | Threat level for skirmish morale checks | `[]`
SkirmishPredominanceWeight | Weight of skirmish predominance affecting main morale | `[]`
SleepHealthRegenBaseSpeed | full regen after 8 world-time hours | `[%/s]`
SleepToAfterBuff | sleeping at least this time gives buff affter waking up. | `[h]`
SleepToSaveThreshold | sleeping at least this time triggers autosave. | `[h]`
SleepwalkerPerkChance | probability for the Sleepwalker perk to trigger | `[]`
SmellBuffDirtinessLevel | Dirtiness level required to activate Smell buff | `[-]`
SoulCourageMoraleWeight | Weight of soul courage affecting morale | `[]`
SoulPoolCombatLevelNormalDistributionSigma | Standard deviation of combat level normal distribution when spawning npc from soul pool | `[CombatLevel]`
SpeechMulOnExtremeExhaustion | Player will have this speech multiplied by this value when he has exhaust equal to 0. Speech will not be changed when exhaust is 50. Linear interpolation on multiplier is applied when exhaust is between 0 and 50; | `[%]`
SpeechXPLevelBase | see GDD 44/218 | `[-]`
SpeechXPLevelDiff | see GDD 44/218 | `[-]`
SprintCost | stam cost of sprint | `[stam/s]`
SprintStaminaSavingLowerBound | When the NPC stops sprinting to conserve stamina | `[stam]`
SprintStaminaSavingUpperBound | When the NPC starts sprinting again after conserving stamina | `[stam]`
StamDamage | see: rpglib::calcStaminaDamageCost, GDD: 21/218 | `[-]`
StamRegenBase | base regeneration speed | `[stam/s]`
StamRegenBlockMod | relative stam regen speed during active block or raised weapon | `[-]`
StamRegenFromVit | how our VIT stat affects stamina regeneration | `[-]`
StamRegenMoveMod | relative stam regen speed during movement | `[-]`
StamRegenRelativeDiff | maximal relative difference to the base speed on low/high stamina | `[-]`
StaminaDamageToInjury | note: stamina is `[0-100]` but injury is `[0-1]` | `[/%]`
StaminaDeficitHealthDamageA | HP damage caused by insufficent stamina (DmgR > 0) | `[-]`
StaminaDeficitHealthDamageB | HP damage caused by insufficent stamina (DmgR < 0) | `[-]`
StaminaDrainRatioCharging | ratio of AttackCost when charging | `[%]`
StaminaDrainRatioStriking | ratio of AttackCost when striking begun (weapon raised is complement) | `[%]`
StarvationExtremeThreshold | &nbsp; | `[%/s]`
StarvationHealthLossSpeed | by design the same speed as the digestion | `[%/s]`
StarvationHugeThreshold | &nbsp; | `[%/s]`
StarvationPlayerEffectMaxMax | the longest interval between effects for high hunger stat | `[s]`
StarvationPlayerEffectMaxMin | the longest interval between effects for low hunger stat | `[s]`
StarvationPlayerEffectMinMax | the shortest interval between effects for high hunger stat | `[s]`
StarvationPlayerEffectMinMin | the shortest interval between effects for low hunger stat | `[s]`
StarvationThreshold | &nbsp; | `[%/s]`
StashRobbedValueBottomThreshold | If the robbed value drops to this threshold, it is no longer considered noteworthy. | `[grosh]`
StashRobbedValueDecayRate | Decay rate of value of items stolen from a stash. | `[grosh/h]`
StatCap | max stat level | `[stat]`
StatToMainLevelBase | a1 of the geometric progression | `[-]`
StatXPAgilityPerDodge | xp gain after a slot dodge to agility | `[-]`
StatXPAgilityPerDodgeOutsideSlot | xp gain after dodge outside slot to agility | `[-]`
StatXPComboHit | xp gain after a hit | `[-]`
StatXPHit | xp gain after a hit | `[-]`
StatXPKill | xp gain after a kill | `[-]`
StatXPSpeechPerSequence | speech xp gain after selecting an unused sequence (multiplied by speech_coef of that sequence) | `[-]`
StatXPSpeechPersuadeCoerceSuccessMax | maximal xp gain for persuade success | `[xp]`
StatXPSpeechSkillCheckFailMax | maximal xp gain for a skillcheck fail | `[xp]`
StatXPSpeechSkillCheckSuccessMax | maximal xp gain for a non persuade skillcheck success | `[xp]`
StatXPSpeechSkillStatSkillCheckFailMax | maximal xp gain for a skill or stat skillcheck fail | `[xp]`
StatXPSpeechSkillStatSkillCheckSuccessMax | maximal xp gain for a skill or stat skillcheck success | `[xp]`
StatXPStrAndVitPerDistanceEncumbered | Strength and vitality xp gain after walking EncumberanceXPAwardDistance meters while encumbered | `[-]`
StatXPVitalityPerDistance | vitality xp gain after sprinting AthleticXPAwardDistance | `[-]`
StatXPVitalityPerDodge | xp gain after a each dodge to vitality | `[-]`
StatXPVitalityPerJump | vitality xp gain for each jump | `[-]`
StatXPVitalityPerKill | vitality xp gain after a kill | `[-]`
StatXPVitalityPerVault | vitality xp gain for each vault over a ledge | `[-]`
StatXpAgilityForStealth | agility XP gain for been undetected in stealth, #perception | `[xp]`
StatsToDodgePowTo | slot = relativeStats ^ this, see GDD: #defense | `[-]`
SteadyAimHysteresis | switch on perk Steady aim after this timeout | `[s]`
StealVisVolumeConspicuousnessMax | Maximum conspicuousness for perceptible volume of type steal. | `[-]`
StealVisVolumeConspicuousnessMin | Minimum conspicuousness for perceptible volume of type steal. | `[-]`
StealVisVolumeTreasureItemTime | Steal volumes for the most precious items will last this long | `[s]`
StealVisVolumeVisibilityMax | Maximum visibility for perceptible volume of type steal. | `[-]`
StealVisVolumeVisibilityMin | Minimum visibility for perceptible volume of type steal. | `[-]`
StealVisVolumeWorthlessItemTime | Steal volumes for the most despicable items will last this long | `[s]`
StealthAttackFailXp | xp gain for failed stealth kill or take-down | `[xp]`
StealthAttackMaxXp | xp gain for successful stealth kill or take-down, strongest enemy | `[xp]`
StealthAttackMinXp | xp gain for successful stealth kill or take-down, weakest enemy | `[xp]`
StealthBackoffMaxTime | max duration for stealth backoff | `[]`
StealthBackoffMinTime | min duration for stealth backoff | `[]`
StealthCooldown | after last detector npc stops seeing player | `[]`
StealthKillDamage | damage given to the victim | `[hp]`
StealthKillMaxSlot | max slot duration for stealth kill/knock-out | `[]`
StealthKillMinSlot | min slot duration for stealth kill/knock-out | `[]`
StealthKillProbCoefA | stealth kill/knock-out probability formula | `[]`
StealthKillProbCoefB | stealth kill/knock-out probability formula | `[]`
StealthKillProbCoefC | stealth kill/knock-out probability formula | `[]`
StealthKnockOutUnconsciousDepthBase | the base unconsciousness depth for stealth knockout | `[depth]`
StealthSkillToFootstepSoundMult | how much how much are footsteps attenuated for the max skill #perception | `[-/skill]`
StealthSkillToRecogTime | how much is the required time extended on max skill level (relative) #perception | `[-/skill]`
StealthSkillToViewRadiusDecr | how much is the view radius decreased on max skill level (relative) #perception | `[-/skill]`
StealthSneakBaseDistance | sneaked distance that triggers stealth leveling, #perception | `[m]`
StealthSneakBaseXp | base xp gain when sneaking, #perception | `[xp]`
StealthSneakCheckRadius | npc query radius when sneaking, #perception | `[m]`
StealthSneakXpSumCoefA | combine xps from more npcs, #perception | `[]`
StealthSneakXpSumCoefB | combine xps from more npcs, #perception | `[]`
StealthToUnconsciousDepth | modifies the time victim is unconscious | `[depth]`
StillAndHiddenHysteresis | switch the state after this timeout | `[s]`
StillBuffDuration | duration of standing still after which Still buff bonuses are activated (in worldtime seconds) | `[s]`
StolenGoodsForcedDiscount | price multiplier for when merchant detects that the sold items are stolen | `[-]`
StolenKeyExpiraitionBlockRadius | NPCs will not change a lock unless it is further from the player than this | `[m]`
StolenKeyExpirationTime | NPCs change their locks after this amount of time since the keys were stolen | `[day]`
StolenKeyLockChangePeriod | NPCs take this long between checking whether they should change locks | `[day]`
StoryProgressXPLevelBase | see GDD 44/218 | `[-]`
StoryProgressXPLevelDiff | see GDD 44/218 | `[-]`
StrToEqwArmorLoad | maximal gain on level cap, GDD: 17/218 | `[-]`
StrengthBaddassWeight | Weight of relative strength affecting badassness | `[]`
StrengthMulOnExtremeExhaustion | Player will have this strength multiplied by this value when he has exhaust equal to 0. Strength will not be changed when exhaust is 50. Linear interpolation on multiplier is applied when exhaust is between 0 and 50; | `[%]`
StrengthToInventoryCapacity | derives the inventory capacity from the strength stat | `[lb/str]`
StrengthXPLevelBase | see GDD 44/218 | `[-]`
StrengthXPLevelDiff | see GDD 44/218 | `[-]`
SuccessSkillCheckLevel | everything above this level from the given range is considered a Success | `[]`
SuperFactionRepWeight | Weight of superfaction reputation (reputation median) | `[]`
SurfaceToSpeedCoef | Global multiplier used when applying surface speed multipler | `[-]`
SurvivalSkillAttackToAnimalOnMaxLevel | attack modifier to animals on maximum survival skill level | `[]`
SurvivalSkillXPPerDiscoveredPOI | Amount XP to survival gained for discovering POI | `[xp]`
SurvivalXPOverride | Multiply XP gained for this skill | `[]`
SurvivalXpRewardPerCookedItem | XP reward to survival skill for every cooked item | `[xp]`
SurvivalXpRewardPerDriedItem | XP reward to survival skill for every dried item | `[xp]`
SurvivalXpRewardPerSmokedItem | XP reward to survival skill for every smoked item | `[xp]`
TheyWillNeverKnowPerkStealthXp | XP gained to stealth skill after They will never know perk activaction | `[xp]`
ThieveryXPOverride | Multiply XP gained for this skill | `[]`
ThreatenStrenghtWeight | `[0,1]`: 0 - full weight to morale; 1- full weight to strength | `[]`
ThunderstormBuffRainIntensity | rain intensity threshold when Thunderstorm buff bonuses are activated | `[-]`
TimeBasedAchievementTRCompliantProlongation | after loading a save in which the conditions of a time based achievement are already fulfilled, you must wait this long to unlock the achievement (TRC R4126) | `[h]`
TireEmToTakeEmRequiredTime | Required time to activate buff | `[s]`
TrackedAreasNPCRadius | While tracking NPCs present in areas only consider those that are this far from the player. | `[m]`
TransferedBloodToAttackerMax | Maximum amount of blood transferred to attacker from an injury they inflicted in melee combat. | `[%]`
TransferedBloodToAttackerMin | Minimum amount of blood transferred to attacker from an injury they inflicted in melee combat. | `[%]`
TransferedBloodToAttackerSecondaryWeaponMax | Maximum amount of blood transferred to attacker secondary weapon from an injury they inflicted in melee combat. | `[%]`
TransferedBloodToAttackerSecondaryWeaponMin | Minimum amount of blood transferred to attacker secondary weapon from an injury they inflicted in melee combat. | `[%]`
TransferedBloodToAttackerWeaponMax | Maximum amount of blood transferred to attacker weapon from an injury they inflicted in melee combat. | `[%]`
TransferedBloodToAttackerWeaponMin | Minimum amount of blood transferred to attacker weapon from an injury they inflicted in melee combat. | `[%]`
TransferedBloodToVictimMax | Maximum amount of blood transferred to victim from an injury they inflicted in melee combat. | `[%]`
TransferedBloodToVictimMin | Minimum amount of blood transferred to victim from an injury they inflicted in melee combat. | `[%]`
TreasureItemPrice | starting price of treasure items | `[grosh]`
TrueRelationDistThresholdRel | distance, relative to observers maximum distance, required to see the true faction #perception | `[-/skill]`
UnarmedAttackReqAgiBase | for attack with relative stam cost = 1 | `[]`
UnarmedAttackReqStrBase | for attack with relative stam cost = 1 | `[]`
UnarmedBlockDefense | defense value for unarmed block | `[]`
UnarmedHitArmorDamageCoef | relative to armed combat | `[-]`
UnconsciousDepthFadeoutSpeedBase | how fast is the depth consumed | `[depth/s]`
UnconsciousTimeWhenTimeIsNotRunning | if world time is not running, skiptime can not be started when player is unconscious; screen will only fade for this long instead; this is slightly modified by some rpg stats | `[s]`
VigourFull | maximum vigour | `[%]`
VisibilityDecrementDaytimeInterior | Limited by MinModVisibility and MaxModVisibility. Implicit constant for DaytimeExterior defaults to 0. See also NightTransitionPeriod. #perception | `[-]`
VisibilityDecrementInFog | Multiply by fog amount and add to visibility while outside. #perception | `[-]`
VisibilityDecrementInVisArea | Hide in tall grass. #perception | `[-]`
VisibilityDecrementNighttimeExterior | Limited by MinModVisibility and MaxModVisibility. See also NightTransitionPeriod. #perception | `[-]`
VisibilityDecrementNighttimeInterior | Limited by MinModVisibility and MaxModVisibility. See also NightTransitionPeriod. #perception | `[-]`
VisionToViewRadius | an increase of FOV caused by the hea stat | `[m/vis]`
VitToEqwArmorLoad | maximal gain on level cap, GDD: 17/218 | `[-]`
VitalityToUnconsciousDepthFadeoutSpeed | relative vitality | `[depth/s]`
VitalityXPLevelBase | see GDD 44/218 | `[-]`
VitalityXPLevelDiff | see GDD 44/218 | `[-]`
WashDirtLimitMax | Possible dirt that can be washed on the maximum skill level. | `[-]`
WashDirtLimitMin | Possible dirt that can be washed on the minimum skill level. | `[-]`
WashItemDirtPriceStatusWeight | item dirt status weight price coef for washing | `[-]`
WashItemsCraftsmanshipXpReward | XP reward to craftsmanship skill for washing items in washing minigame | `[xp]`
WashSoapCostMod | Minimum cost modifier for soap cost calculation | `[-]`
WashSoapCostSkillCoef | Skill coefficient for soap cost calculation | `[-]`
WeakBlockStamCoef | see: rpglib::calcStaminaDamageCost, GDD: 21/218 | `[-]`
WeaponConditionThresholdForDamage | Threshold of weapon condition where weapon damage is increasing. | `[-]`
WeaponDefenseToAttackingWeaponStatus | how opponet's defense value damages my weapon - hit to weapon/block | `[status/defense]`
WeaponStatusToAttackCoef | weapon health to status multiplicative coef | `[-]`
WorthlessItemPrice | The most despicable items are with this value or lower | `[gr]`
XPShootingTargetHitDistanceMod | XP bonus modifier for distance from shooting target | `[m]`
XPShootingTargetHitMinDistance | Minimum distance in which soul get XP for shooting target | `[m]`