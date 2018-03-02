<!-- TITLE: Stats and Derived Stats -->

# Stats and Derived Stats
This table is incomplete and a work-in-progress.

## Usage

In `Libs\Tables\rpg\buff.xml`, buffs are defined in rows. Each row has a `params` property that generally defines the effect of the buff. The value of the `params` property consists of an expression, the abbreviated name of a stat followed by an operator and a number value, or a comma-delimited list of such expressions. For example, the Clinch Master perk has a constant buff with a `params` value of `cli+0.4`, which increases the chance that the player will overpower an opponent in a clinch by 40%. Using a different operator, such as `cli*0.4`, would dramatically change the effect.

```
<!-- Clinch Master -->
<row buff_ai_tag_id=""
     buff_class_id="4"
     buff_desc=""
     buff_exclusivity_id="1"
     buff_id="8dc445d5-cb2b-43eb-92fb-fe929806a86e"
     buff_lifetime_id="1"
     buff_name="perk_clinch_master"
     buff_ui_name=""
     buff_ui_order=""
     buff_ui_type_id="4"
     buff_ui_visibility_id="0"
     duration="-1"
     icon_id="0"
     implementation="Cpp:Constant"
     is_persistent="True"
     params="cli+0.4"
     slot_buff_ui_name=""
     slot_icon_id=""
     visual_effect="" />
```

## Data Table

**Note:** The `×` symbol is used in this table to avoid formatting issues. In practice, the correct operator is the asterisk (`*`).

