# Accessibility Technology Map (SwiftUI + Interop)

Last updated: 2026-03-07
Scope: iOS SwiftUI apps, including SwiftUI-UIKit interoperability where it affects accessibility semantics.

## Purpose

Define what each assistive technology needs from app semantics, and how teams verify support.

## Technologies and Interaction Model

### VoiceOver

- What users do:
  - Swipe left/right to move focus.
  - Explore by touch.
  - Use rotor to navigate by semantics (headings, controls, etc.).
  - Activate default/custom actions.
- UI must expose:
  - Meaningful label/value/hint.
  - Accurate role/traits.
  - Logical reading and focus order.
  - Custom actions where direct manipulation is not available.
- Test coverage:
  - Accessibility Inspector hierarchy inspection.
  - On-device VoiceOver walkthrough per screen.
  - Verify rotor landmarks/headings where applicable.

### Switch Control

- What users do:
  - Sequential scanning and activation.
  - Optional item grouping and menu-based action selection.
- UI must expose:
  - Reachable focusable elements.
  - Predictable activation targets.
  - Clear semantic names and action affordances.
- Test coverage:
  - Manual scanning pass through primary user flows.
  - Confirm no unreachable controls.

### Voice Control

- What users do:
  - Issue command phrases to activate controls by name/number.
  - Navigate UI without touch.
- UI must expose:
  - Distinct, speakable control names.
  - Stable control naming across states where possible.
  - Avoid duplicate/ambiguous labels in same context.
- Test coverage:
  - Manual voice command spot checks for key flows.
  - Confirm command disambiguation is not required for common actions.

### Dynamic Type / Larger Text

- What users do:
  - Increase text size system-wide.
  - Use accessibility text categories.
- UI must expose:
  - Scalable text and controls.
  - Layout resilience without clipped/overlapping text.
  - Usable content hierarchy at large sizes.
- Test coverage:
  - Device and simulator sweeps at largest categories.
  - Screen-by-screen clipping and truncation checks.

### Increase Contrast / Differentiate Without Color

- What users do:
  - Enable higher contrast and color-independent cues.
- UI must expose:
  - Sufficient contrast.
  - Non-color signals for state, errors, and status.
- Test coverage:
  - Settings toggles + visual verification.
  - Inspector contrast and semantic review.

### Reduce Motion

- What users do:
  - Disable or reduce non-essential motion effects.
- UI must expose:
  - Reduced/non-motion alternatives for animations.
  - Equivalent state transition clarity without motion reliance.
- Test coverage:
  - Toggle-based walkthrough of animated flows.
  - Confirm no critical information is motion-only.

### Captions / Audio Descriptions (Media Views)

- What users do:
  - Consume media with captions/subtitles and optional descriptions.
- UI must expose:
  - Captions where spoken content exists.
  - Accessible playback controls and media state labels.
- Test coverage:
  - Media playback flow checks with assistive settings enabled.
  - Confirm controls are discoverable and labelled.

## Cross-Cutting Semantics Requirements

For all technologies above, each interactive UI element should be validated for:

- Label
- Value (if stateful)
- Hint (only when needed)
- Role/Traits
- Available actions
- Reading/focus order

## SwiftUI-UIKit Interop Risk Areas

- `UIHostingController` inside UIKit navigation/container stacks can alter focus order.
- `UIViewRepresentable` and `UIViewControllerRepresentable` wrappers can miss semantic forwarding.
- UIKit parent containers can override or flatten SwiftUI accessibility elements.

Verification rule: whenever interop is introduced, run both hierarchy inspection and on-device VoiceOver flow before merge.
