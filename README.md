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

Project-local Codex install:

```bash
npx skills add https://github.com/SerialForBreakfast/SwiftAccessibilityAgent --skill swift-accessibility-agent --agent codex --yes
```

Global Codex install:

```bash
npx skills add https://github.com/SerialForBreakfast/SwiftAccessibilityAgent --skill swift-accessibility-agent --agent codex --global --yes
```

### Verify Installation

```bash
find .agents/skills ~/.codex/skills -maxdepth 2 -name SKILL.md 2>/dev/null | grep swift-accessibility-agent
```

Expected installed path (global):

```text
~/.codex/skills/swift-accessibility-agent/SKILL.md
```

Expected installed path (project-local):

```text
./.agents/skills/swift-accessibility-agent/SKILL.md
```

If the skill does not appear in the active session skill list, refresh or restart the Codex session.

## Quick Start

1. Pick a platform/framework track:
- `references/swiftui/`
- `references/uikit/`
- `references/tvos/`
- `references/macos/`
- `references/visionos/`

2. Load shared core guidance:
- `references/core/sources/registry.md`
- `references/core/technology-map.md`
- `references/core/taxonomy/semantics-checklist.md`

3. Apply guideline + testing artifacts relevant to your change.

## Core Documents

- Security policy: `AGENT.md`
- Agent operating contract: `SKILL.md`
- UI metadata: `agents/openai.yaml`
- Runtime manifests: `references/manifests/`
- Source registry: `references/core/sources/registry.md`
- Architecture principles: `references/core/architecture/architecture-principles.md`
- Decision matrix: `references/core/decision-matrix.md`
- Pattern review rubric: `references/core/pattern-review-rubric.md`
- External landscape references: `references/core/external-landscape.md`
- Semantics cookbook: `references/core/cookbook/semantics-cookbook.md`
- Known issues catalog: `references/core/known-os-issues.md`
- Version matrix: `references/core/version-matrix.md`
- Testing artifacts: `references/testing/`

## Using With AI Agents

1. Load `AGENT.md` first.
2. Load `SKILL.md`.
3. Choose task workflow from `SKILL.md` first (review, improve, implement).
4. Resolve runtime selection through `references/manifests/` (`platform`, `framework`, `task_type`) only as needed.
5. Load only resolved docs and required verification artifacts.

## Validation Checklist

- `SKILL.md` exists at installed skill root.
- `agents/openai.yaml` exists.
- Manifest and reference paths in `SKILL.md` resolve.
- Skill appears in session available skills list.
- Skill triggers by name: `swift-accessibility-agent`.

## Source Governance

- Tier-1: Apple platform truth
- Tier-2: High-quality implementation references
- Tier-3: Discovery/context only
- If sources conflict, Tier-1 wins

## License

MIT. See `LICENSE`.
