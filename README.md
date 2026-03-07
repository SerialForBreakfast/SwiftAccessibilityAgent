# SwiftAccessibilityAgent

Source-driven accessibility guidance for SwiftUI and UIKit, designed for human developers and AI coding agents.

## What This Is

This repository is an accessibility knowledge base for iOS UI development:

- Tier-backed guidance grounded in Apple documentation.
- Practical implementation guidance for SwiftUI and UIKit.
- Agent-ready packaging via `SKILL.md`.

## Who This Is For

- iOS engineers shipping SwiftUI or UIKit UI.
- Teams reviewing accessibility quality in PRs.
- AI agents generating or modifying UI code.

## Quick Start (2 Minutes)

1. Choose your track:
   - SwiftUI: `docs/swiftui/guidelines/topic-backlog.md`
   - UIKit: `docs/uikit/guidelines/topic-backlog.md`
2. Pick a topic row and open its guideline file.
3. Apply the rule + implementation + testing sections in your code change.
4. Keep citations aligned to Tier-1 Apple sources from `docs/core/sources/registry.md`.

## Project Status

- Workstreams `A` through `G` in `Tasks.txt` are complete.
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
- `docs/testing/`
  - Verification planning artifacts (manual scripts, inspector checklist, XCUITest hooks).
- `SKILL.md`
  - Agent-facing operating contract for using this knowledge base.

## Core Documents

- Source registry: `docs/core/sources/registry.md`
- Technology map: `docs/core/technology-map.md`
- Semantics taxonomy: `docs/core/taxonomy/semantics-checklist.md`
- Guideline template: `docs/core/templates/guideline-template.md`
- SwiftUI backlog: `docs/swiftui/guidelines/topic-backlog.md`
- UIKit backlog: `docs/uikit/guidelines/topic-backlog.md`
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

1. Load `SKILL.md`.
2. Load `docs/core/sources/registry.md`.
3. Load the relevant track backlog and guideline files.
4. Require Tier-1-backed citations for any new guidance.
5. Preserve guideline metadata and evidence fields.

## Conventions

- Tier-1 Apple sources define platform truth.
- Tier-2 sources can support implementation practice.
- Tier-3 sources are reference-only context.
- When sources conflict, Tier-1 takes precedence.

## License

This project is open-source and available under the MIT License. See `LICENSE` for details.
