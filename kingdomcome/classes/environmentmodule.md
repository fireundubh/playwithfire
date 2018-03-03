<!-- TITLE: EnvironmentModule Function Reference -->

# EnvironmentModule Class
## Patreon

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

## Methods

### BlendTimeOfDay

No description entered

#### **Syntax**

`EnvironmentModule.BlendTimeOfDay(profileName, blendDuration, force)`

#### **Parameters**

* `profileName`: A string indicating the name of the weather profile (e.g., foggy_drizzly, foggy_storm, cloudless_sunny) 
* `blendDuration`: A number indicating the duration of the blend
* `force`: A boolean determining whether the blend should be forced

#### **Return value**

`nil`

### CoverHole

No description entered

#### **Syntax**

`EnvironmentModule.CoverHole(cover, entityId)`

#### **Parameters**

* `cover`: Unknown
* `entityId`: A string representing the UUID of an entity

#### **Return value**

`nil`

### ForceImmediateWeatherUpdate

Forces the weather to update immediately

#### **Syntax**

`EnvironmentModule.ForceImmediateWeatherUpdate()`

#### **Return value**

`nil`

### ForceWindDirection

No description entered

#### **Syntax**

`EnvironmentModule.ForceWindDirection(fAngleDeg)`

#### **Parameters**

`fAngleDeg`: A number representing the wind direction angle in degrees

#### **Return value**

`nil`

### MakeHole

No description entered

#### **Syntax**

`EnvironmentModule.MakeHole(make, entityId)`

#### **Parameters**

* `make`: Unknown
* `entityId`: A string representing the UUID of an entity

#### **Return value**

`nil`

### RebuildClouds

No description entered

#### **Syntax**

`EnvironmentModule.RebuildClouds()`

#### **Return value**

`nil`