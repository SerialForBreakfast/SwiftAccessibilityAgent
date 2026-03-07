# Sources of Truth Registry

Last updated: 2026-03-07
Owner: SwiftUI Accessibility Agent project

## Registry Format

Each source entry must include:

- `source_id`: Stable short ID (for citations in guideline docs).
- `title`: Human-readable title.
- `url`: Canonical URL.
- `authority_tier`: Tier-1, Tier-2, or Tier-3.
- `last_reviewed`: Date reviewed for freshness.
- `scope`: What this source is used to validate.
- `notes`: Caveats, version context, or follow-ups.

## Authority Tiers

- Tier-1: Apple platform truth. Use as the baseline source for rules.
- Tier-2: High-quality community sources. Use for implementation practice and examples.
- Tier-3: Reference-only sources. Use with caution and always cross-check.

## Tier-1 Sources (Seed, Validated)

| source_id | title | url | authority_tier | last_reviewed | scope | notes |
|---|---|---|---|---|---|---|
| APPLE-SWIFTUI-ACCESSIBILITY | SwiftUI: Accessibility | https://developer.apple.com/documentation/swiftui/accessibility | Tier-1 | 2026-03-07 | SwiftUI accessibility APIs and modifiers | Primary SwiftUI accessibility API reference hub. |
| APPLE-VIEW-ACCESSIBILITY | Accessibility Modifiers (View Accessibility) | https://developer.apple.com/documentation/swiftui/view-accessibility | Tier-1 | 2026-03-07 | Modifier-level behavior for SwiftUI view semantics | Use for labels, values, hints, traits, actions, grouping, and sort priority guidance. |
| APPLE-CREATING-ACCESSIBLE-VIEWS | Enhancing the Accessibility of Your SwiftUI App | https://developer.apple.com/documentation/accessibility/enhancing-the-accessibility-of-your-swiftui-app | Tier-1 | 2026-03-07 | End-to-end SwiftUI accessibility implementation guidance | Canonical Apple implementation walkthrough. |
| APPLE-HIG-ACCESSIBILITY | Apple Human Interface Guidelines: Accessibility | https://developer.apple.com/design/human-interface-guidelines/accessibility | Tier-1 | 2026-03-07 | Product-level accessibility behavior expectations | Use for rationale and UX expectations. |
| APPLE-AX-HUB | Accessibility Documentation Hub | https://developer.apple.com/documentation/accessibility | Tier-1 | 2026-03-07 | Assistive technologies, testing resources, and broad guidance | Canonical docs hub URL (developer.apple.com/accessibility redirects here). |
| APPLE-AX-INSPECTOR | Accessibility Inspector | https://developer.apple.com/documentation/accessibility/accessibility-inspector | Tier-1 | 2026-03-07 | Tooling workflows and audit checks | Basis for enforceable verification steps. |
| APPLE-AX-TESTING | Performing Accessibility Testing for Your App | https://developer.apple.com/documentation/accessibility/performing-accessibility-testing-for-your-app | Tier-1 | 2026-03-07 | Manual and tool-assisted accessibility testing guidance | Use to define verification workflows. |
| APPLE-WWDC-AX-INDEX | WWDC Accessibility and Inclusion Sessions | https://developer.apple.com/videos/accessibility-inclusion/ | Tier-1 | 2026-03-07 | Session-driven updates and platform changes | Use as discovery index; cite specific sessions for rules. |
| APPLE-WWDC24-SWIFTUI | Catch Up on Accessibility in SwiftUI (WWDC24) | https://developer.apple.com/videos/play/wwdc2024/10073/ | Tier-1 | 2026-03-07 | SwiftUI semantics, modifiers, and interaction updates | High-value session for modern SwiftUI guidance. |
| APPLE-WWDC23-SWIFTUI-UIKIT | Build Accessible Apps with SwiftUI and UIKit (WWDC23) | https://developer.apple.com/videos/play/wwdc2023/10036/ | Tier-1 | 2026-03-07 | Interop guidance for mixed SwiftUI/UIKit apps | Anchor interop-focused guidelines. |
| APPLE-WWDC23-AUDITS | Perform Accessibility Audits for Your App (WWDC23) | https://developer.apple.com/videos/play/wwdc2023/10035/ | Tier-1 | 2026-03-07 | Practical auditing approach and tooling | Anchor Inspector/test-plan guidance. |
| ASC-ANL-OVERVIEW | App Store Connect: Overview of Accessibility Nutrition Labels | https://developer.apple.com/help/app-store-connect/manage-app-accessibility/overview-of-accessibility-nutrition-labels/ | Tier-1 | 2026-03-07 | Label feature definitions and policy framing | Use for feature-scope definitions and app-store reporting context. |
| ASC-ANL-MANAGE | App Store Connect: Manage Accessibility Nutrition Labels | https://developer.apple.com/help/app-store-connect/manage-app-accessibility/manage-accessibility-nutrition-labels/ | Tier-1 | 2026-03-07 | Operational guidance for declaring accessibility support | Use for process and maintenance checks. |

