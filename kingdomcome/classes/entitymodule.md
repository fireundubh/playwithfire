<!-- TITLE: EntityModule Function Reference -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# EntityModule
## Methods

### AcquireInventory

No description entered

#### **Syntax**

`local inventory = EntityModule.AcquireInventory(DBInventoryId, ownerEntityId)`

#### **Parameters**

* `DBInventoryId`: A string indicating the UUID of the inventory database
* `ownerEntityId`: A number indicating the ID of the owner

#### **Return value**

`string`


### AnimCharCopyVisual

No description entered

#### **Syntax**

`EntityModule.AnimCharCopyVisual(entityId)`

#### **Parameters**

`entityId`: A string representing the UUID of the entity

#### **Return value**

`nil`


### AnimCharSetBodyBlood

No description entered

#### **Syntax**

`EntityModule.AnimCharSetBodyBlood(entityId, zone, blood)`

#### **Parameters**

* `entityId`: A string representing the UUID of the entity
* `zone`: A number indicating the blood zone
* `blood`: A number indicating the amount of blood

#### **Return value**

`nil`


### CanUseInventory

No description entered

#### **Syntax**

`local inventory = EntityModule.CanUseInventory(inventoryId)`

#### **Parameters**

`inventoryId`: A string representing the UUID of the inventory

#### **Return value**

`boolean`


### EnableLayerProfile

No description entered

#### **Syntax**

`EntityModule.EnableLayerProfile(profileName, enable)`

#### **Parameters**

* `profileName`: A string indicating the name of the layer profile
* `enable`: A boolean determining whether the profile should be enabled

#### **Return value**

`nil`


### GetEntityScriptMisc

No description entered

#### **Syntax**

`local inventory = EntityModule.GetEntityScriptMisc(entityId)`

#### **Parameters**

`entityId`: An integer indicating the ID of the entity

#### **Return value**

`string`: A string matching the RegEx pattern `([^:]+):([^|]+)`, such as `key:value`


### GetInventoryOwner

No description entered

#### **Syntax**

`local inventory = EntityModule.GetInventoryOwner(inventoryId)`

#### **Parameters**

`inventoryId`: A string representing the UUID of the inventory

#### **Return value**

`WUID`


### GetSlotHand

No description entered

#### **Syntax**

`local inventory = EntityModule.GetSlotHand(slotEntityId)`

#### **Parameters**

`slotEntityId`: A string representing the ID of the entity

#### **Return value**

`table` or `string`


### GetSlotItemClassId

No description entered

#### **Syntax**

`local slotItemClassId = EntityModule.GetSlotItemClassId(slotEntityId)`

#### **Parameters**

`slotEntityId`: A string representing the ID of the entity

#### **Return value**

`string`


### GetSlotSpawnOnStart

No description entered

#### **Syntax**

`local slotSpawnOnStart = EntityModule.GetSlotSpawnOnStart(slotEntityId)`

#### **Parameters**

`slotEntityId`: A string representing the ID of the entity

#### **Return value**

Unknown return value


### IsInventoryReadOnly

No description entered

#### **Syntax**

`local isInventoryReadOnly = EntityModule.IsInventoryReadOnly(inventoryId)`

#### **Parameters**

`inventoryId`: A string representing the UUID of the inventory

#### **Return value**

`boolean`


### LoadInventoryFromDB

No description entered

#### **Syntax**

`EntityModule.LoadInventoryFromDB(ownerEntityId, DBInventoryId)`

#### **Parameters**

* `DBInventoryId`: A string indicating the UUID of the inventory database
* `ownerEntityId`: A number indicating the ID of the owner

#### **Return value**

`nil`


### MakeParticleEffectActive

No description entered

#### **Syntax**

`EntityModule.MakeParticleEffectActive(particleEffectEntityId)`

#### **Parameters**

`particleEffectEntityId`: A string representing the ID of the particle effect entity

#### **Return value**

`nil`


### MakeParticleEffectIdle

No description entered

#### **Syntax**

`EntityModule.MakeParticleEffectIdle(particleEffectEntityId)`

#### **Parameters**

`particleEffectEntityId`: A string representing the ID of the particle effect entity

#### **Return value**

`nil`


### ReleaseInventory

No description entered

#### **Syntax**

`EntityModule.ReleaseInventory(ownerEntityId)`

#### **Parameters**

`ownerEntityId`: A string representing the ID of the owning entity

#### **Return value**

`nil`


### SequenceEntitiesCopyVisual

No description entered

#### **Syntax**

`EntityModule.SequenceEntitiesCopyVisual(sequenceName)`

#### **Parameters**

`sequenceName`: A string indicating the name of the sequence

#### **Return value**

`nil`
