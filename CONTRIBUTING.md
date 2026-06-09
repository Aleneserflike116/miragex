# Contributing to MirageX

Thank you for your interest in contributing to MirageX. This document outlines
the process and standards for contributing to the project.

<br>

## Code of Conduct

By participating in this project, you agree to abide by the
[Code of Conduct](CODE_OF_CONDUCT.md).

<br>

## Getting Started

**Step 1 - Fork the repository**

Click the "Fork" button on the GitHub repository page.

**Step 2 - Clone your fork**

```bash
git clone https://github.com/dulanjayabhanu/miragex.git
cd miragex
```

**Step 3 - Set up the project**

Ensure you have Java 21 and Maven installed, then build the project:

```bash
mvn package
```

**Step 4 - Run the tests**

```bash
mvn test
```

All tests must pass before submitting a pull request.

<br>

## Branching Strategy

Always create a new branch from `main` for your changes:

```bash
git checkout main
git pull origin main
git checkout -b type/short-description
```

Branch naming convention:

| Type | Example |
|---|---|
| New feature | feat/secure-delete-command |
| Bug fix | fix/header-parsing-error |
| Documentation | docs/update-readme |
| Refactor | refactor/crypto-engine-cleanup |
| Tests | test/add-fileutil-tests |
| Chore | chore/update-dependencies |

<br>

## Commit Message Convention

MirageX follows the Conventional Commits standard.

```
<type>: <short summary>

<optional body explaining what and why>
```

Allowed types:

| Type | Purpose |
|---|---|
| feat | New feature |
| fix | Bug fix |
| docs | Documentation changes |
| refactor | Code refactor without behavior change |
| test | Adding or updating tests |
| chore | Build, config, or tooling changes |

Example:

```
feat: add secure delete command after encryption

Added a --shred flag to the lock command that overwrites and deletes
the original plain text file after successful encryption.
```

<br>

## Pull Request Process

1. Ensure all tests pass with `mvn test`
2. Update the README if your change affects usage or behavior
3. Create a pull request against the `main` branch
4. Fill in the pull request template completely
5. Wait for review and address any feedback

<br>

## Code Standards

- Follow the existing package and class structure
- Keep classes focused on a single responsibility
- All public methods must have a Javadoc comment
- No hardcoded secrets, passwords, or sensitive data
- No external network calls under any circumstances
- All cryptographic changes must be clearly justified

<br>

## Reporting Issues

Please use the GitHub issue templates for:

- Bug reports
- Feature requests

Do not open issues for security vulnerabilities. See
[SECURITY.md](SECURITY.md) for the responsible disclosure process.

<br>

## Development Environment

| Tool | Version |
|---|---|
| Java | 21 |
| Maven | 3.x |
| IDE | IntelliJ IDEA (recommended) |