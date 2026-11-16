# Changelog

All notable user-facing changes to **Palcore** are documented in this file.

## [1.0.3] — 2026-10-18

### Fixed
- **Settings Panel Layout:** Redesigned the Settings drawer into a compact layout with keyboard (`Escape`) and outside-click dismissal so controls never overlap key viewport elements on resize.
- **Top-Edge Window Resizing:** Resolved drag/resize conflicts along the top edge and corners of both Desktop and In-Game windows, providing consistent resize cursors and smooth dragging.
- **FTUE Drag & Resize Support:** Kept the Desktop window freely draggable and resizable while the First-Time User Experience (FTUE) walkthrough is active.
- **Second-Monitor Hotkey Stability:** Prevented overlay hotkey toggles from unexpectedly resizing or repositioning an already open Desktop companion window on a secondary monitor.
- **Responsive Scaling:** Enforced DPI-aware minimum window sizes and fixed narrow-width layout clipping across sidebars, radar canvas, and onboarding cards.

---

## [1.0.2] — 2026-10-02

### Added
- **Interactive FTUE Walkthrough:** Added a spotlight-guided onboarding tour highlighting the live radar, storage/Pal tabs, and overlay hotkey, plus a quick-guide replay option from the title bar and Settings.
- **Tactical Radar Empty States:** Added a 4-stage radar state indicator (`Closed`, `In Lobby`, `Searching`, `Live`) with clear status badges when Palworld is closed, in the lobby, or acquiring coordinates.
- **Event Health Indicators:** Added live connection status indicators reflecting game/GPS availability.

### Fixed
- **Live Position Independence:** Decoupled real-time player tracking from placed base chests so the minimap and radar track live coordinates accurately even in brand-new worlds or early gameplay saves.

---

## [1.0.1] — 2026-09-05

### Added
- **Second-Screen Companion Mode:** Automatically moves the Desktop window to an available secondary monitor when Palworld launches and returns it when the game exits; single-monitor setups continue parking the Desktop window cleanly.
- **Auto-Open Overlay Setting:** Added a user preference to control whether the in-game overlay opens automatically on game start (hotkey remains available anytime).
- **Uninstall Feedback Window:** Added an optional uninstall survey prompt opening in the user's default browser.

### Fixed
- **Cold Launch Window Behavior:** Fixed a startup race where the Desktop window could minimize automatically when Palworld was not running.
- **Dock & Launcher Focus:** Clicking the dock/launcher icon now reliably brings the Desktop window to the front.
- **Ad Privacy Shortcut:** Updated the "Manage ad privacy" action to open the dedicated Overwolf Privacy settings directly.
- **Dynamic Hotkey Reminders:** Overlay hotkey hints now read the active user binding immediately when customized instead of showing a static default.
- **Multi-Monitor Detection:** Enabled proper display enumeration for dual-monitor setups.

### Changed
- Disabled unintended text selection on desktop chrome while keeping form controls and settings inputs selectable.
- Hardened production builds by stripping development tooling automatically during release packaging.
