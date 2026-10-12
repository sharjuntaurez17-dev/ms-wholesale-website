## 2024-05-24 - Interactive Spans to Buttons
**Learning:** This app heavily uses inline styles, leading to interactive elements like "Forgot password" and "Sign up" links being implemented as `<span>` tags. These elements are inaccessible via keyboard and lack semantic meaning.
**Action:** Always convert interactive `<span>` elements to semantic native elements (like `<button type="button">`) using a CSS style reset (`background: "none", border: "none", padding: 0, font: "inherit"`) to maintain the existing visual appearance while enabling full keyboard and screen reader accessibility.

## 2024-05-24 - Form Field Associations
**Learning:** Form structures in this app often lack explicit structural associations between `<label>` and `<input>` elements (e.g. missing `htmlFor` and `id` attributes).
**Action:** When improving form accessibility, explicitly pair `<label>` elements with their respective `<input>` elements using matching `htmlFor` and `id` attributes. Additionally, include `required` and `aria-required="true"` where applicable, and add `noValidate` to the `<form>` to handle custom validation logic correctly.
