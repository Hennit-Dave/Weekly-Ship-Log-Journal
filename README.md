# Weekly Ship Log

A modern, distraction-free, single-file personal journal for developers to track and document what they build and ship each week. All logs persist locally in the browser using `localStorage`.

---

## Features

- **Browser Persistence**: All ship log entries are automatically saved to `localStorage` and persist across page refreshes.
- **Modern & Clean Aesthetics**: Designed with a sleek purple-to-indigo gradient header, polished card components, subtle drop shadows, and modern typography powered by Google Fonts (Inter).
- **Lucide Icons**: Fully integrated with crisp Lucide Icons for buttons, status indicators, timestamps, and empty states.
- **Reverse Chronological Order**: Displays entries with newest updates at the very top.
- **Live Character Counter**: Real-time counter (`0 / 1000 characters`) to keep entries concise.
- **Accidental Deletion Protection**: Confirmation modal prompt before deleting any log entry.
- **Keyboard Shortcuts**: Quickly save entries using <kbd>Cmd</kbd> + <kbd>Enter</kbd> (Mac) or <kbd>Ctrl</kbd> + <kbd>Enter</kbd> (Windows/Linux).
- **Inline Error Validation**: User-friendly, temporary inline error messages if an empty submission is attempted.
- **Fully Responsive**: Fluid, mobile-optimized interface with full-width tap targets for devices under `480px`.
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
4. **Delete**: Click the **Delete** button on any entry card to permanently remove it after confirming.

---

## Project Structure

```text
weeklyshiplogtracker/
├── index.html       # Complete single-file application (HTML, CSS, JS)
└── README.md        # Documentation and guide
```
