# Sakura Secrets

Sakura Secrets is a Free and Open Source Software (FOSS), developer‑first secret & credential scanner focused on fast feedback during everyday coding (local edits, pre‑commit, pull requests) and clear triage (via an optional interactive terminal UI).

## Vision (What It Aims To Become)

A lightweight, extensible FOSS engine that helps developers catch accidental exposure of API keys, tokens, private key blocks and other sensitive values as early as possible—before they enter permanent history or production systems.

## Core Principles

1. Developer Experience First  
   Fast to run, easy to integrate, minimal friction.

2. Signal Over Noise  
   Reduce false positives via contextual patterns, entropy tuning, and optional baseline suppression of legacy findings.

3. Transparency, Openness & Extensibility  
   Apache 2.0 licensed. Human‑readable rule definitions (YAML/regex) + documented heuristics so teams can extend confidently.

4. Progressive Adoption  
   Start manual → add pre‑commit → add CI gate → optionally interactive TUI for deeper triage.

5. Community & Trust  
   Clear code layout, reproducible logic, and openness to external rule packs and improvements.

## FOSS Commitment

- Core engine is and will remain Free and Open Source under Apache License 2.0.  
- Public, auditable rule definitions — no opaque “black box” scoring.  
- Modular design so others can reuse components (rules, detectors, output adapters).  
- Any future “open‑core” style additions (if they occur) will not revoke freedoms granted by the current core license.

## Planned High‑Level Capabilities (Future)

- Curated regex rule set (cloud keys, generic tokens, private key markers)  
- Entropy scoring for high‑variance secrets  
- Baseline mechanism to suppress historical/accepted findings (focus on new leaks)  
- Git‑aware modes (changed files / staged only)  
- Output formats: human table, JSON, later SARIF  
- Interactive Bubble Tea TUI: streaming findings, filtering, context inspection, baseline actions  
- Severity tagging + configurable CI fail threshold  
- Extensible rule packs (cloud, framework, org‑specific)  

(Prospective; not guaranteed until implemented.)

## Non‑Goals (Initial Phase)

- Active outbound validation of secrets against provider APIs  
- Deep binary or archive extraction scanning  
- ML‑heavy classification (initial focus = deterministic + heuristic)  
- Hosted backend / centralized cloud service (early versions are local‑only)

## Status

Early concept / scaffold stage. Expect rapid iteration and possible reorganization before the first tagged release.

## Project Rationale

Existing secret scanners can be noisy, opaque, or less friendly for iterative local workflows. Sakura Secrets aims to:
- Provide an ergonomic, interactive triage option without sacrificing scriptability
- Maintain a clean separation between detection engine, rules, and presentation
- Serve as an educational, auditable reference implementation

## Guiding User Story (Future)

“As a developer, I want to scan only the files I changed and, if something triggers, instantly review context and decide to fix, ignore, or baseline it—without drowning in historical noise.”

## Roadmap Style (Directional, Not a Contract)

1. Minimal data models (Finding, Rule, Severity)  
2. Simple file walker + placeholder rule  
3. Configurable regex ruleset  
4. Entropy heuristic & false‑positive safeguards  
5. Baseline persistence  
6. Git diff / staged modes  
7. JSON output + severity gating  
8. Initial TUI (stream findings)  
9. TUI filtering & context panes  
10. SARIF output + CI examples  

## Contributing

Contribution guidelines, code of conduct, security policy, and rule style guide will be published once a functional prototype exists. Until then, early design feedback is welcome after issue tracking opens.

## License

Licensed under the Apache License 2.0.  
Why Apache 2.0? Broad adoption, explicit patent grant, compatibility with future ecosystem extensions, and a permissive stance that encourages community innovation.

See [LICENSE](./LICENSE).

## Disclaimer

Not production ready. Do not rely on current state for real secret detection until a documented release is published.

---

_“Shift‑left security should feel native, not noisy — and it should stay Free and Open Source.”_  
— Sakura Secrets