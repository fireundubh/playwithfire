---
title: xEdit Scripting FAQs
description: 
published: true
date: 2020-02-15T03:07:17.314Z
tags: 
---

# xEdit API Examples

## Access member of element in array of elements

```pascal
function Process(e: IInterface): Integer;
var
	propertyName: IInterface;
	Properties: IInterface;
	i: Integer;
begin
	Properties := ElementByPath(e, 'VMAD\Scripts\Script\Properties');
  
	for i := 0 to Pred(ElementCount(Properties)) do
  begin
  	{Option A} propertyName := ElementByName(ElementByIndex(Properties, i), 'propertyName');
    {Option B} propertyName := ElementByPath(Properties, '[' + i + ']\propertyName');
  end;
end;
```

## Iterate over array of elements

```pascal
function Process(e: IInterface): Integer;
var
	LNAM: IInterface;
	FormIDs: IInterface;
	i: Integer;
begin
	if not (Signature(e) = 'FLST') then
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
	ByRef: IInterface;
	i: Integer;
begin
	for i := 0 to Pred(ReferencedByCount(e)) do
  begin
  	ByRef := ReferencedByIndex(e, i);
    // do something with ByRef
  end;
end;
```

## Get the record assigned to an element

```pascal
function Process(e: IInterface): Integer;
var
	LinkedRef: IInterface;
  RNAM: IInterface;
begin
	if not (Signature(e) = 'ARMO') then
  	Exit;

	RNAM := ElementBySignature(e, 'RNAM');
  LinkedRef := LinksTo(RNAM);
  
  // do something with LinkedRef
end;
```