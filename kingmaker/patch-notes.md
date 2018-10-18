<!-- TITLE: Patch Notes -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Patch Notes
## v1.0.10
Manifest ID: `4137201467282432792`

### Assembly Changes

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp/Kingmaker | `Player.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Achievements | `ActionAchievementIncrementCouner.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Achievements | `ActionAchievementUnlock.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UnitLogic/Mechanics/Actions | `ContextActionResetAlignment.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints/Root | `BlueprintRoot.cs`
Added | cs | Assembly-CSharp/Kingmaker/Blueprints/Root | `PlayerUpgradeActionsRoot.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Controllers/GlobalMap | `LocationRevealController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Controllers/Units | `UnitLifeController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `AddCampingEncounter.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `AlignmentSelector.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `AreaEntranceChange.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `Conditional.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `GainExp.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `GiveObjective.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `IncrementFlagValue.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `ItemGive.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `ItemRemove.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `ItemSetCharges.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `LockFlag.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `MakeItemNonRemovable.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `MarkAnswersSelected.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `MarkCuesSeen.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `MarkLocationClosed.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `MarkLocationExplored.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `RecruitInactive.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `RemoveCampingEncounter.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `ResetLocationPerceptionCheck.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `ResetQuestObjective.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `RomanceDecrease.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `RomanceIncrease.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `RomanceLock.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `RomanceSetMaximum.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `RomanceSetMinimum.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `SetObjectiveStatus.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `SwitchBrain.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `SwitchChapter.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `UnlockCompanionStory.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `UnlockCookingRecipe.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `UnlockFlag.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `UnlockLocation.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `UnlockMapEdge.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `UnmarkAnswersSelected.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `Unrecruit.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `AlignmentCheck.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `AnswerListShown.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `AnswerSelected.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `CompanionInParty.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `CompanionIsDead.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `CompanionIsLost.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `CueSeen.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `CurrentChapter.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `False.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `FlagInRange.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `FlagUnlocked.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `ItemsEnough.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `LocationRevealed.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `ObjectiveStatus.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `OrAndLogic.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `PlayerAlignmentIs.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `QuestStatus.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Evaluators | `CompanionInParty.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `ThreadedGameLoader.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgradeSystem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeAction.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeActionType.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `BlueprintPlayerUpgrader.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgraderAllowedAttribute.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgraderFilterAttribute.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39994_ReplaceAlondiBlueprint.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40067_JubilostFrog.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40242_FixAmiriMortality.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40372_KT_PitaxAftermath.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40377_DismemberedCompanionFixer.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Items | `ItemEntity.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Items | `ItemEntityShield.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom | `KingdomTimelineManager.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionActivateEventDeck.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionAddBPRandom.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionAddBuff.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionAddFreeBuilding.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionArtisanRequestHelp.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionCollectLoot.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionConquerRegion.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionDisable.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionFoundKingdom.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionGetArtisanGift.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionGiveLoot.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionImproveStat.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionModifyBuildTime.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionModifyClaims.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionModifyLeaderBonus.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionModifyMapSpeed.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionModifyRankTime.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionModifyRE.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionModifyStatRandom.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionModifyStats.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionModifyUnrest.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionRemoveBuff.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionRemoveEvent.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionRemoveEventDeck.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionRequestArtisanGift.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionResolveEvent.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionRestartEvent.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionSetAlignment.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionSetPossibleLeader.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionSetRegionalIncome.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionStartEvent.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionUnlockArtisan.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomAlignmentIs.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomArtisanState.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomBPCheck.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomBuffIsActive.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomDay.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomEventCanStart.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomEventIsActive.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomExists.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomHasResolvableEvent.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomHasUpgradeableSettlement.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomLeaderIs.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomLeaderIsAssigned.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomLeaderIsAvailable.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomLeaderSelectionAvailable.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomProjectIsAvailable.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomRegionHasBuilding.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomRegionIsConquered.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomRegionIsUpgraded.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomSettlementCount.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomStatCheck.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomStatIsMaximum.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Conditions | `KingdomUnrestCheck.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Settlements | `SettlementBuildingWindow.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Settlements | `SettlementBuildingWindowBase.cs`
Added | cs | Assembly-CSharp/Kingmaker/PubSubSystem | `IUnitFinallyDeadHandler.cs`
Modified | cs | Assembly-CSharp/Kingmaker/RuleSystem/Rules | `RuleApplyBuff.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI | `DialogNotificationPhrase.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Journal | `JournalQuestLog.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Journal | `JournalQuestNaviElement.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/MapObjectOvertip | `MapObjectOvertipController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Overtip | `OvertipStandartHitPoints.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Settlement | `BuildingItemStatList.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic | `UnitDescriptor.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Alignments | `AlignmentHistoryRecord.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Alignments | `UnitAlignment.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/FactLogic | `AddStatBonus.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/FactLogic | `CompanionImmortality.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/FactLogic | `DropLootAndDestroyOnDeactivate.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Visual/CharacterSystem | `Character.cs`

