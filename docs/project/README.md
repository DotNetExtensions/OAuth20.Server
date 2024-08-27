# DotNetExtensions.OAuth20 - Comprehensive OAuth 2.0 Authorization Server Project

DotNetExtensions.OAuth20 is a modular, cross-platform solution designed to implement OAuth 2.0 authorization flows in .NET applications. This project offers reusable libraries for core OAuth 2.0 functionalities and a fully hosted ASP.NET Core web application, making it easy to deploy and integrate secure authorization services across various environments.

## Table of Contents
- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Roadmap](#roadmap)
- [Task List](#task-list)
- [Project Structure](#project-structure)
  - [DotNetExtensions.OAuth20 (Library Repository)](#1-dotnetextensionsoauth20-library-repository)
  - [DotNetExtensions.OAuth20.Host (Hosted Application Repository)](#2-dotnetextensionsoauth20host-hosted-application-repository)
- [Installation](#installation)
  - [DotNetExtensions.OAuth20 Library Installation](#dotnetextensionsoauth20-library-installation)
    - [Using NuGet Packages](#using-nuget-packages)
    - [Direct Download](#direct-download)
  - [DotNetExtensions.OAuth20.Host Application Installation](#dotnetextensionsoauth20host-application-installation)
    - [Kubernetes Installation](#kubernetes-installation)
    - [Helm Installation](#helm-installation)
    - [Windows Service or IIS Installation](#windows-service-or-iis-installation)
- [Running Tests and Benchmarks](#running-tests-and-benchmarks)
- [Demo Projects](#demo-projects)
- [Repository Links](#repository-links)
- [Community and Support](#community-and-support)
- [References](#references)
- [License](#license)
- [Contributing](#contributing)
  - [Conventions](#conventions)
- [Security](#security)
- [Change Log](#change-log)

## Project Overview

Welcome to the DotNetExtensions.OAuth20 project, a comprehensive solution for implementing OAuth 2.0 authorization flows in .NET applications. This project is divided into two main repositories, each serving a distinct purpose:

1. **Library Repository:** 
   - Contains the core OAuth 2.0 authorization libraries, data source integration libraries, and Blazor-based UI components (Admin Panel and Personal Account).
   - Distributed via NuGet packages for easy integration into .NET projects.

2. **Hosted Application Repository:**
   - Contains an ASP.NET Core hosted web application that provides a fully functional OAuth 2.0 Authorization Server.
   - Utilizes the libraries from the Library Repository to deliver OAuth 2.0 endpoints, UI components, and data storage options.
   - Supports deployment via Docker, Kubernetes, Helm, and as a Windows Service or IIS application.

### Key Features
- **Modular Architecture:** Separates core functionality into reusable libraries and a hosted application, allowing for flexible deployment and integration.
- **Cross-Platform Compatibility:** Supports .NET 8, .NET Standard 2.0/2.1, and .NET Framework 4.8.1.
- **Flexible Data Storage:** Libraries support in-memory, SQLite, MS SQL Server, PostgreSQL, MySQL, and more.
- **User Interfaces:** Includes a Blazor-based user-friendly Admin Panel and Personal Account UI for managing OAuth 2.0 consents and configurations.
- **Security Compliance:** Adheres to the OAuth 2.0 [RFC 6749](https://datatracker.ietf.org/doc/html/rfc6749) specification with additional enhancements.
- **CI/CD Integration:** Automated workflows using GitHub Actions for building, testing, and release uploading.
- **Comprehensive Testing:** Includes unit, integration, and load tests, benchmarks, demo projects, and configuration samples.
- **Container and Cloud Support:** Ready-to-use Docker images with Kubernetes and Helm deployment configurations.
- **Windows Installation:** Install on OS Windows using Installer as a Hosted Service or an IIS application.

## Roadmap
To understand our future plans and milestones, please refer to our [ROADMAP.md](https://DotNetExtensions/OAuth20/docs/project/ROADMAP.md).

## Task List
For a detailed breakdown of ongoing and upcoming tasks, please refer to our [TASKLIST.md](https://DotNetExtensions/OAuth20/docs/project/TASKLIST.md).

## Project Structure

This project is divided into the following repositories:

### 1. DotNetExtensions.OAuth20 (Library Repository)
- **Core Libraries:** Implement the core OAuth 2.0 authorization flows and related functionalities.
- **Data Source Libraries:** Provide integrations with various data storage systems.
- **UI Libraries:** Include Blazor-based UI components for Admin Panel and Personal Account with their integration into .NET applications.
- **Infrastructure:** Contains unit and integration tests, benchmarks, and demo projects.
- **NuGet and Direct Distribution:** All releases of all libraries are available in the NuGet Gallery or via direct download.

### 2. DotNetExtensions.OAuth20.Host (Hosted Application Repository)
- **ASP.NET Core Application:** Provides a hosted OAuth 2.0 Authorization Server.
- **Integration:** Uses the core and UI libraries from the Library Repository.
- **Infrastructure:** Contains integration and load tests, demo scenarios, and configuration samples.
- **Deployment:** Supports deployment through Docker, Kubernetes, Helm, and as a Windows Service or IIS application.

## Installation

### DotNetExtensions.OAuth20 Library Installation

**Prerequisites**
- .NET SDK

#### Using NuGet Packages
The libraries are available as NuGet packages. To install, use the following command in your package manager console:

```bash
dotnet add package DotNetExtensions.OAuth20.Server --version x.x.x
```

#### Direct Download
You can also download the compiled library assemblies directly from the repository and add them to your project manually.

#### Sample of adding services and middleware from the library:

Add the library services (C#):

```cs
app.Services.AddOAuth20Server();
```

And use its middleware (C#):

```cs
app.UseOAuth20Server();
```

### DotNetExtensions.OAuth20.Server.Host (OAuth20 Server / oauth20_server) Application Installation

**Prerequisites**
- Docker (if using containerized deployments)
- Kubernetes (for cluster-based deployments)
- IIS (for IIS installations)

#### Kubernetes Installation
To deploy the server on a Kubernetes cluster, use the following command:

```bash
kubectl apply -f https://github.com/DotNetExtensions/OAuth20.Server.Host/kubernetes-manifest.yaml
```

#### Helm Installation
To install using Helm, use the following command:

```bash
helm install your-release-name dotnetextensions/oauth20serverhost --version x.x.x
```

#### Windows Service or IIS Installation
You can install your OAuth 2.0 Server as a Windows Service or IIS website by following the instructions in the [DotNetExtensions/OAuth20.Server.Host](https://github.com/DotNetExtensions/OAuth20.Server.Host) repository.

## Running Tests and Benchmarks

To run the unit tests included in the Library Repository, use the following command:

```bash
dotnet test
```

To run benchmarks, navigate to the benchmarks directory and use:

```bash
dotnet run -c Release
```

## Demo Projects

This project includes several demo projects within the Library Repository to help you get started with different OAuth 2.0 flows. You can find these in the `Demos` directory. Follow the README files within each demo project for setup and usage instructions.

## Repository Links

Explore the repositories for code, documentation, and issue tracking:

- **Library Repository:** [DotNetExtensions/OAuth20](https://github.com/DotNetExtensions/OAuth20)
- **Hosted Application Repository:** [DotNetExtensions/OAuth20.Server.Host](https://github.com/DotNetExtensions/OAuth20.Server.Host)

## Community and Support
For discussions, support, and feedback, please visit:

- [GitHub Project Page](https://github.com/orgs/DotNetExtensions/projects/17)
- [Project Dedicated Website](https://dotnetextensions.com/oauth20)
- [Community Board](https://dotnetextensions.com/oauth20/community)
- [Support Page](https://dotnetextensions.com/oauth20/support)

## References
This project is based on the OAuth 2.0 Authorization Framework, specifically following the guidelines set forth in [RFC 6749](https://datatracker.ietf.org/doc/html/rfc6749).

## License
This project is licensed under the [MIT License](https://DotNetExtensions/OAuth20/LICENSE).

## Contributing
We welcome contributions! Please read our [Contributing Guidelines](https://DotNetExtensions/OAuth20/CONTRIBUTING.md) to get started.

### Conventions
For detailed information on coding, formatting, and contribution conventions, please refer to our [CONVENTIONS.md](https://DotNetExtensions/OAuth20/CONVENTIONS.md) file.

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

For more details, please refer to our [SECURITY.md](https://DotNetExtensions/OAuth20/SECURITY.md) file.

## Change Log
All notable changes to this project will be documented in [CHANGELOG.md](https://DotNetExtensions/OAuth20/docs/project/CHANGELOG.md).
