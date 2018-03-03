<!-- TITLE: Calendar Function Reference -->

# Calendar Class
## Patreon

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

## Methods

### GetGameTime

No description entered

#### **Syntax**

`local gameTime = Calendar.GetGameTime()`

#### **Return value**

`number`


### GetWorldDay

No description entered

#### **Syntax**

`local worldDay = Calendar.GetWorldDay()`

#### **Return value**

`number`


### GetWorldDayOfWeek

No description entered

#### **Syntax**

`local worldDayOfWeek = Calendar.GetWorldDayOfWeek()`

#### **Return value**

`number`


### GetWorldHourOfDay

No description entered

#### **Syntax**

`local worldHourOfDay = Calendar.GetWorldHourOfDay()`

#### **Return value**

`number`


### GetWorldTime

No description entered

#### **Syntax**

`local worldTime = Calendar.GetWorldTime()`

#### **Return value**

`number`


### GetWorldTimeRatio

No description entered

#### **Syntax**

`local worldTimeRatio = Calendar.GetWorldTimeRatio()`

#### **Return value**

`number`


### IsFakedTimeOfDay

No description entered

#### **Syntax**

`local isFakedTimeOfDay = Calendar.IsFakedTimeOfDay()`

#### **Return value**

`boolean`


### IsNightTimeOfDay

No description entered

#### **Syntax**

`local isNightTimeOfDay = Calendar.IsNightTimeOfDay()`

#### **Return value**

`boolean`


### IsWorldTimePaused

No description entered

#### **Syntax**

`local isWorldTimePaused = Calendar.IsWorldTimePaused()`

#### **Return value**

`boolean`


### SetFakeTimeOfDay

No description entered

#### **Syntax**

`Calendar.SetFakeTimeOfDay(fakeHour)`

#### **Parameters**

`fakeHour`: A number indicating the hour of day

#### **Return value**

`nil`


### SetWorldTime

No description entered

#### **Syntax**

`Calendar.SetWorldTime(worldTime)`

#### **Parameters**

`worldTime`: A number indicating the world time, usually an expression (e.g., `3600*24+3600*hours`)

#### **Return value**

`nil`


### SetWorldTimePaused

No description entered

#### **Syntax**

`Calendar.SetWorldTimePaused(worldTimePaused, reason)`

#### **Parameters**

* `worldTimePaused`: A boolean
* `reason`: (optional) A string indicating the reason why time was paused, usually a quest name

#### **Return value**

`nil`


### SetWorldTimeRatio

No description entered

#### **Syntax**

`Calendar.SetWorldTimeRatio(worldTimeRatio)`

#### **Parameters**

`worldTimeRatio`: A number indicating the world time ratio, usually `60`

#### **Return value**

`nil`


### UnfakeTimeOfDay

No description entered

#### **Syntax**

`Calendar.UnfakeTimeOfDay()`

#### **Return value**

`nil`