## v1.0.9
Manifest ID: `3329346642708156469`

### Assembly Changes

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp | `-PrivateImplementationDetails-.cs`
Modified | cs | Assembly-CSharp/Kingmaker/AreaLogic/Cutscenes/Commands | `CommandCameraFollow.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints | `BlueprintPortrait.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints/Classes/Prerequisites | `PrerequisitePet.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints/Facts | `Fact.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `AddPremiumReward.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `ActivateTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DamageToMapObjectTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DeactivateTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DeviceInteractionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DoorInteractionViewTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `EvaluatedUnitCombatTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `EvaluatedUnitDeathTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `EvaluatedUnitHealthTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `GenericInteractionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `MapObjectPerceptionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `PerceptionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `RestTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `ScriptZoneTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `SkillCheckInteractionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `SpellCastTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `SummonPoolTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `TimeOfDayChangedTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `UIEventTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `UnitDeathTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `UnitHealthTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Facts | `WeaponTypeDamageStatReplacement.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Entities | `AreaEffectEntityData.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `SaveManager.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `SteamSavesReplicator.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgraderBase.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgradeSystem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeAction.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeActionType.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39514_CompleteLostRelic.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39610_HonorAndDuty.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39732_CoronationObjectives.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39777_FixEkunQuestFail.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39964_FeastOfFeasts.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39976_FailAmiriQuest.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40164_Economy7MissingBuffs.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40167_CapitalCityUpgrade.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40170__DivineRank6Unstuck.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40208_CompleteSuramgaminQuest.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40269_ResolveCommunityRankUp.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40361_FixDoomCounter.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40362_CompleteAncestorObjective.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40520_MonsterTactician.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40635_StoneCapitalKingdom.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Stats | `ModifiableValue.cs`
Modified | cs | Assembly-CSharp/Kingmaker/GameModes | `GameModesFactory.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/AI | `KingdomAIRunner.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Blueprints | `BlueprintKingdomProject.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Blueprints | `KingdomRoot.cs`
Added | cs | Assembly-CSharp/Kingmaker/Kingdom/Blueprints | `KingdomProjectType.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Rules | `RuleCalculateBPGain.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI | `GameOverManager.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Common | `UIUtilityItem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Common/Animations | `FadeAnimator.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Kingdom | `KingdomEventHand.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Kingdom | `KingdomEventHandComplite.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Kingdom | `KingdomRegionWindow.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Kingdom | `KingdomRegionWindowUpgradeItem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Vendor | `VendorMassSale.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Vendor | `VendorUISlotsController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Abilities/Blueprints | `BlueprintAbilityAreaEffect.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/FactLogic | `CompanionImmortality.cs`


## v1.0.8c
Manifest ID: `7773343900112385919`

