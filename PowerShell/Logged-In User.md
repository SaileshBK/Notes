#### Via Environment Variables

~~~ 
(Get-ChildItem Env:USERNAME).Value
~~~ 

or simply:
~~~ 
$env:username
~~~ 

#### Via.NET WindowsIdentity Class

~~~ 
[Security.Principal.WindowsIdentity]::GetCurrent().Name
~~~ 

#### Via Win32_ComputerSystem Class
~~~ 
(Get-CimInstance -ClassName Win32_ComputerSystem).UserName
~~~ 

#### Via the Whoami Command
~~~ 
(whoami).Split("\")[1]
~~~ 