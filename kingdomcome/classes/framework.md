<!-- TITLE: Framework Function Reference -->

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Framework Class
## Methods

### Expr

Evaluates the specified expression and returns a number

#### **Syntax**

`local result = Framework.Expr(expr)`

#### **Parameters**

`expr`: An expression to evaluate

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

`scriptHandler`: Unknown type

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

`local wuidString = Framework.WUIDToString(wuid)`

#### **Parameters**

`wuid`: Any WUID

#### **Return value**

`string`: "[Class - ID]"


### WUIDToUI

Converts the specified WUID to a data type usable by the UI system

#### **Syntax**

`local result = Framework.WUIDToUI(wuid)`

#### **Parameters**

`wuid`: Any WUID

#### **Return value**

`unknown type`

When printed as a string, the return value is the WUID prefixed with the letter `w`.