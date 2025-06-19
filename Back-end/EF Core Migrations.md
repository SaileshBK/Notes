## Simple way to create and apply migrations in EF Core

1. Make sure you have EF Core tools installed, if not n the Package Manager Console, run:

   `Install-Package Microsoft.EntityFrameworkCore.Tools`

   This is the package that enables commands like Add-Migration, Update-Database, etc.

2. Make sure you are in correct migration assembly, this means you are executing command in the project where the DB Context is.

   `Add-Migration Initial_Create_table`

   This will create the needed migration.

3. Now to apply the migration, make sure the connection string is pointing to correct database, we need to simply use:

   `update-database`
