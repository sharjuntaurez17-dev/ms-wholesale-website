## 2023-10-25 - Converting span links to buttons for keyboard accessibility
**Learning:** Some interactive UI elements acting as links/buttons in this application are implemented using non-semantic `<span>` elements, causing them to lack keyboard navigability (no tab focus) and screen reader support.
**Action:** Always convert interactive `<span onClick={...}>` elements into native semantic `<button type="button">` or `<a>` elements and apply the CSS style reset `background: "none", border: "none", padding: 0, font: "inherit"` to maintain the existing visual appearance while seamlessly enabling default keyboard and screen reader accessibility.

## 2023-10-25 - React element labels and inputs
**Learning:** Labels that are disconnected structurally from their inputs fail to be announced correctly.
**Action:** When adding labels or fixing disconnected inputs in this codebase, explicitly pair `<label>` elements with their respective `<input>` elements using matching `htmlFor` and `id` attributes.
