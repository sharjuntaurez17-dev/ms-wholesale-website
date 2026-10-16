## 2024-10-16 - Explicit Form Labels and Alert Roles
**Learning:** React elements for forms and dynamic errors occasionally lack proper structural association for screen readers, specifically when input fields are disconnected from their descriptive labels and dynamic error wrappers lack ARIA roles.
**Action:** Always explicitly pair `<label>` and `<input>` using matching `htmlFor` and `id` attributes, including `required` and `aria-required="true"`. Use `role="alert"` and `aria-live="polite"` for dynamic error display containers to improve screen reader communication.
