# Changelog

All notable user-facing changes to ShiftMate ER will be documented in this file.

## [1.1.1] - 2026-11-11

- Improve mobile layouts and update the application icons and desktop binary name (#14, #16).
- Migrate the frontend to Tailwind 4 and coordinate React Router, Vite and Tailwind updates (#12, #24, #32).
- Update dependency security and add continuous integration checks for the web build and Tauri project (#10).
- Update the desktop toolchain to Tauri 2.12.2 with the v1 packaging action (#35), and refresh Rust log and JSON dependencies (#26, #22).

## [1.1.0] - 2026-09-29

### Added

- Cross-platform desktop application support with Tauri
- Linux packages:
  - AppImage
  - DEB
  - RPM
- Windows packages:
  - NSIS installer
  - MSI installer
- GitHub Pages deployment for the web application

### Improved

- Linux AppImage compatibility

[1.1.0]: https://github.com/ShaheenMedTech/ShiftMate-ER/releases/tag/v1.1.0
