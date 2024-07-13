[[https://dotnet.microsoft.com/en-us/download/dotnet/8.0]]

You should now see all installed .NET SDK versions listed, including those installed in `Program Files\dotnet\sdk`.

Display Paths with Custom Separator in PowerShell:
~~~
$paths = $env:PATH -replace ';', "`r`n"
Write-Output $paths
~~~
