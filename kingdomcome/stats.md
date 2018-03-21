<!-- TITLE: Stats and Derived Stats -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Stats and Derived Stats

These tables are incomplete and works-in-progress.

**Note:** The `×` symbol is used in these tables to avoid formatting issues. In practice, the correct operator is the asterisk (`*`).

## Active Stats

Abbr | Example | Description
:--- | :--- | :---
`health` | `health+0.125/s` | Modifies the player's current Health
`stamina` | `stamina+0.125/s` | Modifies the player's current Stamina
`exhaust` | `exhaust-100/s` | Modifies the player's current Exhaustion
`hunger` | `hunger+1000/s` | Modifies the player's current Hunger
`karma` | | Modifies the player's current Karma?
`alcoholism` | | Modifies the player's current Drunkenness?

## Base Stats

Abbr | Name | Description
:--- | :--- | :---
`agi` | Agility | Modifies the Agility stat
`bar` | Barter | Modifies the Barter stat
`cou` | Courage | Modifies the Courage stat
`hea` | Hearing | Modifies the Hearing stat
`prg` | StoryProgress |
`rep` | PlayerReputation |
`spc` | Speech | Modifies the Speech stat
`str` | Strength | Modifies the Strength stat
`vis` | Vision | Modifies the Vision stat
`vit` | Vitality | Modifies the Vitality stat

## Derived Stats

