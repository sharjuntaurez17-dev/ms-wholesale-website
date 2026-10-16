## 2026-05-25 - LoginScreen form inputs accessibility
**Learning:** The LoginScreen component had custom inputs that were missing proper ARIA label associations (`htmlFor` and `id`). This made keyboard navigation less intuitive (couldn't click labels to focus) and impaired screen reader functionality.
**Action:** Always verify that every custom form input has a corresponding `id` that matches its label's `htmlFor` attribute. Added `htmlFor="email"` and `htmlFor="password"` to labels, and matching `id` attributes to inputs.
