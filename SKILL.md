# Swift Accessibility Agent Skill

Use this skill to enforce source-driven accessibility guidance for SwiftUI and UIKit work.

## Canonical Inputs

- Source registry: `docs/core/sources/registry.md`
- Technology map: `docs/core/technology-map.md`
- Semantics taxonomy: `docs/core/taxonomy/semantics-checklist.md`
- Guideline template: `docs/core/templates/guideline-template.md`
- SwiftUI guidelines: `docs/swiftui/guidelines/`
- UIKit backlog: `docs/uikit/guidelines/topic-backlog.md`
- Testing artifacts: `docs/testing/`

## Agent Rules

1. Prefer Tier-1 Apple sources for platform truth.
2. Require at least 2 citations for any new or edited guideline, including at least 1 Tier-1 source.
3. Distinguish platform truth (Apple) from implementation practice (community).
4. Include an explicit verification method for each guideline:
   - Accessibility Inspector checks
   - VoiceOver walkthrough
   - Optional XCUITest hook where applicable
5. Preserve and validate semantics when changing UI:
   - Label
   - Value
   - Hint
   - Role/Traits
   - Actions
6. When interop is present (`UIHostingController`, representables, UIKit containers), include interop risk notes and on-device validation.

## Output Contract For New Guidelines

Every guideline must include:

- Problem statement
- Testable rule
- Rationale
- SwiftUI implementation notes
- UIKit interop notes
- Testing section (Inspector + VoiceOver minimum)
- Do/Don't examples
- Citations
- Metadata (`Status`, `Last Reviewed`, `Last Verified`, `Platforms`, `Confidence`)

## Review Gate

A guideline is review-ready only when:

- Citations meet project quality rules.
- Testing steps are executable by a reviewer.
- Metadata is current.
