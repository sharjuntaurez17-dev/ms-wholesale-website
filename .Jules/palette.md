## 2024-07-17 - Dynamic Error Message Accessibility
**Learning:** Conditional or dynamically rendered error messages in React forms are not automatically announced by screen readers when they appear, leaving visually impaired users unaware of validation failures.
**Action:** Always add `role="alert"` and `aria-live="polite"` to dynamically rendered error containers to ensure screen readers announce the message as soon as it is injected into the DOM.
