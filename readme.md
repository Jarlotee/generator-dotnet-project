## Dotnet Project Generator 
[![Build Status](https://travis-ci.org/Jarlotee/generator-dotnet-project.svg?branch=master)](https://travis-ci.org/Jarlotee/generator-dotnet-project)

Helps you bootstrap your respository for a dotnet project.

Project strucure based on [.Net Project Structure](https://gist.github.com/davidfowl/ed7564297c61fe9ab814)

Uses `dotnet new` to scaffold the project to keep up as the cli templates change.

### Getting Started

* Install `npm install -g generator-dotnet-project`
* Run `yo dotnet-project`

### Options
```bash
New project huh? Weve got you covered, just answer a few questions...
 What is the name of your project? Project.Web
 What is the name of your solution? Project
 What kind of project? webapi
 Would you like a unit test project? Yes
 Would you like an .editorconfig? Yes
 Do you need to install private nuget packages? Yes
 What is the url to the private nuget server? https://nuget.company.com/nuget
 ```

### What you get

```bash
├── Project.sln
├── nuget.config
├── readme.md
├── src
│   └── Project.Web
│       ├── Controllers
│       │   └── ValuesController.cs
│       ├── Program.cs
│       ├── Project.Web.csproj
│       ├── Properties
│       │   └── launchSettings.json
│       ├── Startup.cs
│       └── appsettings.json
└── tests
    └── Project.Web.Tests.Unit
        ├── Project.Web.Tests.Unit.csproj
        └── UnitTest1.cs
```

## Opinions

Options may be added later, but here is they are:

* Removes appsettings.Development.json (you should store overrides in your environment)
* Adds `Environment` setting to appsettings.json (most projects use this eventually)
* Unit test style xUnit + Moq

## License
MIT
