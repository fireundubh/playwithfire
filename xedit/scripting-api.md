---
title: xEdit Scripting API
description: 
published: true
date: 2020-03-22T21:53:54.726Z
tags: 
---

# Common Problems

## Access member of element in array of elements

```pascal
var
	ScriptProperties : IInterface;
	PropertyName : IInterface;
	i : Integer;
begin
	ScriptProperties := ElementByPath(e, 'VMAD\Scripts\[0]\Properties');

  for i := 0 to Pred(ElementCount(ScriptProperties)) do
  begin
    PropertyName := ElementByPath(ScriptProperties, '[' + IntToStr(i) + ']\propertyName');
    
    // do something with PropertyName
  end;
end;
```


## Iterate over array of elements

```pascal
var
	FormIDs : IInterface;
	LNAM    : IInterface;
	i       : Integer;
begin
	FormIDs := ElementByName(e, 'FormIDs');

  for i := 0 to Pred(ElementCount(FormIDs)) do
  begin
    LNAM := ElementByIndex(FormIDs, i);
    
    // do something with LNAM
  end;
end;
```


## Iterate over Main Records

### Without user interaction

This approach does not require the user to select any records.

```pascal
function Initialize: Integer;
var
	SourceFile : IwbFile;
  MainRecord : IInterface;
  i          : Integer;
begin
	SourceFile := FileByName('Skyrim.esm');  // FileByName natively available in only dev-4.1.4, use FileByIndex
    
  // this is a very inefficient approach if you want to process only records with a specific signature 
	for i := 0 to Pred(RecordCount(SourceFile)) do
  begin
  	MainRecord := RecordByIndex(SourceFile, i);
    
    if Signature(MainRecord) <> 'ARMO' then
    	Continue;
      
    // do something with MainRecord
  end;
end;
```

Alternatively:

```pascal
function Initialize: Integer;
var
	SourceFile  : IwbFile;
  GroupRecord : IwbGroupRecord;
  MainRecord  : IInterface;
  i           : Integer;
begin
	SourceFile := FileByName('Skyrim.esm');  // FileByName natively available in only dev-4.1.4, use FileByIndex
    
  // this is a more efficient approach when you want to process only records with a specific signature
  GroupRecord := GroupBySignature(SourceFile, 'ARMO');
  if not Assigned(GroupRecord) then
  	Exit;
  
	for i := 0 to Pred(ElementCount(GroupRecord)) do
  begin
  	MainRecord := ElementByIndex(GroupRecord, i);
    
    // do something with MainRecord
  end;
end;
```

### With user interaction

This approach requires the user to select one or more records to process.

```pascal
function Process(e: IInterface): Integer;
begin
	if Signature(e) <> 'ARMO' then
  	Exit;
    
  // do something with ARMO records in selection
end;
```


## Iterate over Referenced By records

```pascal
function Process(e: IInterface): Integer;
var
	MainRecord : IInterface;
	i          : Integer;
begin  
  for i := 0 to Pred(ReferencedByCount(e)) do
  begin
    MainRecord := ReferencedByIndex(e, i);
    
    // do something with MainRecord
  end;
end;
```


## Get record assigned to element

```pascal
function Process(e: IInterface): Integer;
var
	RNAM      : IInterface;
	LinkedRef : IInterface;
begin
	if Signature(e) <> 'ARMO' then
  	Exit;

  RNAM := ElementBySignature(e, 'RNAM');
  if not Assigned(RNAM) then
  	Exit;
    
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