### Assembly Changes

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `UnitIsDead.cs`
Added | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `UnitIsNull.cs`

## v1.0.8b
Manifest ID: `4551845841087663139`

### Assembly Changes

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp/Kingmaker | `Player.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints/Facts | `Fact.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `ActivateTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DamageToMapObjectTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DeactivateTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DeviceInteractionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DoorInteractionViewTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `EvaluatedUnitCombatTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `EvaluatedUnitDeathTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `EvaluatedUnitHealthTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `GenericInteractionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `MapObjectPerceptionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `PerceptionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `RestTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `ScriptZoneTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `SkillCheckInteractionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `SpellCastTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `SummonPoolTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `TimeOfDayChangedTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `UIEventTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `UnitDeathTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `UnitHealthTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `SaveManager.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `SceneLoader.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `ThreadedGameLoader.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `IJsonUpgrader.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgraderBase.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgradeSystem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeAction.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeActionType.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `ActiveKingdomEventsRemover.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40021_FixKingdomStoryDestruction.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40174_NokNokOtpExit.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40291_MakeTristianMortal.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40305_BokkenResurrection.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Common | `UIUtilityItem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/MapObjectOvertip | `AreaTransitionController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic | `UnitDescriptor.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Mechanics | `MechanicsContext.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Parts | `UnitPartSummonedMonster.cs`
Modified | cs | Assembly-CSharp/Kingmaker/View | `ObstacleAnalyzer.cs`
Modified | cs | Assembly-CSharp/Kingmaker/View/MapObjects | `RestInteraction.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Visual | `BackgroundBlurForUI.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Visual/CharacterSystem | `Character.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Visual/CharacterSystem | `CharacterTextureDescription.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Visual/LocalMap | `LocalMapRenderer.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Visual/Water | `PlanarReflectionAndRefraction.cs`

## v1.0.7
Manifest ID: `5750998838144035341`

### Assembly Changes

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Added | cs | Assembly-CSharp/Kingmaker | `GameVersion.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints | `CalendarRoot.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints | `GameDateFormat.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Controllers | `EntityDestructionController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `ActivateTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DamageToMapObjectTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DeactivateTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DeviceInteractionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DoorInteractionViewTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `EvaluatedUnitCombatTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `EvaluatedUnitDeathTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `EvaluatedUnitHealthTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `GenericInteractionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `MapObjectPerceptionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `PerceptionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `RestTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `ScriptZoneTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `SkillCheckInteractionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `SpellCastTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `SummonPoolTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `TimeOfDayChangedTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `UIEventTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `UnitDeathTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `UnitHealthTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Buffs | `DifficultyStatAdvancement.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Buffs | `SpeedBonusInArmorCategory.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Facts | `ArcaneBloodlineArcana.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Facts | `MetamagicRodMechanics.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `ZipSaver.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgraderBase.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgradeSystem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39479_AmiriUnhide1.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39649_SeedOfSorrowObjective.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39649_SeedOfSorrowObjective2.cs`
Modified | cs | Assembly-CSharp/Kingmaker/RuleSystem/Rules/Abilities | `RuleCalculateAbilityParams.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Common | `UIUtilityItem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/IngameMenu | `IngameMenuController.cs`
Added | cs | Assembly-CSharp/Kingmaker/UI/MainMenuUI | `MainMenuVersion.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/ActivatableAbilities | `ActivatableAbilityResourceLogic.cs`
Modified | cs | Assembly-CSharp/Kingmaker/View/MapObjects | `LootComponent.cs`

## 3625063316203614488
### Assembly Changes

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem | `SceneEntitiesState.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgradeSystem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeAction.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeActionType.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `EnchantmentFeaturesForFixing.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40261_FixDuplicateEnchantments.cs`

