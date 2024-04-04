**Tags**: #dotnet  #visual-studio #back-end #internal-members #CSharp #InternalVisibleTo


Lets say we have a project and that project have some internal classes and methods that are only accessible to the assembly itself. However, the testing project is outside of the assembly. We can not directly access those internal members. What we can do is :

In Directory.Build.targets file:
~~~ 
<Project>
	<ItemGroup>
		<InternalVisibleTo Include="$(AssemblyName).Tests" />
		<InternalVisibleTo Include="$(AssemblyName).New.Tests" />
		<InternalVisibleTo Include="Integration.Tests" />
	</ItemGroup>
</Project>
~~~

Note: Directory.Build.targets is the file that our msbuild will look and apply anything we provide in there during the build process.

This approach is really good for big projects with same naming conventions.


