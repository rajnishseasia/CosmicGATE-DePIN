# Security Policy

## Supported Versions
The `CosmicGATE-DePIN` project currently supports the latest version of the repository (main branch) for security updates. We recommend always using the latest release to ensure you have the most recent security patches.

| Version | Supported          |
|---------|--------------------|
| main    | :white_check_mark: |
| Older   | :x:                |

## Reporting a Vulnerability
We take the security of CosmicGATE-DePIN seriously. If you discover a security vulnerability, please report it responsibly by following these steps:

1. **Do Not Report Publicly**: Avoid disclosing the issue in public forums, such as GitHub issues, until it has been addressed to prevent exploitation.
2. **Contact Us Privately**:
   - Email the maintainers at [security@cosmicgate.ai](mailto:security@cosmicgate.ai) with a detailed description of the vulnerability.
   - Include steps to reproduce, potential impact, and any suggested fixes.
   - If possible, use encrypted communication (e.g., PGP key available upon request).
3. **Expected Response**:
   - You will receive an acknowledgment within 48 hours.
   - We aim to resolve critical vulnerabilities within 14 days and will keep you updated on progress.
4. **Disclosure Process**:
   - Once the issue is resolved, we may coordinate with you for responsible disclosure, including credit in release notes (if desired).
   - Public disclosure will occur only after a fix is deployed, unless otherwise agreed.

## Security Guidelines
- **Sensitive Data**: Never commit sensitive information (e.g., API keys, database credentials) to the repository. Use environment variables or a secure vault (e.g., AWS Secrets Manager).
- **Dependencies**: Ensure all Go dependencies in `go.mod` are up-to-date. Use `go get -u` to update dependencies and check for known vulnerabilities with tools like `govulncheck`.
- **Docker**: If using Docker, ensure images are built from trusted base images and scanned for vulnerabilities (e.g., using `docker scan`).
- **Code Review**: All contributions are subject to review to ensure no security issues are introduced.

## Reporting Issues
For non-security-related issues, please use the [issue tracker](https://github.com/rajnishseasia/CosmicGATE-DePIN/issues).

## Contact
For further inquiries, reach out via [security@cosmicgate.ai](mailto:security@cosmicgate.ai) or open a non-security issue in the [issue tracker](https://github.com/rajnishseasia/CosmicGATE-DePIN/issues).

Thank you for helping keep CosmicGATE-DePIN secure!