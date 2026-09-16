## 2024-05-24 - Form Accessibility
**Learning:** In the LoginScreen, form elements were missing explicit connections between labels and inputs via `htmlFor` and `id`, and dynamic error messages lacked aria attributes (`role="alert"` and `aria-live="polite"`) necessary for screen readers.
**Action:** Ensure that all inputs have an `id` that matches their label s `htmlFor` attribute. When implementing dynamic UI error states, always wrap the error text in an element that includes `role="alert"` and `aria-live="polite"`.
