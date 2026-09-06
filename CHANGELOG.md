# Change Log

All notable changes to the "lenscope" extension will be documented in this file.

Check [Keep a Changelog](http://keepachangelog.com/) for recommendations on how to structure this file.

## [Unreleased]

## [0.0.3] - 2026-09-06

### Added
- **Find Files** — fuzzy search all workspace files with live preview; respects `.gitignore`
- **Current Buffer Fuzzy Find** — search lines in the active file, opens beside the editor in a single-pane layout
- `lenscope.ripgrepPath` setting — override the ripgrep binary path when auto-discovery fails
- Cross-platform keybindings — `ctrl+shift+*` for Windows/Linux alongside `cmd+shift+*` for Mac
- Windows ripgrep discovery — checks scoop shims, chocolatey, and cargo installs

### Changed
- `find_files` keybinding changed to `cmd+shift+alt+f` / `ctrl+shift+alt+f` to avoid conflicting with VS Code's built-in Find in Files
- `live_grep` and `find_files` shortcuts now fire from anywhere in VS Code (`!terminalFocus`), not only when an editor has focus
- Removed `preview` flag — extension is no longer pre-release
- Refactored ripgrep path resolution into `findRgWindows` / `findRgUnix` helpers
- Path normalisation now uses `path.resolve` for correct handling of `.\` relative paths on Windows
