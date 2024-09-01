# Security Policy

DotNetExtensions.OAuth20 is committed to maintaining project security and ensuring a safe experience for all users. We appreciate your efforts to responsibly disclose vulnerabilities and help us improve our software.

## Supported Versions

The following versions of DotNetExtensions.OAuth20 currently receive security updates:

| Version | Supported          |
| ------- | ------------------ |
| 0.0.0   | :white_check_mark: |
| 0.0.0   | :x:                |

## Reporting a Vulnerability

If you discover a security vulnerability within the DotNetExtensions.OAuth20 project, we encourage you to report it to us responsibly. Please do not disclose the details of the vulnerability publicly until we have had a chance to address it.

### Preferred Method: GitHub Private Vulnerability Reporting

We strongly recommend that you report vulnerabilities directly through GitHub’s "Private vulnerability reporting" feature. This method ensures that your report is securely transmitted to us, and we can begin addressing the issue immediately.

To report a vulnerability via GitHub:

1. Go to the [Security tab of our repository](https://github.com/DotNetExtensions/OAuth20/security).
2. Click on "Report a vulnerability."
3. Fill in the "Advisory Details" form provided.

This method is the most secure and streamlined way to handle vulnerability disclosures. The GitHub form includes the following fields:

- **Title:** A brief, descriptive title of the vulnerability.
- **Description:** A detailed explanation of the vulnerability. 
  - _Summary:_ A short summary of the problem.
  - _Details:_ A more in-depth explanation, ideally with references to the affected code.
  - _Proof of Concept (PoC):_ Steps to reproduce the vulnerability.
  - _Impact:_ The type and scope of the vulnerability, including potential impacts.
- **Affected Products:** Information on the ecosystem, package name, affected versions, and patched versions, if any.
- **Severity:** An assessment of the severity of the vulnerability, including a vector string and CVSS scoring.
- **Weakness:** Any relevant CWE identifiers.

### Alternative Method: Email Reporting

If you prefer or are unable to use GitHub’s reporting feature, you can also report vulnerabilities via email. Please use the following format to ensure that we have all the information needed to assess and address the issue:

Send your report to: [security@dotnetextensions.com](mailto:security@dotnetextensions.com)

**Email Report Template:**

```markdown
### Title
[Provide a brief, descriptive title of the vulnerability]

### Summary
[Short summary of the problem. Make the impact and severity as clear as possible. For example: An unsafe deserialization vulnerability allows any unauthenticated user to execute arbitrary code on the server.]

### Details
[Give all details on the vulnerability. Pointing to the incriminated source code is very helpful for the maintainer.]

### Proof of Concept (PoC)
[Complete instructions, including specific configuration details, to reproduce the vulnerability.]

### Impact
[What kind of vulnerability is it? Who is impacted?]

### Affected Products
1. Product 1
    - Ecosystem: [e.g., .NET, NuGet]
    - Package Name: [e.g., DotNetExtensions.OAuth20]
    - Affected Versions: [e.g., 1.0.0 - 1.2.3]
    - Patched Versions: [e.g., 1.2.4]

### Severity
- Severity Level: [e.g., Critical, High, Moderate, Low]
- Vector String: [CVSS vector string, if known]
- CVSS Score: [Numeric score, if known]

### Weakness
[Provide any relevant CWE identifiers, if known]
```

[Learn more about CVSS scoring](https://www.first.org/cvss/v3.1/user-guide)

**Important Note:** We prefer you to report vulnerabilities via the GitHub [Security tab](https://github.com/DotNetExtensions/OAuth20/security) for a more streamlined and secure process.

## Security Update Process

After a vulnerability is reported, our team will:

1. **Verify the Issue:** We will reproduce and confirm the reported vulnerability.
2. **Assess the Impact:** We will evaluate the severity and impact of the vulnerability.
3. **Develop a Fix:** Our team will work on a patch or update to fix the vulnerability.
4. **Notify Users:** After the fix is developed and tested, we will notify users about the update.
5. **Public Disclosure:** Once the vulnerability is resolved, we will disclose the details in our [CHANGELOG.md](https://github.com/DotNetExtensions/OAuth20/CHANGELOG.md) file.

## Disclosure Policy

We believe in responsible disclosure and will follow these principles:

- Vulnerabilities will be disclosed publicly only after a fix has been implemented and released.
- We will credit the individual or organization that reported the vulnerability unless they prefer to remain anonymous.
- In cases where a vulnerability cannot be immediately fixed, we will provide temporary mitigations or workarounds.

## Code Scanning and Security Automation

At present, we thoroughly review all code pushed to our repositories to ensure that it meets our security and quality standards. As our project progresses, we plan to enhance this process by integrating automated code scanning tools, such as GitHub's CodeQL analysis, and configuring CI/CD pipelines on Actions runners. This will allow us to detect vulnerabilities and code quality issues more efficiently and systematically.

In the future, during the milestone dedicated to CI/CD setup, we will be enabling and thoroughly customizing "Code Scanning" to automatically analyze our code for security vulnerabilities and other potential issues. This step will help us maintain the highest security standards as we continue to develop and refine our project.

We will keep the community informed about these enhancements and encourage everyone to stay updated on our progress.

## Security Automation with Dependabot

We use GitHub's Dependabot to help maintain the security and stability of our dependencies. Currently, we have **Dependabot alerts** enabled to monitor and notify us of any vulnerabilities in our dependencies.

### Future Automation Plans
In the future, we plan to extend our security automation by carefully enabling and configuring the following:

- **Dependabot Security Updates:** Automatically generating pull requests to update dependencies with known vulnerabilities.
- **Dependabot Version Updates:** Regularly checking for and updating to the latest versions of dependencies.
- **Dependabot on Actions Runners:** Integrating Dependabot with our CI/CD pipeline using GitHub Actions runners, which will be fully implemented during the milestone dedicated to CI/CD setup.

We are committed to ensuring that our project remains secure and up-to-date, and these enhancements will further strengthen our security practices.

## Important Note: Do Not Push Secrets

We take the security of our project seriously and have implemented automated tools to prevent the accidental exposure of sensitive information. **Secret Scanning** and **Push Protection** are enabled in this repository. These tools will automatically scan for secrets such as API keys, passwords, and other sensitive data in your commits.

**What You Need to Know:**
- **Do not include any secrets** in your commits. This includes but is not limited to API keys, passwords, access tokens, or any other sensitive information.
- If a secret is accidentally committed, it may be flagged by our automated tools, requiring its removal before merging.
- To prevent issues, always review your commits and ensure no sensitive information is included.

These measures are in place to protect both you and the project. If you have any questions about how to safely handle sensitive information in your contributions, please contact us.

## Additional Information

### Dependency Graph and Automatic Dependency Submission

The DotNetExtensions.OAuth20 project utilizes GitHub's **Dependency Graph** feature to track and manage the dependencies used in our project. You can view the full dependency graph by navigating to the [Dependency Graph section](https://github.com/DotNetExtensions/OAuth20/network/dependencies) in our repository.

We have enabled **Automatic Dependency Submission** to ensure that our dependency data is up-to-date. This feature allows GitHub to automatically submit dependencies detected during builds to the dependency graph. While we currently use GitHub-hosted runners, we plan to implement labeled runners with custom GitHub Actions workflows for "Automatic Dependency Submission" as part of our CI/CD setup milestone.

## Additional Resources

- [OAuth 2.0 RFC 6749](https://datatracker.ietf.org/doc/html/rfc6749)
- [OWASP Security Best Practices](https://owasp.org/www-project-top-ten/)

Thank you for helping us maintain the security of DotNetExtensions.OAuth20.