Abbr | Name | Description | Base Value
:--- | :--- | :--- | :---
 `aco` | ArmorCollisionWeight | Modifies the impact weight of armor when colliding with another entity | Derived from equipped items
 `adm` | AlcoholDigestMod | Modifies the rate of alcohol digestion | 1
 `alc` | Alcoholism | | 0
 `alo` | ArmorLoad | test buffs: suppress armor load | Derived from `EquippedWeight`, `Strength`, `Agility`, `MaxArmorLoad`, `StrAgiToEqwArmorLoad` and `ArmorLoadDiffToMax`
 `apa` | AlcoholPoisoningAntidote | | 0
 `apr` | AttackProtection | | Derived from `soul.soul_vip_class_id`
 `arr` | ArmorRating | Modifies the chance to cause enemies to flee | `clamp(OverallArmorDefense / GoodArmorDefense, 0, 1)`
 `bad` | Badassness | Modifies the Badassness derived stat | `lerp(Morale, Strength / StatCap, ThreatenStrenghtWeight)`
 `bld` | Bloodiness | | Derived from equipped items
 `ble` | BleedingTotal | | Derived from buffs which have a special `Bleeding` modifier
 `bma` | BuyMarginAdjust | Modifies the percentage amount of money received in trade | 0
 `bow` | BodyWeight | | Derived from `soul_archetype.normal_body_weight`, `SlimCollisionWeightMul` and `FatCollisionWeightMul`
 `brm` | BadReputationMod | Modifies the influence of negative actions on reputation | 1
 `bso` | BasketSuspiciencyMod | | 0
 `btw` | BoidThreatWeight | Modifies the skittishness of wild animals | 1
 `caf` | Caffeine | | 0
 `cag` | CombatAggression | | Derived from `Defense`, `Fencing`, `SkillCap` and `CombatAutoAggressionDiffScale`
 `cap` | InventoryCapacity | Modifies the amount of weight that can be carried before becoming encumbered | `(BaseInventoryCapacity + StrengthToInventoryCapacity * Strength) * soul_archetype.inventory_capacity_multiplier`
 `caw` | CarriedWeight | | Derived from inventory
 `cbi` | CharismaFromBuffedItems | | 0
 `cds` | ClothDirtyingSpeedKm | Modifies the rate at which clothing becomes dirty | Derived from surface, `FullClothDirtyingOnZeroSpeed` and `FullClothDirtyingOnFullSpeed`
 `cdw` | ClinchDamageToWeapon | Modifies the percentage damage inflicted on an opponent's weapon durability | 0
 `cha` | Charisma | Modifies the Charisma stat | Derived from equipped items, `soul.charisma` and `CharismaFromBuffedItems`.
 `coc` | Consciousness | | 1
 `con` | Conspicuousness | Modifies the hostile search duration of NPCs | Derived from equipped items.
 `cow` | CollisionWeight | Modifies the overall impact of colliding with another entity | `BodyWeight + ArmorCollisionWeight`
 `dbf` | DiceBustFixing | | 0
 `def` | Defensiveness | | Derived from `Stamina`, `CombatAggression`, `MeanAttackPeriod`, `CombatAutoScaleDefensivenessDelayRel` and `CombatAutoAttackDelaySigma`
 `drt` | Dirtiness | | Derived from equipped items
 `dru` | Drunkenness | | 0
 `dtf` | DiceThrowFixing | | 0
 `edm` | EquipmentUseDamageMultiplier | | 1
 `enc` | Encumberance | | Derived from surface, `RelativeCarriedWeight` and `EncumberedToSpeedSurfaceCoef`
 `eqw` | EquippedWeight | | Derived from equipped items
 `erq` | EffectiveReadingQuality | | `ReadingQuality`
 `evi` | EquipVisib | | Derived from equipped items
 `fdm` | FallDamageMultiplier | Modifies the amount of damage received after falling | `lerp(1, FallDamageMultiplierAtMaxAgility, Agility / StatCap)`
 `fol` | DistanceFollowing | | `Fencing / SkillCap`
 `fov` | FieldOfView | | `min(PerceptionMinFov + HearingToFov * Hearing, PerceptionMaxFov)`
 `fpa` | FoodPoisoningAntidote | | 0
 `fsm` | FootstepSoundMultiplier | Modifies the noise produced by walking and running | `clamp(1 - StealthSkillToFootstepSoundMult * Stealth / SkillCap, 0, 1)`
 `grm` | GoodReputationMod | Modifies the influence of positive actions on reputation | 1
 `hac` | HaggleAdditionalChances | Modifies the number of times a trader will haggle | 0
 `hcm` | HorseCourageMod | Modifies the Courage stat of the mounted horse | `1 + HorseRiding * HorseRidingToHorseCourage`
 `hgs` | HerbGatherStrengthXp | Modifies the amount of Strength skill experience gained from herb gathering | 0
 `hko` | HeadHitKnockOutProbability | Modifies the chance of knocking out an opponent with a blow to the head | `HeadHitKnockOutBaseProbability`
 `hlt` | Healthiness | | `MaxStamina` / `MaxHealthyStamina`
 `hml` | HorseThrowDownMoraleLimit | Determines whether the player's horse will throw the player outside of combat | `HorseMoraleToThrowOffRider`
 `ibi` | InjuryBleedingInterval | | `InjuryBleedingInterval`
 `iex` | ItemExpert | | 0
 `imm` | Immortality | | Derived from `soul.soul_vip_class_id`
 `jrm` | JailRecoverySpeedMod | Modifies the rate at which the player recovers from jail time | 1
 `lfu` | LockFailUnlockProb | 10% chance of opening locks instantly | 0
 `lio` | LockInstantOpenDifficulty | Modifies the maximum lock difficulty of instantly unlockable locks | 0
 `lpv` | LightProbeVisibility | | Calculated from light probe. Value between `MinLightProbeVisibility` and `MaxLightProbeValue`.
 `lsa` | LockStartAngle | Modifies the lockpick's proximity to the end of the lockpicking minigame | 0
 `lvl` | MainLevel | Modifies the player's Main Level | Derived from `Strength`, `Agility`, `Vitality`, `Speech` and `StoryProgress`
 `map` | MeanAttackPeriod | | Derived from `Stamina`, `Fencing`, `CombatAggression` and `CombatAutoMaxAttackDelay`
 `mcf` | MoraleContextFadingMod | | Derived from `Courage`, `StatCap` and `MaxCourageMoraleContextFadingMod`
 `mhs` | MaxHealthyStamina | | `soul_archetype.base_stamina + soul_archetype.relative_vitality_to_stamina * Vitality / StatCap`
 `mor` | Morale | | `clamp( ( (Courage / StatCap) * SoulCourageMoraleWeight + clamp(soul_class.soul_class_courage, 0, 1) * ClassCourageMoraleWeight + ArmorRating * OverallArmorDefenseMoraleWeight + clamp(OverallWeaponAttack / GoodWeaponAttack, 0, 1) * OverallWeaponAttackMoraleWeight ) / ( SoulCourageMoraleWeight + ClassCourageMoraleWeight + OverallArmorDefenseMoraleWeight + OverallWeaponAttackMoraleWeight ) * ( HealthToMoraleMinCoef + (1 - HealthToMoraleMinCoef) * (Health / HealthFull) ) , 0, 1)`
 `mst` | MaxStamina | Modifies the maximum amount of the Stamina stat | Derived from `MaxHealthyStamina` and `Health`
 `mut` | Mute | | 1 if soul is Unconscious or Dead, 0 otherwise
 `nbi` | NoiseFromBuffedItems | | 0
 `noi` | Noise | Modifies the Noise derived stat | Derived from equipped items and `NoiseFromBuffedItems`
 `nrs` | NormalizedRunSpeed | | Derived from movement
 `oad` | OverallArmorDefense | | Derived from equipped items
 `ore` | Overreadness | | 0
 `osl` | Oversleepness | | 0
 `owa` | OverallWeaponAttack | | Derived from equipped items
 `owl` | Owl | Whether you can see in the dark | 0
 `pbm` | CraftedPotionsBuyMarginAdjust | Modifies the percentage amount of money received in trade for crafted potions | 0
 `pds` | PicklockDmgSpeed | Modifies the rate at which lockpicks are damaged | `PicklockDmgSpeed`
 `pla` | PlatingRatio | | Derived from equipped items
 `poi` | Poisoning | You've been poisoned | 0
 `pos` | PocketSight | reveals some number of items while pickpocketing | 0
 `ppr` | PickpocketProtection | | Derived from `soul.soul_vip_class_id`
 `prb` | PerceptionPriorityBoost | | 0
 `prc` | PicklockReturnChance | Modifies the percentage chance of repairing a broken lockpick | 0
 `pt1` | PerfectThrowMultiplier1 | | 1
 `pt5` | PerfectThrowMultiplier5 | | 1
 `ran` | RobbedAngriness | | 0
 `rch` | RelativeCharisma | | `Charisma / StatCap`
 `rcw` | RelativeCarriedWeight | | `CarriedWeight / InventoryCapacity`
 `rdq` | ReadingQuality | It doesn't matter to you where you read, you get a learning bonus anywhere you read | `DefaultReadingQuality`
 `rml` | RandomMoneyLoot | | 0
 `rms` | RealMoveSpeedMod | | 1
 `rsa` | RelativeMovementSpeedAddition | | `lerp(-MaxAgilityToMovementSpeedAddition, MaxAgilityToMovementSpeedAddition, Agility / StatCap)`
 `sdt` | StaminaDerivation | | Derived from Vitality, MaxHealthyStamina, ArmorLoad, Stamina, HorseRiding, and many others.
 `sha` | BowSelfHarmAttack | | 0
 `sle` | Sleeping | | 0
 `sma` | SellMarginAdjust | Modifies the percentage amount of money given in trade | 0
 `src` | StaminaRegenCooldown | Used in injured_head buff effect | `StamRegenCooldown`
 `sur` | Surrendering | 0 - opponent is not surrendering, 1 - opponent is surrendering | 0
 `ufo` | UnconsciousnessFadeoutSpeed | infinite_unconsciousness buff | `UnconsciousDepthFadeoutSpeedBase + VitalityToUnconsciousDepthFadeoutSpeed * Vitality / StatCap`
 `upr` | UnconsciousnessProtection | 0 - disabled, 1 - enabled | Derived from `soul.soul_vip_class_id`
 `vib` | Visibility | Adjusts visibility | `EquipVisib + MovementVisibilityPenalization + LightProbeVisibility`
 `vir` | ViewRadius | | `min(MinViewRadius + VisionToViewRadius * TimeOfDayCoef * (Vision - 1), MaxViewRadius)`
 `was` | RangedWeaponAimSpread | Ranged weapon accuracy | `AimSpreadMax * (1 - WeaponBow * AimSpreadSkillDecrease)`
 `wbc` | WeaponBuffCharges | Adjusts the number of poison charges applied to a weapon | `lerp(MinWeaponBuffCharge, MaxWeaponBuffCharge, random)`
 `wud` | WeaponUsageDamageMod | | `lerp(1, MaxFencingWeaponUsageMod, Fencing / SkillCap)`
 `xpm` | XPMultiplier | Modifies the amount of experience gained | `soul.xp_multiplier`

