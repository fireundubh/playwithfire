<!-- TITLE: Framework Function Reference -->

# Framework Class
## Patreon

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

## Methods

### Expr

Evaluates the specified expression and returns a number

#### **Syntax**

`local result = Framework.Expr(expr)`

#### **Parameters**

`expr`: An expression to be evaluated

#### **Return value**

`number`


### IsValidWUID

Returns `true` when the specified WUID is valid

#### **Syntax**

`local validWuid = Framework.IsValidWUID(wuid)`

#### **Parameters**

`wuid`: Any WUID

#### **Return value**

`boolean`


### ScriptHandlerToString

Converts the specified script handler to a string.

#### **Syntax**

`local result = Framework.ScriptHandlerToString(scriptHandler)`

#### **Parameters**

`scriptHandler`: Unknown type.

#### **Return value**

`string`


### WUIDToMsg

Converts the specified WUID to an unsigned 64-bit integer value

#### **Syntax**

`local result = Framework.WUIDToMsg(wuid)`

#### **Parameters**

`wuid`: Any WUID

#### **Return value**

`UInt64`


### WUIDToString

Converts the specified WUID to a string

#### **Syntax**

`local result = Framework.WUIDToString(wuid)`

#### **Parameters**

`wuid`: Any WUID

#### **Return value**

`string`: A string formatted as `[Class - ID]`


### WUIDToUI

Converts the specified WUID to a data type usable by the UI system

#### **Syntax**

`local result = Framework.WUIDToUI(wuid)`

#### **Parameters**

`wuid`: Any WUID

#### **Return value**

`"w"-prefixed WUID`