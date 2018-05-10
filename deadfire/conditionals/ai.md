<!-- TITLE: Conditional AI Scripts -->
<!-- SUBTITLE: Conditional AI Scripts -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Conditional AI Scripts
## Has Forced Action

```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool HasForcedAction(Guid objectGuid)
```

## Has Queued Action
```csharp
[ScriptParam0("Object", "Object to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool HasQueuedAction(Guid objectGuid)
```

## Has Valid Interaction Object
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool HasValidInteractionObject(Guid objectGuid)
```

## Is Auto Attack Enabled
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsAutoAttackEnabled(Guid objectGuid)
```

## Is Casting Ability
```csharp
[ScriptParam0("Object", "Object to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
[ScriptParam1("Ability", "Ability to test.", "", "07e64617-1712-4cc0-b72a-d513a5dbcfae", Scripts.BrowserType.GameData)]
public static bool IsCastingAbility(Guid objectGuid, Guid abilityGuid)
```

## Is Casting With Primary Attack
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsCastingWithPrimaryAttack(Guid objectGuid)
```

## Is Current Action Finished
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsCurrentActionFinished(Guid objectGuid)
```

## Is Current Action Mid Cast
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsCurrentActionMidCast(Guid objectGuid)
```

## Is Current Action Ready
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsCurrentActionReady(Guid objectGuid)
```

## Is Current Action Type
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
[ScriptParam1("Action Type", "Check if the current action is this type.", Game.AI.Action.ActionType.Attack)]
public static bool IsCurrentActionType(Guid objectGuid, Game.AI.Action.ActionType actionType)
```

## Is Current Action Valid
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsCurrentActionValid(Guid objectGuid)
```

## Is Far From Follow Object
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
[ScriptParam1("Distance Squared", "Check if follow object is further than specified distance.", 36)]
public static bool IsFarFromFollowObject(Guid objectGuid, float distanceSquared)
```

## Is Forced Action Targeting Hostile
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsForcedActionTargetingHostile(Guid objectGuid)
```

## Is Forced Action Valid
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsForcedActionValid(Guid objectGuid)
```

## Is Full Attack
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsFullAttack(Guid objectGuid)
```

## Is Grapple Interrupted
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsGrappleInterrupted(Guid objectGuid)
```

## Is Grapple Missed
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsGrappleMissed(Guid objectGuid)
```

## Is Hostile Investigation
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsHostileInvestigate(Guid objectGuid)
```

## Is Instant Cast
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsInstantCast(Guid objectGuid)
```

## Is Mover Blocked
```csharp
[ScriptParam0("Character", "Character to check for movement block (should only be called directly after a MoveState completes).", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsMoverBlocked(Guid objectGuid)
```

## Is Reload Required
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsReloadRequired(Guid objectGuid)
```

## Is Schedule Interacting With Time Slice Object
```csharp
[ScriptParam0("Object", "Object to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
[ScriptParam1("Time Slice Index", "Index of the AI schedule time slice to compare.", 0)]
public static bool IsScheduleInteractingWithTimeSliceObject(Guid objectGuid, int timeSliceIndex)
```

## Is Time To
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsTimeTo(Guid objectGuid)
```

## Is Time To Reevaluate Primary Attack
```csharp
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsTimeToReevaluatePrimaryAttack(Guid objectGuid)
```

## Is Within Range and LOS
```csharp
[ConditionalScript("Is Within Range and LOS", "Conditionals\\AI")]
[ScriptParam0("Character", "Character to check.", "7d150000-0000-0000-0000-000000000000", Scripts.BrowserType.ObjectGuid)]
public static bool IsWithInRangeAndLOS(Guid objectGuid)
```
