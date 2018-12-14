<!-- TITLE: Patchwork Project Structure -->

[&lsaquo; Unity Modding](/unity)

If you want to see more resources like this:

[![https://www.patreon.com/fireundubh](https://i.imgur.com/llPEyru.png)](https://www.patreon.com/fireundubh)

# Patchwork Project Structure
This reference is aimed at how to structure a basic Patchwork project.

## Requirements

Patchwork includes a generic launcher, which can be used for any Patchwork project. The launcher requires:

* an `AppInfoFactory` library that describes your application; and
* one or more `PatchInfo` libraries for your patches.

### AppInfoFactory

1. Create a new project named `AppInfoDLLProj`.
2. Add a new reference to `Patchwork.Attributes`. _Recommendation: Use the compiled DLL, not the project._
3. Create a new class file named `AppInfoDLL.cs`.
4. Inherit from `AppInfoFactory` and add the `[AppInfoFactory]` attribute to the class.

Within `AppInfoDLL.cs` should be the following code:

```csharp
using System.Linq;
using Patchwork.AutoPatching;
using System.IO;

namespace AppInfoDLLProj
{
	[AppInfoFactory]
	public class AppInfoDLL : AppInfoFactory
	{
		public override AppInfo CreateInfo(DirectoryInfo folderInfo)
		{
			var appInfo = new AppInfo
			{
				AppName = "Pillars of Eternity II",
				AppVersion = "1.0.0.0",
				BaseDirectory = folderInfo
			};

			string appPath = Combine(appInfo.BaseDirectory.ToString(), "PillarsOfEternityII.exe");
			appInfo.Executable = new FileInfo(appPath);

			return appInfo;
		}

		public static string Combine(params string[] paths)
		{
			string current = paths.Aggregate(@"", Path.Combine);
			return current;
		}
	}
}
```

### PatchInfo

1. Create a new project named whatever you want.
2. Add a new reference to `Patchwork.Attributes`. _Recommendation: Use the compiled DLL, not the project._
3. Create a new class named `PatchAssemblyInfo`.
4. Inherit from `IPatchInfo` and add the assembly attribute `[assembly: PatchAssembly]`.

Within `PatchAssemblyInfo.cs` should be the following code:

```csharp
using System.IO;
using System.Linq;
using Patchwork;
using Patchwork.AutoPatching;

[assembly: PatchAssembly]

namespace DeadfireMods
{
	[PatchInfo]
	public class PatchAssemblyInfo : IPatchInfo
	{
		public string PatchVersion { get; } = "1.0.0.000";

		public string Requirements { get; } = "None";

		public string PatchName { get; } = "DeadfireMods";

		public FileInfo GetTargetFile(AppInfo app)
		{
			string file = Combine(app.BaseDirectory.FullName, "PillarsOfEternityII_Data", "Managed", "Assembly-CSharp.dll");
			return new FileInfo(file);
		}

		public string CanPatch(AppInfo app)
		{
			return null;
		}

		public static string Combine(params string[] paths)
		{
			string current = paths.Aggregate(@"", Path.Combine);
			return current;
		}
	}
}
```

## Next steps

Structure and implement your patches as desired, adding more references as needed.