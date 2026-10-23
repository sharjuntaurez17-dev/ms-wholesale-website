## 2024-05-20 - Converting styled spans to buttons
**Learning:** In this application, interactive text links are often implemented as <span> elements with cursor: "pointer". This makes them inaccessible to keyboard users and screen readers.
**Action:** When finding these, always convert them to semantic <button type="button"> elements (or <a> tags if appropriate). Use the CSS reset `background: "none", border: "none", padding: 0, font: "inherit"` to maintain the exact visual styling while adding full accessibility.