## Intermediate Stats

ID | Abbr | Name | Example | Description
---: | :--- | :--- | :--- | :---
180 | `act` | MovementActivity | | 
175 | `ade` | ArmorDefense | ade×0.9 | Defence
178 | `ahm` | AttackFromHorseMod | ahm×1.15 | Modifies the amount of attack damage while mounted
200 | `ain` | AttackInjury | ain×1.3 | Modifies the chance to cause bleeding
181 | `asp` | AttackSpeed01 | asp×0.75 | Used in arm injury buff effect
183 | `cli` | ClinchAdvantage | cli+0.4 | Modifies the chance to overpower an opponent in a clinch
205 | `cos` | ComboSlot01 | cos=0 | Used in limited_combat buff
202 | `dee` | DamageToEnemyEquipment | dee+0.15 | Damage to armor
187 | `dig` | DigestionSpeed | dig×0 | Hunger?
204 | `dsl` | DodgeSlot | dsl×1.5 | Modifies the difficulty of dodging in combat
197 | `eep` | RandomEventEscapeProbability | eep×1.1 | Evasion Chance
188 | `exh` | ExhaustionSpeed | exh×0 | Rate at which you're exhausted
201 | `fae` | FirstAidEfficiency | fae×2 | Bandage effectiveness
184 | `hlh` | HealthLossHit | hlh×0.5 | Amount of health lost when hit, always used with `slh`
189 | `lcs` | LockCursorShake | lcs=0 | perk_steady_hand buff - nonexistent perk
207 | `lpb` | LockpickingLockpickBreakChance | lpb×0.1 | Adjusts the chance to break lockpicks
198 | `lpd` | LockpickingDifficulty | lpd×0.5 | Adjusts the difficulty rating of locks
199 | `lpn` | LockpickingNoiseMultiplier | lpn×1.3 | Modifies the amount of noise produced by lockpicking
208 | `ors` | ObserverRecognitionSpeed | ors=-1 | With Cpp:VersusDog, whether dogs bark at you. As a constant, whether souls react to you?
203 | `osb` | OpponentStaminaLossBlocking | osb×1.15 | Opponent's stamina cost of attacking while you're blocking
206 | `pac` | WeaponPoisonApplyChance | pac×1.5 | Chance to poison on attack
182 | `pbs` | PerfectBlockSlot01 | pbs×2 | 
196 | `pdp` | PullDownProbability | pdp×1.15 | Chance to remain in saddle when opponents attempts to unhorse you
195 | `rst` | RelativeStaminaMax | rst < 0.6 | Used in the overeating buff effect
179 | `rtm` | RiderThreatsToHorseMorale | rtm×0.5 | Chance for horse to shy at nearby foes
191 | `sco` | StaminaConsumption | sco=0 | Used in god_mode buff effect 
194 | `skp` | StealthKillProbability | skp=0 | 0 - stealth kill fail, 1 - stealth kill success
185 | `slh` | StaminaLossHit | slh×0.5 | Amount of stamina to lose when attacked
186 | `sls` | StaminaLossBlockingShield | sls×0.7 | Stamina cost of blocking with a shield
193 | `sra` | StaminaRegenAttack | sra×1.5 | Stamina regeneration rate while attacking
192 | `srb` | StaminaRegenBlock | | Stamina regeneration rate while blocking 
190 | `srg` | StaminaRegen | srg×1.5 | Modifies the rate at which stamina regenerates
177 | `wac` | WeaponAttackCost | wac×0.7 | Weapon attack stamina cost
176 | `wat` | WeaponAttack | wat×1.2 | Weapon attack damage

