# About 
This package simply provides the sqlean extension libraries for easier usage within dotnet.

# Usage
```
DatabaseConnection.Open();
DatabaseConnection.EnableExtensions(true);

// dotnet should include the binaries dependend on the OS. 
if (RuntimeInformation.IsOSPlatform(OSPlatform.Windows)) {
    DatabaseConnection.LoadExtension(@"./sqlean.dll");
} else if (RuntimeInformation.IsOSPlatform(OSPlatform.OSX)) {
    DatabaseConnection.LoadExtension(@"./sqlean.dylib");
} else if (RuntimeInformation.IsOSPlatform(OSPlatform.Linux)) {
    DatabaseConnection.LoadExtension(@"./sqlean.so");
} else {
    // Handle unsupported OS!
}
```

# Documentation
Please refer to the [sqlean's](https://github.com/nalgeon/sqlean) documentation.

# Issues
Feel free to add issues, though most probably are related to sqlean or it's dependencies.

# Manual build
## (Windows) download latest NuGet CLI tool
Get the latest NuGet CLI Tool at `https://dist.nuget.org/win-x86-commandline/latest/nuget.exe`
Place it the project's root.

## pack the NuGet package 
`./nuget.exe pack TTS.sqlean/TTS.sqlean.nuspec`

# License
Copyright 2021-2024 [Anton Zhiyanov](https://antonz.org/), [Contributors of sqlean](https://github.com/nalgeon/sqlean/graphs/contributors) and [Third-party Authors](https://github.com/nalgeon/sqlean/blob/main/docs/third-party.md).

The software is available under the MIT License.

Copyright 2024 Tele'Train Software GmbH (Moers, Germany)