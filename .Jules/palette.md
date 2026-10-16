## 2026-06-01 - Missing Label Associations in Custom Form Styling
**Learning:** Custom styled inputs using generic `div` wrapping and React state (`focused`) can obscure a basic accessibility requirement: missing `htmlFor` attributes on labels and missing `id`s on inputs.
**Action:** Always verify proper `label -> input` binding using `htmlFor` and `id`, even when visual state is entirely custom, so users can click on labels to focus and screen readers have correct associations. Add `autoComplete` to support password managers.
