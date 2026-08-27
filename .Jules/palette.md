## 2025-02-28 - Add missing structural associations in form fields
**Learning:** Found that some forms lack explicit structural associations (like `htmlFor` and `id`) and dynamic UI error containers lack accessibility attributes (like `role="alert"`). This impacts screen reader accessibility.
**Action:** Always verify that input fields are explicitly linked to their labels and dynamic error messages contain `role="alert"` and `aria-live="polite"`.