Abbr. | Internal Name | Example | Description
--- | --- | --- | ---
aco | DerivStat_ArmorCollisionWeight | aco×6 | Modifies the impact weight of armor when colliding with another entity 
act |  |  | No description entered
ade |  |  | No description entered
adm | DerivStat_AlcoholDigestMod |  | Modifies the rate of alcohol digestion
agi | Stat_Agility | agi+1 | Modifies the Agility stat
ahm | Mounted Attack Damage | ahm×1.15 | Modifies the amount of attack damage while mounted
ain | | ain×1.3 | Modifies the chance to cause bleeding
alc | DerivStat_Alcoholism |  | No description entered
alo | DerivStat_ArmorLoad | alo=-0.2 | test buffs: suppress armor load
apa |  |  | No description entered
apr |  |  | No description entered
arr | | arr×1.3 | Modifies the chance to cause enemies to flee
asp |  |  | No description entered
bad | DerivStat_Badassness | bad+3 | Modifies the Badassness derived stat
bar | Stat_Barter | bar+3 | Modifies the Barter stat
bld |  |  | No description entered
ble |  |  | No description entered
bma | DerivStat_BuyMarginAdjust | bma+0.15 | Modifies the percentage amount of money received in trade
bow |  |  | No description entered
brm | DerivStat_BadReputationMod | brm×1.5 | Modifies the influence of negative actions on reputation
bso | Buy Stolen Objects | bso+0.5 | Modifies the willingness of traders to buy stolen objects
btw | DerivStat_BoidThreatWeight | btw×0.4 | Modifies the skittishness of wild animals
caf | DerivStat_Caffeine |  | No description entered
cag | DerivStat_CombatAggression |  | No description entered
cap | Carrying Capacity | cap+1000 | Modifies the amount of weight that can be carried before becoming encumbered
caw |  |  | No description entered
cbi | DerivStat_CharismaFromBuffedItems |  | No description entered
cds | DerivStat_ClothDirtyingSpeedKm |  | Modifies the rate at which clothing becomes dirty
cdw | DerivStat_ClinchDamageToWeapon | cdw+0.15 | Modifies the percentage damage inflicted on an opponent's weapon durability
cha | DerivStat_Charisma | cha+1 | Modifies the Charisma stat
cli | | cli+0.4 | Modifies the chance to overpower an opponent in a clinch
coc |  |  | No description entered
con | DerivStat_Conspicuousness | con-1 | Modifies the hostile search duration of NPCs
cos |  |  | No description entered
cou | Stat_Courage |  | Modifies the Courage stat
cow | DerivStat_CollisionWeight | cow+1200 | Modifies the overall impact of colliding with another entity 
dbf | DerivStat_DiceBustFixing |  | No description entered
dee |  |  | No description entered
def | DerivStat_Defensiveness |  | No description entered
dig | Hunger | dig×0 | No description entered
drt | DerivStat_Dirtiness |  | No description entered
dru | DerivStat_Drunkenness |  | No description entered
dsl |  | dsl×1.5 | Modifies the difficulty of dodging in combat
dtf | DerivStat_DiceThrowFixing |  | No description entered
edm | DerivStat_EquipmentUseDamageMultiplier | edm×0.8 | 
eep |  |  | No description entered
enc | Encumberance |  | No description entered
eqw | DerivStat_EquippedWeight |  | No description entered
erq | DerivStat_EffectiveReadingQuality |  | No description entered
evi | DerivStat_EquipVisib |  | No description entered
exh | Tiredness | exh×0 | No description entered
fae |  |  | No description entered
fdm | DerivStat_FallDamageMultiplier |  | Modifies the amount of damage received after falling
fol |  |  | No description entered
fov | DerivStat_FieldOfView |  | No description entered
fpa | DerivStat_FoodPoisoningAntidote |  | No description entered
fsm | DerivStat_FootstepSoundMultiplier |  | Modifies the noise produced by walking and running
grm | DerivStat_GoodReputationMod |  | Modifies the influence of positive actions on reputation
hac | DerivStat_HaggleAdditionalChances |  | Modifies the number of times a trader will haggle
hcm | DerivStat_HorseCourageMod |  | Modifies the Courage stat of the mounted horse
hea | Stat_Hearing |  | Modifies the Hearing stat
hgs | DerivStat_HerbGatherStrengthXp |  | Modifies the amount of Strength skill experience gained from herb gathering
hko | DerivStat_HeadHitKnockOutProbability |  | Modifies the chance of knocking out an opponent with a blow to the head
hlh |  | hlh×0.5 | not_so_tough_guy buff
hlt |  |  | No description entered
hml | DerivStat_HorseThrowDownMoraleLimit | hml=0 | Determines whether the player's horse will throw the player outside of combat
ibi | DerivStat_InjuryBleedingInterval |  | No description entered
iex | DerivStat_ItemExpert |  | No description entered
imm | DerivStat_Immortality |  | No description entered
jrm | DerivStat_JailRecoverySpeedMod | jrm×0.8 | Modifies the rate at which the player recovers from jail time
lcs |  |  | perk_steady_hand buff - nonexistent perk
lfu | DerivStat_LockFailUnlockProb | lfu=0.1 | 10% chance of opening locks instantly
lio | DerivStat_LockInstantOpenDifficulty | lio=0.3 | Modifies the maximum lock difficulty of instantly unlockable locks
lpb |  |  | No description entered
lpd | Lockpicking Difficulty |  | Adjusts the difficulty rating of locks
lpn | Lockpicking Noise |  | Modifies the amount of noise produced by lockpicking
lpv | DerivStat_LightProbeVisibility |  | No description entered
lsa | DerivStat_LockStartAngle |  | Modifies the lockpick's proximity to the end of the lockpicking minigame
lvl | DerivStat_MainLevel |  | Modifies the player's Main Level
map | DerivStat_MeanAttackPeriod |  | No description entered
mcf | DerivStat_MoraleContextFadingMod |  | No description entered
mhs | DerivStat_MaxHealthyStamina |  | No description entered
mor | DerivStat_Morale |  | No description entered
mst | DerivStat_MaxStamina | mst×1.5 | Modifies the maximum amount of the Stamina stat
mut | DerivStat_Mute |  | No description entered
nbi | DerivStat_NoiseFromBuffedItems |  | No description entered
noi | DerivStat_Noise | noi×0.8 | lowers or increases noise of armor
nrs | DerivStat_NormalizedRunSpeed |  | No description entered
oad | DerivStat_OverallArmorDefense |  | No description entered
ore | DerivStat_Overreadness |  | No description entered
ors |  |  | No description entered
osb |  |  | No description entered
osl | DerivStat_Oversleepness |  | No description entered
owa | DerivStat_OverallWeaponAttack |  | No description entered
pac |  |  | No description entered
pbm | DerivStat_CraftedPotionsBuyMarginAdjust |  | Modifies the percentage amount of money received in trade for crafted potions 
pbs |  |  | No description entered
pdp |  |  | No description entered
pds | DerivStat_PicklockDmgSpeed |  | Modifies the rate at which lockpicks are damaged
pla | DerivStat_PlatingRatio |  | No description entered
poi | DerivStat_Poisoning | poi=1 | You've been poisoned
pos | DerivStat_PocketSight | pos+2 | reveals some number of items while pickpocketing
ppr | DerivStat_PickpocketProtection |  | No description entered
prb | DerivStat_PerceptionPriorityBoost |  | No description entered
prc | DerivStat_PicklockReturnChance | prc+0.2 | Modifies the percentage chance of repairing a broken lockpick
prg |  |  | No description entered.
pt1 | DerivStat_PerfectThrowMultiplier1 |  | No description entered
pt5 | DerivStat_PerfectThrowMultiplier5 |  | No description entered
ran | DerivStat_RobbedAngriness | ran+1 | No description entered
rch | DerivStat_RelativeCharisma |  | No description entered
rcw | DerivStat_RelativeCarriedWeight |  | No description entered
rdq | DerivStat_ReadingQuality | rdq>1 | It doesn't matter to you where you read, you get a learning bonus anywhere you read
rep | Stat_PlayerReputation |  | Modifies the player's reputation
rml | DerivStat_RandomMoneyLoot |  | No description entered
rms | DerivStat_RelativeMovementSpeedAddition |  | No description entered
rsa |  |  | No description entered.
rst |  |  | No description entered.
rtm |  |  | No description entered.
sco |  |  | No description entered.
sdt |  |  | No description entered.
sha |  |  | No description entered.
skp |  |  | No description entered.
sle | DerivStat_Sleeping |  | No description entered
slh | |  | Unknown - Could modified the rate at which stamina recovers
sls |  | sls×0.7 | blocking costs 30% less stamina
sma | DerivStat_SellMarginAdjust | sma-0.2 | Modifies the percentage amount of money given in trade
spc | Stat_Speech | spc+1 | Modifies the Speech stat
sra | | sra×1.5 | 
srb |  |  | No description entered
src | DerivStat_StaminaRegenCooldown |  | No description entered
srg | | srg×1.5 | Modifies the rate at which stamina regenerates
str | Stat_Strength | str+1 | Modifies the Strength stat
sur | DerivStat_Surrendering |  | No description entered
ufo | DerivStat_UnconsciousnessFadeoutSpeed | ufo×100 | infinite_unconsciousness buff
upr | DerivStat_UnconsciousnessProtection |  | No description entered
vib | DerivStat_Visibility | vib-10 | Dog Person
vir | DerivStat_ViewRadius |  | No description entered
vis | Stat_Vision |  | Modifies the Vision stat
vit | Stat_Vitality | vit+1 | Modifies the Vitality stat
wac |  |  | No description entered
was |  |  | No description entered
wat | Weapon Attack | wat×1.2 | Modifies the amount of attack damage inflicted
wbc | DerivStat_WeaponBuffCharges |  | No description entered
wud | DerivStat_WeaponUsageDamageMod |  | No description entered
xpm | DerivStat_XPMultiplier |  | Modifies the amount of experience gained