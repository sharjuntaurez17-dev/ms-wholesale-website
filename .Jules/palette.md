## 2023-10-27 - Form Accessibility Enhancements
**Learning:** Found several common accessibility anti-patterns in React forms using inline styles:
1. Missing explicit `<label>` connections (`htmlFor` -> `id`), requiring users to hit tiny input touch targets rather than allowing label clicks to focus inputs.
2. Link-like text elements implemented as `<span>` tags rather than `<button>` tags, completely bypassing keyboard accessibility and screen-reader interaction.
3. Custom React validation errors displayed without ARIA live regions, causing them to be silently ignored by screen readers when they pop up.
**Action:**
- Converted interactive spans to semantic `<button type="button">` using a simple inline reset (`background: "none", border: "none", padding: 0, font: "inherit"`) to achieve accessibility while perfectly maintaining visual design.
- Connected all form labels using `id` and `htmlFor`.
- Wrapped dynamic error messages with `role="alert" aria-live="polite"`.
- When writing Playwright tests to test custom React validation logic alongside HTML5 `required` attributes, added the `noValidate` attribute to the form to prevent the browser from blocking submission before React can handle it.