## 946625482595150857
### Assembly Changes

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints/Facts | `Fact.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `ActivateTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DamageToMapObjectTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DeactivateTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DeviceInteractionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `DoorInteractionViewTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `EvaluatedUnitCombatTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `EvaluatedUnitDeathTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `EvaluatedUnitHealthTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `GenericInteractionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `MapObjectPerceptionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `PerceptionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `RestTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `ScriptZoneTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `SkillCheckInteractionTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `SpellCastTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `SummonPoolTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `TimeOfDayChangedTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `UIEventTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `UnitDeathTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `UnitHealthTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Items | `ItemEntityShield.cs`

## v1.0.6
Manifest ID: `6336459653349909543`

### Assembly Changes

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp/Kingmaker | `Player.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints | `FactCollection.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints/Facts | `Fact.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints/Root/Strings | `UITooltips.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `Unrecruit.cs`
Added | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Conditions | `ChangeableDynamicIsLoaded.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Buffs | `PowerfulCharge.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/EquipmentEnchants | `EquipmentWeaponTypeDamageStatReplacement.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/EquipmentEnchants | `NaturalDamageStatReplacement.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Facts | `DamageGrace.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Facts | `WeaponConditionalEnhancementBonus.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Facts | `WeaponParametersDamageBonus.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Facts | `WeaponTypeDamageStatReplacement.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/WeaponEnchants | `WeaponDamageMultiplierStatReplacement.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/WeaponEnchants | `WeaponDamageStatReplacement.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/TempMapCode/Capital | `CapitalCompanionLogic.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Entities | `UnitEntityData.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `AreaDataStash.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `SceneLoader.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgraderBase.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgradeSystem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeAction.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeActionType.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39745_Tristian_Part1_CapitalTrigger.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39745_Tristian_Part2_LockFlag.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39810_EkundayoLateRecruit.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39925_AmiriUnhide3.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF40011_CloseBrevoyBorderlands.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Items | `ItemEntity.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Items | `ItemsCollection.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Items/Slots | `ItemSlot.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom | `KingdomTimelineManager.cs`
Modified | cs | Assembly-CSharp/Kingmaker/RuleSystem/Rules | `RuleCalculateWeaponStats.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/GlobalMap | `GlobalMapLocationInfo.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/GlobalMap | `GlobalMapMessageBox.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/ServiceWindow/CharacterScreen | `CharSComponentAbilitySlot.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/SettingsUI | `DifficultySettingsController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/SettingsUI | `SettingsRoot.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Tooltip | `DescriptionBuilderTemplates.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Utility | `TypeExtensions.cs`

## v1.0.5
Manifest ID: `7894022154904016667`

### Assembly Changes

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp/Kingmaker | `Player.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBFeatureSelector.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBSelectorLayer.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBuildSelectorItem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints | `CalendarRoot.cs`
Added | cs | Assembly-CSharp/Kingmaker/Blueprints/Classes/Prerequisites | `PrerequisiteParametrizedWeaponSubcategory.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints/Root/Strings | `UITooltips.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Controllers/GlobalMap | `MapMovementController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `AreaDidLoadTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Facts | `ReplaceCasterLevelOfAbility.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Facts | `WeaponGroupAttackBonus.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `AreaDataStash.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `SceneLoader.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgradeSystem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeAction.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeActionType.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39479_AmiriUnhide1.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `BuildVarnhold.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `DisappearedTristianFix.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39479_AmiriUnhide2.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39783_OpenTechnicLeagueEncampment.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Globalmap | `GlobalMapRules.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Globalmap/State | `MapTravelData.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom | `RegionState.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Actions | `KingdomActionFillSettlement.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/AI | `KingdomAIRunner.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Kingdom/Settlements | `SettlementState.cs`
Modified | cs | Assembly-CSharp/Kingmaker/RuleSystem/Rules/Damage | `RulePrepareDamage.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI | `CursorController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Common | `UIUtility.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/IngameMenu | `IngameMenuController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Journal | `JournalQuestElement.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp | `CharBSelectionSwitchSpells.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp | `CharBSelectorFilter.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp/Phase | `CharBPhaseSpells.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/ServiceWindow | `SpellBookCharacteristics.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/ServiceWindow | `SpellBookLevelTabs.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Settlement | `SettlementsBuildSlots.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Tooltip | `DescriptionBuilderTemplates.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Vendor | `CharDollInTrade.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Abilities/Components/TargetCheckers | `AbilityTargetStatCondition.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Buffs | `BuffCollection.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/FactLogic | `IncreaseResourceAmount.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Visual/Particles | `SnapToLocator.cs`

