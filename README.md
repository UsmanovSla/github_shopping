# Shopping

The project was generated using the Shoping Architecture.

## Build

View `yard.txt` for more information.

The template includes [EditorConfig](https://editorconfig.org/) support to help maintain consistent coding styles for multiple developers working on the same project across various editors and IDEs. The **.editorconfig** file defines the coding styles applicable to this solution.


Create a new command:

```
dotnet new ca-usecase --name CreateTodoList --feature-name TodoLists --usecase-type command --return-type int
```

Create a new query:

```
dotnet new ca-usecase -n GetTodos -fn TodoLists -ut query -rt TodosVm
```

If you encounter the error *"No templates or subcommands found matching: 'ca-usecase'."*, install the template and try again:


## Test

<!--#if (UseApiOnly) -->
The solution contains unit, integration, and functional tests.

To run the tests:
```bash
dotnet test
```
<!--#else -->
The solution contains unit, integration, functional, and acceptance tests.

To run the unit, integration, and functional tests (excluding acceptance tests):
```bash
dotnet test --filter "FullyQualifiedName!~AcceptanceTests"
```
  
To run the acceptance tests, first start the application:
```bash
cd .\src\Web\
dotnet run
```
Then, in a new console, run the tests:
```bash
cd .\src\Web\
dotnet test
```
<!--#endif -->

## Help
To learn more about the template go to the [project website](caRepositoryUrl). Here you can find additional guidance, request new features, report a bug, and discuss the template with other users.