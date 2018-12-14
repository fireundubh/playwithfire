<!-- TITLE: Patchwork Design Patterns -->

[&lsaquo; Unity Modding](/unity)

If you want to see more resources like this:

[![https://www.patreon.com/fireundubh](https://i.imgur.com/llPEyru.png)](https://www.patreon.com/fireundubh)

# Patchwork Design Patterns
## Basics

### Classes

#### Instanced Classes

When you need to modify an instanced class:

```csharp
[ModifiesType]
public class SomeClassMod : SomeClass
{
	// class body
}
```

#### Static Classes

When you need to modify a static class:

```csharp
[ModifiesType("Fully.Qualified.Path.To.SomeClass")]
public static class SomeClassMod
{
	// class body
}
```

Static classes include `abstract` and `sealed` classes.

### Constructors

When you need to modify the body of a constructor:

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

When you need to reference a private field:

```csharp
[ModifiesMember("privateFieldName", ModificationScope.Nothing)]
private bool alias_privateFieldName;
```

Sometimes source methods will have overly complex bodies, in which case you may need to copy the source body. However, the source body will typically reference a number of private fields, which are inaccessible outside the constructor. Fortunately, you can simply replace all occurrences of the original field name with `alias_privateFieldName`. Patchwork will take care of substitution.

### Properties

#### Creating Properties

When you need to create a property with a backing field:

```csharp
[NewMember]
private bool _propertyName;

[NewMember]
public bool PropertyName
{
	[NewMember]
	get
	{
		return this._propertyName;
	}
	[NewMember]
	private set
	{
		this._propertyName = value;
	}
}
```

#### Modifying Properties

When you need to modify the methods of a property:

```csharp
[NewMember]
[DuplicatesBody("get_PropertyName")]
public bool source_get_PropertyName()
{
	// ignored
	return true;
}

[NewMember]
[DuplicatesBody("set_PropertyName")]
private void source_set_PropertyName(bool value)
{
	// ignored
}

[ModifiesMember("PropertyName")]
public bool PropertyName
{
	[ModifiesMember("get_PropertyName")]
	get
	{
		return this.source_get_PropertyName();
	}
	[ModifiesMember("set_PropertyName")]
	private set
	{
		this.source_set_PropertyName(value);
	}
}
```

### Methods

#### Creating Methods

When you need to create a method:

```csharp
[NewMember]
public void NewMethod()
{
	// your code
}
```

#### Modifying Methods

When you need to modify a method:

```csharp
[ModifiesMember("SomeMethod")]
public void SomeMethod()
{
	// your code
}
```

## Advanced

### Adding Patch Settings

Patch configuration can be achieved in a number of ways. You could create a GUI, for example.

#### INI File Parser

Personally, I prefer INI settings. On the patch side, I use static nested classes for each INI section.

```csharp
// PatchSettings.cs

[NewType]
public static class PatchSettings
{
	[NewType]
	public static class Cheats
	{
		private const string SECTION = "Cheats";
		
		public static bool GodMode { get; set; }
		
		static Cheats() {
			// UserConfig is a generic wrapper for the portable Mono-compatible INI File Parser library.
			GodMode = UserConfig.Parser.TryGetBool(SECTION, "bMyCheat", false);
		}
	}
}

// Player.cs/ApplyDamage

[ModifiesMember("ApplyDamage")]
public void mod_ApplyDamage()
{
	if (PatchSettings.Cheats.GodMode)
	{
		return;
	}
	
	this.source_ApplyDamage();
}
```

You can [download Ricardo Hernández's INI File Parser library from GitHub](https://github.com/rickyah/ini-parser) or NuGet.

### Duplicating Methods

Duplicating the original method is always a good idea when you want to support configuration, or return the value of the original method.

```csharp
[NewMember]
[DuplicatesBody("SomeMethod")]
public void source_SomeMethod()
{
	// ignored
}

[ModifiesMember("SomeMethod")]
public void mod_SomeMethod()
{
	if (PatchSettings.DoSomethingElse.Enabled)
	{
		// your code
		return;
	}
	
	this.source_SomeMethod();
}
```

### Throwing Unreachable Exceptions

Unreachable exceptions are exceptions that should never happen; they are useful for structuring code, returning from typed methods, and, in case they ever happen, indicating where something went really, _really_ wrong.

#### Practical Example

You want to duplicate a method that returns a value, but to compile, the method requires a return statement.

```csharp
[NewMember]
[DuplicatesBody("SomeMethod")]
public bool source_SomeMethod() { }
```

Instead:

```csharp
[NewMember]
[DuplicatesBody("SomeMethod")]
public bool source_SomeMethod()
{
	// you should throw your own exception, but throwing NotImplementedException is fine, too.
	throw new NotImplementedException("source_SomeMethod");
}
```

You could just return an appropriate value assuming Patchwork will override the body, but if something does go horribly wrong, how will you know?