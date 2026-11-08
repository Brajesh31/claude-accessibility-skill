# claude-accessibility-skill

A Claude Code skill for evaluating and improving web accessibility with practical WCAG-based review workflows.

## Overview

This skill helps identify barriers that prevent people from perceiving, understanding, or operating a website or application. It focuses on actionable accessibility improvements across structure, semantics, keyboard interaction, forms, visual presentation, and assistive-technology support.

Accessibility should be considered throughout design and development, not treated as a final cosmetic pass.

## Core Principles

The skill uses the four POUR principles:

- **Perceivable:** Information and interface elements must be available through appropriate sensory channels.
- **Operable:** Users must be able to navigate and interact with the interface.
- **Understandable:** Content, controls, and feedback should behave predictably.
- **Robust:** Markup and interactions should work with browsers and assistive technologies.

## What It Helps Review

### Semantic Structure

- Correct heading hierarchy.
- Landmark regions and page structure.
- Native HTML elements before custom controls.
- Accessible names and descriptions.
- Meaningful link and button text.

### Keyboard Accessibility

- Complete keyboard operation.
- Logical focus order.
- Visible focus indicators.
- Correct focus management for dialogs and menus.
- No keyboard traps.

### Forms and Validation

- Programmatic labels and instructions.
- Clear required-field communication.
- Useful error messages.
- Error identification that does not rely on color alone.
- Accessible status and success feedback.

### Visual Accessibility

- Text and non-text contrast.
- Text resizing and zoom behavior.
- Responsive layouts and reflow.
- Reduced-motion preferences.
- Avoiding color as the only way to communicate meaning.

### Assistive Technology

- Appropriate ARIA use.
- Screen-reader names, roles, and states.
- Live-region behavior where needed.
- Accessible dynamic updates.

## Installation

```bash
git clone https://github.com/Brajesh31/claude-accessibility-skill.git ~/.claude/skills/accessibility
```

## Usage

Use the skill when reviewing a page, component, design implementation, or accessibility defect:

```text
/accessibility
```

Provide the relevant source files, target page, expected interactions, and any known accessibility requirements.

## Recommended Audit Workflow

1. Inspect the page structure and interactive elements.
2. Review semantic HTML and accessible names.
3. Test all controls using only a keyboard.
4. Inspect focus order and visible focus.
5. Check text and interface contrast.
6. Review forms, errors, dialogs, and dynamic updates.
7. Run automated checks as a supplement, not as the sole audit.
8. Report each finding with its location, user impact, severity, and recommended fix.
9. Re-test the affected interaction after changes.

## Example Finding Format

| Field | Description |
|---|---|
| Issue | Concise description of the barrier |
| Location | Page, component, or source location |
| Impact | How the issue affects users |
| Priority | Severity and practical urgency |
| Fix | Specific implementation change |
| Verification | How to confirm the fix |

## Validation Checklist

- Every interactive control is keyboard accessible.
- Focus is visible and follows a sensible order.
- Images have appropriate alternative text or are marked decorative.
- Form controls have accessible labels.
- Errors are announced and associated with their fields.
- Headings and landmarks communicate page structure.
- Contrast is sufficient for text and controls.
- Zoom and reflow do not hide content or functionality.
- Motion-sensitive users have suitable alternatives.
- ARIA is used only when native HTML does not provide the needed semantics.

## Repository Contents

- `SKILL.md`: Main accessibility review instructions.
- `references/WCAG.md`: Detailed accessibility reference material.
- `README.md`: Overview, audit workflow, and checklist.

## Important Note

An automated scan cannot establish full accessibility conformance. Combine automated checks with keyboard testing, manual inspection, and assistive-technology testing appropriate to the product.
