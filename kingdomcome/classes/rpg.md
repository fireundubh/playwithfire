<!-- TITLE: RPG Function Reference -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 
# RPG Class
## Methods

### _GetConstant

Returns the value of a key-value pair in a table

#### **Syntax**

`local result = RPG._GetConstant(table, key)`

#### **Parameters**

* `table`: A table
* `key`: A string key

#### **Return value**

`string`


### AddStatXP

Adds stat experience to a soul

#### **Syntax**

`RPG.AddStatXP(rpgEvent, soulId, statName, totalXp, oldProgress, newProgress)`

#### **Parameters**

* `rpgEvent`: Unknown
* `soulId`: A string representing the UUID of a soul
* `statName`: A string abbreviated name of a stat or derived stat
* `totalXp`: A number amount of experience to add
* `oldProgress`: Unknown
* `newProgress`: Unknown

#### **Return value**

`nil`


### CaptionObjectUsed

No description entered

#### **Syntax**

`RPG.CaptionObjectUsed(objectEntityId, isDiscovered)`

#### **Parameters**

* `objectEntityId`: A string representing the UUID of an entity
* `isDiscovered`: A boolean determining whether the object is discovered

#### **Return value**

`nil`


### GetFactionById

No description entered

#### **Syntax**

`local faction = RPG.GetFactionById(factionId)`

#### **Parameters**

`factionId`: An expression to be evaluated

#### **Return value**

`userdata`


### GetFactions

No description entered

#### **Syntax**

`local table = RPG.GetFactions()`

#### **Return value**

`table`


### GetHobbies

No description entered

#### **Syntax**

`local hobbies = RPG.GetHobbies()`

#### **Return value**

`table`


### GetLocationById

No description entered

#### **Syntax**

`local location = RPG.GetLocationById(locationId)`

#### **Parameters**

`locationId`: A string representing the UUID of a location

#### **Return value**

`userdata`


### GetLocationByName

No description entered

#### **Syntax**

`local location = RPG.GetLocationByName(locationName)`

#### **Parameters**

`locationName`: A string representing the name of a location

#### **Return value**

`userdata`


### GetLocations

No description entered

#### **Syntax**

`local locations = RPG.GetLocations()`

#### **Return value**

`table`


### NotifyLevelXpGain

Displays a UI message indicating whether experience was gained

#### **Syntax**

`RPG.NotifyLevelXpGain(skillName)`

#### **Parameters**

`skillName`: An abbreviated name of a stat or derived stat

#### **Return value**

`nil`


### UnlockRecipe

Unlocks a recipe for an entity

#### **Syntax**

`RPG.UnlockRecipe(userId, recipeId, stepId)`

#### **Parameters**

* `userId`: A string representing the UUID of an entity
* `recipeId`: A number indicating the `recipe_id` of a recipe
* `stepId`: A number indicating the `recipe_step_id` of a recipe step

#### **Return value**

`nil`