
# Lab 11: Accessible Custom Components & Widgets

## Questions and Answers

### 1. What is the keyboard interaction missing?

The original accordion component was missing the following keyboard interactions:
- **Focus Navigation**: Users could not navigate through the accordion buttons using the Tab key because there were no proper focus styles or keyboard support implemented.
- **Expand/Collapse Using Enter and Space Keys**: The accordion did not allow toggling the sections using the `Enter` or `Space` keys, which is a common accessibility requirement for interactive elements like buttons.


### 2. What is the ARIA missing?

The original accordion component was missing key ARIA attributes required for accessible accordions:
- **`aria-expanded`**: This attribute was missing on the buttons to indicate whether a section is expanded (`true`) or collapsed (`false`).
- **`aria-controls`**: This attribute was not used to link each button to its corresponding content section, allowing screen readers to associate the button with the collapsible region.
- **`role="region"`**: The content sections did not have the `region` role to mark them as landmark regions for screen readers.
- **`aria-labelledby`**: This attribute was missing on the content sections to associate them with the corresponding buttons for screen reader users.

By addressing these issues, the component is now fully accessible, supporting both keyboard and screen reader users.
