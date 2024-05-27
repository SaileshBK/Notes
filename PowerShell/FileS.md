# Create a new access rule 
$accessRule = New-Object System.Security.AccessControl.FileSystemAccessRule($userOrGroup, $permission, 'ContainerInherit,ObjectInherit', 'None', 'Allow')