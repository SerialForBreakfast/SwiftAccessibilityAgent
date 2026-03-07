# SwiftAccessibilityAgent

Source-driven accessibility guidance for SwiftUI and UIKit, designed for both human developers and AI coding agents.

## Repo Model

- `docs/core/`: shared truth used by all tracks (sources, taxonomy, template, technology map).
- `docs/swiftui/`: SwiftUI-specific guidance and backlog.
- `docs/uikit/`: UIKit-specific guidance and backlog.

Teams can consume one track at a time (`swiftui` or `uikit`) while still inheriting shared `core` standards.

## Project Status

- Workstreams `A` through `G` are complete in `Tasks.txt`.
- SwiftUI guideline set (`G-001` to `G-015`) is accepted.
- UIKit guideline set (`U-001` to `U-015`) is accepted.
- Topic backlogs use tier-based evidence fields (`acceptance_status`, `review_evidence`, `citation_tiers`).

## Current Deliverables

- Source registry: `docs/core/sources/registry.md`
- Technology map: `docs/core/technology-map.md`
- Semantics taxonomy: `docs/core/taxonomy/semantics-checklist.md`
- Guideline template: `docs/core/templates/guideline-template.md`
- SwiftUI topic backlog: `docs/swiftui/guidelines/topic-backlog.md`
- SwiftUI guideline set: `docs/swiftui/guidelines/`
- UIKit topic backlog: `docs/uikit/guidelines/topic-backlog.md`
- UIKit guideline set: `docs/uikit/guidelines/`
- Testing artifacts: `docs/testing/`
- Agent package: `SKILL.md`
- Project changelog: `docs/changelog.md`
- Planning backlog: `Tasks.txt`

## Usage

For agent or reviewer workflows:

1. Start with track backlog (`docs/swiftui/guidelines/topic-backlog.md` or `docs/uikit/guidelines/topic-backlog.md`).
2. Open the linked guideline file for implementation rules and citations.
3. Use `docs/testing/` artifacts for verification planning.
4. Follow `SKILL.md` as the agent-facing contract.

## License

This project is open-source and available under the MIT License. See `LICENSE` for details.
