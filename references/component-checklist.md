# Interactive Component Accessibility Checklist

Use this checklist when implementing or reviewing dialogs, tabs, accordions, menus, and custom controls. Follow established interaction patterns and verify behavior in the actual application.

## General component checks

- [ ] Component has an accessible name.
- [ ] Native HTML semantics are used where possible.
- [ ] Role, state, and relationships match the actual behavior.
- [ ] Keyboard interaction follows expected platform patterns.
- [ ] Focus is visible.
- [ ] Focus order is logical.
- [ ] Dynamic state changes are exposed to assistive technology.
- [ ] Disabled, expanded, selected, and invalid states are communicated.
- [ ] Component remains usable at zoom and narrow viewports.

## Dialogs and modals

- [ ] Dialog has a clear title.
- [ ] Opening the dialog moves focus to an appropriate element.
- [ ] Modal focus remains within the dialog while it is open.
- [ ] Escape closes the dialog where appropriate.
- [ ] Closing restores focus to the invoking control.
- [ ] Background content is not interactable while modal behavior is active.
- [ ] Dialog controls have accessible names.

## Tabs

- [ ] Tablist has an accessible label where needed.
- [ ] Each tab exposes selected state.
- [ ] Each tab is associated with its panel.
- [ ] Arrow keys move between tabs according to the chosen pattern.
- [ ] Focus and selected state remain synchronized.
- [ ] Panel content is available to assistive technology.

## Accordions

- [ ] Trigger is a button.
- [ ] Expanded state is exposed.
- [ ] Trigger references the controlled panel.
- [ ] Expanded and collapsed content visibility is accurate.
- [ ] Focus remains predictable when panels change.

## Menus and navigation

- [ ] Navigation is structured using appropriate semantic elements.
- [ ] Menu items are reachable and operable by keyboard.
- [ ] Expanded state is communicated.
- [ ] Escape and outside interaction behavior are predictable.
- [ ] Opening and closing does not unexpectedly lose focus.

## Forms and custom controls

- [ ] Visible label or accessible name is provided.
- [ ] Current value and state are exposed.
- [ ] Keyboard interaction matches the control pattern.
- [ ] Errors and help text are programmatically associated.
- [ ] State changes are announced where necessary.
