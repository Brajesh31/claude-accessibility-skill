# claude-accessibility-skill

A Claude Code skill for evaluating and improving web accessibility with practical WCAG-based review workflows.

## Overview

This skill identifies barriers that prevent people from perceiving, understanding, or operating a website or application. It focuses on actionable improvements across semantics, keyboard interaction, forms, visual presentation, and assistive-technology support.

## Core Principles

The skill uses the four POUR principles:

- **Perceivable:** Information and interface elements must be available through appropriate sensory channels.
- **Operable:** Users must be able to navigate and interact with the interface.
- **Understandable:** Content, controls, and feedback should behave predictably.
- **Robust:** Markup and interactions should work with browsers and assistive technologies.

## What It Helps Review

- Semantic structure, headings, landmarks, and accessible names.
- Keyboard operation, focus order, focus visibility, and keyboard traps.
- Form labels, instructions, validation, and error feedback.
- Text and non-text contrast, zoom, reflow, and reduced motion.
- ARIA, screen-reader names, roles, states, and dynamic updates.

## Installation

```bash
git clone https://github.com/Brajesh31/claude-accessibility-skill.git ~/.claude/skills/accessibility
```

## Usage

Invoke `/accessibility` when reviewing a page, component, design implementation, or accessibility defect. Provide relevant source files, target page, expected interactions, and known requirements.

## Recommended Audit Workflow

1. Inspect page structure and interactive elements.
2. Review semantic HTML and accessible names.
3. Test all controls using only a keyboard.
4. Inspect focus order and visible focus.
5. Check text and interface contrast.
6. Review forms, errors, dialogs, and dynamic updates.
7. Use automated checks as a supplement, not as the sole audit.
8. Report findings with location, user impact, severity, and recommended fix.
9. Re-test affected interactions after changes.

## Important Note

An automated scan cannot establish full accessibility conformance. Combine automated checks with keyboard testing, manual inspection, and assistive-technology testing appropriate to the product.

## Repository Contents

- `SKILL.md`: Main accessibility review instructions.
- `references/WCAG.md`: Detailed accessibility reference material.
- `README.md`: Overview, audit workflow, and checklist.

## Creator and maintainer

Created and maintained by **Brajesh Kumar**.
