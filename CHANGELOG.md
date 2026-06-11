# Changelog

All notable changes to the Skin in the Game plugin.

## [0.1.2] — 2026-06-11

### Fixed
- The SessionStart hook now fires on **all** session-start events (startup, resume, `/clear`, compaction) instead of startup only. Previously, a `/clear` or a context compaction silently dropped the operating contract for the rest of the session.

### Changed
- README restructured for first-time visitors: the before/after example moved up front and sharpened, added a sample `constitution-check` output, and documented that the contract re-loads after `/clear`.

## [0.1.1] — 2026-06-07

### Fixed
- Plugin failed to load: removed the redundant `hooks` field from `plugin.json`. Hooks are auto-discovered at `hooks/hooks.json`, and declaring the path a second time in the manifest broke installation.

## [0.1.0] — 2026-06-07

### Added
- Initial release: the twelve build principles (`PRINCIPLES.md`), six enforcement skills (`operating-contract`, `grill-me`, `delete-the-requirement`, `research-first`, `reality-check`, `constitution-check`), and a SessionStart hook that injects the operating contract into every session.
