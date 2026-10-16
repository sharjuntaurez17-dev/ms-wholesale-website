## 2026-05-26 - [Added htmlFor to connect inputs with labels]
**Learning:** Found that custom form implementations often miss the explicit linkage between `<label>` and `<input>` elements. Even if wrapped nearby or styled clearly for visual users, screen readers rely on `id` and `htmlFor` (in React).
**Action:** Always verify form field labeling. If the label isn't wrapping the input implicitly, enforce explicit `htmlFor` linking to ensure screen reader compatibility and to increase the clickable area (clicking label focuses input).
