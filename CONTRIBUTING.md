# Contributing to Lodestar Security

Thanks for your interest in contributing. This guide applies to every repository in the organization unless a repository provides its own `CONTRIBUTING.md`.

## Before you start

- **Security issues** go through the [security policy](SECURITY.md), never public issues.
- **Bugs and small fixes** — open an issue or go straight to a pull request.
- **New features or behavior changes** — open an issue first so we can agree on the approach before you invest time.
- **Architectural changes** — propose an Architecture Decision Record (ADR) in `docs/adr/` as part of the pull request.

## Workflow

1. Fork the repository and create a branch from `main`:
   `feat/short-description`, `fix/short-description`, or `docs/short-description`.
2. Make focused changes — one logical change per pull request.
3. Add or update tests. Pull requests that change behavior without tests will not be merged.
4. Update documentation affected by the change.
5. Open a pull request using the template and link the related issue.

## Commit messages and PR titles

We use [Conventional Commits](https://www.conventionalcommits.org/). Pull request titles are validated automatically and become the squash-merge commit message.

```
feat(gates): add SBOM attestation step
fix(hub): de-duplicate findings with identical fingerprints
docs: clarify exception expiry behavior
```

Allowed types: `feat`, `fix`, `docs`, `refactor`, `perf`, `test`, `build`, `ci`, `chore`, `revert`.
Mark breaking changes with `!` (e.g. `feat!:`) and describe the migration in the PR.

## Quality bar

A pull request is ready for review when:

- [ ] All CI checks pass, including the security baseline
- [ ] New code has tests; coverage does not decrease
- [ ] No new secrets, credentials, or internal hostnames are introduced
- [ ] New dependencies are justified in the PR description
- [ ] GitHub Actions are pinned to a full commit SHA
- [ ] Documentation and `CHANGELOG.md` are updated where relevant

## Signed commits

Signed commits (GPG, SSH, or Sigstore Gitsign) are strongly encouraged and may be required on protected branches.

## Code of conduct

By participating, you agree to follow our [Code of Conduct](CODE_OF_CONDUCT.md).
