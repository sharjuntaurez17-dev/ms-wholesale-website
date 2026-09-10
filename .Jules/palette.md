## YYYY-MM-DD - Initial Entry
**Learning:** Started tracking critical UX/a11y learnings.
**Action:** Will document app-specific patterns here.

## 2026-09-10 - Login Screen Accessibility
**Learning:** Interactive elements implemented as `<span>` need explicit CSS resets (`background: "none", border: "none", padding: 0, font: "inherit"`) when converted to `<button>` to maintain visual appearance while fixing keyboard accessibility. Dynamic error states should use `role="alert"` and `aria-live="polite"`.
**Action:** Will proactively convert interactive spans to buttons with resets and ensure conditional error messages have aria-live attributes.
