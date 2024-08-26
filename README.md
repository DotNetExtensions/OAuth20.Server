# DotNetExtensions.OAuth20 - Core OAuth 2.0 Authorization Libraries

## Repository Overview

**DotNetExtensions.OAuth20** provides a set of core libraries for implementing OAuth 2.0 authorization flows in .NET applications. This repository includes essential components such as data source integration libraries and Blazor-based UI components for Admin Panel and Personal Account. 

For a comprehensive overview of the entire project, including how this repository fits into the larger architecture, visit the [DotNetExtensions.OAuth20 GitHub Project Page](https://github.com/orgs/DotNetExtensions/projects/17).

## Table of Contents
- [Repository Overview](#repository-overview)
- [Key Features](#key-features)
- [Installation](#installation)
  - [Using NuGet Packages](#using-nuget-packages)
  - [Direct Download](#direct-download)
- [Running Tests and Benchmarks](#running-tests-and-benchmarks)
- [Demo Projects](#demo-projects)
- [Linked Repositories](#linked-repositories)
- [Community and Support](#community-and-support)
- [References](#references)
- [License](#license)
- [Contributing](#contributing)
- [Security](#security)
- [Change Log](#change-log)

### Key Features
- **Modular Architecture:** Core libraries for OAuth 2.0, UI components, and data source integrations.
- **Cross-Platform Compatibility:** Supports .NET 8, .NET Standard 2.0/2.1, and .NET Framework 4.8.1.
- **Flexible Data Storage:** Libraries support in-memory, SQLite, MS SQL Server, PostgreSQL, MySQL, and more.
- **Blazor-Based UI:** User-friendly Admin Panel and Personal Account components.
- **NuGet Distribution:** Available as NuGet packages for easy integration into .NET projects.
- **Comprehensive Testing:** Includes unit tests, integration tests, benchmarks, and demo projects.

## Installation

### Using NuGet Packages
Install the core library via NuGet:

```
dotnet add package DotNetExtensions.OAuth20 --version x.x.x
```

### Direct Download
Download the compiled library assemblies directly from the repository and add them to your project manually.

#### Sample of adding services and middleware from the library:

Add the library services (C#):

```cs
app.Services.AddOAuth20Server();
```

And use its middleware (C#):

```cs
app.UseOAuth20Server();
```

## Running Tests and Benchmarks

Run unit tests:

```
dotnet test
```

Run benchmarks:

```
dotnet run -c Release --project benchmarks
```

## Demo Projects

Explore demo projects in the `Demos` directory to see how to implement different OAuth 2.0 flows.

## Linked Repositories

- **Hosted Application Repository:** [DotNetExtensions/OAuth20.Server.Host](https://github.com/DotNetExtensions/OAuth20.Server.Host)

## Community and Support
For discussions, support, and feedback, visit:

- [Project Website](https://dotnetextensions.com/oauth20)
- [Community Board](https://dotnetextensions.com/oauth20/community)
- [Support Page](https://dotnetextensions.com/oauth20/support)

## References
This project is based on the OAuth 2.0 Authorization Framework, specifically following the guidelines set forth in [RFC 6749](https://datatracker.ietf.org/doc/html/rfc6749).

## License
This project is licensed under the [MIT License](./LICENSE).

## Contributing
We welcome contributions! Please read our [Contributing Guidelines](./CONTRIBUTING.md) to get started.

## Security

We take the security of our project seriously. If you discover any security vulnerabilities, please follow the instructions below to report them:

### Security Policy

Our security policy ensures that any discovered vulnerabilities are addressed promptly and responsibly. We are committed to maintaining the security of the DotNetExtensions.OAuth20 project and its related repositories.

### Reporting a Vulnerability

If you find a vulnerability, please report it by emailing [security@dotnetextensions.com](mailto:security@dotnetextensions.com). Provide as much information as possible, including:

- A description of the vulnerability.
- Steps to reproduce the issue.
- Potential impact of the vulnerability.
- Any possible mitigations you may have already implemented.

We will respond to your report as quickly as possible and keep you informed of the progress in resolving the issue.

For more details, please refer to our [SECURITY.md](./SECURITY.md) file.

## Change Log
All notable changes to this project will be documented in [CHANGELOG.md](./CHANGELOG.md).
