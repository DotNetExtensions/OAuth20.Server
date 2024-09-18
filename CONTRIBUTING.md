# Contributing to DotNetExtensions.OAuth20.Server

Thank you for your interest in contributing to DotNetExtensions.OAuth20.Server! We appreciate all contributions, whether big or small, and we aim to make the process as clear and efficient as possible. Please review the following guidelines to ensure a smooth collaboration.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Contributing Code and Documentation](#contributing-code-and-documentation)
    - [Development Environment Setup](#development-environment-setup)
    - [Branching Strategy](#branching-strategy)
    - [Commit Messages](#commit-messages)
    - [Pull Requests](#pull-requests)
- [Style Guides](#style-guides)
  - [Coding Standards](#coding-standards)
  - [Writing Standards](#writing-standards)
- [Running Tests](#running-tests)
- [Security Vulnerabilities](#security-vulnerabilities)
- [Additional Notes](#additional-notes)

---

## Code of Conduct

This project follows the [Contributor Covenant Code of Conduct](./CODE_OF_CONDUCT.md). Please familiarize yourself with this document to ensure a positive and inclusive community environment.

---

## How Can I Contribute?

### Reporting Bugs

1. [**Search for existing issues**](https://github.com/DotNetExtensions/OAuth20.Server/issues) to avoid duplication.
2. If no issue exists, create a new one via the GitHub Issues section.
3. Provide as much detail as possible:
   - Description of the bug.
   - Steps to reproduce.
   - Expected vs. actual behavior.
   - Environment details (e.g., OS version, .NET version).
   - Relevant screenshots or logs, if applicable.

### Suggesting Enhancements

To propose new features or improvements:

1. [**Create an issue**](https://github.com/DotNetExtensions/OAuth20.Server/issues/new/choose) in GitHub with a detailed description of your idea, including:
   - The reasoning behind the enhancement.
   - How it benefits the project.
   - Any relevant details or examples.

### Contributing Code and Documentation

We welcome contributions to our codebase, documentation, and project files, including fixing bugs, adding new features, improving code quality, and enhancing documentation.

#### Development Environment Setup

1. **Fork the repository** and clone it to your local machine:

   ```bash
   git clone https://github.com/your-username/OAuth20.Server.git
   ```

2. **Install required tools and dependencies**:

   - Install the [.NET SDK](https://dotnet.microsoft.com/download) (version 8.0 or later).
   - Install any other dependencies as specified in the `README.md` or project documentation.

3. **Build the project** to ensure everything is set up correctly:

   ```bash
   cd src\DotNetExtensions.OAuth20
   dotnet build
   ```

4. **Run tests** to confirm the environment is properly configured:

   ```bash
   dotnet test
   ```

#### Branching Strategy

1. **Update your local `develop` branch**:

   ```bash
   git checkout develop
   git pull origin develop
   ```

2. **Create a new branch** following our branching strategy:

   - For new features or significant updates:

     ```bash
     git checkout -b feature/your-feature-name develop
     ```

   - For fixing non-critical issues:

     ```bash
     git checkout -b bugfix/your-bugfix-name develop
     ```

   - For fixing critical issues that require immediate attention:

     ```bash
     git checkout -b hotfix/your-hotfix-name main
     ```

3. **Make your changes** to the code or documentation.

4. **Commit your changes** with clear and descriptive commit messages.

5. **Push your branch** to your forked repository:

   ```bash
   git push origin your-branch-name
   ```

6. **Submit a pull request** to the main repository. All changes made in `feature` and `bugfix` branches should be merged into the `develop` branch, while changes from `hotfix` branches should be merged into the `main` branch via pull requests.

For detailed information on branching strategies (e.g., `feature/`, `bugfix/`, `hotfix/`), please refer to the [GITFLOW.md](./GITFLOW.md).

#### Commit Messages

- Use **sentence case** for commit messages (start with a capital letter, avoid periods).
- **Format:** `[scope] #issue_number Description of the change`.
  - **Scopes:** Use scopes relevant to the codebase, such as `[feature]`, `[fix]`, `[test]`, `[docs]`, `[config]`, `[workflow]`.
  - **Example:**

    - `[feature] #25 Add support for OAuth 2.0 PKCE flow`
    - `[fix] #30 Correct token expiration handling`

- Place the issue number directly after the scope to quickly reference related issues.

#### Pull Requests

- Ensure your pull request is **linked to a GitHub issue** if applicable.
- Use clear, descriptive titles and provide a detailed summary of the changes in the pull request.
- Include the **issue number** in the pull request title and description if it's related to an existing issue.
- Our pull request template includes a checklist; please ensure you review and complete it before submitting.
- **Target the `develop` branch** when creating your pull request (unless it's a hotfix, which should target `main`).

---

## Style Guides

### Coding Standards

- Adhere to the coding conventions outlined in our [CONVENTIONS.md](./CONVENTIONS.md) file.
- Ensure your code is well-documented and uses clear function/method names.
- Follow best practices for secure and efficient C# development.

### Writing Standards

- **Clarity and Conciseness:** Ensure that your code comments and documentation are clear and concise.
- **Tone:** Use a professional and friendly tone in documentation.
- **Language:** All contributions should be in English.
- **Formatting:** Follow the existing formatting styles used in the code and documents.
- **Markdown Best Practices:** Use proper Markdown syntax for documentation.

---

## Running Tests

- Before submitting your pull request, ensure that all tests pass:

  ```bash
  dotnet test
  ```

- If you have added new functionality, please include corresponding unit tests.

---

## Security Vulnerabilities

If you discover a security vulnerability, please follow our [SECURITY.md](./SECURITY.md) guidelines for responsible disclosure. We take security seriously and will address issues promptly.

---

## Additional Notes

- We value all contributions—no matter the size—whether it's fixing a typo, improving performance, or adding new features.
- If you have any questions or need clarification, feel free to reach out via GitHub issues or discussions.
- **Open Communication:** We're here to help. Don't hesitate to ask questions if you're unsure about any process.

Thank you for helping us improve DotNetExtensions.OAuth20.Server!
