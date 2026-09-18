# Ship Log Journal

A written development log to accompany the Weekly Ship Log Tracker application. Use this journal to document weekly highlights, technical decisions, achievements, and retrospectives.

---

## Log Template

Use the following template for adding manual weekly notes or milestone reviews:

```markdown
### Week of [Month Day, Year]

**What I Shipped:**
- [Feature / Bug fix / Improvement 1]
- [Feature / Bug fix / Improvement 2]

**Key Learnings & Challenges:**
- [Note technical roadblocks, discoveries, or useful tools]

**Goals for Next Week:**
- [Goal 1]
- [Goal 2]
```

---

## Log Entries

### Week of September 18, 2026

**What I Shipped:**
- **Feature: Edit Entries** — Added an inline edit mode to every entry card. Clicking Edit replaces the content with a pre-filled textarea. The user can save changes (persisted to `localStorage` with an `(edited)` badge) or cancel to restore the original text. Supports `Cmd/Ctrl + Enter` shortcut inside the edit textarea.
- **Feature: Clear All Entries** — Added a "Clear All Entries" ghost button to the header, visible only when entries exist. Triggers a confirmation prompt before wiping all data from `localStorage`.
- **Full Lucide Icon Migration** — Replaced all remaining emoji (✏️ Edit, 💾 Save Changes, ❌ Cancel, 🧹 Clear All) with native Lucide icon elements (`pencil`, `save`, `x`, `trash-2`). The UI is now entirely emoji-free.
- **Edit & Delete Button Styling** — Unified the Edit button to match the Delete button: same muted grey (`#94a3b8`) default color, same padding and minimum tap target size (44px), same flex alignment. Edit hover uses a subtle dark-grey effect (`#e2e8f0` bg, `#334155` text) and active state adds a `scale(0.95)` press. Added an `8px` gap between Edit and Delete.
- **Clear All Button Styling** — Restyled the Clear All button as a ghost button native to the gradient header: semi-transparent white fill (`rgba(255,255,255,0.12)`), white text and icon, soft white border. Properly centered horizontally and vertically within the header frame, with clear `gap` between icon and label text.
- **Critical Bug Fix** — The `clearAllBtn` HTML element was missing from the DOM, causing an uncaught `TypeError` that crashed the entire JavaScript IIFE on startup — preventing entries from rendering or saving. Fixed by re-adding the missing HTML and adding null guards around all `clearAllBtn` references.

**Key Learnings & Challenges:**
- A missing DOM element referenced at the top level of an IIFE will silently crash all downstream event listeners and rendering logic. Null guards (`if (clearAllBtn)`) are essential for resilience.
- When using `multi_replace_file_content`, CSS injected with an incorrect line number target can land inside a `<script>` block, causing a syntax error. Always verify the file state after each multi-chunk edit.
- Lucide icons injected via `innerHTML` in dynamically rendered cards require `refreshIcons()` (`lucide.createIcons()`) to be called after every render cycle.

**Goals for Next Week:**
- Explore tag/category filtering for log entries.
- Add export/import functionality (JSON or CSV) for data backups.

---

### Week of September 1, 2026

**What I Shipped:**
- Built the complete, single-file Weekly Ship Log Journal application (`index.html`).
- Implemented browser `localStorage` integration for persistent entry storage.
- Integrated Lucide icon set for interface controls, timestamps, actions, and empty states.
- Added live character counting and keyboard shortcut support (`Cmd/Ctrl + Enter`).
- Designed a mobile-first responsive layout with custom gradients and soft card elevation.
- Created project documentation (`README.md` and `Journal.md`).

**Key Learnings & Challenges:**
- Building self-contained web applications with zero external build tools allows for rapid prototyping and deployment.
- Dynamic Lucide icon instantiation via `lucide.createIcons()` provides scalable vector icons within client-side rendered DOM nodes.

**Goals for Next Week:**
- Add the ability to edit existing entries inline.
- Add a bulk "Clear All" action for fast resets.
