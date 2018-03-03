<!-- TITLE: Alchemy -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Alchemy Class

### GetFlagTextFor

No description entered

#### **Syntax**

`local flagText = Alchemy.GetFlagTextFor(userId, item_type)`

#### **Parameters**

* `userId`: An integer indicating the ID of the user
* `item_type`: An integer indicating the type of alchemy

#### **Return value**

`string`


### GetUsableFor

No description entered

#### **Syntax**

`local usableFor = Alchemy.GetUsableFor(userId, item_type)`

#### **Parameters**

* `userId`: An integer indicating the ID of the user
* `item_type`: An integer indicating the type of alchemy

#### **Return value**

`integer`

Value | Description | Hint Text
--- | --- | ---
`0` | Undefined | @ui_hud_undefined
`1` | Take | @ui_hud_take
`2` | Use | @ui_hud_use_item


### IsUsableByHold

No description entered

#### **Syntax**

`local isUsableByHold = Alchemy.IsUsableByHold(userId, item_Type)`

#### **Parameters**

* `userId`: An integer indicating the ID of the user
* `item_type`: An integer indicating the type of alchemy

#### **Return value**

`boolean`


### IsUsableEnabledFor

No description entered

#### **Syntax**

`local isUsableEnabledFor = Alchemy.IsUsableEnabledFor(userId, item_type)`

#### **Parameters**

* `userId`: An integer indicating the ID of the user
* `item_type`: An integer indicating the type of alchemy

#### **Return value**

`boolean`


### ResetTable

No description entered

#### **Syntax**

`Alchemy.ResetTable(tableId)`

#### **Parameters**

`tableId`: A string representing the UUID of the alchemy table

#### **Return value**

`nil`


### StartAlchemy

No description entered

#### **Syntax**

`Alchemy.StartAlchemy(userId, tableId)`

#### **Parameters**

* `userId`: An integer indicating the ID of the user
* `tableId`: A string representing the UUID of the alchemy table

#### **Return value**

`nil`