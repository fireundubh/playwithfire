<!-- TITLE: Dice Function Reference -->

# Dice Class
## Patreon

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

## Methods

### OverrideNextThrow

No description entered

#### **Syntax**

`Dice.OverrideNextThrow(playerIndex, dieValues)`

#### **Parameters**

* `playerIndex`: A number indicating the index of the throwing player
* `dieValues`: A table of dice values

#### **Return value**

`nil`

### RollDie

No description entered

#### **Syntax**

`Dice.RollDie(userId, dieEntityId, dieNumber)`

#### **Parameters**

* `userId`: A string representing the UUID of an entity
* `dieEntityId`: Unknown
* `dieNumber`: Unknown

#### **Return value**

`nil`

### SetAIDifficulty

No description entered

#### **Syntax**

`Dice.SetAIDifficulty(difficulty)`

#### **Parameters**

`difficulty`: A number indicating the difficulty level of the AI player

#### **Return value**

`nil`

### SetAIRiskTaking

No description entered

#### **Syntax**

`local result = Dice.SetAIRiskTaking(riskTaking)`

#### **Parameters**

`riskTaking`: A number indicating the AI player's propensity to take risks

#### **Return value**

`nil`

### SetAdvantage

No description entered

#### **Syntax**

`Dice.SetAdvantage(playerIndex, advantage)`

#### **Parameters**

* `playerIndex`: A number indicating the index of the advantaged player
* `advantage`: A number indicating the advantage of the player

#### **Return value**

`nil`

### SetScore

No description entered

#### **Syntax**

`Dice.SetScore(player1Score, player2Score)`

#### **Parameters**

* `player1Score`: A number indicating the first player's score
* `player2Score`: A number indicating the second player's score

#### **Return value**

`nil`

### ToggleHoldDie

No description entered

#### **Syntax**

`Dice.ToggleHoldDie(userId, dieEntityId, dieNumber, hold)`

#### **Parameters**

* `userId`: A string representing the UUID of an entity
* `dieEntityId`: Unknown
* `dieNumber`: Unknown
* `hold`: A boolean indicating whether the entity should hold

#### **Return value**

`nil`