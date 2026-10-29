## 2024-10-29 - Improve Login Accessibility
**Learning:** In custom React forms, pairing `<label>` with `<input>` using `htmlFor` and `id` along with `aria-required="true"` improves screen reader experiences significantly. Error messages should also use `role="alert"` to notify users immediately. Finally, interactive text elements should be `<button>` rather than `<span>` to support keyboard navigation.
**Action:** Always ensure `<label>` and `<input>` are linked and `role="alert"` is present for dynamic form errors. Convert clickable `<span>` elements to native `<button type="button">`.
