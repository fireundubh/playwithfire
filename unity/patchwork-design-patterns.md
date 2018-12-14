<!-- TITLE: Patchwork Design Patterns -->

[&lsaquo; Unity Modding](/unity)

If you want to see more resources like this:

[![https://www.patreon.com/fireundubh](https://i.imgur.com/llPEyru.png)](https://www.patreon.com/fireundubh)

# Patchwork Design Patterns
## Basics

### Classes/Types

When you need to modify a class:

```csharp
[ModifiesType]
public class SomeClassMod : SomeClass
{
	// class body
}
```

When you need to modify a static class:

```csharp
[ModifiesType("Fully.Qualified.Path.To.SomeClass")]
public static class SomeClassMod
{
	// class body
}
```

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

Simply replace all references to the private field with `alias_privateFieldName`. Patchwork will take care of substitution.

### Properties

When you need to modify the methods of a property:

```csharp
[NewMember]
[DuplicatesBody("get_PropertyName")]
public bool source_get_PropertyName()
{
	return true;
}

[NewMember]
[DuplicatesBody("set_PropertyName")]
private void source_set_PropertyName(bool value) { }

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

When you need to modify a method:

```csharp
[ModifiesMember("SomeMethod")]
public void SomeMethod()
{
	// your code
}
```

## Advanced

### Configuration

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

### Duplicate Methods

Duplicating the original method is always a good idea when you want to support configuration, or return the value of the original method.

```csharp
[NewMember]
[DuplicatesBody("SomeMethod")]
public void source_SomeMethod() { }

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

### Throwing Impossible Exceptions

Impossible exceptions are exceptions that should never happen; they are useful for structuring code, returning from typed methods, and, in case they ever happen, tell you where something went really, really wrong.

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

You could simply return an appropriate value assuming Patchwork will override the body, but in case something really does go horribly wrong, how will you know?