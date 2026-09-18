# Weekly Ship Log

A modern, distraction-free, single-file personal journal for developers to track and document what they build and ship each week. All logs persist locally in the browser using `localStorage`.

---

## Features

- **Browser Persistence**: All ship log entries are automatically saved to `localStorage` and persist across page refreshes.
- **Modern & Clean Aesthetics**: Designed with a sleek purple-to-indigo gradient header, polished card components, subtle drop shadows, and modern typography powered by Google Fonts (Inter).
- **Lucide Icons**: Every button, status indicator, timestamp, and empty state uses crisp Lucide Icons — no emoji anywhere in the UI.
- **Reverse Chronological Order**: Displays entries with newest updates at the very top.
- **Live Character Counter**: Real-time counter (`0 / 1000 characters`) to keep entries concise.
- **Edit Entries**: Each entry card has an ✏️ Edit button that opens an inline textarea pre-filled with the original text. Changes are saved instantly with a `(edited)` badge, or discarded with Cancel.
- **Clear All Entries**: A ghost-style "Clear All Entries" button appears in the header whenever entries exist. It prompts for confirmation before wiping all data.
- **Accidental Deletion Protection**: Confirmation prompt before deleting any individual log entry.
- **Keyboard Shortcuts**: Quickly save entries using <kbd>Cmd</kbd> + <kbd>Enter</kbd> (Mac) or <kbd>Ctrl</kbd> + <kbd>Enter</kbd> (Windows/Linux). Also supports <kbd>Cmd/Ctrl</kbd> + <kbd>Enter</kbd> inside the edit textarea to save changes.
- **Inline Error Validation**: User-friendly, temporary inline error messages if an empty submission is attempted.
- **Fully Responsive**: Fluid, mobile-optimized interface with full-width tap targets for devices under `600px`.
- **Zero Build Tools Required**: Pure HTML, CSS, and Vanilla JavaScript inside a single `index.html` file.

---

## Tech Stack

- **Structure**: Semantic HTML5
- **Styling**: Vanilla CSS3 (CSS Variables, Flexbox, Keyframe Animations, Media Queries)
- **Logic**: Vanilla JavaScript (ES6+, DOM APIs, `localStorage`)
- **Icons**: [Lucide Icons](https://lucide.dev/)
- **Typography**: [Inter](https://fonts.google.com/specimen/Inter) via Google Fonts

---

## Getting Started

Since the entire application is self-contained in a single file, no build steps or dependencies are needed.

### Option 1: Direct File Open
Simply double-click `index.html` or open it directly in your browser:
```bash
# macOS
open index.html

# Linux
xdg-open index.html

# Windows
start index.html
```

### Option 2: Live Server (VS Code / CLI)
Run a local static server if you prefer:
```bash
# Using Python
python3 -m http.server 8080

# Using npx serve
npx serve .
```

---

## How to Use

1. **Write Your Update**: Type what you shipped or built into the input area.
2. **Save**: Click **Save Entry** or press <kbd>Cmd/Ctrl</kbd> + <kbd>Enter</kbd>.
3. **Review**: See your previous entries rendered in reverse chronological order with formatted timestamps.
4. **Edit**: Click the **Edit** button on any entry card to update its content inline. Save or Cancel when done.
5. **Delete**: Click the **Delete** button on any entry card to permanently remove it after confirming.
6. **Clear All**: Use the **Clear All Entries** button in the header to wipe the entire log after confirming.

---

## Project Structure

```text
weeklyshiplogtracker/
├── index.html       # Complete single-file application (HTML, CSS, JS)
├── README.md        # Documentation and guide
└── Journal.md       # Development log and changelog
```