## Skill Stats

ID | Abbr | Internal Name | Description | Comments
---: | :--- | :--- | :--- | :---
0 | `stealth` | `Stealth` | Modifies the player's Stealth skill level
1 | `horse_riding` | `HorseRiding` | Modifies the player's Horsemanship skill level
2 | `fencing` | `Fencing` | Modifies the player's Fencing skill level | Not implemented
3 | `bard` | `Bard` | Modifies the player's Bard skill level | Not implemented
4 | `lockpicking` | `Lockpicking` | Modifies the player's Lockpicking skill level
5 | `pickpocketing` | `Pickpocketing` | Modifies the player's Pickpocketing skill level
6 | `alchemy` | `Alchemy` | Modifies the player's Alchemy skill level
7 | `cooking` | `Cooking` | Modifies the player's Cooking skill level | Not implemented
8 | `repairing` | `Repairing` | Modifies the player's Maintenance skill level
9 | `smithing` | `Smithing` | Modifies the player's Smithing skill level | Not implemented
10 | `fishing` | `Fishing` | Modifies the player's Fishing skill level | Not implemented
11 | `mining` | `Mining` | Modifies the player's Mining skill level | Not implemented
12 | `first_aid` | `FirstAid` | Modifies the player's First Aid skill level | Not implemented
13 | `drinking` | `Drinking` | Modifies the player's Drinking skill level
14 | `hunter` | `Hunter` | Modifies the player's Hunting skill level
15 | `defense` | `Defense` | Modifies the player's Defence skill level
16 | `weapon_sword` | `WeaponSword` | Modifies the player's Swords skill level
17 | `weapon_axe` | `WeaponAxe` | Modifies the player's Axes skill level
18 | `weapon_bow` | `WeaponBow` | Modifies the player's Bows skill level
19 | `weapon_crossbow` | `WeaponCrossbow` | Modifies the player's Crossbows skill level | Not implemented
20 | `weapon_shield` | `WeaponShield` | Modifies the player's Shields skill level
21 | `weapon_mace` | `WeaponMace` | Modifies the player's Maces skill level
22 | `weapon_dagger` | `WeaponDagger` | Modifies the player's Daggers skill level | Not implemented
23 | `weapon_large` | `WeaponLarge` | Modifies the player's Polearms skill level | Not implemented
24 | `weapon_unarmed` | `WeaponUnarmed` | Modifies the player's Unarmed skill level
25 | `herbalism` | `Herbalism` | Modifies the player's Herbalism skill level
26 | `reading` | `Reading` | Modifies the player's Reading skill level
27 | `tailoring` | `Tailoring` | Modifies the player's Tailoring skill level
28 | `armourer` | `Armourer` | Modifies the player's Armourer skill level | Not implemented
29 | `weaponsmithing` | `WeaponSmithing` | Modifies the player's Weaponsmithing skill level | Not implemented
30 | `shoemaking` | `Shoemaking` | Modifies the player's Shoemaking skill level | Not implemented

## Limit Stats

Abbr | Description
:--- | :---
`LimitRun` | Used without expression
`LimitSprint` | Used without expression

## Other Stats

**Note:** Some of this data probably doesn't belong on this page.

Name | Description
:--- | :---
`StaminaRegenCooldown` |
`HasUnholsteredWeapon` |
`HasUnholsteredMissileWeapon` |
`HasRaisedWeapon` |
`IsBlocking` |
`IsAiming` |
`HasActiveThreats` |
`IsInCombatDanger` |
`IsActiveInCombat` |
`IsRunning` |
`WasRunning` |
`WannaSprint` |
`IsMoving` |
`WasMoving` |
`IsSprinting` |
`WasSprinting` |
`IsOnHorse` |
`IsStealth` |
`IsPotentialStealth` |
`IsInAir` |
`HasLimitedRunByItem` |
`HasLimitedSprintByItem` |

## Unknown Stats

Abbr | Internal Name | Example | Description
:--- | :--- | :--- | :---
`---` | Stat_Last | |
`---` | DerivStat_Last | |