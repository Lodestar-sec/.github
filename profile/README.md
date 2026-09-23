<p align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=soft&color=0:0b1e4d,60:1e40af,100:22d3ee&height=160&section=header&text=Lodestar%20Security&fontSize=48&fontColor=ffffff&fontAlignY=42&desc=Secure%20delivery%2C%20by%20default.&descSize=18&descAlignY=68" alt="Lodestar Security"/>
</p>

<p align="center">
  Open-source tooling where <b>binary security</b> meets <b>DevSecOps</b> — exploit mitigations, crash analysis, and binary insight, enforced in CI/CD.
</p>

---

### Why Lodestar

A lodestar is the star navigators steer by. Security teams should play the same role: set a clear direction, then make the secure path the easiest path for engineers.

Most pipelines scan source code and dependencies, then ship the compiled binary without looking at it. Yet the binary is what attackers actually exploit. We build tools that bring binary-level security — the knowledge of exploit developers and reverse engineers — into the delivery pipeline.

### Products

| Product | Problem it solves | Status |
|---|---|---|
| **Binary Hardening Gate** *(working title)* | A compiler, base-image, or build-flag change can silently strip PIE, RELRO, stack canaries, or CET/BTI from shipped binaries — and nobody notices until a memory-corruption bug becomes easy to exploit. Inspects every ELF in container images and release artifacts, enforces a hardening policy in CI, and catches regressions between releases. | Discovery |
| **Crash Triage** *(working title)* | Fuzzing in CI produces hundreds of duplicate crashes, and nobody knows which ones are exploitable. De-duplicates crashes, reproduces them in a sandbox, classifies exploitability, and bisects the commit that introduced them. | Planned |
| **Binary SBOM** *(working title)* | Statically linked C/C++ binaries carry no package metadata, so SBOM tools miss the libraries compiled into them — such as an outdated OpenSSL. Identifies embedded libraries and versions from the binary itself. | Research |

### How we build

Every product goes through the same phase-gated lifecycle — no phase starts before the previous gate is passed:

`Charter → Requirements → Technology selection → Architecture → Data design → Threat model → Walking skeleton → Delivery → Verification → Operations`

- **Evidence before code** — every product starts by measuring the problem in the wild, not by assuming it.
- **Requirements first, technology second** — language, framework, and database are chosen with a weighted evaluation and recorded as ADRs.
- **Verified against ground truth** — analysis engines are tested against corpora built with known compiler and linker settings.
- **Threat-modeled** — tools that parse untrusted binaries are themselves an attack surface; every product ships a STRIDE threat model and security requirements mapped to OWASP ASVS Level 2.
- **Supply-chain hardened** — actions pinned to commit SHAs, multi-arch images signed with Cosign, SBOM and SLSA provenance attestations, releases re-verified in a cluster that rejects unsigned images.

### Contributing & security

- Contributions are welcome — start with the [contributing guide](https://github.com/Lodestar-sec/.github/blob/main/CONTRIBUTING.md).
- Found a vulnerability? Please **do not open a public issue**. Follow our [security policy](https://github.com/Lodestar-sec/.github/blob/main/SECURITY.md).

<p align="center"><sub>Maintained by <a href="https://github.com/Lewall-theart">@Lewall-theart</a></sub></p>
