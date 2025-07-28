# Security Policy

## Supported Versions
The `CosmicGATE-DePIN` project currently supports the latest version of the repository (main branch) for security updates. We recommend using the latest release to ensure you have the most recent security patches.

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

## Access Control
To ensure the security and integrity of the CosmicGATE-DePIN repository, access is tightly controlled:
- **Repository Permissions**:
  - Only authorized maintainers have write access to the `main` branch.
  - External contributors must submit changes via pull requests (PRs) to a feature branch.
  - GitHub branch protection rules are enabled for the `main` branch, requiring at least one maintainer review and passing CI checks before merging.
- **AWS Amplify Access**:
  - Deployment access is restricted to maintainers with AWS credentials configured in the Amplify Console.
  - Environment variables (e.g., API keys, database credentials) are stored securely in AWS Amplify or AWS Secrets Manager, not in the repository.
- **Configuring Access**:
  - To request access (e.g., collaborator status), contact the maintainers via the [issue tracker](https://github.com/rajnishseasia/CosmicGATE-DePIN/issues) with your GitHub username and justification.
  - Maintainers will review and grant access based on project needs.

## Pull Request (PR) Security
To maintain code quality and security, all contributions must follow a secure PR process:
- **Submission**: Submit PRs from a forked repository or a feature branch (e.g., `feature/<your-feature-name>`).
- **Review Process**:
  - PRs require at least one approval from a maintainer.
  - Automated checks (e.g., `golangci-lint`, `go test ./...`) must pass via GitHub Actions.
  - Sensitive data (e.g., API keys) is scanned using GitHub’s secret scanning feature.
- **Branch Protection**:
  - The `main` branch is protected to prevent direct pushes.
  - PRs must be up-to-date with `main` before merging.
- See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed PR submission guidelines.

## Deployment Security
Deployments for CosmicGATE-DePIN are managed securely to prevent unauthorized access or data exposure:
- **AWS Amplify**:
  - Only maintainers with AWS Amplify Console access can trigger deployments.
  - Environment variables are configured in the Amplify Console, not hardcoded in the repository.
  - Use `amplify env` to manage environment-specific settings securely.
- **Docker**:
  - Docker images are built from trusted base images (e.g., official Go images).
  - Run `docker scan` to check for vulnerabilities before deployment.
  - Store Docker credentials securely and avoid exposing them in the repository.
- **Deployment Process**:
  - Deployments are triggered via the Amplify Console or GitHub Actions after PR approval.
  - Ensure all tests pass (`go test ./...`) before deployment.
- Any deployment issues should be reported via the [issue tracker](https://github.com/rajnishseasia/CosmicGATE-DePIN/issues).

## Security Guidelines
- **Sensitive Data**: Never commit sensitive information (e.g., API keys, database credentials) to the repository. Use environment variables or AWS Secrets Manager.
- **Dependencies**: Ensure all Go dependencies in `go.mod` are up-to-date. Use `go get -u` to update dependencies and check for known vulnerabilities with `govulncheck`.
- **Docker**: If using Docker, ensure images are built from trusted base images and scanned for vulnerabilities (e.g., using `docker scan`).
- **Code Review**: All contributions are subject to review to ensure no security issues are introduced.

## Reporting Issues
For non-security-related issues, please use the [issue tracker](https://github.com/rajnishseasia/CosmicGATE-DePIN/issues).

## Contact
For security concerns, reach out via [security@cosmicgate.ai](mailto:security@cosmicgate.ai). For other inquiries, use the [issue tracker](https://github.com/rajnishseasia/CosmicGATE-DePIN/issues).

Thank you for helping keep CosmicGATE-DePIN secure!