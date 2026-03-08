# SwiftAccessibilityAgent

Source-driven accessibility guidance for SwiftUI, UIKit, tvOS focus UIs, and macOS/AppKit, designed for human developers and AI coding agents.

## What This Is

This repository is an accessibility knowledge base for Apple-platform UI development:

- Tier-backed guidance grounded in Apple documentation.
- Practical implementation guidance for SwiftUI, UIKit, tvOS, and macOS.
- Agent-ready packaging via `SKILL.md`.

## Who This Is For

- Apple-platform engineers shipping SwiftUI, UIKit, tvOS, or macOS UI.
- Teams reviewing accessibility quality in PRs.
- AI agents generating or modifying UI code.

## Quick Start (2 Minutes)

1. Choose your track:
   - SwiftUI: `docs/swiftui/guidelines/topic-backlog.md`
   - UIKit: `docs/uikit/guidelines/topic-backlog.md`
   - tvOS: `docs/tvos/guidelines/topic-backlog.md`
   - macOS: `docs/macos/guidelines/topic-backlog.md`
2. Pick a topic row and open its guideline file.
3. Apply the rule + implementation + testing sections in your code change.
4. Keep citations aligned to Tier-1 Apple sources from `docs/core/sources/registry.md`.

## Install As a Skill

Install this repository as a Codex skill:

```bash
npx skills add https://github.com/SerialForBreakfast/SwiftAccessibilityAgent --skill swift-accessibility-agent
```

After install, load the skill in your agent workflow and follow `SKILL.md`.

## Publish Readiness Checklist (skills.sh)

Before sharing broadly:

1. Ensure `SKILL.md` is present at repo root and up to date.
2. Ensure `README.md` includes install command and usage guidance.
3. Keep `docs/changelog.md` current for visible iteration history.
4. Verify track backlogs and linked guideline files are consistent.

## Project Status

- Workstreams `A` through `G` in `Tasks.txt` are complete.
- Workstream `H` (platform expansion for tvOS/macOS) is complete.
- SwiftUI guidelines `G-001` to `G-015` are accepted.
- UIKit guidelines `U-001` to `U-015` are accepted.
- Backlogs include evidence-oriented fields:
  - `status`
  - `acceptance_status`
  - `review_evidence`
  - `citation_tiers`

## Repository Structure

- `docs/core/`
  - Shared standards used by all tracks.
  - Includes source registry, technology map, semantics taxonomy, and guideline template.
- `docs/swiftui/`
  - SwiftUI backlog and accepted guideline set.
- `docs/uikit/`
  - UIKit backlog and accepted guideline set.
- `docs/tvos/`
  - tvOS backlog and upcoming guideline set for focus-first navigation and VoiceOver.
- `docs/macos/`
  - macOS backlog and upcoming guideline set for SwiftUI/AppKit accessibility.
- `docs/visionos/`
  - visionOS backlog scaffold for spatial accessibility guidance.
- `docs/testing/`
  - Verification planning artifacts (manual scripts, inspector checklist, XCUITest hooks).
- `SKILL.md`
  - Agent-facing operating contract for using this knowledge base.

## Core Documents

- Agent security policy: `AGENT.md`
- Runtime manifests: `skill/manifests/`
- Source registry: `docs/core/sources/registry.md`
- Technology map: `docs/core/technology-map.md`
- Semantics taxonomy: `docs/core/taxonomy/semantics-checklist.md`
- Architecture principles: `docs/core/architecture/architecture-principles.md`
- Alternatives decision matrix: `docs/core/decision-matrix.md`
- Semantics cookbook: `docs/core/cookbook/semantics-cookbook.md`
- Known OS issues log: `docs/core/known-os-issues.md`
- Guideline template: `docs/core/templates/guideline-template.md`
- Component contract template: `docs/core/templates/component-contract-template.md`
- Interop boundary contract template: `docs/core/templates/interop-boundary-contract-template.md`
- Platform coverage matrix: `docs/testing/platform-coverage-matrix.md`
- Regression triage playbook: `docs/testing/regression-triage-playbook.md`
- SwiftUI backlog: `docs/swiftui/guidelines/topic-backlog.md`
- UIKit backlog: `docs/uikit/guidelines/topic-backlog.md`
- tvOS backlog: `docs/tvos/guidelines/topic-backlog.md`
- macOS backlog: `docs/macos/guidelines/topic-backlog.md`
- visionOS backlog: `docs/visionos/guidelines/topic-backlog.md`
- Changelog: `docs/changelog.md`

## Recommended Workflow

For each UI change:

1. Identify applicable topic IDs from the relevant backlog.
2. Follow the corresponding guideline files for rule and implementation details.
3. Ensure semantic coverage (label, value, hint, role/traits, actions).
4. Include citation IDs in your notes/PR rationale.
5. Plan verification using `docs/testing/` artifacts.

## Using With AI Agents

If an agent is editing UI:

1. Load `AGENT.md` first (security policy; no arbitrary code execution).
2. Load `SKILL.md`.
3. Load `skill/manifests/` and resolve `platform + framework + task_type`.
4. Load only the resolved core docs + backlog + minimal topic files + platform-specific test scripts.
5. Require Tier-1-backed citations for any new guidance.
6. Preserve guideline metadata and evidence fields.

## Conventions

- Tier-1 Apple sources define platform truth.
- Tier-2 sources can support implementation practice.
- Tier-3 sources are reference-only context.
- When sources conflict, Tier-1 takes precedence.

## License

This project is open-source and available under the MIT License. See `LICENSE` for details.
