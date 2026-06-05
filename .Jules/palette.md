## 2024-03-24 - Interactive Elements using Inline Styles
**Learning:** Because the app uses inline styles extensively, interactive elements like links or secondary actions are sometimes implemented as `<span>`s with `cursor: pointer` to easily style them, bypassing native keyboard accessibility and screen reader support.
**Action:** Always use native interactive elements (`<button type="button">`, `<a>`) for clickable text, resetting default styles (e.g., `background: "none"`, `border: "none"`, `padding: 0`) inline to match the desired visual appearance.
