# Contributing to EUDI Keycloak Plugin


Thanks for your interest in contributing! 🎉


## How to Contribute
1. **Fork** the repository and create your branch from `main`.
2. **Code style**: Follow existing formatting; run `mvn clean install` before PR.
3. **Tests**: Add/extend unit and integration tests where possible.
4. **Commit messages**: Use [Conventional Commits](https://www.conventionalcommits.org/).
5. **Pull Requests**: Keep them small and focused; link related issues.


## Development Setup
- Java 21+
- Maven 3.9+
- Docker (for Keycloak + example RP)


```bash
# Build the plugin
mvn clean install


# Run the dev environment
docker compose up
```
## Reporting Issues

Use [GitHub Issues](../../issues) with clear steps to reproduce, expected vs actual behavior, and logs if possible. Please include environment details (Keycloak version, plugin version, Java version, OS). Screenshots or logs are highly appreciated.

## Community
- Discussions: [GitHub Discussions](../../discussions)
- Security issues: report privately (see [SECURITY_POLICY.md](SECURITY_POLICY.md).

---
