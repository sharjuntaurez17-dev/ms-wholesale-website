## 2024-05-18 - Convert interactive spans to semantic buttons
**Learning:** Interactive elements implemented as `<span>` tags with `cursor: "pointer"` are inaccessible to keyboard users and lack semantic meaning for screen readers.
**Action:** Always replace these `<span>` elements with semantically correct `<button type="button">` or `<a>` elements, applying CSS reset styles (`background: "none", border: "none", padding: 0, font: "inherit"`) to maintain their visual appearance while ensuring accessibility.
