[[https://dotnet.microsoft.com/en-us/download/dotnet/8.0]]

Display Paths with Custom Separator in PowerShell:
~~~
$paths = $env:PATH -replace ';', "`r`n"
Write-Output $paths
~~~
