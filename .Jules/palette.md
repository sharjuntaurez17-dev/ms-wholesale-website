## 2025-02-27 - Custom React validation with noValidate
**Learning:** When using custom React `onSubmit` validation in forms, adding native HTML5 `required` attributes will block the form submission because native browser validation tooltips take precedence.
**Action:** Always add the `noValidate` attribute to the `<form>` element when combining custom React submission validation with semantic accessibility attributes like `required` to prevent tooltip interference while maintaining accessibility.
