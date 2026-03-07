# Manual Accessibility Test Scripts

Last updated: 2026-03-07
Scope: iOS app screens implemented with SwiftUI, UIKit, or mixed stacks.

## Script 1: VoiceOver Smoke Test (Per Screen)

Purpose: verify semantic announcements and focus flow for core user tasks.

1. Enable VoiceOver on device or simulator.
2. Enter the target screen from the same app state each run.
3. Swipe right from top to bottom and record:
   - First focused element.
   - Spoken label/value/role for each actionable control.
   - Any skipped or duplicate items.
4. Activate each primary action and verify updated state is announced.
5. If a modal/sheet opens, verify focus lands in modal context and returns to trigger anchor on close.

Pass criteria:
- All meaningful elements are reachable and announced with clear semantics.
- Focus order follows task flow with no trap/jump regressions.

Fail examples:
- Icon-only button announced as unlabeled/generic.
- Focus moves behind active modal content.

## Script 2: Dynamic Type and Larger Text Sweep

Purpose: ensure readability and operability at large content sizes.

1. Set text size to largest accessibility category.
2. Traverse all primary screens.
3. Verify:
   - No clipped critical text.
   - Primary actions remain visible/reachable.
   - Form rows and table/list items still communicate semantics clearly.

Pass criteria:
- All essential content remains readable and actionable.

Fail examples:
- Truncated error label hides required action context.
- Button text clips and changes meaning.

## Script 3: Contrast and Differentiate-Without-Color Sweep

Purpose: ensure state and status do not depend on color alone.

1. Enable higher-contrast and differentiate-without-color settings.
2. Visit screens with selection/error/success/status states.
3. Verify each state has non-color cue (text, symbol, shape, pattern).
4. Run brief VoiceOver pass to confirm spoken semantics include state context.

Pass criteria:
- State/status remains identifiable without color interpretation.

Fail examples:
- Selected state indicated only by tint change.
- Error state shown as red text with no semantic label.

## Script 4: Reduce Motion Sweep

Purpose: verify transitions remain understandable with reduced motion.

1. Enable Reduce Motion.
2. Execute flows with heavy animation (navigation, modal transitions, state changes).
3. Verify:
   - UI state is still obvious without motion effects.
   - No timing-dependent controls become unusable.

Pass criteria:
- Final state and context remain clear for all tested transitions.

Fail examples:
- Completion feedback appears only through motion.
- Transition leaves ambiguous current context.

## Logging Template

Use this for each executed script:

- Date:
- Build/version:
- Device + OS:
- Screen/flow:
- Script:
- Result: Pass/Fail
- Notes:
- Follow-up issue link:
