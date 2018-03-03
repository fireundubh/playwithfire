<!-- TITLE: Backgammon -->
<!-- SUBTITLE: Backgammon -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Backgammon Class
## Methods

### AcceptGame

No description entered

#### **Syntax**

`Backgammon.AcceptGame(playerId, opponentId)`

#### **Parameters**

* `playerId`: A string representing the UUID of an entity
* `opponentId`: A string representing the UUID of an entity

#### **Return value**

`nil`


### EndGame

No description entered

#### **Syntax**

`Backgammon.EndGame(playerId, end)`

#### **Parameters**

* `playerId`: A string representing the UUID of an entity
* `end`: A boolean determining whether the game should end

#### **Return value**

`nil`


### MoveChecker

No description entered

#### **Syntax**

`Backgammon.MoveChecker(playerId, pointFrom, pointTo)`

#### **Parameters**

* `playerId`: A string representing the UUID of an entity
* `pointFrom`: A number (?) indicating the last move position
* `pointTo`: A number (?) indicating the new move position

#### **Return value**

`nil`


### OfferBet

No description entered

#### **Syntax**

`Backgammon.OfferBet(playerId, money)`

#### **Parameters**

* `playerId`: A string representing the UUID of an entity
* `money`: A number indicating the bet amount

#### **Return value**

`nil`


### RequestGame

No description entered

#### **Syntax**

`Backgammon.RequestGame(playerId, opponentId, boardId)`

#### **Parameters**

* `playerId`: A string representing the UUID of an entity
* `opponentId`: A string representing the UUID of an entity
* `boardId`: A string representing the UUID of an entity

#### **Return value**

`nil`


### RollDice

No description entered

#### **Syntax**

`Backgammon.RollDice(playerId)`

#### **Parameters**

`playerId`: A string representing the UUID of an entity

#### **Return value**

`nil`


### RolledDice

No description entered

#### **Syntax**

`local result = Backgammon.RolledDice(playerId)`

#### **Parameters**

`playerId`: A string representing the UUID of an entity

#### **Return value**

`boolean`
