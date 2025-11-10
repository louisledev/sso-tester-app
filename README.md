# SSO Tester App

This project is an ASP.NET Core web application for testing SSO integrations.
When running the application, it connects to a specified identity provider using OpenID Connect, and displays user information upon successful authentication.

## Prerequisites

### Installing LibMan

LibMan is a .NET global tool. To install it, run:

```
dotnet tool install -g Microsoft.Web.LibraryManager.Cli
```

If you get a "command not found" error after installation, add the .NET global tools path to your shell profile:

```
export PATH="$PATH:$HOME/.dotnet/tools"
```

You can now use `libman` from your terminal.

## Restoring Client Libraries

To restore the client-side libraries (Bootstrap, jQuery, etc.), run:

```
libman restore
```

## Building the Project

To build the project, run:

```
dotnet build ./oidc-tester-app.sln
```

## Running the Project

To run the project locally, use:

```
dotnet run
```

The application will start and provide a local URL (e.g., https://localhost:5001) in the console output.

## Configuration

- App settings are in `appsettings.json` and you should create an `appsettings.Development.json` with the client details.
- Launch profiles are in `Properties/launchSettings.json`.

## Additional Notes

- Do not commit the contents of `wwwroot/lib` to source control. Use `libman.json` to restore libraries.
- For troubleshooting, check the output in the terminal and review logs in the `bin/Debug/net8.0` directory.

## Useful Commands

- Restore NuGet packages:
  ```
  dotnet restore
  ```
- Run tests (if any):
  ```
  dotnet test
  ```

## License

Specify your license here.
