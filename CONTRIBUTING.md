# Contributing to DotNetExtensions.OAuth20

Thank you for your interest in contributing to DotNetExtensions.OAuth20! We appreciate all contributions, whether big or small, and we aim to make the process as clear and efficient as possible. Please review the following guidelines to ensure a smooth collaboration.

## Table of Contents
- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Contributing Code](#contributing-code)
    - [Branching](#branching)
    - [Commit Messages](#commit-messages)
    - [Pull Requests](#pull-requests)
- [Style Guides](#style-guides)
  - [Coding Standards](#coding-standards)
- [Security Vulnerabilities](#security-vulnerabilities)
- [Additional Notes](#additional-notes)

---

## Code of Conduct

This project follows the [Contributor Covenant Code of Conduct](./CODE_OF_CONDUCT.md). Please familiarize yourself with this document to ensure a positive and inclusive community environment.

---

## How Can I Contribute?

### Reporting Bugs

1. [**Search for existing issues**](https://github.com/DotNetExtensions/OAuth20/issues) to avoid duplication.
2. If no issue exists, create a new one via the GitHub Issues section.
3. Provide as much detail as possible:
   - Description of the bug.
   - Steps to reproduce.
   - Expected vs actual behavior.
   - Relevant logs or screenshots.

### Suggesting Enhancements

To propose new features or improvements:
1. **Create an issue** in GitHub with a detailed description of your idea, including:
   - The reasoning behind the enhancement.
   - How it benefits the project.
   - Any technical details if relevant.

### Contributing Code

#### Branching

1. **Fork the repository** and clone it to your local machine:
   ```bash
   git clone https://github.com/your-username/OAuth20.git
   ```
2. **Create a new branch** from the `develop` branch:
   ```bash
   git checkout -b feature/your-feature develop
   ```
3. **Test your changes** thoroughly before submitting a pull request.
4. **Ensure all feature, bugfix, and hotfix branches** are merged into the `develop` branch via pull requests.

For detailed information on branching strategies (e.g., `feature/`, `bugfix/`, `hotfix/`), please refer to the [GITFLOW.md](./GITFLOW.md).

#### Commit Messages

- Use **sentence case** for commit messages (start with a capital letter, avoid periods).
- **Scopes** should be written in **lowercase** (e.g., `[docs]`, `[feature]`, `[fix]`).
- **Format**: `[scope] #issue_number Description of the change`.
  - Example: `[docs] #5 Add CONTRIBUTING.md file`
  - Example: `[feature] #10 Add OAuth20 token generation`
- Place the issue number at the **beginning** of the commit message to quickly reference related issues.

#### Pull Requests

- Ensure your pull request is **linked to a GitHub issue** if applicable.
- Ensure all **tests pass** and your changes do not break existing functionality.
- Use clear, descriptive titles and provide a detailed summary of the changes in the PR.
- Include the **issue number** in the pull request title and description.

You can submit a PR through the [GitHub Pull Request](https://github.com/DotNetExtensions/OAuth20/pulls) section.

---

## Style Guides

### Coding Standards

- Adhere to the coding conventions outlined in [CONVENTIONS.md](./CONVENTIONS.md).
- Ensure your code is well-documented and uses clear function/method names.
- Follow best practices for secure and efficient C# development (e.g., using async methods and thread-safe code).

---

## Security Vulnerabilities

If you discover a security vulnerability, please follow our [SECURITY.md](./SECURITY.md) guidelines for responsible disclosure. We take security seriously and will address issues promptly.

---

## Additional Notes

- We value all contributions—no matter the size—whether it's a typo fix or a new feature.
- If you have any questions or need clarification, feel free to reach out via GitHub issues or discussions.

Thank you for helping us improve DotNetExtensions.OAuth20!
