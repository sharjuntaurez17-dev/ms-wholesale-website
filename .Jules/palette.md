## 2026-06-15 - Interactive Element Implementation Pattern
**Learning:** The application heavily relies on interactive `<span>` elements styled with inline CSS. Converting these to semantic `<button>`s requires specifically overriding default browser button styles with `background: "none", border: "none", padding: 0, margin: 0, font: "inherit"` to prevent visual regressions while enabling native keyboard navigation.
**Action:** Always scan for clickable `<span>` elements when doing accessibility reviews and use this specific CSS reset pattern when converting them to buttons.
