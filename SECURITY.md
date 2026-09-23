# Security Policy

This policy applies to every repository in the Lodestar Security organization unless a repository provides its own `SECURITY.md`.

## Reporting a vulnerability

**Please do not report security vulnerabilities through public issues, discussions, or pull requests.**

Report privately through GitHub:

1. Open the affected repository.
2. Go to **Security → Advisories → Report a vulnerability**.
3. Include as much of the following as you can:
   - Affected product, version, or commit
   - Type of issue (e.g. injection, authentication bypass, supply-chain)
   - Steps to reproduce, or a proof of concept
   - Impact — what an attacker could achieve
   - Any suggested mitigation

## What to expect

| Stage | Target |
|---|---|
| Acknowledgement of your report | 3 business days |
| Initial triage and severity assessment (CVSS v4) | 7 days |
| Fix released — Critical | 30 days |
| Fix released — High | 60 days |
| Fix released — Medium / Low | Next planned release |

We will keep you informed throughout, and credit you in the advisory unless you prefer to remain anonymous.

## Coordinated disclosure

We follow coordinated disclosure with a default window of **90 days** from the initial report. If a fix ships earlier, we publish the advisory when the fix is available. If we need longer, we will explain why and agree on a new date with you.

## Supported versions

Only the latest minor release of each product receives security fixes, unless a product's own `SECURITY.md` states otherwise.

## Safe harbor

We will not pursue legal action against researchers who:

- Make a good-faith effort to avoid privacy violations, data destruction, and service disruption
- Only test against their own deployments, never against third-party systems
- Give us reasonable time to respond before any public disclosure

## Out of scope

- Vulnerabilities in third-party dependencies that are already publicly known — please report those upstream
- Findings from automated scanners without a demonstrated impact
- Social engineering of maintainers or contributors
