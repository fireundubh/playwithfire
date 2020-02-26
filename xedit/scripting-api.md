---
title: xEdit Scripting API
description: 
published: true
date: 2020-02-26T08:50:14.588Z
tags: 
---

At some point, the Current API will be replaced.

Implementations of the following solutions are provided using both APIs to demonstrate how scripts will need to change.

# Common Problems

## Access member of element in array of elements

### Current API

```pascal
var
	ScriptProperties : IInterface;
	PropertyName : IInterface;
	i : Integer;
begin
	ScriptProperties := ElementByPath(e, 'VMAD\Scripts\[0]\Properties');

  for i := 0 to Pred(ElementCount(ScriptProperties)) do
  begin
    PropertyName := ElementByPath(ScriptProperties, '[' + IntToStr(i) + ']\propertyName');  // returns object of type IwbElement
    // do something with kPropertyName
  end;
end;
```

### New API

```pascal
var ScriptProperties := ElementByPath(e, 'VMAD\Scripts\[0]\Properties');

for var i := 0 to Pred(ScriptProperties.ElementCount) do
begin
	var PropertyName := ScriptProperties.ElementByPath['[' + IntToStr(i) + ']\propertyName'];  // returns object of type IwbElement
  // do something with PropertyName
end;
```

## Iterate over array of elements

### Current API

```pascal
var
	FormIDs : IInterface;
	LNAM : IInterface;
	i : Integer;
begin
	FormIDs := ElementByName(e, 'FormIDs');

  for i := 0 to Pred(ElementCount(FormIDs)) do
  begin
    LNAM := ElementByIndex(FormIDs, i);  // returns object of type IwbElement
    // do something with LNAM
  end;
end;
```

### New API

```pascal
begin
  var FormIDs := e.ElementByName['FormIDs'];

  for var i := 0 to Pred(FormIDs.ElementCount) do
  begin
    var LNAM := FormIDs.Elements[i];  // returns object of type IwbElement
    // do something with LNAM
  end;
end;
```

## Iterate over Referenced By records

### Current API

```pascal
var
	ByRef : IInterface;
	i : Integer;
begin
  for i := 0 to Pred(ReferencedByCount(e)) do
  begin
    ByRef := ReferencedByIndex(e, i);  // returns object of type IwbMainRecord
    // do something with ByRef
  end;
end;
```

### New API

```pascal
begin
  for var i := 0 to Pred(e.ReferencedByCount) do
  begin
    var ByRef := e.ReferencedBy[i];  // returns object of type IwbMainRecord
    // do something with ByRef
  end;
end;
```

## Get record assigned to element

### Current API

```pascal
var
	RNAM : IInterface;
	LinkedRef : IInterface;
begin
  RNAM := ElementBySignature(e, 'RNAM');
  LinkedRef := LinksTo(RNAM);  // returns object of type IwbMainRecord
  // do something with LinkedRef
end;
```

### New API

```pascal
begin
  var RNAM := e.ElementBySignature['RNAM'];
  var LinkedRef := RNAM.LinksTo;  // returns object of type IwbMainRecord
  // do something with LinkedRef
end;
```

## Print message with non-string data type

Non-string types must be converted to strings first.

```pascal
// printing integers
AddMessage(IntToStr(iNumber));

// printing floats
AddMessage(FloatToStr(fNumber));

// printing Form IDs (cardinals/unsigned integers) as hexadecimal strings
AddMessage(IntToHex(GetLoadOrderFormID(e), 8));
```

# Scripting Resources

External Link | Description
:--- | :---
[API Function Reference](https://tes5edit.github.io/docs/13-Scripting-Functions.html) | Functions and procedures unique to xEdit
[Delphi Language Guide](http://docwiki.embarcadero.com/RADStudio/Rio/en/Delphi_Language_Guide_Index) | Official guide to the Delphi language, including syntax 
[Delphi Basics](http://www.delphibasics.co.uk/index.html) | Examples of how to use Delphi functions and procedures

*Note: The xEdit script interpreter uses a subset of Delphi. There are language features that cannot be used in scripts.*