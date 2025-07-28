# Contributing to CosmicGATE-DePIN

Thank you for contributing to CosmicGATE-DePIN, the server component for decentralized infrastructure in the CosmicGATE.ai ecosystem. We welcome improvements to the server logic, performance, or documentation.

## Table of Contents
- [Code of Conduct](#code-of-conduct)
- [How to Contribute](#how-to-contribute)
- [Setting Up the Development Environment](#setting-up-the-development-environment)
- [Coding Guidelines](#coding-guidelines)
- [Submitting Changes](#submitting-changes)
- [Testing](#testing)
- [Reporting Issues](#reporting-issues)
- [Security](#security)
- [License](#license)

## Code of Conduct
Adhere to our [Code of Conduct](CODE_OF_CONDUCT.md) to maintain a positive community.

## How to Contribute
1. Check the [issue tracker](https://github.com/rajnishseasia/CosmicGATE-DePIN/issues) or create a new issue.
2. Fork the repository and create a feature branch.
3. Follow the setup and coding guidelines.
4. Submit a pull request with a clear description.

## Setting Up the Development Environment
### Prerequisites
- **Go**: Version 1.18 or later.
- **Python**: Version 3.8 or later.
- **Docker** (optional): For containerized testing.
- **Git**: For version control.

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/rajnishseasia/CosmicGATE-DePIN.git
   cd CosmicGATE-DePIN
   ```
2. Install dependencies:
   ```bash
   go mod tidy
   ```
3. Configure environment variables:
   - Create a `.env` file based on `.env.example`.
4. Run locally:
   ```bash
   go run .
   ```

## Coding Guidelines
- **Code Style**: Follow Go conventions as per `gofmt`. Run `go fmt ./...` to format code.
- **Linting**: Use `golangci-lint` for static analysis. Install with:
   ```bash
   go install github.com/golangci/golangci-lint/cmd/golangci-lint@latest
   ```
   Run: `golangci-lint run`.
- **Commits**: Follow [Conventional Commits](https://www.conventionalcommits.org/) (e.g., `feat: add new API endpoint`).
- **Structure**: Place server logic in `/src` and configurations in `/config`.
- **Packages**: Keep dependencies minimal and list them in `go.mod`.

## Submitting Changes
1. Create a branch:
   ```bash
   git checkout -b feature/<your-feature-name>
   ```
2. Make and test changes.
3. Commit changes:
   ```bash
   git commit -m "feat: add new API endpoint"
   ```
4. Push and open a pull request:
   ```bash
   git push origin feature/<your-feature-name>
   ```

## Testing
- Run tests: `go test ./...`.
- Test APIs locally or with Docker.
- Ensure all tests pass before submitting.
- Add unit tests for new functionality in `<package>_test.go` files.

## Reporting Issues
- Use the [issue tracker](https://github.com/rajnishseasia/CosmicGATE-DePIN/issues) for bugs or suggestions.
- Include detailed steps to reproduce.

## Security
- Avoid committing sensitive data (e.g., API keys).
- Use environment variables for credentials.
- Report vulnerabilities via [SECURITY.md](SECURITY.md).

## License
Contributions are licensed under the MIT License. See [LICENSE](LICENSE).