<p align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=soft&color=0:0b1e4d,60:1e40af,100:22d3ee&height=160&section=header&text=Lodestar%20Security&fontSize=48&fontColor=ffffff&fontAlignY=42&desc=Secure%20delivery%2C%20by%20default.&descSize=18&descAlignY=68" alt="Lodestar Security"/>
</p>

<p align="center">
  Open-source DevSecOps services, each built the way enterprise software should be — <b>requirements first</b>, <b>threat-modeled</b>, and <b>proven by CI/CD on every change</b>.
</p>

---

### Why Lodestar

A lodestar is the star navigators steer by. Security teams should play the same role: set a clear direction, then make the secure path the easiest path for engineers.

Each product here is an independent service that solves one problem security and platform teams face every day — built from scratch, with its own stack chosen from its own requirements.

### Products

| Product | Problem it solves | Status |
|---|---|---|
| **risk-exception-registry** | Security exceptions live in spreadsheets and never expire. A workflow to request, approve, expire, and audit risk acceptances — with an immutable audit trail. | Planned |
| **vuln-sla-tracker** | Findings from many scanners, no ownership, no deadlines. De-duplicates findings, prioritizes by EPSS and CISA KEV, assigns owners, and tracks remediation SLAs. | Planned |
| **sbom-inventory** | "A new CVE just dropped — which of our services are affected?" Ingests CycloneDX/SPDX SBOMs and answers that in seconds. | Planned |
| **compliance-evidence** | Audit season means screenshots. Continuously collects control evidence (branch protection, reviews, 2FA) and maps it to CIS / ISO 27001 controls. | Planned |
| **secret-inventory** | Nobody knows where secrets live or when they were last rotated. Tracks location, owner, and rotation age — never the secret values. | Planned |

### How we build

Every product goes through the same phase-gated lifecycle — no phase starts before the previous gate is passed:

`Charter → Requirements → Technology selection → Architecture → Data design → Threat model → Walking skeleton → Delivery → Verification → Operations`

- **Requirements first, technology second** — language, framework, and database are chosen with a weighted evaluation and recorded as ADRs.
- **Rigorous data design** — 3NF with justified deviations, business rules enforced in the database, an index for every core query, least-privilege database roles.
- **Threat-modeled** — every product ships a STRIDE threat model and security requirements mapped to OWASP ASVS Level 2.
- **Proven on every change** — every pull request deploys to an ephemeral Kubernetes cluster and passes Helm tests and a DAST scan before it can merge.
- **Supply-chain hardened** — actions pinned to commit SHAs, multi-arch images signed with Cosign, SBOM and SLSA provenance attestations, releases re-verified in a cluster that rejects unsigned images.

### Contributing & security

- Contributions are welcome — start with the [contributing guide](https://github.com/Lodestar-sec/.github/blob/main/CONTRIBUTING.md).
- Found a vulnerability? Please **do not open a public issue**. Follow our [security policy](https://github.com/Lodestar-sec/.github/blob/main/SECURITY.md).

<p align="center"><sub>Maintained by <a href="https://github.com/Lewall-theart">@Lewall-theart</a></sub></p>
