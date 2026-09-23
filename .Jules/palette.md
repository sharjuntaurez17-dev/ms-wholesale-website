## 2024-05-24 - Accessibility: Form Labels and Error Messages
**Learning:** Found instances where forms in the application lacked explicit structural associations between `<label>` and `<input>` tags, as well as unannounced conditional form error messages.
**Action:** Always explicitly pair `<label>` elements with their respective `<input>` elements using matching `htmlFor` and `id` attributes. Add `required` and `aria-required="true"` where applicable. Use `role="alert"` and `aria-live="polite"` on dynamically rendered error message containers to ensure screen reader compatibility.
