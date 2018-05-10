<!-- TITLE: Conditional AI Scripts -->
<!-- SUBTITLE: Conditional AI Scripts -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Conditional AI Scripts
```csharp
[ConditionalScript("Has Forced Action", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool HasForcedAction(Guid objectGuid)

[ConditionalScript("Has Queued Action", "Conditionals\\AI")]
[ScriptParam0("Object", "Object to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool HasQueuedAction(Guid objectGuid)

[ConditionalScript("Has Valid Interaction Object", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool HasValidInteractionObject(Guid objectGuid)

[ConditionalScript("Is Auto Attack Enabled", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsAutoAttackEnabled(Guid objectGuid)

[ConditionalScript("Is Casting Ability", "Conditionals\\AI")]
[ScriptParam0("Object", "Object to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
[ScriptParam1("Ability", "Ability to test.", "", "07e64617-1712-4cc0-b72a-d513a5dbcfae", Scripts.BrowserType.GameData)]
public static bool IsCastingAbility(Guid objectGuid, Guid abilityGuid)

[ConditionalScript("Is Casting With Primary Attack", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsCastingWithPrimaryAttack(Guid objectGuid)

[ConditionalScript("Is Current Action Finished", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsCurrentActionFinished(Guid objectGuid)

[ConditionalScript("Is Current Action Mid Cast", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsCurrentActionMidCast(Guid objectGuid)

[ConditionalScript("Is Current Action Ready", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsCurrentActionReady(Guid objectGuid)

[ConditionalScript("Is Current Action Type", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
[ScriptParam1("Action Type", "Check if the current action is this type.", Game.AI.Action.ActionType.Attack)]
public static bool IsCurrentActionType(Guid objectGuid, Game.AI.Action.ActionType actionType)

[ConditionalScript("Is Current Action Valid", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsCurrentActionValid(Guid objectGuid)

[ConditionalScript("Is Far From Follow Object", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
[ScriptParam1("Distance Squared", "Check if follow object is further than specified distance.", 36)]
public static bool IsFarFromFollowObject(Guid objectGuid, float distanceSquared)

[ConditionalScript("Is Forced Action Targeting Hostile", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsForcedActionTargetingHostile(Guid objectGuid)

[ConditionalScript("Is Forced Action Valid", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsForcedActionValid(Guid objectGuid)

[ConditionalScript("Is Full Attack", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsFullAttack(Guid objectGuid)

[ConditionalScript("Is Grapple Interrupted", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsGrappleInterrupted(Guid objectGuid)

[ConditionalScript("Is Grapple Missed", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsGrappleMissed(Guid objectGuid)

[ConditionalScript("Is Hostile Investigation", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsHostileInvestigate(Guid objectGuid)

[ConditionalScript("Is Instant Cast", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsInstantCast(Guid objectGuid)

[ConditionalScript("Is Mover Blocked", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check for movement block (should only be called directly after a MoveState completes).", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsMoverBlocked(Guid objectGuid)

[ConditionalScript("Is Reload Required", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsReloadRequired(Guid objectGuid)

[ConditionalScript("Is Schedule Interacting With Time Slice Object", "Conditionals\\AI")]
[ScriptParam0("Object", "Object to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
[ScriptParam1("Time Slice Index", "Index of the AI schedule time slice to compare.", 0)]
public static bool IsScheduleInteractingWithTimeSliceObject(Guid objectGuid, int timeSliceIndex)

[ConditionalScript("Is Time To", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsTimeTo(Guid objectGuid)

[ConditionalScript("Is Time To Reevaluate Primary Attack", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsTimeToReevaluatePrimaryAttack(Guid objectGuid)

[ConditionalScript("Is Within Range and LOS", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsWithInRangeAndLOS(Guid objectGuid)
```
