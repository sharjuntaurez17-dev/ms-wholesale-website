## 2023-10-03 - Accessible Form Validation
**Learning:** When using React for custom form validation and displaying custom error messages, adding native HTML5 `required` attributes will block the `onSubmit` handler.
**Action:** When adding HTML5 `required` attributes for semantics, be sure to add `noValidate` on the `<form>` element so React can handle custom validation display logic. Also, map `<label>` correctly using `htmlFor` matching the input `id`, and ensure conditional error components announce dynamically to screen readers by setting `role="alert"` and `aria-live="polite"`.
