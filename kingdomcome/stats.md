<!-- TITLE: Stats and Derived Stats -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Stats and Derived Stats

These tables are incomplete and works-in-progress.

**Note:** The `×` symbol is used in these tables to avoid formatting issues. In practice, the correct operator is the asterisk (`*`).

## Stats

ID | Abbr. | Internal Name | Example | Description
--- | --- | --- | --- | ---
33 | `agi` | Stat_Agility | agi+1 | Modifies the Agility stat
38 | `bar` | Stat_Barter | bar+3 | Modifies the Barter stat
39 | `cou` | Stat_Courage | cou+2 | Modifies the Courage stat
37 | `hea` | Stat_Hearing | hea=0 | Modifies the Hearing stat
41 | `prg` | Stat_StoryProgress | | 
40 | `rep` | Stat_PlayerReputation | | 
35 | `spc` | Stat_Speech | spc+1 | Modifies the Speech stat
32 | `str` | Stat_Strength | str+1 | Modifies the Strength stat
36 | `vis` | Stat_Vision | vis×0.3 | Modifies the Vision stat
34 | `vit` | Stat_Vitality | vit+1 | Modifies the Vitality stat

## Derived Stats

ID | Abbr. | Internal Name | Example | Description
--- | --- | --- | --- | ---
78 | `aco` | DerivStat_ArmorCollisionWeight | aco×6 | Modifies the impact weight of armor when colliding with another entity 
180 | `act` | | | 
175 | `ade` | | ade×0.9 | Defence
141 | `adm` | DerivStat_AlcoholDigestMod | | Modifies the rate of alcohol digestion
178 | `ahm` | Mounted Attack Damage | ahm×1.15 | Modifies the amount of attack damage while mounted
200 | `ain` | | ain×1.3 | Modifies the chance to cause bleeding
139 | `alc` | DerivStat_Alcoholism | | 
65 | `alo` | DerivStat_ArmorLoad | alo=-0.2 | test buffs: suppress armor load
95 | `apa` | DerivStat_AlcoholPoisoningAntidote | | 
127 | `apr` | DerivStat_AttackProtection | | 
123 | `arr` | DerivStat_ArmorRating | arr×1.3 | Modifies the chance to cause enemies to flee
181 | `asp` | | asp×0.75 | Related to (right arm?) injuries
99 | `bad` | DerivStat_Badassness | bad+3 | Modifies the Badassness derived stat
122 | `bld` | DerivStat_Bloodiness | | 
74 | `ble` | DerivStat_BleedingTotal | | 
114 | `bma` | DerivStat_BuyMarginAdjust | bma+0.15 | Modifies the percentage amount of money received in trade
76 | `bow` | DerivStat_BodyWeight | | 
108 | `brm` | DerivStat_BadReputationMod | brm×1.5 | Modifies the influence of negative actions on reputation
121 | `bso` | DerivStat_BasketSuspiciencyMod | bso+0.5 | 
142 | `btw` | DerivStat_BoidThreatWeight | btw×0.4 | Modifies the skittishness of wild animals
86 | `caf` | DerivStat_Caffeine | | 
96 | `cag` | DerivStat_CombatAggression | | 
64 | `cap` | DerivStat_InventoryCapacity | cap+1000 | Modifies the amount of weight that can be carried before becoming encumbered
79 | `caw` | DerivStat_CarriedWeight | | 
137 | `cbi` | DerivStat_CharismaFromBuffedItems | | 
130 | `cds` | DerivStat_ClothDirtyingSpeedKm | | Modifies the rate at which clothing becomes dirty
133 | `cdw` | DerivStat_ClinchDamageToWeapon | cdw+0.15 | Modifies the percentage damage inflicted on an opponent's weapon durability
43 | `cha` | DerivStat_Charisma | cha+1 | Modifies the Charisma stat
183 | `cli` | | cli+0.4 | Modifies the chance to overpower an opponent in a clinch
90 | `coc` | DerivStat_Consciousness | | 
48 | `con` | DerivStat_Conspicuousness | con-1 | Modifies the hostile search duration of NPCs
205 | `cos` | | cos=0 | Used in limited_combat buff
77 | `cow` | DerivStat_CollisionWeight | cow+1200 | Modifies the overall impact of colliding with another entity 
57 | `dbf` | DerivStat_DiceBustFixing | | 
202 | `dee` | | dee+0.15 | Damage to armor
97 | `def` | DerivStat_Defensiveness | | 
187 | `dig` | | dig×0 | Hunger?
109 | `drt` | DerivStat_Dirtiness | | 
100 | `dru` | DerivStat_Drunkenness | | 
204 | `dsl` | | dsl×1.5 | Modifies the difficulty of dodging in combat
56 | `dtf` | DerivStat_DiceThrowFixing | | 
131 | `edm` | DerivStat_EquipmentUseDamageMultiplier | edm×0.8 | 
197 | `eep` | | eep×1.1 | Evasion Chance
111 | `enc` | DerivStat_Encumberance | | 
134 | `eqw` | DerivStat_EquippedWeight | | 
88 | `erq` | DerivStat_EffectiveReadingQuality | | 
46 | `evi` | DerivStat_EquipVisib | | 
188 | `exh` | | exh×0 | Tiredness?
201 | `fae` | | fae×2 | First Aid
112 | `fdm` | DerivStat_FallDamageMultiplier | | Modifies the amount of damage received after falling
98 | `fol` | DerivStat_DistanceFollowing | | 
54 | `fov` | DerivStat_FieldOfView | | 
94 | `fpa` | DerivStat_FoodPoisoningAntidote | | 
71 | `fsm` | DerivStat_FootstepSoundMultiplier | | Modifies the noise produced by walking and running
107 | `grm` | DerivStat_GoodReputationMod | | Modifies the influence of positive actions on reputation
60 | `hac` | DerivStat_HaggleAdditionalChances | | Modifies the number of times a trader will haggle
105 | `hcm` | DerivStat_HorseCourageMod | | Modifies the Courage stat of the mounted horse
115 | `hgs` | DerivStat_HerbGatherStrengthXp | | Modifies the amount of Strength skill experience gained from herb gathering
110 | `hko` | DerivStat_HeadHitKnockOutProbability | | Modifies the chance of knocking out an opponent with a blow to the head
184 | `hlh` | | hlh×0.5 | Chance to be wounded when attacked? Always used with `slh`
51 | `hlt` | DerivStat_Healthiness | | 
120 | `hml` | DerivStat_HorseThrowDownMoraleLimit | hml=0 | Determines whether the player's horse will throw the player outside of combat
75 | `ibi` | DerivStat_InjuryBleedingInterval | | 
104 | `iex` | DerivStat_ItemExpert | | 
126 | `imm` | DerivStat_Immortality | | 
124 | `jrm` | DerivStat_JailRecoverySpeedMod | jrm×0.8 | Modifies the rate at which the player recovers from jail time
189 | `lcs` | | lcs=0 | perk_steady_hand buff - nonexistent perk
62 | `lfu` | DerivStat_LockFailUnlockProb | lfu=0.1 | 10% chance of opening locks instantly
63 | `lio` | DerivStat_LockInstantOpenDifficulty | lio=0.3 | Modifies the maximum lock difficulty of instantly unlockable locks
207 | `lpb` | | lpb×0.1 | Adjusts the AI noise level of broken lockpicks
198 | `lpd` | | lpd×0.5 | Adjusts the difficulty rating of locks
199 | `lpn` | | lpn×1.3 | Modifies the amount of noise produced by lockpicking
47 | `lpv` | DerivStat_LightProbeVisibility | | 
61 | `lsa` | DerivStat_LockStartAngle | | Modifies the lockpick's proximity to the end of the lockpicking minigame
69 | `lvl` | DerivStat_MainLevel | | Modifies the player's Main Level
140 | `map` | DerivStat_MeanAttackPeriod | | 
82 | `mcf` | DerivStat_MoraleContextFadingMod | | 
50 | `mhs` | DerivStat_MaxHealthyStamina | | 
81 | `mor` | DerivStat_Morale | | 
49 | `mst` | DerivStat_MaxStamina | mst×1.5 | Modifies the maximum amount of the Stamina stat
92 | `mut` | DerivStat_Mute | | 
138 | `nbi` | DerivStat_NoiseFromBuffedItems | | 
70 | `noi` | DerivStat_Noise | noi×0.8 | Modifies the Noise derived stat
72 | `nrs` | DerivStat_NormalizedRunSpeed | | 
66 | `oad` | DerivStat_OverallArmorDefense | | 
85 | `ore` | DerivStat_Overreadness | | 
208 | `ors` | | ors=-1 | With Cpp:VersusDog, whether dogs bark at you. As a constant, whether souls react to you?
203 | `osb` | | osb×1.15 | Opponent's stamina cost of attacking your shield?
84 | `osl` | DerivStat_Oversleepness | | 
67 | `owa` | DerivStat_OverallWeaponAttack | | 
143 | `owl` | | owl+1 | Whether you can see in the dark 
206 | `pac` | | pac×1.5 | Chance to poison on attack
118 | `pbm` | DerivStat_CraftedPotionsBuyMarginAdjust | | Modifies the percentage amount of money received in trade for crafted potions 
182 | `pbs` | | pbs×2 | 
196 | `pdp` | | pdp×1.15 | Chance to remain in saddle when opponents attempts to unhorse you
116 | `pds` | DerivStat_PicklockDmgSpeed | | Modifies the rate at which lockpicks are damaged
135 | `pla` | DerivStat_PlatingRatio | | 
101 | `poi` | DerivStat_Poisoning | poi=1 | You've been poisoned
102 | `pos` | DerivStat_PocketSight | pos+2 | reveals some number of items while pickpocketing
128 | `ppr` | DerivStat_PickpocketProtection | | 
93 | `prb` | DerivStat_PerceptionPriorityBoost | | 
132 | `prc` | DerivStat_PicklockReturnChance | prc+0.2 | Modifies the percentage chance of repairing a broken lockpick
58 | `pt1` | DerivStat_PerfectThrowMultiplier1 | | 
59 | `pt5` | DerivStat_PerfectThrowMultiplier5 | | 
103 | `ran` | DerivStat_RobbedAngriness | ran+1 | 
44 | `rch` | DerivStat_RelativeCharisma | | 
80 | `rcw` | DerivStat_RelativeCarriedWeight | | 
87 | `rdq` | DerivStat_ReadingQuality | rdq>1 | It doesn't matter to you where you read, you get a learning bonus anywhere you read
119 | `rml` | DerivStat_RandomMoneyLoot | | 
144 | `rms` | DerivStat_RealMoveSpeedMod | | 
73 | `rsa` | DerivStat_RelativeMovementSpeedAddition | | 
195 | `rst` | | rst < 0.6 | Related to the overeating buff
179 | `rtm` | | rtm×0.5 | Chance for horse to shy at nearby foes
191 | `sco` | | sco=0 | Used in god_mode buff effect 
52 | `sdt` | DerivStat_StaminaDerivation | | 
117 | `sha` | DerivStat_BowSelfHarmAttack | | 
194 | `skp` | | skp=0 | 0 - stealth kill fail, 1 - stealth kill success
89 | `sle` | DerivStat_Sleeping | | 
185 | `slh` | | slh×0.5 | Chance to be wounded when attacked
186 | `sls` | | sls×0.7 | Stamina cost of blocking
113 | `sma` | DerivStat_SellMarginAdjust | sma-0.2 | Modifies the percentage amount of money given in trade
193 | `sra` | | sra×1.5 | Stamina regeneration rate
192 | `srb` | | | 
53 | `src` | DerivStat_StaminaRegenCooldown | src+1 | Used in injured_head buff effect
190 | `srg` | | srg×1.5 | Modifies the rate at which stamina regenerates
125 | `sur` | DerivStat_Surrendering | sur=1 | 0 - opponent is not surrendering, 1 - opponent is surrendering 
91 | `ufo` | DerivStat_UnconsciousnessFadeoutSpeed | ufo×100 | infinite_unconsciousness buff
129 | `upr` | DerivStat_UnconsciousnessProtection | upr=1 | 0 - disabled, 1 - enabled
45 | `vib` | DerivStat_Visibility | vib-10 | Adjusts visibility
55 | `vir` | DerivStat_ViewRadius | | 
177 | `wac` | | wac×0.7 | Weapon attack stamina cost
106 | `was` | DerivStat_RangedWeaponAimSpread | was-0.25 | Ranged weapon accuracy
176 | `wat` | | wat×1.2 | Weapon attack damage
136 | `wbc` | DerivStat_WeaponBuffCharges | wbc×1.3 | Adjusts the number of poison charges applied to a weapon
68 | `wud` | DerivStat_WeaponUsageDamageMod | | 
83 | `xpm` | DerivStat_XPMultiplier | | Modifies the amount of experience gained

