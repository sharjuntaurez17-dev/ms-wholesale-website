## 2024-05-24 - Form Accessibility Importance
**Learning:** Proper linkage between labels and inputs using `htmlFor` and `id`, along with explicit `role="alert"` and `aria-live="polite"` for dynamic error messages, is critical for screen reader compatibility and overall accessibility in forms. This is a common pattern to ensure users of assistive tech get proper context.
**Action:** Always link `<label>` and `<input>` elements using explicit `htmlFor` and `id` attributes. Always add `role="alert"` and `aria-live="polite"` to conditional error messages.
