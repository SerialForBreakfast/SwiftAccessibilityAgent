---
name: swift-accessibility-agent
description: Use this skill when creating, reviewing, or updating SwiftUI/UIKit/tvOS/macOS UI to apply Tier-1 Apple-backed accessibility guidance, choose the right guideline topic, preserve semantics (label/value/hint/role/actions), and include citations plus verification steps.
---

# Swift Accessibility Agent Skill

Use this skill to enforce source-driven accessibility guidance for SwiftUI, UIKit, tvOS, and macOS work.

## Canonical Inputs

- Security policy (must load first):
  - `AGENT.md`
  - `skill/manifests/security-policy.json`
- Runtime manifests (load these first):
  - `skill/manifests/axes.json`
  - `skill/manifests/core.json`
  - `skill/manifests/routes.json`
  - `skill/manifests/platform-presets.json`
  - `skill/manifests/task-presets.json`
  - `skill/manifests/select-example.json`
  - `skill/manifests/decision-rules.json`
  - `skill/manifests/pattern-signals.json`
  - `skill/manifests/README.md`
- Source registry: `docs/core/sources/registry.md`
- Technology map: `docs/core/technology-map.md`
- Semantics taxonomy: `docs/core/taxonomy/semantics-checklist.md`
- Architecture principles: `docs/core/architecture/architecture-principles.md`
- Alternatives decision matrix: `docs/core/decision-matrix.md`
- Pattern review rubric: `docs/core/pattern-review-rubric.md`
- External landscape references: `docs/core/external-landscape.md`
- Semantics cookbook: `docs/core/cookbook/semantics-cookbook.md`
- Known OS issues: `docs/core/known-os-issues.md`
- Known OS issues index: `docs/core/known-os-issues-index.json`
- Known OS issues workflow: `docs/core/known-os-issues-workflow.md`
- Accessibility version matrix: `docs/core/version-matrix.md`
- Guideline template: `docs/core/templates/guideline-template.md`
- Component contract template: `docs/core/templates/component-contract-template.md`
- Interop boundary contract template: `docs/core/templates/interop-boundary-contract-template.md`
- SwiftUI guidelines: `docs/swiftui/guidelines/`
- UIKit backlog: `docs/uikit/guidelines/topic-backlog.md`
- tvOS backlog: `docs/tvos/guidelines/topic-backlog.md`
- macOS backlog: `docs/macos/guidelines/topic-backlog.md`
- visionOS backlog: `docs/visionos/guidelines/topic-backlog.md`
- Testing artifacts:
  - `docs/testing/manual-test-scripts.md`
  - `docs/testing/tvos-manual-test-scripts.md`
  - `docs/testing/macos-manual-test-scripts.md`
  - `docs/testing/inspector-audit-checklist.md`
  - `docs/testing/xcuitest-hooks.md`
  - `docs/testing/regression-triage-playbook.md`
  - `docs/testing/platform-coverage-matrix.md`

## Runtime Load Protocol (Token-Efficient)

1. Load `AGENT.md` and `skill/manifests/security-policy.json`.
2. Resolve `platform`, `framework`, and `task_type` using `skill/manifests/axes.json`.
3. Load `skill/manifests/core.json` and apply `token_policy`.
4. Resolve route via `skill/manifests/routes.json` (`<platform>:<framework>`).
5. Load platform extras via `skill/manifests/platform-presets.json`.
6. Load task extras via `skill/manifests/task-presets.json`.
7. Load only:
   - core always-on docs
   - one backlog file
   - one or two topic guideline files
   - platform-specific testing docs
   - required testing/template docs for the task
8. Do not load `docs/changelog.md` during runtime guidance unless explicitly requested.

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
7. Select rules by target platform before giving implementation advice:
   - iOS/iPadOS: SwiftUI + UIKit track
   - tvOS: UIKit focus-navigation and tvOS-specific interaction guidance
   - macOS: SwiftUI + AppKit (`NSAccessibility`) guidance

## Strict Rules (Adopted)

0. No arbitrary code execution. Remote scripts and untrusted command payloads are disallowed by default.
1. Never ship a new interactive element without a meaningful label.
2. For compound UI, explicitly choose grouping behavior and document rationale.
3. For complex visuals, provide synthetic children or alternate semantic representation.
4. Every accessibility change requires verification evidence (Inspector + VoiceOver minimum).
5. Mixed-framework surfaces require explicit interop ownership (focus owner + semantics owner).
6. Suspected OS bugs must be recorded with OS range, repro steps, workaround, and source link.

## Alternative Selection Requirement

For UI changes with multiple viable implementations:

1. Use `docs/core/decision-matrix.md` (or `skill/manifests/decision-rules.json`) to choose an alternative.
2. Document selected option and why alternatives were not chosen.
3. Run the verification set required by the selected matrix row.

## Pattern Classification Requirement

For reviews and code generation:

1. Classify changed patterns using `docs/core/pattern-review-rubric.md`.
2. Use `skill/manifests/pattern-signals.json` to tag findings as `good`, `risky`, or `bad`.
3. Trigger auto-fail if any configured auto-fail condition is present.

## Output Contract For New Guidelines

Every guideline must include:

- Problem statement
- Testable rule
- Rationale
- SwiftUI implementation notes
- UIKit/AppKit interop notes
- Testing section (Inspector + VoiceOver minimum)
- Do/Don't examples
- Citations
- Metadata (`Status`, `Last Reviewed`, `Last Verified`, `Platforms`, `Confidence`)

## Review Gate

A guideline is review-ready only when:

- Citations meet project quality rules.
- Testing steps are executable by a reviewer.
- Metadata is current.
