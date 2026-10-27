## 2023-10-27 - Semantic Elements and Form Accessibility
**Learning:** The application's heavy reliance on inline styles often led to semantic HTML elements being replaced with inaccessible generic elements (like `<span>` with pointer cursor) or missing structural associations like `id`/`htmlFor`.
**Action:** Convert faux-buttons back to native `<button type="button">` using style resets (`background: "none", border: "none", padding: 0, font: "inherit"`) and explicitly pair `<label>` and `<input>` using `htmlFor` and `id`, including `role="alert"` for custom errors.