## Other Stats

ID | Abbr | Description
--- | --- | ---
0 | `Stealth`
1 | `HorseRiding`
2 | `Fencing`
3 | `Bard`
4 | `Lockpicking`
5 | `Pickpocketing`
6 | `Alchemy`
7 | `Cooking`
8 | `Repairing`
9 | `Smithing`
10 | `Fishing`
11 | `Mining`
12 | `FirstAid`
13 | `Drinking`
14 | `Hunter`
15 | `Defense`
16 | `WeaponSword`
17 | `WeaponAxe`
18 | `WeaponBow`
19 | `WeaponCrossbow`
20 | `WeaponShield`
21 | `WeaponMace`
22 | `WeaponDagger`
23 | `WeaponLarge`
24 | `WeaponUnarmed`
25 | `Herbalism`
26 | `Reading`
27 | `Tailoring`
28 | `Armourer`
29 | `WeaponSmithing`
30 | `Shoemaking`
146 | `health`
147 | `stamina`
148 | `exhaust`
149 | `hunger`
150 | `karma`
151 | `alcoholism`
153 | `StaminaRegenCooldown`
154 | `HasUnholsteredWeapon`
155 | `HasUnholsteredMissileWeapon`
156 | `HasRaisedWeapon`
157 | `IsBlocking`
158 | `IsAiming`
159 | `HasActiveThreats`
160 | `IsInCombatDanger`
161 | `IsActiveInCombat`
162 | `IsRunning`
163 | `WasRunning`
164 | `WannaSprint`
165 | `IsMoving`
166 | `WasMoving`
167 | `IsSprinting`
168 | `WasSprinting`
169 | `IsOnHorse`
170 | `IsStealth`
171 | `IsPotentialStealth`
172 | `IsInAir`
173 | `HasLimitedRunByItem`
174 | `HasLimitedSprintByItem`
210 | `Dodge`
211 | `PerfectBlock`
212 | `Riposte`
213 | `Finticka`
214 | `StealthKnockOut`
215 | `StealthKill`
216 | `HorsePullDown`
217 | `Bumper`
218 | `Deprecated2`
219 | `Deprecated1`
220 | `Comrade`
221 | `Deprecated5`
222 | `EasyWayOut`
223 | `Deprecated4`
224 | `Reading_ArtAdmirer`
225 | `Reading_AvidReader`
226 | `_unused_`
227 | `SteakTartare`
228 | `TrialAndError`
229 | `EasyDrunk`
230 | `Deprecated3`
231 | `TrueSlav`
232 | `Bacchus`
233 | `AlchemyRoutine1`
234 | `AlchemyRoutine2`
235 | `WineBibber`
236 | `BeerBibber`
237 | `LiquorBibber`
238 | `LooseTongue`
239 | `BundleAlchemist`
240 | `HumanDustbin`
241 | `SaltAndSmoke`
242 | `_unused3_`
243 | `Witcher`
244 | `_unused2_`
245 | `EutuBrutus`
246 | `Reading_Wanderer`
247 | `Butcher`
248 | `Antlers`
249 | `Tusks`
250 | `Tanner`
251 | `Salty`
252 | `WaterOfLife`
253 | `Taunt`
254 | `HuntAttack`
255 | `MercyKill`
256 | `FirstAid`
257 | `Empathic`
258 | `Serration`
259 | `HeavyTip`
260 | `ChainStrike`
261 | `SevenLeague`
262 | `Letailleur`
263 | `Padding`
264 | `Blacksmithsson`
265 | `Last`
266 | `MovementModifier`
267 | `Inventory`
268 | `MovementType`
269 | `Stance`
270 | `Surface`
271 | `MovementSpeeds`
272 | `CombatMovement`
273 | `Perception`
275 | `StaminaUpdate`

## Unknown Stats

Abbr. | Internal Name | Example | Description
--- | --- | --- | ---
`---` | Stat_Last | |
`---` | DerivStat_Last | |