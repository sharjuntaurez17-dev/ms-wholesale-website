## 2024-05-28 - LoginScreen Accessibility
**Learning:** Custom form fields often miss fundamental `htmlFor`/`id` linking and lack `aria-describedby` when conditionally rendering inline validation errors, disrupting the screen reader experience.
**Action:** Always link form labels to their inputs using `htmlFor` and `id`, and ensure dynamic error messages use `role="alert"` and link to inputs via `aria-describedby` and `aria-invalid`.
