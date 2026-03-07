# Changelog

All notable changes to this documentation project are tracked here.

## [Unreleased]

### Added

- `docs/testing/manual-test-scripts.md`
- `docs/testing/inspector-audit-checklist.md`
- `docs/testing/xcuitest-hooks.md`
- `SKILL.md` agent packaging document.
- UIKit P0 guideline drafts:
  - `docs/uikit/guidelines/u-001-labels-meaningful-names.md`
  - `docs/uikit/guidelines/u-002-hints-when-to-use.md`
  - `docs/uikit/guidelines/u-003-values-stateful-controls.md`
  - `docs/uikit/guidelines/u-004-traits-roles.md`
  - `docs/uikit/guidelines/u-005-grouping-containment.md`
  - `docs/uikit/guidelines/u-006-focus-reading-order.md`
  - `docs/uikit/guidelines/u-010-dynamic-type-layout-resilience.md`
  - `docs/uikit/guidelines/u-011-color-contrast-non-color-cues.md`
- UIKit remaining guideline drafts:
  - `docs/uikit/guidelines/u-007-accessibility-custom-actions.md`
  - `docs/uikit/guidelines/u-008-custom-controls-semantic-equivalence.md`
  - `docs/uikit/guidelines/u-009-rotor-friendly-structure.md`
  - `docs/uikit/guidelines/u-012-reduced-motion.md`
  - `docs/uikit/guidelines/u-013-modal-focus-containment.md`
  - `docs/uikit/guidelines/u-014-table-collection-form-semantics.md`
  - `docs/uikit/guidelines/u-015-media-captions-descriptions-controls.md`

### Changed

- Corrected SwiftUI backlog guideline paths and core reference links in `docs/swiftui/guidelines/topic-backlog.md`.
- Updated UIKit backlog statuses and file links for drafted P0 topics in `docs/uikit/guidelines/topic-backlog.md`.
- Completed structured guideline QA pass across SwiftUI and UIKit sets (sections, metadata, citation counts, and source-ID integrity).
- Strengthened reviewer execution readiness in `docs/testing/manual-test-scripts.md` with preconditions and minimum PR evidence requirements.
- Expanded `SKILL.md` canonical inputs to reference explicit testing artifact files.
- Added actionable stale-source downgrade workflow to `docs/core/sources/registry.md`.
- Marked core workstreams A/B/C as complete in `Tasks.txt` after artifact and consistency verification scans.
- Added `acceptance_status` and `review_evidence` tracking columns to SwiftUI and UIKit topic backlogs using tier-based positive evidence language, and marked topics as `Tier-Validated`.
- Promoted all SwiftUI and UIKit guidelines to `Status: Accepted` and aligned backlog `status`/`acceptance_status` entries to `Accepted`.
