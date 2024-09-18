# Security Policy

DotNetExtensions.OAuth20.Server is committed to maintaining project security and ensuring a safe experience for all users. We appreciate your efforts to responsibly disclose vulnerabilities and help us improve our software.

## Supported Versions

The following versions of DotNetExtensions.OAuth20.Server currently receive security updates:

| Version | Supported          |
| ------- | ------------------ |
| 0.0.0   | :white_check_mark: |
| 0.0.0   | :x:                |

*Note: As the project is still in development, actual release versions will be updated here once available.*

## Reporting a Vulnerability

If you discover a security vulnerability within the DotNetExtensions.OAuth20.Server project, we encourage you to report it responsibly. Please do not disclose the details publicly until we have addressed it.

### How to Report

1. **GitHub Private Vulnerability Reporting (Preferred):**

   - Navigate to the [Security tab of our repository](https://github.com/DotNetExtensions/OAuth20.Server/security).
   - Click on **"Report a vulnerability"**.
   - Fill out the form with detailed information about the vulnerability.

   For more information, see [GitHub's guide on reporting vulnerabilities](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing/privately-reporting-a-security-vulnerability).

2. **Email Reporting:**

   - If you are unable to use GitHub's reporting feature, please send an email to [security@dotnetextensions.com](mailto:security@dotnetextensions.com).
   - Include as much detail as possible about the vulnerability to help us assess and address it promptly.

**Confidentiality:**

We take your privacy seriously. All communications regarding security vulnerabilities are kept confidential. We will not share your personal information without your explicit permission.

## Security Update Process

After a vulnerability is reported, our team will:

1. **Verify the Issue:** Reproduce and confirm the vulnerability.
2. **Assess the Impact:** Evaluate the severity and potential impact.
3. **Develop a Fix:** Work on a patch or update to resolve the issue.
4. **Release Updates:** Publish the necessary updates and inform users.
5. **Public Disclosure:** Once resolved, we will disclose the details in the [CHANGELOG.md](https://github.com/DotNetExtensions/OAuth20.Server/blob/main/CHANGELOG.md).

## Disclosure Policy

We believe in responsible disclosure and adhere to the following principles:

- Vulnerabilities will be disclosed publicly only after a fix has been implemented and released.
- We will credit the individual or organization that reported the vulnerability unless they prefer to remain anonymous.
- If a vulnerability cannot be immediately fixed, we will provide temporary mitigations or workarounds.

## Security Update Policy

We aim to release security updates promptly after confirming a vulnerability and developing a fix. While we cannot commit to specific timelines, we prioritize security issues and strive to address them as quickly as possible.

## Code Scanning and Security Automation

We continuously enhance our security practices using automated tools:

- **Code Scanning:** Utilizing GitHub's CodeQL to automatically analyze our code for vulnerabilities.
- **Dependabot Alerts:** Enabled to monitor and notify us of vulnerabilities in our dependencies.

*Note: As the project is still in development, security automation building is currently in the setup phase.*

## Important Note: Do Not Push Secrets

Please ensure that you do not commit any sensitive information to the repository, such as API keys, passwords, or access tokens. Our repository has **Secret Scanning** and **Push Protection** enabled to prevent accidental exposure of secrets.

**Guidelines:**

- Review your commits to ensure they do not contain sensitive data.
- If you accidentally commit a secret, please contact us immediately so we can assist in mitigating any potential risks.

## Additional Information

For more details on our security practices and policies, please refer to:

- [OAuth 2.0 RFC 6749](https://datatracker.ietf.org/doc/html/rfc6749)
- [OWASP Security Best Practices](https://owasp.org/www-project-top-ten/)

Thank you for helping us maintain the security of DotNetExtensions.OAuth20.Server.
