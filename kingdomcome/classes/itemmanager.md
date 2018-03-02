<!-- TITLE: ItemManager Function Reference -->

# ItemManager Class
## Patreon

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

## Methods

### AddOnEquipBuff

No description entered

#### **Syntax**

`ItemManager.AddOnEquipBuff(itemId, buffId, add)`

#### **Parameters**

* `itemId`: A string representing the UUID of an item
* `buffId`: A string representing the UUID of a buff
* `add`: A boolean determining whether the buff is added or removed

#### **Return value**

`nil`


### CreateItem

Instantiates a copy of the specified item and returns the instance ID

#### **Syntax**

`local instanceId = ItemManager.CreateItem(itemId, health, amount)`

#### **Parameters**

* `itemId`: A string representing the UUID of an item
* `health`: A number from 0 to 100 indicating the durability of an item
* `amount`: A number indicating the quantity of an item

#### **Return value**

`string`


### GetItem

Returns item userdata associated with the specified UUID

#### **Syntax**

`local result = ItemManager.GetItem(itemId)`

#### **Parameters**

`itemId`: A string representing the UUID of an item

#### **Return value**

`userdata`


### GetItemName

Returns the name of an item as a string

#### **Syntax**

`local result = ItemManager.GetItemName(itemId)`

#### **Parameters**

`itemId`:  A string representing the UUID of an item

#### **Return value**

`string`


### GetItemOwner

Returns the owning entity of an item

#### **Syntax**

`local result = ItemManager.GetItemOwner(itemId)`

#### **Parameters**

`itemId`: A string representing the UUID of an item

#### **Return value**

`userdata`


### GetItemUIName

Returns the UI name of an item as a string

#### **Syntax**

`local result = ItemManager.GetItemUIName(itemId)`

#### **Parameters**

`itemId`: A string representing the UUID of an item

#### **Return value**

`string`


### IsItemOversized

Returns `true` if the specified item is oversized

#### **Syntax**

`local result = ItemManager.IsItemOversized(itemId)`

#### **Parameters**

`itemId`: A string representing the UUID of an item

#### **Return value**

`boolean`


### RemoveItem

Removes the specified item

#### **Syntax**

`ItemManager.RemoveItem(itemId)`

#### **Parameters**

`itemId`: A string representing the UUID of an item

#### **Return value**

`nil`


### SetItemOwner

Changes the ownership of an item

#### **Syntax**

`ItemManager.SetItemOwner(itemId, ownerId, markAsStolen)`

#### **Parameters**

* `itemId`: A string representing the UUID of an item
* `ownerId`: A string representing the UUID of the item's new owner
* `markAsStolen` A boolean determining whether the item is stolen

#### **Return value**

`nil`