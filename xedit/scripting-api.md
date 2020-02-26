---
title: xEdit Scripting API
description: 
published: true
date: 2020-02-26T08:16:37.485Z
tags: 
---

# Common Problems

## Access member of element in array of elements

### Option 1
```pascal
for i := 0 to Pred(ElementCount(ScriptProperties)) do
begin
	kPropertyName := ElementByName(ElementByIndex(ScriptProperties, i), 'propertyName');
  // do something with kPropertyName
end;
```

### Option 2
```pascal
for i := 0 to Pred(ElementCount(ScriptProperties)) do
begin
	kPropertyName := ElementByPath(ScriptProperties, '[' + IntToStr(i) + ']\propertyName');
  // do something with kPropertyName
end;
```

### Option 3
```pascal
for i := 0 to Pred(ElementCount(ScriptProperties)) do
begin
	kPropertyName := GetElementEditValues(ElementByIndex(ScriptProperties, i), 'propertyName');
  // do something with kPropertyName
end;
```

### Option 4
```pascal
for i := 0 to Pred(ElementCount(ScriptProperties)) do
begin
	sPropertyName := GetElementEditValues(ScriptProperties, '[' + IntToStr(i) + ']\propertyName');
  // do something with sPropertyName
end;
```

## Iterate over array of elements

```pascal
function Process(e: IInterface): Integer;
var
	LNAM    : IInterface;
	FormIDs : IInterface;
	i       : Integer;
begin
	if Signature(e) <> 'FLST' then
		Exit;
    
	FormIDs := ElementByName(e, 'FormIDs');
  
	for i := 0 to Pred(ElementCount(FormIDs)) do
	begin
		LNAM := ElementByIndex(FormIDs, i);
		// do something with LNAM
	end;
end;
```

## Iterate over Referenced By records

```pascal
function Process(e: IInterface): Integer;
var
	ByRef : IInterface;
	i     : Integer;
begin
	for i := 0 to Pred(ReferencedByCount(e)) do
	begin
		ByRef := ReferencedByIndex(e, i);
		// do something with ByRef
	end;
end;
```

## Get record assigned to element

```pascal
function Process(e: IInterface): Integer;
var
	LinkedRef : IInterface;
	RNAM      : IInterface;
begin
	if Signature(e) <> 'ARMO' then
		Exit;

	RNAM := ElementBySignature(e, 'RNAM');
	LinkedRef := LinksTo(RNAM);
  
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