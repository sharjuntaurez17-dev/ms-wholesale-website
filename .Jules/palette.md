## 2025-02-23 - Login Form Accessibility Improvement
**Learning:** This app's form fields occasionally lack explicit structural associations (`htmlFor` matching input `id`). Error containers dynamically rendered to show conditional errors also often miss ARIA attributes.
**Action:** When working on forms, explicitly associate `<label>` elements with their inputs using `htmlFor` and `id`. Also, ensure dynamic error containers have `role="alert"` and `aria-live="polite"`.
