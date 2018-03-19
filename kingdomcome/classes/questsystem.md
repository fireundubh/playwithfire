<!-- TITLE: Questsystem -->
<!-- SUBTITLE: Questsystem -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# QuestSystem Class
## Methods

Method | Return Type | Description
--- | --- | ---
`ActivateQuest(string: questName, [boolean: unknown])` |
`AreQuestVIPsAlive(string: questName)` | boolean
`CancelObjective(string: questName, string: objectiveName, boolean: sendMessage)` |
`CancelQuest(string: questName, [unknown: flag])` | 
`CanRepeatQuest(string: questName)` | boolean
`CompleteObjective(string: questName, string: objectiveName)` |
`DeactivateQuest(string: questName)`  |
`GetActiveObjectives(string: questName)` |
`GetObjectiveExpCoeff(string: questName, string: objectiveName)` | float
`IsObjectiveCanceled(string: questName, string: objectiveName)` | boolean
`IsObjectiveCompleted(string: questName, string: objectiveName)` | boolean
`IsObjectiveStarted(string: questName, string: objectiveName)` | boolean
`IsObjectiveTrackedCompleted(string: questName, string: objectiveName)` | boolean
`IsObjectiveUnchanged(string: questName, string: objectiveName)` | boolean
`IsQuestActivated(string: questName)` | boolean
`IsQuestAvailable(string: questName)` | boolean
`IsQuestCanceled(string: questName)` | boolean
`IsQuestCompleted(string: questName)` | boolean
`IsQuestStarted(string: questName)` | boolean
`IsQuestUnchanged(string: questName)` | boolean
`RegisterQuestEntity(uuid: entityId)` |
`ResetQuest(string: questName)` |
`StartObjective(string: questName, string: objectiveName)` | 
`StartQuest(string: questName)` |
`TriggerCondition(string: questName, string: objectiveName, conditionId)` |
`UserEnteredTrigger(placeAssetId, user)` | boolean