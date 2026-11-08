# Accessibility Skill

A practical accessibility skill for evaluating and improving websites and applications using structured WCAG-based review workflows. It helps identify barriers, understand their impact, choose appropriate implementation patterns, and validate fixes.

Accessibility is part of product quality. It should be considered during design and development, not postponed until the final release review.

## What This Skill Covers

- The four POUR principles: Perceivable, Operable, Understandable, and Robust.
- WCAG 2.1 success criteria and conformance levels.
- Semantic HTML, heading hierarchy, and landmarks.
- Text alternatives for images and accessible names for controls.
- Color contrast and non-color indicators.
- Keyboard access, visible focus, and skip links.
- Forms, instructions, validation, and error feedback.
- Accessible dialogs, tabs, accordions, and dynamic content.
- Media alternatives, zoom, responsive reflow, and reduced motion.
- Automated and manual testing workflows.

## When to Use It

Use this skill when asked to improve a website's accessibility, conduct an a11y review, improve screen-reader support, check keyboard navigation, or plan accessibility remediation.

It can be used during design reviews, development, QA, and pre-release validation.

## Installation

~~~bash
git clone https://github.com/Brajesh31/claude-accessibility-skill.git ~/.claude/skills/accessibility
~~~

## Invocation

~~~text
/accessibility
~~~

Provide the URL, component, framework, user journey, target conformance level, and any known assistive-technology requirements.

## Recommended Workflow

1. Identify the user journey and page states being reviewed.
2. Inspect semantics, headings, landmarks, labels, and accessible names.
3. Test keyboard reachability, activation, focus order, and focus visibility.
4. Review forms, instructions, validation, and status messaging.
5. Check images, contrast, zoom, reflow, and motion preferences.
6. Run automated tools for detectable issues.
7. Verify critical flows manually with keyboard and screen readers.
8. Record each issue with user impact, evidence, priority, and a fix.
9. Re-test after changes and document remaining limitations.

## WCAG Principles

| Principle | What it means in practice |
|---|---|
| Perceivable | Information and controls can be perceived through appropriate sensory channels. |
| Operable | Users can navigate and operate controls with different input methods. |
| Understandable | Content and interaction behavior are clear and predictable. |
| Robust | Content and controls work with browsers and assistive technologies. |

## Common Review Areas

### Text alternatives

Provide text alternatives appropriate to the image's purpose. Informative images need a meaningful description, decorative images should generally be ignored by assistive technology, and functional images should describe the action.

### Contrast and visual states

Check text and non-text contrast. Ensure focus, selection, validation, and other states are not communicated by color alone.

### Semantic HTML

Prefer native buttons, links, headings, lists, tables, and form elements. Use ARIA to supplement semantics when necessary, not to replace correct native elements.

### Keyboard operation

Ensure every interactive feature can be reached and operated using the keyboard. Focus should be visible, follow a logical order, and never become trapped unintentionally.

### Forms and validation

Associate labels, hints, required states, and errors with their fields. Explain how to correct errors and make dynamic feedback available to assistive technology.

### Interactive components

Dialogs, tabs, accordions, menus, and custom controls need clear names, states, keyboard behavior, and focus management. Follow established interaction patterns instead of inventing new ones.

## Included References and Resources

- [WCAG 2.1 quick reference](references/WCAG.md)
- [Interactive component checklist](references/component-checklist.md)
- [Accessibility issue report template](templates/accessibility-issue-template.md)

## Testing Strategy

| Method | What it can reveal | Important limitation |
|---|---|---|
| Automated tools | Detectable markup, contrast, and rule violations | Cannot assess all user journeys or meaning |
| Keyboard-only review | Focus order, traps, and operability | Does not replace screen-reader testing |
| Screen-reader review | Reading order, names, states, and announcements | Depends on browser and screen-reader combination |
| Zoom and reflow | Layout and content behavior at larger sizes | Must be tested on realistic screens |
| Code review | Semantic structure and implementation quality | Runtime behavior still needs validation |

A clean automated scan is not a conformance certificate. Combine tools with hands-on testing.

## Quality Checklist

- Semantic HTML is used appropriately.
- Headings and landmarks describe the page structure.
- Images have appropriate alternatives.
- Form controls have accessible names.
- Keyboard interaction is complete and predictable.
- Focus remains visible and is managed correctly.
- Errors and dynamic status updates are communicated.
- Contrast and visual states are sufficient.
- Content remains usable when enlarged or reflowed.
- The same user journey has been retested after fixes.

## Limitations

WCAG conformance depends on the complete experience, including content, code, third-party widgets, and user journeys. Requirements and legal obligations vary by jurisdiction. State the tested scope and version, and avoid claiming legal compliance based on a checklist or automated score alone.

## Repository Structure

~~~text
claude-accessibility-skill/
├── SKILL.md
├── README.md
├── LICENSE
├── references/
│   ├── WCAG.md
│   └── component-checklist.md
└── templates/
    └── accessibility-issue-template.md
~~~

## License

Released under the MIT License. Copyright (c) 2026 Brajesh Kumar. See the root `LICENSE` file for the complete terms.
