# Access rule for directory

~~~ 
$accessRule = New-Object System.Security.AccessControl.FileSystemAccessRule($userOrGroupOrIdentityRef, $permission, 'ContainerInherit,ObjectInherit', 'None', 'Allow')
~~~ 

# Access rule for file

~~~ 
$accessRule = New-Object System.Security.AccessControl.FileSystemAccessRule($userOrGroupOrIdentityRef, $permission, 'None', 'Allow') 
~~~ 

Note:  For Access rule for file we don't need to provide  inheritanceFlags