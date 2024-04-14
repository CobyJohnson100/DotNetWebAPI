# Microsoft .NET Learn Todo Tutorial on Creating a Minimal Web API
Following this tutorial link: [Creating Minimal API without use of Controllers](https://learn.microsoft.com/en-us/aspnet/core/tutorials/min-web-api?view=aspnetcore-8.0&tabs=visual-studio-code)

## Current .NET SDK
Get the .NET SDK 8.0 (latest LTS as of 3/28/24)
Can check if you have the .NET SDK by version CLI command:
```
dotnet --version
8.0.103
```

If you don’t have it, then run the command:
`sudo apt-get install dotnet-sdk-8.0`

## Create Minimal Web API ASP.NET Core Project
Minimal APIs are architected to create HTTP APIs with minimal dependencies. This means eliminating the need for certain conventions and structures such as explicit definition of controllers in Model-View-Controller architecture. Can simply define endpoints directly in the program's entry point.

Create the new web minimal API project with CLI command:
`dotnet new web -o [name of web minimal API project directory]`

This will make a WebApplicationBuilder and WebApplication
 - WebApplicationBuilder: Builder class that provides a streamlined and flexible way to configure and set up a web application. It offers a consolidated approach for defining settings, services, and middleware through a fluent API.
 - WebApplication: Represents the configured web application instance, allows for the configuration of middleware in the app's request processing pipeline and starts the web server. Listens for incoming HTTP requests. Created by WebApplicationBuilder class.

Will need two packages:
 - [EntityFramework](https://learn.microsoft.com/en-us/ef/core/) is an open-source object-relational mapping (ORM) framework for .NET. Creates connection between databases and .NET objects, eliminating the need for most of the data-access code that developers usually need to write. EF supports LINQ queries, change tracking, updates, and schema migrations
```
dotnet add package Microsoft.EntityFrameworkCore.InMemory
dotnet add package Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore
```
.NET uses [NuGet](https://www.nuget.org/) as the primary package manager

Model is a class that represents data that the app manages, [Todo.cs](./Todo.cs) is model for this app where the data is:
 - id integer field
 - name string field
 - IsComplete boolean field

Database context is the main class that coordinates Entity Framework, [TodoDb.cs](./TodoDb.cs) is the database context for this app.