## 4920380694923421717
### Assembly Changes

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp/Kingmaker | `GameStarter.cs`
Modified | cs | Assembly-CSharp/Kingmaker | `MainMenu.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBFeatureSelector.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBSelectorLayer.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBuildSelectorItem.cs`
Added | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `AreaDidLoadTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Facts | `AdditionalSneakDamageOnHit.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Facts | `BackToBack.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgradeSystem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeAction.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeActionType.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `JaethalQ3EssentialForGameFixer.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39479_AmiriUnhide1.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39480_JubilostQuest.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `RemoveCutsceneRaiseDeadFromSpellbooks.cs`
Modified | cs | Assembly-CSharp/Kingmaker/RuleSystem/Rules/Abilities | `RuleCastSpell.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Group | `GroupController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/SettingsUI | `GameSettingsController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/SettingsUI | `GraphicsSettingsController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic | `Spellbook.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic | `UnitDescriptor.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Buffs | `RemoveBuffOnLoad.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Buffs/Blueprints | `BlueprintBuff.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Mechanics/Components | `AddInitiatorSkillRollTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Utility | `SystemUtil.cs`
Modified | cs | Assembly-CSharp/Kingmaker/View | `CameraRig.cs`

## v1.0.4
Manifest ID: `6358573070219561752`

### Assembly Changes

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp/Kingmaker | `Player.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBSelectionSwitchItem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBSelectorLayer.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Controllers/Clicks/Handlers | `ClickGroundHandler.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Controllers/Rest | `RestController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `AddPremiumReward.cs`
Added | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Events | `TurnOnTrigger.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Buffs | `SpeedBonusInArmorCategory.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI | `ClickPointerManager.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI | `ClickPointerPrefab.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI | `DoubleClickableElement.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Common | `UIUtilityTexts.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Group | `GroupCharacterPortraitController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp | `CharacterBuildController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp | `CharBSelectionSwitchFeatures.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/RestCamp | `RestTimelineEvent.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/ServiceWindow | `ItemSlot.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/ServiceWindow/CharacterScreen | `CharSClassTree.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/UnitSettings | `MechanicActionBarSlotItem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Vendor | `FilterController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Vendor | `SlotsGroup.cs`
Modified | cs | Assembly-CSharp/UIExtension/Controllers | `VirtualList.cs`

## v1.0.2
Manifest ID: `229482041491868730`

### Assembly Changes

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp/Kingmaker | `Player.cs`
Modified | cs | Assembly-CSharp/Kingmaker/AreaLogic/QuestSystem | `QuestBook.cs`
Modified | cs | Assembly-CSharp/Kingmaker/AreaLogic/QuestSystem | `QuestObjective.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBFeatureSelector.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBSelectionSwitch.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBSelectionSwitchItem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBSelectorLayer.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Assets/UI/LevelUp | `CharBuildSelectorItem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Controllers/Clicks/Handlers | `ClickWithSelectedAbilityHandler.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Controllers/Units | `UnitActivatableAbilitiesController.cs`
Added | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `ResetQuestObjective.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `AreaDataStash.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgraderBase.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgradeSystem.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeAction.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `PlayerUpgradeActionType.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `ArtisanAddMim.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `KillingEkunFailQuest.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `MorgalanArrestQuestObjectiveFixer.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `PF39413_JaethalUnhide.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `VarraskQuests.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp | `CharacterBuildController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp | `CharBMenu.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp | `CharBMenuButton.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp | `CharBSelectorFilter.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp | `CharBSelectorFilterState.cs`
Added | cs | Assembly-CSharp/Kingmaker/UI/LevelUp | `CharBSelectionSwitchFeatures.cs`
Added | cs | Assembly-CSharp/Kingmaker/UI/LevelUp | `CharBSelectionSwitchSpells.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp/NewGame | `NewGameWinMenu.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp/Phase | `CharBPhase.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp/Phase | `CharBPhaseClass.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp/Phase | `CharBPhaseClassInChargen.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp/Phase | `CharBPhaseFeatures.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp/Phase | `CharBPhasePortrait.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp/Phase | `CharBPhaseRace.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/LevelUp/Phase | `CharBPhaseSpells.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Abilities | `AbilityData.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/ActivatableAbilities | `BlueprintActivatableAbility.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Class/LevelUp | `LevelUpController.cs`

