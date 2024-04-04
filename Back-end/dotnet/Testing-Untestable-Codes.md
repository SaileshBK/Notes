
Lets say we have a project and that project have some internal classes and methods that are only accessible to the assembly itself. However, the testing project is outside of the assembly. We can not directly access those internal members. What we can do is :

In Directory.Build.targets file:
~~~ 
<Project>
	<ItemGroup>
		<InternalVisibleTo Include="$(AssemblyName).Tests" />
	</ItemGroup>
</Project>
~~~


