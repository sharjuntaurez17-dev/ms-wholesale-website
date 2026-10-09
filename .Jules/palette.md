## 2025-02-28 - Explicit form accessibility in React
**Learning:** Explicitly pairing `<label>` to `<input>` with matching `htmlFor` and `id`, as well as adding `role="alert"` and `aria-live="polite"` on error containers, ensures structural association for screen readers testing React application forms, avoiding missing states without disrupting validation flow.
**Action:** Always add `htmlFor` and `id` mapping to form elements and ARIA live regions for dynamically rendered form errors.
