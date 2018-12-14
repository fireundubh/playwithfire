<!-- TITLE: Patchwork Design Patterns -->

[&lsaquo; Unity Modding](/unity)

If you want to see more resources like this:

[![https://www.patreon.com/fireundubh](https://i.imgur.com/llPEyru.png)](https://www.patreon.com/fireundubh)

# Patchwork Design Patterns
## Basics

### Classes/Types

When you need to modify a class.

```csharp
[ModifiesType]
public class SomeClassMod : SomeClass
{
	// class body
}
```

When you need to modify a static class.

```csharp
[ModifiesType("Fully.Qualified.Path.To.SomeClass")]
public static class SomeClassMod
{
	// class body
}
```

### Constructors

When you need to modify the body of a constructor.

```csharp
[MemberAlias(".ctor", typeof(object))]
private void object_ctor() { }

[ModifiesMember(".ctor")]
public void CtorNew()
{
	this.object_ctor();
	// duplicate any constructor code
	// add your own code
}
```

Static constructors are named `.cctor`.

### Fields

#### Initializers

Field initializers are not supported outside method bodies; therefore, you will need to modify the constructor or initialize the field where needed.

#### Aliases

When you need to reference a private field.

```csharp
[ModifiesMember("privateFieldName", ModificationScope.Nothing)]
private bool alias_privateFieldName;
```

Simply replace all references to the private field with `alias_privateFieldName`. Patchwork will take care of substitution.

### Properties

When you need to modify the methods of a property.

```csharp
[NewMember]
[DuplicatesBody("get_PropertyName")]
public bool source_get_PropertyName()
{
	return true;
}

[ModifiesMember("PropertyName")]
public bool PropertyName
{
	[ModifiesMember("get_PropertyName")]
	get {
		return this.source_get_PropertyName();
	}
}
```

### Methods

When you need to modify a method.

```csharp
[ModifiesMember("SomeMethod")]
public void SomeMethod()
{
	// your code
}
```