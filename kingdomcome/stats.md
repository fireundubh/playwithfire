<!-- TITLE: Stats and Derived Stats -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Stats and Derived Stats

These tables are incomplete and works-in-progress.

**Note:** The `×` symbol is used in these tables to avoid formatting issues. In practice, the correct operator is the asterisk (`*`).

## Active Stats

ID | Abbr/Internal Name | Example | Description
---: | :--- | :--- | :---
146 | `health` | health+0.125/s | Modifies the player's current Health
147 | `stamina` | stamina+0.125/s | Modifies the player's current Stamina
148 | `exhaust` | exhaust-100/s | Modifies the player's current Exhaustion
149 | `hunger` | hunger+1000/s | Modifies the player's current Hunger
150 | `karma` | | Modifies the player's current Karma?
151 | `alcoholism` | | Modifies the player's current Drunkenness?

## Base Stats

ID | Abbr | Internal Name | Example | Description
---: | :--- | :--- | :--- | :---
33 | `agi` | Agility | agi+1 | Modifies the Agility stat
38 | `bar` | Barter | bar+3 | Modifies the Barter stat
39 | `cou` | Courage | cou+2 | Modifies the Courage stat
37 | `hea` | Hearing | hea=0 | Modifies the Hearing stat
41 | `prg` | StoryProgress | | 
40 | `rep` | PlayerReputation | | 
35 | `spc` | Speech | spc+1 | Modifies the Speech stat
32 | `str` | Strength | str+1 | Modifies the Strength stat
36 | `vis` | Vision | vis×0.3 | Modifies the Vision stat
34 | `vit` | Vitality | vit+1 | Modifies the Vitality stat

## Derived Stats

