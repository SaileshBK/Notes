[[https://dotnet.microsoft.com/en-us/download/dotnet/8.0]]

## Install .NET SDK 8 :
~~~
winget install Microsoft.DotNet.SDK.8
~~~

## Uninstall .NET SDK 8 :
~~~
winget uninstall Microsoft.DotNet.SDK.8
~~~

You should now see all installed .NET SDK versions listed, including those installed in `Program Files\dotnet\sdk`.

## Display Paths with Custom Separator in PowerShell:
~~~
$paths = $env:PATH -replace ';', "`r`n"
Write-Output $paths
~~~

## Check .NET SDK Locations

Visual Studio, by default, checks these locations for .NET SDKs:

- `%ProgramFiles%\dotnet\sdk` (system-wide installation)
- `%USERPROFILE%\.dotnet\sdk` (user-specific installation)
- `%APPDATA%\Local\Microsoft\dotnet\sdk` (user-specific for .NET tools)