## Tier-2 Sources (Seed)

| source_id | title | url | authority_tier | last_reviewed | scope | notes |
|---|---|---|---|---|---|---|
| SWIFTLEE-A11Y | SwiftLee Accessibility Articles | https://www.avanderlee.com | Tier-2 | 2026-03-07 | Pragmatic Swift/SwiftUI techniques | Find and pin specific article URLs before citation in rules. |
| HWS-SWIFTUI-A11Y | Hacking with Swift: SwiftUI Accessibility | https://www.hackingwithswift.com | Tier-2 | 2026-03-07 | Practical examples and beginner-to-mid workflows | Must be anchored to Tier-1 when promoted to rules. |
| MAJID-A11Y | Swift with Majid: Accessibility Topics | https://swiftwithmajid.com | Tier-2 | 2026-03-07 | Advanced SwiftUI patterns (e.g., representations/rotors) | Pin exact posts in topic-specific docs. |
| USEYOURLOAF-A11Y | Use Your Loaf: Accessibility Updates | https://useyourloaf.com | Tier-2 | 2026-03-07 | API changes and migration notes | Confirm recency before relying on old modifiers. |
| CVS-SWIFTUI-A11Y-TECHNIQUES | CVS Health iOS SwiftUI Accessibility Techniques | https://github.com/cvs-health/ios-swiftui-accessibility-techniques | Tier-2 | 2026-03-07 | Open-source technique examples | Cross-reference each adopted pattern to Tier-1. |

## Tier-3 Sources (Seed)

| source_id | title | url | authority_tier | last_reviewed | scope | notes |
|---|---|---|---|---|---|---|
| COMMUNITY-CONFERENCE-SLIDES | Conference Slide Decks | N/A | Tier-3 | 2026-03-07 | Background context only | Do not cite as sole source for any rule. |
| COMMUNITY-VENDOR-BLOGS | Vendor Blogs | N/A | Tier-3 | 2026-03-07 | Supplemental examples | Require Tier-1 corroboration before adoption. |
| COMMUNITY-FORUM-POSTS | Community Posts/Threads | N/A | Tier-3 | 2026-03-07 | Edge-case discovery | Treat as anecdotal until validated. |

## Tiering Policy Notes

- Open-source repos can be Tier-2 when maintained and consistent with Apple guidance.
- Any repo-derived technique must map to at least one Tier-1 Apple source before it becomes a project rule.
- When Tier-1 and Tier-2 conflict, Tier-1 wins.

## Freshness Policy

- Apple docs: review quarterly and at each major iOS release.
- WWDC sources: review annually after WWDC season.
- Community sources: review annually and downgrade if stale.

## Stale-Source Downgrade Rules (Actionable)

Apply these rules during freshness review:

1. Trigger conditions:
   - `last_reviewed` exceeds freshness interval for source tier/type.
   - Link is dead, redirected to unrelated content, or materially changed.
   - Guidance conflicts with current Tier-1 Apple documentation.
2. Required actions:
   - Mark source notes with stale/conflict reason and review date.
   - Remove source from new guideline citations until revalidated.
   - If source is Tier-2 and remains stale after one review cycle, downgrade to Tier-3.
   - If source is irrecoverably outdated or unavailable, remove from registry.
3. Guideline impact handling:
   - For each guideline citing a downgraded/removed source, open a follow-up to replace citation.
   - Do not keep a guideline in `Accepted` status if its required Tier-1 citation is invalid.
4. Completion criteria:
   - Registry entry updated (`last_reviewed`, notes, tier if changed).
   - Affected guideline files updated or follow-up issues recorded.
