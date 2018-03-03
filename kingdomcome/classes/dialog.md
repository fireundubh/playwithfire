<!-- TITLE: DialogModule Function Reference -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# DialogModule Class
## Methods

### ForceDialog

No description entered

#### **Syntax**

`DialogModule.ForceDialog(speakerId, listenerId)`

#### **Parameters**

* `speakerId`: A string representing the UUID of the speaker
* `listenerId`: A string representing the UUID of the listener

#### **Return value**

`nil`


### IsDialogInterruptibleByPlayer

No description entered

#### **Syntax**

`local isDialogInterruptible = DialogModule.IsDialogInterruptibleByPlayer(soulId)`

#### **Parameters**

`soulId`: A string representing the UUID of the soul

#### **Return value**

`boolean`


### IsSequenceAvailable

No description entered

#### **Syntax**

`local isSequenceAvailable = DialogModule.IsSequenceAvailable(sequenceId)`

#### **Parameters**

`sequenceId`: A number indicating the ID of the sequence

#### **Return value**

`boolean`


### IsSoulInDialog

No description entered

#### **Syntax**

`local isSoulInDialog = DialogModule.IsSoulInDialog(soulId)`

#### **Parameters**

`soulId`: A string representing the UUID of the soul

#### **Return value**

`boolean`


### ResetHaveDialogCache

No description entered

#### **Syntax**

`DialogModule.ResetHaveDialogCache()`

#### **Return value**

`nil`


### ResetSequenceTimer

No description entered

#### **Syntax**

`DialogModule.ResetSequenceTimer(sequenceId)`

#### **Parameters**

`sequenceId`: A number indicating the ID of the sequence

#### **Return value**

`nil`


### SetAIInteractionState

No description entered

#### **Syntax**

`DialogModule.SetAIInteractionState(soulId, state)`

#### **Parameters**

* `soulId`: A string representing the UUID of the soul
* `state`: An boolean determining the interaction state

#### **Return value**

`nil`


### StartMonolog

No description entered

#### **Syntax**

`DialogModule.StartMonolog(speakerId, topicId)`

#### **Parameters**

* `speakerId`: An string representing the UUID of the speaker
* `topicId`: A number indicating the ID of the topic

#### **Return value**

`nil`