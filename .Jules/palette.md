## 2024-05-14 - Accessible Forms with React onSubmit Validation
**Learning:** When using React's `onSubmit` for custom form validation along with native HTML5 `required` attributes, the browser's native validation tooltips can block the React `onSubmit` handler from executing. However, omitting `required` breaks semantic accessibility.
**Action:** Always include `noValidate` on the `<form>` element when combining `required` inputs with a custom React `onSubmit` handler. This allows screen readers to announce fields as required while allowing custom logic to handle validation UI.
