# SwiftAccessibilityAgent

Source-driven accessibility guidance for SwiftUI, UIKit, tvOS, macOS, and visionOS, designed for both human developers and AI coding agents.

## What This Is

SwiftAccessibilityAgent is a documentation-first accessibility knowledge base for Apple-platform UI development.

It provides:
- Tiered source governance (Apple-first platform truth)
- Implementation guidance for SwiftUI/UIKit/AppKit and interop boundaries
- Testing and regression-triage workflows
- Agent-ready manifests and runtime loading rules

## Who This Is For

- Engineers building Apple-platform UI
- Teams running accessibility-focused PR reviews
- AI agents generating or modifying UI code

## Install As a Skill

```bash
npx skills add https://github.com/SerialForBreakfast/SwiftAccessibilityAgent --skill swift-accessibility-agent
```

Then load `SKILL.md` in your agent workflow.

## Quick Start

1. Pick a platform/framework track:
- `docs/swiftui/`
- `docs/uikit/`
- `docs/tvos/`
- `docs/macos/`
- `docs/visionos/`

2. Load shared core guidance:
- `docs/core/sources/registry.md`
- `docs/core/technology-map.md`
- `docs/core/taxonomy/semantics-checklist.md`

3. Apply guideline + testing artifacts relevant to your change.

## Core Documents

- Security policy: `AGENT.md`
- Agent operating contract: `SKILL.md`
- Runtime manifests: `skill/manifests/`
- Source registry: `docs/core/sources/registry.md`
- Architecture principles: `docs/core/architecture/architecture-principles.md`
- Decision matrix: `docs/core/decision-matrix.md`
- Pattern review rubric: `docs/core/pattern-review-rubric.md`
- External landscape references: `docs/core/external-landscape.md`
- Semantics cookbook: `docs/core/cookbook/semantics-cookbook.md`
- Known OS issues log: `docs/core/known-os-issues.md`
- Accessibility version matrix: `docs/core/version-matrix.md`
- Guideline template: `docs/core/templates/guideline-template.md`
- Component contract template: `docs/core/templates/component-contract-template.md`
- Interop boundary contract template: `docs/core/templates/interop-boundary-contract-template.md`
- Platform coverage matrix: `docs/testing/platform-coverage-matrix.md`
- Regression triage playbook: `docs/testing/regression-triage-playbook.md`
- Known issues catalog: `docs/core/known-os-issues.md`
- Version matrix: `docs/core/version-matrix.md`
- Testing artifacts: `docs/testing/`

## Using With AI Agents

1. Load `AGENT.md` first.
2. Load `SKILL.md`.
3. Resolve runtime selection through `skill/manifests/` (`platform`, `framework`, `task_type`).
4. Load only resolved docs and required verification artifacts.

## Source Governance

- Tier-1: Apple platform truth
- Tier-2: High-quality implementation references
- Tier-3: Discovery/context only
- If sources conflict, Tier-1 wins

## License

MIT. See `LICENSE`.
