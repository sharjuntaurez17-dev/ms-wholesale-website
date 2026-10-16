## 2026-08-02 - Improve Form Accessibility in React Components
**Learning:** React elements utilizing `<span>` with inline styles for interaction break keyboard accessibility and native browser behavior. Forms with dynamic error messages lack screen reader notifications.
**Action:** Replace interactive `<span>` elements with native `<button type="button">`, applying `background: "none", border: "none", padding: 0, font: "inherit"` to maintain visual consistency. Add `role="alert"` and `aria-live="polite"` to conditionally rendered error containers to guarantee screen reader announcements.
