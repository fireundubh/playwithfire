<!-- TITLE: Minigame Function Reference -->
<!-- SUBTITLE: kingdomcome/classes/minigame -->

# Minigame Class
## Methods

### BookTranscriptionNextPage

#### Syntax

`Minigame.BookTranscriptionNextPage()`

#### Return value

`nil`


### CloseInventory

#### Syntax

`Minigame.CloseInventory()`

#### Return value

`nil`


### GetBookStudyProgress

#### Syntax

`local studyProgress = Minigame.GetBookStudyProgress(documentGuidStr)`

#### Parameters

* `documentGuidStr`: A string reference to the book UUID

#### Return value

A `number` representing the study progress for the specified book


### StartDice

#### Syntax

`Minigame.StartDice(tableId, playerId, opponentId)`

#### Parameters

* `tableId`: A string reference to the dice table UUID
* `playerId`: A string reference to the player UUID
* `opponentId`: A string reference to the opponent UUID

#### Return value

`nil`


### StartDiceByName

This function is internal or may not be implemented.

#### Syntax

`Minigame.StartDiceByName(entityName)`

#### Parameters

`entityName`: A string reference to the entity name.

#### Return value

`nil`


### StartDiceWithScore

This function is internal or may not be implemented.

#### Syntax

`Minigame.StartDiceWithScore(targetScore)`

#### Parameters

`targetScore`: A number reference to the score required to trigger the win condition.

#### Return value

`nil`


### StartHerbGathering

Plays the herb gathering animation, collects the targeted herb, and adds additional herbs based on the player's Herbalism skill level.

#### Syntax

`Minigame.StartHerbGathering(areaId)`

#### Parameters

`areaId`: A string reference to the UUID of the pickable area.

#### Return value

`nil`


### StartHoleDigging

Plays the digging animation and activates the targeted entity.

#### Syntax

`Minigame.StartHoleDigging(entityId)`

#### Parameters

`entityId`: A string reference to the UUID of the interactive entity.

#### Return value

`nil`


### StartLockPicking

Activates the lockpicking minigame.

#### Syntax

`Minigame.StartLockPicking(entityId)`

#### Parameters

`entityId`: A string reference to the UUID of the interactive entity.

#### Return value

`nil`


### WasBookOpened

Returns `true` if the specified book was opened.

#### Syntax

`local bookOpened = Minigame.WasBookOpened(documentGuidStr)`

#### Parameters

`documentGuidStr`: A string reference to the UUID of the specified book.

### Return value

`boolean`
