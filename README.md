# Microsoft .Net Learn Tutorials on Creating Web APIs
Following [Microsoft's .NET Learn](https://learn.microsoft.com/en-us/dotnet) Tutorials on Creating Web APIs in ASP.NET by Example of a Todo List API:
 - [Creating Minimal API without use of Controllers (TodoApi directory)](https://learn.microsoft.com/en-us/aspnet/core/tutorials/min-web-api?view=aspnetcore-8.0&tabs=visual-studio-code)
 - [Creating API using Controllers (TodoApi_controllers directory)](https://learn.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-8.0&tabs=visual-studio)

# Common of the Two Tutorials:
## .NET SDK
Used [.NET SDK 8.0](https://dotnet.microsoft.com/en-us/download/visual-studio-sdks) which is latest LTS release (3/31/24)
Can check if you have the SDK and the right version by command in terminal:
`dotnet --version`

If you don’t have .NET SDK 8.0, then run the command in terminal:
`sudo apt-get install dotnet-sdk-8.0`

## Other
Both built in [ASP.NET Core](https://learn.microsoft.com/en-us/aspnet/core/?view=aspnetcore-8.0)
The example is API calls for a Todo list:
- **GET** `/todoitems` - Retrieves a list of all todo items.
- **GET** `/todoitems/complete` - Fetches all todo items that are marked as complete.
- **GET** `/todoitems/{id}` - Gets a specific todo item by its ID. Returns NotFound if the item does not exist.
- **POST** `/todoitems` - Creates a new todo item and adds it to the database. Returns the created item's details.
- **PUT** `/todoitems/{id}` - Updates an existing todo item identified by its ID. It modifies both the name and completion status. Returns NotFound if the item does not exist.
- **DELETE** `/todoitems/{id}` - Deletes a todo item by its ID. Returns NotFound if the item does not exist.
Utilizes [Swagger](https://swagger.io/) to test APIs in a nice web UI