## v1.0.2
Manifest ID: `2451367926564256244`

### Assembly Changes

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp | -PrivateImplementationDetails-.cs
Modified | cs | Assembly-CSharp | `SaveField.cs`
Modified | cs | Assembly-CSharp/Kingmaker | `GameStarter.cs`
Modified | cs | Assembly-CSharp/Kingmaker | `Runner.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints/GameDifficulties | `BlueprintDifficultyList.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints/Root/Strings | `UICommonTexts.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Blueprints/Root/Strings/GameLog | `DamageLogMessage.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/EventConditionActionSystem/Actions | `Recruit.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/EquipmentEnchants | `EquipmentWeaponTypeEnhancement.cs`
Added | cs | Assembly-CSharp/Kingmaker/Designers/Mechanics/Facts | `SavesFixerFactReplacer.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `LoadingProcess.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `SaveManager.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `ThreadedGameLoader.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgraderBase.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning | `JsonUpgradeSystem.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `ActiveKingdomEventsRemover.cs`
Added | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence/Versioning/Upgraders | `TutorialWolvesRemover.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Localization | `LocalizationManager.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Localization/Shared | `LocaleExtensions.cs`
Modified | cs | Assembly-CSharp/Kingmaker/RuleSystem/Rules/Damage | `RuleCalculateDamage.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI | `DialogMessageBox.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/CombatText | `CombatTextManager.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Loot | `LootCollector.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/SettingsUI | `SettingsListItemGameDifficulty.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Tooltip | `TooltipsController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Vendor | `SlotsGroup.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic | `UnitDescriptor.cs`
Added | cs | Assembly-CSharp/Kingmaker/UnitLogic/Buffs | `RemoveBuffOnLoad.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UnitLogic/Buffs/Components | `AddEffectRegeneration.cs`
Added | cs | Assembly-CSharp/Kingmaker/UnitLogic/FactLogic | `AddPostLoadActions.cs`

## v1.0.1
Manifest ID: `1412067188604596331`

### Assembly Changes

Modification | Ext. | Relative Directory | Name
:--- | :--- | :--- | :---
Modified | cs | Assembly-CSharp/Kingmaker | `GameStatistic.cs`
Modified | cs | Assembly-CSharp/Kingmaker | `Player.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `AreaDataStash.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `SaveManager.cs`
Modified | cs | Assembly-CSharp/Kingmaker/EntitySystem/Persistence | `SceneLoader.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Localization/Shared | `LocaleData.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Localization/Shared | `LocalizedStringData.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Common/Animations | `WindowAnimator.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Group | `GroupCharacter.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Group | `GroupController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/Kingdom | `KingdomRecurrentRavenController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/UI/SettingsUI | `GraphicsSettingsController.cs`
Modified | cs | Assembly-CSharp/Kingmaker/View | `CameraRig.cs`
Modified | cs | Assembly-CSharp/Kingmaker/Visual/Decals | `ScreenSpaceDecalRenderer.cs`
