## 2024-11-07 - Add accessibility features to Login Form
**Learning:** When using custom React error states and validation for forms, adding the native HTML5 `required` attribute to inputs will block the `onSubmit` handler.
**Action:** Add the `noValidate` attribute to the `<form>` element to bypass native validation while maintaining accessibility through `required` and `aria-required="true"` on inputs.