ID | Abbr | Name | Base Value | Description | Example
---: | :--- | :--- | :--- | :--- | :---
78 | `aco` | ArmorCollisionWeight | Derived from equipped items | Modifies the impact weight of armor when colliding with another entity | `aco*6`
141 | `adm` | AlcoholDigestMod | 1 | Modifies the rate of alcohol digestion | 
139 | `alc` | Alcoholism | 0 | | 
65 | `alo` | ArmorLoad | Derived from `EquippedWeight`, `Strength`, `Agility`, `MaxArmorLoad`, `StrAgiToEqwArmorLoad` and `ArmorLoadDiffToMax` | test buffs: suppress armor load | `alo=-0.2`
95 | `apa` | AlcoholPoisoningAntidote | 0 | | 
127 | `apr` | AttackProtection | Derived from `soul.soul_vip_class_id` | | 
123 | `arr` | ArmorRating | `clamp(OverallArmorDefense / GoodArmorDefense, 0, 1)` | Modifies the chance to cause enemies to flee | `arr*1.3`
99 | `bad` | Badassness | `lerp(Morale, Strength / StatCap, ThreatenStrenghtWeight)` | Modifies the Badassness derived stat | `bad+0.5`
122 | `bld` | Bloodiness | Derived from equipped items | | 
74 | `ble` | BleedingTotal | Derived from buffs which have a special `Bleeding` modifier | | 
114 | `bma` | BuyMarginAdjust | 0 | Modifies the percentage amount of money received in trade | `bma+0.15`
76 | `bow` | BodyWeight | Derived from `soul_archetype.normal_body_weight`, `SlimCollisionWeightMul` and `FatCollisionWeightMul` | | 
108 | `brm` | BadReputationMod | 1 | Modifies the influence of negative actions on reputation | `brm*1.5`
121 | `bso` | BasketSuspiciencyMod | 0 | | `bso+0.5`
142 | `btw` | BoidThreatWeight | 1 | Modifies the skittishness of wild animals | `btw*0.4`
86 | `caf` | Caffeine | 0 | | 
96 | `cag` | CombatAggression | Derived from `Defense`, `Fencing`, `SkillCap` and `CombatAutoAggressionDiffScale` | | 
64 | `cap` | InventoryCapacity | `(BaseInventoryCapacity + StrengthToInventoryCapacity * Strength) * soul_archetype.inventory_capacity_multiplier` | Modifies the amount of weight that can be carried before becoming encumbered | `cap+1000`
79 | `caw` | CarriedWeight | Derived from inventory | | 
137 | `cbi` | CharismaFromBuffedItems | 0 | | 
130 | `cds` | ClothDirtyingSpeedKm | Derived from surface, `FullClothDirtyingOnZeroSpeed` and `FullClothDirtyingOnFullSpeed` | Modifies the rate at which clothing becomes dirty | 
133 | `cdw` | ClinchDamageToWeapon | 0 | Modifies the percentage damage inflicted on an opponent's weapon durability | `cdw+0.15`
43 | `cha` | Charisma | Derived from equipped items, `soul.charisma` and `CharismaFromBuffedItems`. | Modifies the Charisma stat | `cha+1`
90 | `coc` | Consciousness | 1 | | 
48 | `con` | Conspicuousness | Derived from equipped items. | Modifies the hostile search duration of NPCs | `con-1`
77 | `cow` | CollisionWeight | `BodyWeight + ArmorCollisionWeight` | Modifies the overall impact of colliding with another entity | `cow+1200`
57 | `dbf` | DiceBustFixing | 0 | | 
97 | `def` | Defensiveness | Derived from `Stamina`, `CombatAggression`, `MeanAttackPeriod`, `CombatAutoScaleDefensivenessDelayRel` and `CombatAutoAttackDelaySigma` | | 
109 | `drt` | Dirtiness | Derived from equipped items | | 
100 | `dru` | Drunkenness | 0 | | 
56 | `dtf` | DiceThrowFixing | 0 | | 
131 | `edm` | EquipmentUseDamageMultiplier | 1 | | `edm*0.8`
111 | `enc` | Encumberance | Derived from surface, `RelativeCarriedWeight` and `EncumberedToSpeedSurfaceCoef` | | 
134 | `eqw` | EquippedWeight | Derived from equipped items | | 
88 | `erq` | EffectiveReadingQuality | `ReadingQuality` | | 
46 | `evi` | EquipVisib | Derived from equipped items | | 
112 | `fdm` | FallDamageMultiplier | `lerp(1, FallDamageMultiplierAtMaxAgility, Agility / StatCap)` | Modifies the amount of damage received after falling | 
98 | `fol` | DistanceFollowing | `Fencing / SkillCap` | | 
54 | `fov` | FieldOfView | `min(PerceptionMinFov + HearingToFov * Hearing, PerceptionMaxFov)` | | 
94 | `fpa` | FoodPoisoningAntidote | 0 | | 
71 | `fsm` | FootstepSoundMultiplier | `clamp(1 - StealthSkillToFootstepSoundMult * Stealth / SkillCap, 0, 1)` | Modifies the noise produced by walking and running | 
107 | `grm` | GoodReputationMod | 1 | Modifies the influence of positive actions on reputation | 
60 | `hac` | HaggleAdditionalChances | 0 | Modifies the number of times a trader will haggle | 
105 | `hcm` | HorseCourageMod | `1 + HorseRiding * HorseRidingToHorseCourage` | Modifies the Courage stat of the mounted horse | 
115 | `hgs` | HerbGatherStrengthXp | 0 | Modifies the amount of Strength skill experience gained from herb gathering | 
110 | `hko` | HeadHitKnockOutProbability | `HeadHitKnockOutBaseProbability` | Modifies the chance of knocking out an opponent with a blow to the head | 
51 | `hlt` | Healthiness | `MaxStamina` / `MaxHealthyStamina` | | 
120 | `hml` | HorseThrowDownMoraleLimit | `HorseMoraleToThrowOffRider` | Determines whether the player's horse will throw the player outside of combat | `hml=0`
75 | `ibi` | InjuryBleedingInterval | `InjuryBleedingInterval` | | 
104 | `iex` | ItemExpert | 0 | | 
126 | `imm` | Immortality | Derived from `soul.soul_vip_class_id` | | 
124 | `jrm` | JailRecoverySpeedMod | 1 | Modifies the rate at which the player recovers from jail time | `jrm*0.8`
62 | `lfu` | LockFailUnlockProb | 0 | 10% chance of opening locks instantly | `lfu=0.1`
63 | `lio` | LockInstantOpenDifficulty | 0 | Modifies the maximum lock difficulty of instantly unlockable locks | `lio=0.3`
47 | `lpv` | LightProbeVisibility | Calculated from light probe. Value between `MinLightProbeVisibility` and `MaxLightProbeValue`. | | 
61 | `lsa` | LockStartAngle | 0 | Modifies the lockpick's proximity to the end of the lockpicking minigame | 
69 | `lvl` | MainLevel | Derived from `Strength`, `Agility`, `Vitality`, `Speech` and `StoryProgress` | Modifies the player's Main Level | 
140 | `map` | MeanAttackPeriod | Derived from `Stamina`, `Fencing`, `CombatAggression` and `CombatAutoMaxAttackDelay` | | 
82 | `mcf` | MoraleContextFadingMod | Derived from `Courage`, `StatCap` and `MaxCourageMoraleContextFadingMod` | | 
50 | `mhs` | MaxHealthyStamina | `soul_archetype.base_stamina + soul_archetype.relative_vitality_to_stamina * Vitality / StatCap` | | 
81 | `mor` | Morale | `clamp( ( (Courage / StatCap) * SoulCourageMoraleWeight + clamp(soul_class.soul_class_courage, 0, 1) * ClassCourageMoraleWeight + ArmorRating * OverallArmorDefenseMoraleWeight + clamp(OverallWeaponAttack / GoodWeaponAttack, 0, 1) * OverallWeaponAttackMoraleWeight ) / ( SoulCourageMoraleWeight + ClassCourageMoraleWeight + OverallArmorDefenseMoraleWeight + OverallWeaponAttackMoraleWeight ) * ( HealthToMoraleMinCoef + (1 - HealthToMoraleMinCoef) * (Health / HealthFull) ) , 0, 1)` | | 
49 | `mst` | MaxStamina | Derived from `MaxHealthyStamina` and `Health` | Modifies the maximum amount of the Stamina stat | `mst×1.5`
92 | `mut` | Mute | 1 if soul is Unconscious or Dead, 0 otherwise | | 
138 | `nbi` | NoiseFromBuffedItems | 0 | | 
70 | `noi` | Noise | Derived from equipped items and `NoiseFromBuffedItems` | Modifies the Noise derived stat | `noi*0.8`
72 | `nrs` | NormalizedRunSpeed | Derived from movement | | 
66 | `oad` | OverallArmorDefense | Derived from equipped items | | 
85 | `ore` | Overreadness | 0 | | 
84 | `osl` | Oversleepness | 0 | | 
67 | `owa` | OverallWeaponAttack | Derived from equipped items | | 
143 | `owl` | Owl | 0 | Whether you can see in the dark | `owl+1`
118 | `pbm` | CraftedPotionsBuyMarginAdjust | 0 | Modifies the percentage amount of money received in trade for crafted potions | 
116 | `pds` | PicklockDmgSpeed | `PicklockDmgSpeed` | Modifies the rate at which lockpicks are damaged | 
135 | `pla` | PlatingRatio | Derived from equipped items | | 
101 | `poi` | Poisoning | 0 | You've been poisoned | `poi=1`
102 | `pos` | PocketSight | 0 | reveals some number of items while pickpocketing | `pos+2`
128 | `ppr` | PickpocketProtection | Derived from `soul.soul_vip_class_id` | | 
93 | `prb` | PerceptionPriorityBoost | 0 | | 
132 | `prc` | PicklockReturnChance | 0 | Modifies the percentage chance of repairing a broken lockpick | `prc+0.2`
58 | `pt1` | PerfectThrowMultiplier1 | 1 | | 
59 | `pt5` | PerfectThrowMultiplier5 | 1 | | 
103 | `ran` | RobbedAngriness | 0 | | `ran+1`
44 | `rch` | RelativeCharisma | `Charisma / StatCap` | | 
80 | `rcw` | RelativeCarriedWeight | `CarriedWeight / InventoryCapacity` | | 
87 | `rdq` | ReadingQuality | `DefaultReadingQuality` | It doesn't matter to you where you read, you get a learning bonus anywhere you read | `rdq>1`
119 | `rml` | RandomMoneyLoot | 0 | | 
144 | `rms` | RealMoveSpeedMod | 1 | | 
73 | `rsa` | RelativeMovementSpeedAddition | `lerp(-MaxAgilityToMovementSpeedAddition, MaxAgilityToMovementSpeedAddition, Agility / StatCap)` | | 
52 | `sdt` | StaminaDerivation | Derived from Vitality, MaxHealthyStamina, ArmorLoad, Stamina, HorseRiding, and many others. | | 
117 | `sha` | BowSelfHarmAttack | 0 | | 
89 | `sle` | Sleeping | 0 | | 
113 | `sma` | SellMarginAdjust | 0 | Modifies the percentage amount of money given in trade | `sma-0.2`
53 | `src` | StaminaRegenCooldown | `StamRegenCooldown` | Used in injured_head buff effect | `src+1`
125 | `sur` | Surrendering | 0 | 0 - opponent is not surrendering, 1 - opponent is surrendering | `sur=1`
91 | `ufo` | UnconsciousnessFadeoutSpeed | `UnconsciousDepthFadeoutSpeedBase + VitalityToUnconsciousDepthFadeoutSpeed * Vitality / StatCap` | infinite_unconsciousness buff | `ufo×100`
129 | `upr` | UnconsciousnessProtection | Derived from `soul.soul_vip_class_id` | 0 - disabled, 1 - enabled | `upr=1`
45 | `vib` | Visibility | `EquipVisib + MovementVisibilityPenalization + LightProbeVisibility` | Adjusts visibility | `vib-10`
55 | `vir` | ViewRadius | `min(MinViewRadius + VisionToViewRadius * TimeOfDayCoef * (Vision - 1), MaxViewRadius)` | | 
106 | `was` | RangedWeaponAimSpread | `AimSpreadMax * (1 - WeaponBow * AimSpreadSkillDecrease)` | Ranged weapon accuracy | `was-0.25`
136 | `wbc` | WeaponBuffCharges | `lerp(MinWeaponBuffCharge, MaxWeaponBuffCharge, random)` | Adjusts the number of poison charges applied to a weapon | `wbc×1.3`
68 | `wud` | WeaponUsageDamageMod | `lerp(1, MaxFencingWeaponUsageMod, Fencing / SkillCap)` | | 
83 | `xpm` | XPMultiplier | `soul.xp_multiplier` | Modifies the amount of experience gained | 

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

ID | Abbr | Internal Name | Description
---: | :--- | :--- | :---
153 | | `StaminaRegenCooldown` |
154 | | `HasUnholsteredWeapon` |
155 | | `HasUnholsteredMissileWeapon` |
156 | | `HasRaisedWeapon` |
157 | | `IsBlocking` |
158 | | `IsAiming` |
159 | | `HasActiveThreats` |
160 | | `IsInCombatDanger` |
161 | | `IsActiveInCombat` |
162 | | `IsRunning` |
163 | | `WasRunning` |
164 | | `WannaSprint` |
165 | | `IsMoving` |
166 | | `WasMoving` |
167 | | `IsSprinting` |
168 | | `WasSprinting` |
169 | | `IsOnHorse` |
170 | | `IsStealth` |
171 | | `IsPotentialStealth` |
172 | | `IsInAir` |
173 | | `HasLimitedRunByItem` |
174 | | `HasLimitedSprintByItem` |

## Unknown Stats

Abbr | Internal Name | Example | Description
:--- | :--- | :--- | :---
`---` | Stat_Last | |
`---` | DerivStat_Last | |