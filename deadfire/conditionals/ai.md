<!-- TITLE: Conditional AI Scripts -->
<!-- SUBTITLE: Conditional AI Scripts -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Conditional AI Scripts

## Has Forced Action

```csharp
public static bool HasForcedAction(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Has Queued Action
```csharp
public static bool HasQueuedAction(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Object | Object to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Has Valid Interaction Object
```csharp
public static bool HasValidInteractionObject(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Auto Attack Enabled
```csharp
public static bool IsAutoAttackEnabled(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Casting Ability
```csharp
public static bool IsCastingAbility(Guid objectGuid, Guid abilityGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Object | Object to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`
Ability | Ability to test. |  | `07e64617-1712-4cc0-b72a-d513a5dbcfae` | `Scripts.BrowserType.GameData`


## Is Casting With Primary Attack
```csharp
public static bool IsCastingWithPrimaryAttack(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Current Action Finished
```csharp
public static bool IsCurrentActionFinished(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Current Action Mid Cast
```csharp
public static bool IsCurrentActionMidCast(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Current Action Ready
```csharp
public static bool IsCurrentActionReady(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Current Action Type
```csharp
public static bool IsCurrentActionType(Guid objectGuid, Game.AI.Action.ActionType actionType)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`
Action Type | Check if the current action is this type. | `Game.AI.Action.ActionType.Attack` |


## Is Current Action Valid
```csharp
public static bool IsCurrentActionValid(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Far From Follow Object
```csharp
public static bool IsFarFromFollowObject(Guid objectGuid, float distanceSquared)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`
Distance Squared | Check if follow object is further than specified distance. | 36 | 


## Is Forced Action Targeting Hostile
```csharp
public static bool IsForcedActionTargetingHostile(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Forced Action Valid
```csharp
public static bool IsForcedActionValid(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Full Attack
```csharp
public static bool IsFullAttack(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Grapple Interrupted
```csharp
public static bool IsGrappleInterrupted(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Grapple Missed
```csharp
public static bool IsGrappleMissed(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Hostile Investigation
```csharp
public static bool IsHostileInvestigate(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Instant Cast
```csharp
public static bool IsInstantCast(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Mover Blocked
```csharp
public static bool IsMoverBlocked(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check for movement block (should only be called directly after a MoveState completes). | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Reload Required
```csharp
public static bool IsReloadRequired(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Schedule Interacting With Time Slice Object
```csharp
public static bool IsScheduleInteractingWithTimeSliceObject(Guid objectGuid, int timeSliceIndex)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Object | Object to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`
Time Slice Index | Index of the AI schedule time slice to compare. | 0 |


## Is Time To
```csharp
public static bool IsTimeTo(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Time To Reevaluate Primary Attack
```csharp
public static bool IsTimeToReevaluatePrimaryAttack(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`


## Is Within Range and LOS
```csharp
public static bool IsWithInRangeAndLOS(Guid objectGuid)
```<br>

### Parameters

Display Name | Description | Default Value | Browser Type
--- | --- | --- | ---
Character | Character to check. | `7d150000-0000-0000-0000-000000000000` | `Scripts.BrowserType.ObjectGuid`

