---
title: xEdit Scripting FAQs
description: 
published: true
date: 2020-02-15T03:10:41.393Z
tags: 
---

# Access member of element in array of elements

```pascal
function Process(e: IInterface): Integer;
var
	propertyName: IInterface;
	ScriptProperties: IInterface;
	i: Integer;
begin
	ScriptProperties := ElementByPath(e, 'VMAD\Scripts\Script\Properties');
  
	for i := 0 to Pred(ElementCount(ScriptProperties)) do
	begin
		{Option A} propertyName := ElementByName(ElementByIndex(ScriptProperties, i), 'propertyName');
		{Option B} propertyName := ElementByPath(ScriptProperties, '[' + i + ']\propertyName');
	end;
end;
```

# Iterate over array of elements

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

# Iterate over Referenced By records

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

# Get record assigned to element

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